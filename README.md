# VISPROG

Visual programming framework that utilizes natural language instructions and integrates with OpenAI's API for seamless visual program creation, debugging, and evaluation.

## HOW TO USE VISPROG

1. **Install Anaconda (If you haven't installed it yet)**  
   Follow the instructions to install Anaconda from [here](https://docs.anaconda.com/anaconda/install/).

2. **Create a new folder to use VISPROG**

3. **Open terminal and follow the steps:**

    1. **Git clone the main branch of the VISPROG GitHub repository**
        ```bash
        git clone https://github.com/hyunhp/VISPROG.git
        ```
    
    2. **Change directory to the cloned Git folder**
        ```bash
        cd visprog
        ```
    
    3. **Install dependencies**
        ```bash
        conda env create -f environment.yaml
        ```
    
    4. **Activate the conda virtual environment**
        ```bash
        conda activate visprog
        ```

4. **Create a `.env` file inside the `visprog` folder, and insert your OPENAI_API_KEY information without quotes:**
    ```
    OPENAI_API_KEY=your_api_key
    ```

5. **Debug and update the original VISPROG repo:**
    1. Update the OpenAI model calling part ("text-davinci-003" has been deprecated as of January 4th, 2024).
    2. Update the code `vis_masks` in `vis_utils.py`.
    3. Update CUDA usage inside `step_interpreters.py`.
    4. Update NLVR prompts to debug answers in digit format (e.g., 1, 2, 3) instead of text format (e.g., one, two, three) in the eval interpreters function.

6. **Handle the 410 error encountered when using the `FaceDetInterpreter` class:**
    - Download the [DSFD_RES152.pth](https://drive.google.com/file/d/1WeXlNYsM6dMP3xQQELI-4gxhwKUQxc3-/view) model and save it into your local torch hub folder directory (e.g., `C:/{USER_NAME}/.cache/torch/hub/checkpoints`).

**UPDATED AT:** 7th July, 2024