# SDLX finetuned on LoRA for synthetic image dataset generation for Indian roads and driving scenarios

- **Challenge**:
This problem statement involves creating photo-realistic images of urban
Indian driving scenes. They should accurately depict the complexities of
everyday Indian roads in terms of (but not limited to):
● Traffic congestion
● Unexpected/Atypical elements on the roads
● Different weather conditions

- **Approach**:
Some very popular text-to-image checkpoint models are the stabilityai-stable-diffusion-1.5v, 2.1v and the SDXL 1.0.
**SDXL 1.0** being the latest is more intelligent and is also flexible on the input resolution of Images and also generates better output images even with shorter prompts as compared with the former models.

But to make the images generated more challenge specific (Specific to Indian roads) the model was finetuned using **LoRA (Low Rank Adaptation)** which is a good pick when there is time constrant and GPU limitations, thus somewhere lying inbetween the popular and most liked "Dreambooth" which overwrites the checkpoint post-training, making it the heaviest model and the least popular "Hypernetworks" which require more hyperparameter tuning and processes for control. Thus combining the best features of other popular finetuning techniques such as Dreambooth and Textual inversion.

Few common findings (Objects) observed from multiple images of Indian roads were considered for finetuning SDXL performance using LoRA, such as:
- Potholes
- Cows
- Dogs
- Multiple Indian vehicle classes (Bullock Carts to Suzuki Vitara Brezza)
- Footpaths/Sidewalks.
- Road constructions, etc...

The UI is built on streamlit (Easy rapid deployment).

**Running the Application:**
The github repo can be cloned on your local machine in a new folder:
[cmd]:
```
git clone https://github.com/vishwesh2000/LoRA-Chaining-on-SDXL-for-Better-Synthetic-Datasets
```
```
cd <new folder created>
```
```
pip install requirements.txt
```

**Prerequisites:**
You will have to create a replicate account: https://replicate.com/
Go to your profile and collect your replicate token.
Endpoint to update in the ```/.streamlit/secrets.toml``` file --> "shashankanil/sdxl-test:7fab3afbe2fdb77fe26e8af29511895499b2f27daa26b145d2178118a5972212"

**Run:**
```
streamlit run app.py
```
