# Tool Learning Log

## Tool: **Unity**

## Project: **visual novel thingy**

---

### 10/5/25:
* Ended up reviewing what I learned from Game Academy on how to code on Unity, such as making dialouge boxes, platformers, and such.
* found out about [this playlist](https://www.youtube.com/playlist?list=PLGSox0FgA5B58Ki4t4VqAPDycEpmkBd0i) that goes over how to make a visual novel in unity
* found out about old code I used for past projects involving unity at Game Academy, such as:
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
* I will have to get started on making the art and the story soon

### X/X/XX:
* Text


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
