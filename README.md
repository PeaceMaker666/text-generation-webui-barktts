# Please read and follow these instructions
1. When you clone or install this via the Oobabooga UI please rename the extension (located in the extensions folder) from "text-generation-webui-barktts" to "bark_tts"
2. When you load it up for the first time you might get an error, please try to reload the program and extension once more.
3. This version is currently working with Oobabooga, I will try to keep it up to date with changes to the program.
4. Check out this commit change to see how this version is different than the other: https://github.com/RandomInternetPreson/text-generation-webui-barktts/commit/c1d64d91bb6b6ff87e00e3a0090870dcc8fe5736
Other than working with Oobabooga it also allows one to change characters that the AI voice model receives and converts.  For example 's would be read as &#x27 ; in the previous implementation of bark

This is an audio sample from a short story an AI wrote using Oobabooga's textgen-webui

https://github.com/RandomInternetPreson/text-generation-webui-barktts/assets/6488699/98df51e5-aa51-49ad-a055-b2aa18535f4a

These are the settings used to produce the sample and story.

![Settings](https://github.com/RandomInternetPreson/text-generation-webui-barktts/assets/6488699/a5cbb3cf-ed92-4ad2-a044-c15fd2842128)

# text-generation-webui-barktts
A simple extension for the [text-generation-webui by oobabooga](https://github.com/oobabooga/text-generation-webui) that uses [Bark](https://github.com/suno-ai/bark) for audio output.

## How to install - via Windows and Oobabooga UI
1. With Oobabooga's textgen_webui installed go to the "Session" tab and paste https://github.com/RandomInternetPreson/text-generation-webui-barktts into the "Install or update an extension" window, very importantly press "Enter" after entering and the UI will clone this repo

![clone](https://github.com/RandomInternetPreson/text-generation-webui-barktts/assets/6488699/68f0db12-4c2e-4154-a5f5-04965bd447d3)

2. Once cloned, close the UI and command windows and change the name of the folder which was created to clone this repo, change it from "text-generation-webui-barktts" to "bark_tts":

![name change](https://github.com/RandomInternetPreson/text-generation-webui-barktts/assets/6488699/f69f3cd8-ac8e-4906-a762-b20b05b31de8)

3. In the text-generation-webui-main folder, click on "cmd_windows.bat" and navigate to the directory for this extension using the phrassing below with cd before the folder directory:

   cd L:\OobTesting\text-generation-webui-main\extensions\bark_tts
   You would use your own directory mine is just an example
   `cd your-directory-here`
   
   and press "Enter"

5. Now enter this "pip install -r requirements.txt" in the command prompt and press "Enter", this will install all the stuff needed to get this running.

   ![installing](https://github.com/RandomInternetPreson/text-generation-webui-barktts/assets/6488699/8028787d-b22b-405b-8cc1-0f9a81fb401e)

6. Once complete you can close the command prompt window and start the textgen-webui again.  Please note that you may get an error when you load the extension for the first time, please restart textgen-webui and load again.  It's some issue with downloading the models for the first time.


## How to install - via Conda Enviroment
Assuming you already have the webui set up:

1. Activate the conda environment with the `cmd_xxx.bat` or using `conda activate textgen`
2. Enter the  `text-generation-webui/extensions/` directory and clone this repository
```
cd text-generation-webui/extensions/
git clone https://github.com/minemo/text-generation-webui-barktts bark_tts/
```
3. install the requirements
```
pip install -r extensions/bark_tts/requirements.txt
```
4. Add `--extensions bark_tts` to your startup script <br/> <b>or</b> <br/> enable it through the `Interface Mode` tab in the webui

## Tips
The full version of Bark requires around 12Gb of memory to hold everything on GPU at the same time. However, even smaller cards down to ~2Gb work with some additional settings. For this extension, you could open `extensions/bark_tts/.env`, then set `USE_SMALL_MODELS` and `USE_CPU` to `true`:

```
# Whether to use small models
USE_SMALL_MODELS=true

# Whether to use CPU
USE_CPU=true
```



