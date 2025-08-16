---
title: Mobile Development
---
<nav>
  <a href="/">About</a>
  <a href="/ai">Artificial Intelligence</a>
  <a href="/software">Software Development</a>
  <a href="/network">Networking and Architecture</a>
  <a href="/mobile" class="active">Mobile Development</a>
  <a href="/other">Logical and Functional Programming</a>
</nav>

<style>
nav {
  display: flex;
  gap: 20px;
  margin-bottom: 40px;
}
nav a {
  color: #00ffff;
  text-decoration: none;
  font-weight: bold;
  padding: 6px 12px;
  border: 1px solid #00ffff;
  border-radius: 4px;
  transition: background 0.2s, color 0.2s;
  font-size: 13px;

}
nav a:hover {
  background: #00ffff;
  color: #000;
}
nav a.active {
  background: #00ff00;
  color: #000;
  border-color: #00ff00;
}
</style>

### Mobile Development

**(IOS)Power Level to Joules Calculator:**


<video controls="controls" src="vids/PowerLevelCalc.mp4">
    Your browser does not support the HTML5 Video element.
</video>


A quick and simple app developed using Dart and Flutter. Calculation credits to SeththeProgrammer. The App takes an input of a powerlevel, and then converts it into the amount of joules of force one is able to output using the Dragon Ball Anime feats as guidelines. When no feats are present, the joules output takes on a linear scale as that's how techniques like the kaioken work. Some quick feats it follows:

Master Roshi with a power level of 180 could blow up the moon, so the joules output would be greater or equal to the force needed to do that.

King Vegeta with a power level of 10000 could destroy 3 small planets with ease, so the joules output would be greater or equal to the force needed for that.

Cell is stated to be a solar system buster, so his power level, while not stated in the series, would be where the joules output would be big enough to wipe one out.



**(Android)BMI Calculator:**

<video controls="controls" src="vids/bmi.mp4">
    Your browser does not support the HTML5 Video element.
</video>


I Developed an Android App through the use of Android Studio. It calculates the BMI and gives proper advice
based on on the Department of Health and Human Services. The app allows users to enter their weight and
height in either customary or metric units. The activity will then shift depending on whether or not the user
wants advice from the app.