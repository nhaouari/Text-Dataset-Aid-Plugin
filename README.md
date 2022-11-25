

![image](https://user-images.githubusercontent.com/88785126/203184536-9199f720-a03b-423b-9bf6-81a68c7fbd28.png)

## Personalize your Second Brain Buddy(Text Generation Model)

[![Build obsidian plugin](https://github.com/conneroisu/Text-Dataset-Aid-Plugin/actions/workflows/release.yml/badge.svg)](https://github.com/conneroisu/Text-Dataset-Aid-Plugin/actions/workflows/release.yml)


# Context 
## Condition: Fully Working	
The creation of NLP and text generation datasets are extremely impactual and has the potential to allow for researchers to train models that can automatically generate text. However, the creation of custom datasets is a teadious and slow process.

The text dataset aid is a helpful tool that can aid the creation of finetuning datasets for text generation models like GPT-3 by hand! This can make the text generated by your model after finetuning to be more personalized, detailed, or better formatted. Say no to dealing with menus through hotkey configurations!

This plugin can be used to quickly generate training data for NLP and text generation models. This would speed up research in these areas, as well as make it easier for practitioners to train these models.

The text dataset aid plugin is a helpful tool that can aid the creation of finetuning datasets for text generation models like GPT-3 by hand. This can make the text generated by your model after finetuning to be more personalized, detailed, or better formatted. Say no to dealing with menus through hotkey configurations!

## Context within your second brain 
Updating your own text generation model on your collected dataset whilst working in your second brain allows for your model to better fit your second brain's needs. This plugin fits in any creation or editing workflow because of the nature of commands within obsidian. Hope that you use this plugin as much as I do!

# Advantages of Finetuning
Fintuning your text generation model allows for the creation of text that is more natural and expressive. 
1. increased accuracy in text prediction/generation 
2. increased fluency and coherence in text generation
3. greater control over the style and content of generated text
4. More control over the types of outputs the model produces
5. Greater flexibility in the types of inputs the model can accept
6. The ability to produce more human-like outputs
7. Increased accuracy in the prediction of certain types of outputs

An great resource for fine-tuning principles from [microsoft](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/how-to/prepare-dataset)

# Usage
The core function of this plugin is made easier through the use of vim mode, but should work in either case. 
There are two commands offered currently:(Each of these commands has an acommpanying hotkey configureable from hotkeys) 

When you send the prompt to the dataset if there is already a prompt there, the plugin does nothing. 

When you send the completion to the dataset and there is already a prompt the text selection is sent to the dataset as a completion to that prompt.

## Open Ended Generation Support!
When you send the completion to the dataset  and there is not a prompt, the text selection is inserted into the dataset with a empty prompt prepended to the text selection.

an example of this 
```json
{"prompt":"", "completion":"Hello can I help you?"}
```
another example 
```json 
{"prompt":"", "completion":"Hi, How can I help you today"}
```

Send the Selection to send to your dataset file as prompt
Send the Selection to send to your dataset file as completion


Example of finetuning dataset
```json
{"prompt":"Company: BHFF insurance\nProduct: allround insurance\nAd:One stop shop for all your insurance needs!\nSupported:", "completion":" yes"}
{"prompt":"Company: Loft conversion specialists\nProduct: -\nAd:Straight teeth in weeks!\nSupported:", "completion":" no"}
```

# Installation
## Installing from the community plugins page in obsidian
-   Open Settings > Third-party plugin
-   Make sure Safe mode is **off**
-   Click Browse community plugins
-   Search for "Dataset Finetuning Aid Plugin"
-   Click Install
-   Once installed, close the community plugins window and activate the newly installed plugin
## Manually Installing from github 
-   Download the Latest Release from the Releases section of the GitHub Repository(if you can't find this it should be to the right while your viewing this)
-   Extract the plugin folder from the zip to your vault's plugins folder: `<vault>/.obsidian/plugins/`  
    Note: On some machines the `.obsidian` folder may be hidden. On MacOS you should be able to press `Command+Shift+Dot` to show the folder in Finder.
-   Reload Obsidian

# Settings
There are four main settings that are configurable within the settings panel of the plugin, but the default values are set up for the popular format for datasets for text generation models called jsonl.

| Setting Name          | Description                                                                     | Default       |
| --------------------- | ------------------------------------------------------------------------------- | ------------- |
| Prefix for Prompts    | This is the string that is prepended to the prompt when sent to the dataset     | `{"prompt":`    |
| Suffix for Prompts    | This is the string that is appended to the prompt when sent to the dataset      | `,`             |
| Prefix for Completion | This is the string that is prepended to the completion when sent to the dataset | `"completion":` |
| Suffix for Completion | This is the string that is appended to the completion when sent to the dataset  | `}\n`              |


[Help within development](https://github.com/TfTHacker/obsidian42-text-transporter/blob/main/src/features/transporterFunctions.ts)

# Inspiration

Inspired by the efficiency and appeal of fine-tuning your own language model, this plugin allows for you to build datasets from your notes in the form of prompts and responses. Automatically formats the text to the specification of [OpenAI](https://openai.com/) for finetuning models like GPT3.

This plugin shares simularities to the textTransporter Plugin made by [TfTHacker](https://github.com/TfTHacker/obsidian42-text-transporter/)

# Versioning notes
You can simplify the version bump process by running `npm version patch`, `npm version minor` or `npm version major` after updating `minAppVersion` manually in `manifest.json`. The command will bump version in `manifest.json` and `package.json`, and add the entry for the new version to `versions.json`


