### Overview
We  propose  a  Korean  singing  voice  synthe-sis  system  based  on  auto-regressive  generative  adversarialnetwork (GAN). In an end-to-end framework, the proposed system generates spectrogram from score and text information. Focusing on the difference between the speech synthesisand the singing voice synthesis problem, we develop a model based on GAN for singing voice synthesis. To solve discontinuity problem in conventional GAN,we proposed auto-regressive method for convolutional neuralnetwork (CNN). Additionally, We adopted boundary equilib-rium GAN objective to generates high quality spectrogram.

![Model Architecture Ver 5 2](https://user-images.githubusercontent.com/15067112/67158656-dadab400-f375-11e9-8bfc-5bc57a45c28a.jpg)

### Results
<style>
#player{
    width: 100%;
}
</style>

<!--
<style type="text/css">
.tg {border-collapse:collapse;border-spacing:0;}
.tg td{overflow:hidden;}
.tg th{overflow:hidden;}
</style>
-->

<table>
    <tr>
        <th> Song </th>
        <th> Ground Truth </th>
        <th> Reconstruction </th>
        <th> Generated </th>
    </tr>
    <tr>
        <th> 작은 별 <br> Twinkle Twinkle Little Star </th>
        <th> <audio controls id="player"><source src="assets/audios/ground/star1_ground.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/recon/star1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/model4/star1_model4.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 거미가 줄을 타고 <br> Itchy Bitsy Spider </th>
        <th> <audio controls id="player"><source src="assets/audios/ground/spider1_ground.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/recon/spider1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/model4/spider1_model4.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 나비야 <br> Butterfly </th>
        <th> <audio controls id="player"><source src="assets/audios/ground/butterfly1_ground.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/recon/butterfly1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/model4/butterfly1_model4.mp3" type="audio/mpeg"></audio> </th>
    </tr>
</table>