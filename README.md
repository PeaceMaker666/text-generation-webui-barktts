# Please read and follow these instructions
1. When you clone or install this via the Oobabooga UI please rename the extension (located in the extensions folder) from "text-generation-webui-barktts" to "bark_tts"
2. When you load it up for the first time you might get an error, please try to reload the extension once more.
3. This version is currently working with Oobabooga, I will try to keep it up to date with changes to the program.
4. Check out this commit change to see how this version is different than the others: https://github.com/RandomInternetPreson/text-generation-webui-barktts/commit/c1d64d91bb6b6ff87e00e3a0090870dcc8fe5736
Other than working with Oobabooga it also allows one to change characters that the AI voice model converts.  For example the 's would be read as &#x27 ; in previous implementations of bark

This is an audio sample from a short story an AI in oobabooga wrote
<audio controls>
  <source src="StorySampleStart/1698812202.wav" type="audio/wav">
  Your browser does not support the audio element.
</audio>

# text-generation-webui-barktts
A simple extension for the [text-generation-webui by oobabooga](https://github.com/oobabooga/text-generation-webui) that uses [Bark](https://github.com/suno-ai/bark) for audio output.

## How to install
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
