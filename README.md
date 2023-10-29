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
