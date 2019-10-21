
### Overview
<p align="justify">
In this post, we  introduce  a  Korean  singing  voice  synthesis  system  based  on  auto-regressive  generative  adversarialnetwork (GAN). In an end-to-end framework, the system generates spectrogram from score and text information. Focusing on the difference between the speech synthesisand the singing voice synthesis problem, we develop a model based on GAN for singing voice synthesis. To solve discontinuity problem in conventional GAN, we proposed auto-regressive method for convolutional neural network (CNN). Additionally, We adopted boundary equilibrium GAN objective to generates high quality spectrogram.
</p>

![Model Architecture Ver 5 small artboard 2](https://user-images.githubusercontent.com/15067112/67160811-804e5180-f38f-11e9-8304-1c99420d644a.jpg)
<p align="center">Figure.1 Overview of the proposed singing voice synthesis system.</p>

### Auto-Regressive Method
<p align="justify">
A fundamental issue in the image-based approach when it is applied to audio data is that the model can span only a short audio segment and therefore successive segments generated over time can be discontinuous. To address this problem, we propose an auto-regressive conditional GAN which uses spectrogram in a previous time step as input to produce spectrogram in the current time step. 
Following figure shows how auto-regressive (AR) method helps generating continuous spectrogram. Without AR method the model generates distinct images of spectrogram but with AR method spectrogram is generated refered to previous spectrogram. 
</p>

![Spectrograms for upload 2](https://user-images.githubusercontent.com/15067112/67160822-a4aa2e00-f38f-11e9-969e-6f2fd1b878eb.jpg)
<p align="center">Figure.2 Spectrogram from ground truth and generated spectrograms from the proposed system.</p>

### Results
<p align="justify">
We compared generated samples from the proposed model with ground truth samples and reconstructed samples. The ground truth samples are from original records and the reconstructed samples are processed same as generated samples to evaluate the sound quality loss from signal processing. 
</p>

<script>
function pauseOthers(ele) {
    $("audio").not(ele).each(function (index, audio) {audio.pause();});
}
</script>

<style>
.main-content table {
    display: inline-table;
}
table {
    table-layout:fixed;
    width: 100%;
    overflow: hidden;
}
#player{
    width: 100%;
}
</style>

<table>
    <tr>
        <th> Song </th>
        <th> Generated </th>
        <th> Reconstruction </th>
        <th> Ground Truth </th>
    </tr>
    <tr>
        <th> 작은 별 <br> Twinkle Twinkle <br> Little Star </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/model4/star1_model4.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/recon/star1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/ground/star1_ground.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 거미가 줄을 타고 <br> Itchy Bitsy Spider </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/model4/spider1_model4.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/recon/spider1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/ground/spider1_ground.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 퐁당퐁당 <br> Plop Plop </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/model4/pong1_model4.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/recon/pong1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/ground/pong1_ground.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 마법의 성 <br> Magic Castle </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/model4/magic1_model4.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/recon/magic1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/ground/magic1_ground.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 빙고 <br> Bingo </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/model4/bingo1_model4.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/recon/bingo1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/ground/bingo1_ground.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 나비야 <br> Butterfly </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/model4/butterfly1_model4.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/recon/butterfly1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/ground/butterfly1_ground.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 알파벳 송 <br> Alphabet Song </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/model4/alpha1_model4.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/recon/alpha1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/ground/alpha1_ground.mp3" type="audio/mpeg"></audio> </th>
    </tr>
    <tr>
        <th> 솜사탕 <br> Cotten Candy </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/model4/candy1_model4.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/recon/candy1_recon.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/audios/ground/candy1_ground.mp3" type="audio/mpeg"></audio> </th>
    </tr>
</table>