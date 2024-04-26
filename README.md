# **zzho8986_9106_Quiz8**
 
## **Part 1: Imaging Technique Inspiration**

![An image of low piano sound level](/assets/piano1.png)
Low sound level of piano

![An image of high piano sound level](/assets/piano2.png)
High sound level of piano

__*"Piano Piano"*__ by Adrien M & Claire B, a visual design that translates sounds into undulating lines. The artwork features two representations: one depicting a relatively static sound and another showing dynamic feedback. Each image consists of a single line. For the major project, this can be paired with Nasreen Mohamedi's __*"Untitled-1"*__ or Piet Mondrian's __*"Broadway Boogie Woogie"*__ to create a multi-dimensional exploration of auditory and visual interactions, thereby enriching the sensory experience.

## **Part 2: Coding Technique Exploration**

![An image of Low sound level](../zzho8986_9106_Quiz8/assets/sound1.png)
![An image of High sound level](../zzho8986_9106_Quiz8/assets/sound2.png)

The audio signal is captured via the code, then quantized and transformed into a digital signal. Input through the microphone generates shapes of varying sizes. Low volume levels produce small circles, while higher volumes expand the circle's radius, creating larger shapes. Utilizing this process can lead to more innovative designs!

For example, artwork can be converted into a dot matrix pattern, with the size of the dots adjusted based on the audio signal. Additionally, incorporating more design elements, such as random factors or setting the image to match the audio's high and low frequencies, will make the visual effect more structured and appealing.

According to the code obtained from the [Working with sounds and speech in P5.js](https://medium.spatialpixel.com/sounds-bd05429aba38), this website contains many methods for using audio in p5.js.

**Here is the code used from the link:**
```
let mic;

function setup() {
  createCanvas(400, 400);
  mic = new p5.AudioIn();
  mic.start();
}

function draw() {
  background(0);

  let volume = mic.getLevel(); 
  let circleSize = map(volume, 0, 1, 20, 400); 
  ellipse(width / 2, height / 2, circleSize, circleSize);
}
```