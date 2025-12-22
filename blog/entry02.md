# Entry 2
##### 12/21/25

## How the project has been going
So far so good, to be honest. I ended up making a lot of parts of my project that I'm proud of, and I believe I do indeed have enough time to at least finish the first few parts of the project that is presentable enough for the end of the year. But what about the specifics? My plans for *next year*? Well, let's get into that.

### What I'd done so far
So far, I'd say that I've done a lot of progress for my project. I ended up reviewing what I done in the past with Unity back at my game program, and I ended up using a lot of the skills I learned there to here. For example, I ended up making a text box using what Unity has to offer. I ended up experimenting **a lot** with the UI Unity has, which is helpful as the UI in Unity is easy to get through once you get used to it. Anyways, I ended up using this code to help with things such as the text speed and actually changing the dialogue: 
```c#
IEnumerator TypeLine()
{
    foreach(char c in lines[index].ToCharArray()) // types out each char
    {
        textComponent.text += c;
        yield return new WaitForSeconds(textSpeed);
    }
}

public void NextLine()
{
    if (index < lines.Length - 1) // length of array
    {
        index++; // go to next line
        textComponent.text = string.Empty;
        StartCoroutine(TypeLine());
    }
    else
    {
        sceneStop = true;
        gameObject.SetActive(false); // all activity is stopped
    }
}
```
Basically the IEnumerator helps time how each character in the dialogue shows up, while the NextLine() method helps transition into another line of the dialogue itself. It was really useful to use for the dialogue, at least for the little bit of dialogue I have. I also ended up making a settings page, which is simple enough, as it's reliant on Unity built-in settings, so the code ended up like this:
```c#
public AudioMixer audioMixer;
public GameObject dialogue;
public void SetVolume(float volume) 
{
    audioMixer.SetFloat("volume", volume);
}

public void SetFullScreen(bool isFullScreen) 
{
    Screen.fullScreen = isFullScreen;
}

public void SetTextSpeed(float txtSpeed) 
{
    dialogue.GetComponent<Dialogue>().textSpeed = txtSpeed;
}
```

I also ended up making the main menu, and this is what it looks like:
<img width="961" height="543" alt="image" src="https://github.com/user-attachments/assets/04523da7-2632-4351-aa1d-700fdbaf7111" />

Overall, I had a good time with what I'm doing so far, and I think I made decent progress.

### Plan for Winter Break
I thought that I would originally have *plenty* of time to work on the game as 1. winter break lasts a few days so I have plenty of time, and 2. I don't really have any plans nor distractions during the time, so I should be good, right? Well in reality all I got is 1. exactly 12 days for the project, and 2. I have college applications and a couple of assignments to finish over the break. So yeah, I need to plan **carefully** on what to do over the break, as there's just so much to do to prepare once the actual deadline for the project comes. 

First off, I'll have to further plan out the story with my friends who are helping me. While we got the beginning part done, we still need to work on writing...the rest of the story for the project. Realistically, the first part of the writing, as that's the milestone I intend to reach for the freedom project to present it. Second, I have to still work on character sprites and art, as the art is arguably the most important part of a visual novel, besides the story and actual code of course. I'll have to contact my friends who are helping me as well for the art part. 

Finally, I have to work on you know, coding the project. I plan to work on figuring out how to change dialogue depending on choices, along with adding and changing more scenes for the game. I also plan to actually try to add some sprites in the game and how to change them as well. I'll use free assets since the actual assets aren't done yet, but I still have to make good practice with the code until we actually have to put the assets in. Then, I can work on making the settings more customizable and making universal variables, as I need to figure out how to connect certain things in all scenes somehow.

Overall, I think that this is a rather decent plan for the break, and I'll try to make sure to balance it all out at the end of it.

## EDP
I'm currently on steps 4 and 5 of the Engineering Design Process, which is planning the most promising solution and testing the prototype perspectively. I'm still planning the storyline and character designs of the game, and I'm still making the game. However, I believe that I'll get to the next steps soon though with the game, which is good.
## Skills
Of course, with what I've been doing, I learned new skills along the way. Here are some I learned.

### Trying out new things
I ended up learning new things as a result of making my game on Unity, such as making use of the UI for example. I ended up learning a lot more about how to make setting pages for the first time, and I ended up learning how to utilize my skills from the past for what I'm making in the present. I ended up getting a lot of progress done thanks to me deciding to try out new things.

### Learning things on my own
Similar to what I said before, I ended up getting a lot of things done thanks to learning certain things on my own, such as making a settings page and learning how to make a main menu. That led me to become more knowledgeable in Unity as a result of this. Overall, I had a decent time learning Unity, and I look forward to doing more over the break!

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
