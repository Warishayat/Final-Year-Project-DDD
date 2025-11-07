adb kill-server
adb start-server
if you want to run in a local env use python version 3.11.0 
run commands 
py -3.11 -m venv env
env\Scripts\activate
python --version
and change the requrirements to following these 
torch==2.5.0
torchaudio==2.5.0
torchvision==0.20.0
pip install -r requirements.txt

also you need to update in app.py with this line
    uvicorn.run(app, host="0.0.0.0", port=int(os.getenv("PORT", 8000)))