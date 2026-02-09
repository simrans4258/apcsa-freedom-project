# Entry 3
##### 2/8/26

## What I did during Winter Break
Since we had time during winter break to work on our projects, here are some things that I did during the break for my project.

### Working on Game More
I ended up working on the game more during the break, as my main goals were to figure out how to change text boxes for choices in the game, as that's the main component of the game. I ended up looking up **a lot** of tutorials as a result in order to help me with the code of the game. One _very_ helpful source I found was [this website](https://madwomb.com/tutorials/GameDesign_UnityVisualNovel.html), which goes into a deep dive on how specifically visual novels in Unity work, and how to make them. One helpful source of code is the code below, which basically helps you move onto dialogue faster with the space button, and the `Next()` function serves as a gateway for the dialogue to go by faster:
```c#
 if (Input.GetKeyDown("space")){
    Next();
}
```

I also learned that I could straight up use variables as a way to track how dialogue goes by in the game, as not only do they help actually change the dialogue each time you click on the screen, but also help with dialogue choices, which are a **core** part of visual novels. I could use buttons to represent the choices, and then I could change the numbers to go to different dialogue choices and scene changes. Here's an example of it being used, which I tested out, and it works!
```c#
public void Choice1aFunct(){
        Char1name.text = "YOU";
        Char1speech.text = "I don't know what you're talking about!";
        Char2name.text = "Character 2";
        Char2speech.text = "What?";
        primeInt = 19; // so hitting "NEXT" goes to primeInt==20!
        Choice1a.SetActive(false);
        Choice1b.SetActive(false);
        nextButton.SetActive(true);
        allowSpace = true;
}
public void Choice1bFunct(){
        Char1name.text = "YOU";
        Char1speech.text = "Sure, anything you want... just lay off the club.";
        Char2name.text = "Character 2";
        Char2speech.text = "Great! See you later then!";
        primeInt = 29; // so hitting "NEXT" goes to primeInt==30!
        Choice1a.SetActive(false);
        Choice1b.SetActive(false);
        nextButton.SetActive(true);
        allowSpace = true;
}
```
Overall, I ended up making a lot of progress with the game, and I hope to continue this work ethic in the future.

### Planning some more
Since mid-winter break is coming up, this is a great opportunity for me to exploit the time in order to continue making my game. I plan to keep on making and utilizing transitions and dialogue scenes, and I also plan to work on making character sprites change, as that is a core part of visual novels too. I also plan to work more on the art and a bit of the story as well, as those are important to the game as well. Overall, I plan to just keep on working towards my Minimum Viable Product, and maybe even go beyond that given enough time.

## EDP
Currently I'm in step 5 of the Engineering Design Process, which is creating a prototype. Technically, I'm still in the process of making the game, and I plan to test the game once it's actually playable later.

## Skills
Of course, with what I've been doing, I learned new skills along the way. Here are some I learned.

### Taking your time
Sometimes it's good to take your time when it comes to making projects like this. I was pressurizing myself so much to complete certain parts of the project under a certain amount of time, that I forgot that I do indeed have enough time to finish at least a MVP for the Freedom Project. I have a few months, and while **of course** I have to plan efficiently to get the project done, I should also keep in mind that I have plenty of time.

### Trying Again and Again
During the process of continuing my project, I ended up getting pretty **frustrated** at certain times, as sometimes when I code something in Unity, it doesn't work. And when I try to fix it, sometimes the end result turns out to be worse than in the beginning. However, I wasn't keen on giving up just yet, as I wanted to at least finish some parts before anything else. So, I looked up what was wrong with my code, and kept on trying until I solved my problem. Sure, it's a long process, but I'm sure it'll pay off in the long run with my project.   

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
