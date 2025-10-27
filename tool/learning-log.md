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
* Also checked out Ren'Py and what tools they have to make visual novels, such as this [video](https://www.youtube.com/watch?v=C3Ldd-5PKCw)
* I will have to get started on making the art and the story soon

### 10/26/25:
* Ended up reviewing 2D game development on Unity with Game Academy, such as how to make players move and collide with other objects in the game, as shown in the code below
```c#
if (Input.GetKey(KeyCode.D))
       {
            playerFacing = 1;
            GetComponent<Transform>().position += rightMoveForce;
       }

       if (Input.GetKey(KeyCode.A))
       {
            playerFacing = -1;
            GetComponent<Transform>().position += leftMoveForce;
        }

       if (Input.GetKeyDown(KeyCode.W))
       {
            if (canJump == true)
            {
                canJump = false;
                GetComponent<Rigidbody2D>().AddForce(jumpForce);
            }
            else if (doubleJump == true)
            {

                GetComponent<Rigidbody2D>().AddForce(jumpForce);
                doubleJump = false;
            }
        }

```
* also reviewed old code on Game Academy with past projects
* have to learn on how to combine character dialogue and movement for the game
<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
