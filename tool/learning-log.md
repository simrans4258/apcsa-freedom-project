# Tool Learning Log

## Tool: **Unity**

## Project: **visual novel + mini rpg? (still deciding to add rpg or not)**

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
if (Input.GetKey(KeyCode.D)) // checks to see if player is pressing D
{
    GetComponent<Transform>().position += rightMoveForce; //adds integer rightMoveForce to position
}
//same type of logic for A for left

if (Input.GetKey(KeyCode.A))
{
    GetComponent<Transform>().position += leftMoveForce;
}

if (Input.GetKeyDown(KeyCode.W)) //used for jump
{
    if (canJump == true) //checks boolean if canJump true (in context when you are on ground you are able to jump)
    {
        canJump = false; //sets it back to false
        GetComponent<Rigidbody2D>().AddForce(jumpForce); //adds force to the player to make it jump
    }
    else if (doubleJump == true) //if player is in sky, then they could jump
    {
        GetComponent<Rigidbody2D>().AddForce(jumpForce);
        doubleJump = false;
    }
}

```
* also reviewed old code on Game Academy with past projects
* have to learn on how to combine character dialogue and movement for the game

## 11/2/25:
* found this video about how to make a [dialogue system in unity](https://www.youtube.com/watch?v=1198z5dDc8g)
* also found this video about how to make [tilemaps](https://youtu.be/DTp5zi8_u1U?si=Nb5-lEFUKpmifbTi), which I might be using for my game
* experimented with old code and remembered how to do collision with other objects and destroy them, to get points for example:
```c#
void OnCollisionEnter2D(Collision2D collision)
{
    if(collision.gameObject.tag == "gem") //checks to see if player collided with object of that tab
    {
        gameManager.GetCompenent<GameManagerScript>().score += 1; //gets score that is variable stored in a game manager, which is a separate object
        Destroy(collision.gameObject); // destroys the gem, which is being collided with the player in this case
    }
}
```
* rather easy to remember as C# is very similar to Java
* will learn more on how to use more variety of code and more elements of Unity in the game
* also planning to use twinery.org to set up basic narrative of story soon
<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
