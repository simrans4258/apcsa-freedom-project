# Entry 5
##### 4/29/26

## Finishing MVP
So, I **finally** finished my MVP after all this time. Here is what I did.

### What I completed
It's near the end of the marking period, and I **finally** managed to complete my project to it's full extent. I managed to do *a lot* of things for the project. First, I was able to successfully make the UI of the game, since that is a major part of how visual novels work, and I'm happy that it all got sorted out. I managed to input sounds as well, using the free audio source website [freesound](freesound.org), which is quite literal to its title. I also made a background art by myself by using [Pixilart](pixilart.com), which is a free drawing source to make you know, pixel art. Here is the background (along with the UI buttons):

<img width="727" height="426" alt="image" src="https://github.com/user-attachments/assets/1b487565-2b0b-4c82-bd9e-da90ea3d148d" />

I also ended up making a ton of background pictures using free photos from [Pexels](pexels.com) and editing them on [Canva](Canva.com) myself. Here is one example of one of the backgrounds I used, along with the panel for the text:
<img width="672" height="434" alt="image" src="https://github.com/user-attachments/assets/8c104162-4ccb-490c-acd6-9480c4e37775" />

Last but not least, I managed to **finally** get my code back on track by using *so* many different resources that I found online. This [website](https://madwomb.com/tutorials/GameDesign_UnityVisualNovel.html) really helped me along the way when it comes to coding visual novels in Unity, especially in the beginning part where I was struggling. Thanks to the website, I managed to learn so many things, such as how to use for loops for texts, different classes for different functions for buttons, or even pure Unity stuff where you can control timing and Game Object coordination. The code below is one key example of that, where I used special types of functions to make typing and fading effects:
```c#
IEnumerator TypeText(TMP_Text target, string fullText)
{
    float delay = 0.01f;
    nextButton.SetActive(false);
    allowSpace = false;
    for (int i = 0; i <= fullText.Length; i++)
    {
        string currentText = fullText.Substring(0, i);
        target.text = currentText;
        yield return new WaitForSeconds(delay);
    }
    nextButton.SetActive(true);
    allowSpace = true;
}
IEnumerator FadeIn(GameObject fadeImage)
{
    float alphaLevel = 0;
    fadeImage.GetComponent<Image>().color = new Color(1, 1, 1, alphaLevel);
    for (int i = 0; i < 100; i++)
    {
        alphaLevel += 0.01f;
        yield return null;
        fadeImage.GetComponent<Image>().color = new Color(1, 1, 1, alphaLevel);
        Debug.Log("Alpha is: " + alphaLevel);
    }
}

IEnumerator FadeOut(GameObject fadeImage)
{
    float alphaLevel = 1;
    fadeImage.GetComponent<Image>().color = new Color(1, 1, 1, alphaLevel);
    for (int i = 0; i < 100; i++)
    {
        alphaLevel -= 0.01f;
        yield return null;
        fadeImage.GetComponent<Image>().color = new Color(1, 1, 1, alphaLevel);
        Debug.Log("Alpha is: " + alphaLevel);
    }
}
```
I also have to shoutout to Game Academy at Urban Arts, as I wouldn't have gotten the idea to start my project in Unity in the first place without their help, as I managed to get my project done in the nick of time thanks to me reviewing their lessons I took over last summer. I really couldn't have done it without them.

I ended up having to make a separate repository for my project due to the amount of files in the project, plus it was just easier for me to do that than to risk putting my project in the actual apcsa freedom project repository. Here is the [link](https://github.com/simrans4258/forget-me-not) to that. I also made an itch.io link to actually preview the game, which is [here](https://galaxia08.itch.io/forget-me-not). Overall, while there had been *a lot* to do, I'm glad that I had got it done in time. 

### Plans for Beyond MVP
My plans for the beyond MVP are actually pretty simple. Since I have relatively simple art and UI designs for the game, I plan to improve on those things to make the game look more nice. Plus, I plan to add more to the game, such as more scenes, characters, story lines, and more. However, due to AP Exams coming up next month, the due date for the Beyond MVP itself, and the fact that I completed my MVP **pretty late**, it can be pretty difficult for me to actually do a lot of things for the Beyond MVP. But hey, that doesn't mean that it's not worth trying! I just have to make sure to schedule my time well for me to complete my Beyond MVP while also making sure to study for my AP Exams. I've done that before, so I can do that again!

## EDP
Currently, I am on steps 6 and 7 of the Engineering Designing Program, which is testing the prototype and improving on it if needed. Since I'm done with the MVP, I have to keep on testing the game to see if it's good enough for presenting at the expo, and I can improve it further either by fixing some stuff or even working on the Beyond MVP.

## Skills
Of course, as I was making the game, I learned some skills along the way. Here are some I learned.

### Balancing My Schedule
The first skill I learned was being able to balance my work schedule efficiently so I was able to do my project enough while also being able to complete all my other assignments in time. Around the time the marking period was ending, my teachers decide to give me big tests and exams to prepare for, which added to the stress I had already. However, with timing all my tasks carefully, plus making sure to take breaks in the meantime, I was able to finish all my assignments on time, so I was greatful for myself for being able to do some of my project at the end of it. I hope to continue this method some time.

### Don't Procrastanate
The second skill I learned is to not procrastanate. Due to extreme burn out, I suffered from not being able to do anything during the time I had, which is something that I regret doing. I ended up having not much time to spare, so I had to rush my project and do as much as I can in order to complete something working and viable enough. However, I was proud of myself for being able to do so much in so little time, and makes me wonder how much I could actually do if I gave myself the time. I now know that I _really_ shouldn't procrastonate next time.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
