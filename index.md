### Overview
We  propose  a  Korean  singing  voice  synthe-sis  system  based  on  auto-regressive  generative  adversarialnetwork (GAN). In an end-to-end framework, the proposed system generates spectrogram from score and text information. Focusing on the difference between the speech synthesisand the singing voice synthesis problem, we develop a model based on GAN for singing voice synthesis. To solve discontinuity problem in conventional GAN,we proposed auto-regressive method for convolutional neuralnetwork (CNN). Additionally, We adopted boundary equilib-rium GAN objective to generates high quality spectrogram.

![Model Architecture Ver 5 small](https://user-images.githubusercontent.com/15067112/67159763-21cfa600-f384-11e9-905f-e5446dc44cc0.jpg)

### Results
<style>
table {
    display: inline-table
    table-layout:fixed;
    width: 100%;
}
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
        <th> 작은 별 <br> Twinkle Twinkle <br> Little Star </th>
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
        <th> 퐁당퐁당 <br> Plop Plop </th>
        <th> <audio controls id="player"><source src="assets/audios/ground/pong1_ground.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/recon/pong1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/model4/pong1_model4.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 마법의 성 <br> Magic Castle </th>
        <th> <audio controls id="player"><source src="assets/audios/ground/magic1_ground.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/recon/magic1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/model4/magic1_model4.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 빙고 <br> Bingo </th>
        <th> <audio controls id="player"><source src="assets/audios/ground/bingo1_ground.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/recon/bingo1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/model4/bingo1_model4.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 나비야 <br> Butterfly </th>
        <th> <audio controls id="player"><source src="assets/audios/ground/butterfly1_ground.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/recon/butterfly1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/model4/butterfly1_model4.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 알파벳 송 <br> Alphabet Song </th>
        <th> <audio controls id="player"><source src="assets/audios/ground/alpha1_ground.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/recon/alpha1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/model4/alpha1_model4.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 솜사탕 <br> Cotten Candy </th>
        <th> <audio controls id="player"><source src="assets/audios/ground/candy1_ground.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/recon/candy1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player"><source src="assets/audios/model4/candy1_model4.mp3" type="audio/mpeg"></audio> </th>
    </tr>
</table>