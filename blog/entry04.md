# Entry 4
##### 3/15/26

## What I did so far
Ever since my last blog, I ended up doing a bit for my project. Here's what I've done so far.
### Coding some more
Of course, since it's almost April, I had to make sure to get stuff done with the limited amount of time I had left. So I ended up polishing up some core mechanics of the game. First, I was struggling a bit with how to move on with my scenes, as I didn't want to overwhelm my UI with so many buttons, as that was only applicable with the choices. However, I ended up finding out how to do that in the `Update()` function. I just needed to make another function where the scene takes place, and everytime you press on it, it moves on to the next lines of dialogue. Here's the code for that below:
```c#
void Update()
{        
     if (Input.GetKeyDown("space")){
          Next();
     }

     // secret debug code: go back 1 Story Unit, if NEXT is visible
     if (Input.GetKeyDown("p")) {
          primeInt -= 2;
          Next();
     }
}
```
Another thing that I discovered is how to actually make choices function in the game. It was similar to what I learned in Game Academy with UI, as all I needed to do was to assign it a function where the different choice of text takes place. Here is one example of the choice function in motion:
```c#
public void Choice1aFunct(){
       Char1name.text = "Father";
       Char1speech.text = "But you loved her, didn't you?";
       Char2name.text = "Laura";
       Char2speech.text = "...";
       primeInt = 19;
       Choice1a.SetActive(false);
       Choice1b.SetActive(false);
       nextButton.SetActive(true);
}
```
Overall, I feel like I've been making pretty good progress with my project. 
### Plans for the Spring Break
My plans for the spring break are to *obviously* continue with the project, as I have plenty of time to catch up with my project since there won't be much to do. Specifically, I want to continue making the assets, music, and overall make the game a bit more pretty once the mechanics are fully complete, as it's a visual novel, so **of course** it has to look pretty. Overall, I hope to achieve these goals before the MVP is done.
## EDP
Currently I'm in step 5 of the Engineering Design Process, which is creating a prototype. Technically, I'm still in the process of making the game, and I plan to test the game once it's actually playable later.
## Skills
Of course, as I was making the game, I learned some skills along the way. Here are some I learned.
### Balancing my schedule
The first skill I learned was being able to balance my work schedule efficiently so I was able to do my project enough while also being able to complete all my other assignments in time. Around the time the marking period was ending, my teachers decide to give me big tests and exams to prepare for, which added to the stress I had already. However, with timing all my tasks carefully, plus making sure to take breaks in the meantime, I was able to finish all my assignments on time, so I was greatful for myself for being able to do some of my project at the end of it. I hope to continue this method some time.
### Learning things as I go on
Even with my familiarity of Unity, I ended up learning new things as a result of making my game on Unity, such as making use of buttons and how to work Unity itself, for example. I ended up learning a lot more about how to make things I thought weren't possible on Unity, and I ended up learning how to utilize my skills from the past for what I'm making in the present. While making a visual novel on Unity may seem rough, I ended up getting a lot of progress done thanks to me deciding to try out new things.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
