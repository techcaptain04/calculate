<!-- create an invisible audio player -->
<script lang="ts">
    let audioPlayer: HTMLAudioElement;
    
    $: if (audioPlayer) {
        audioPlayer.currentTime = 1.75;
        setTimeout(() => {
            audioPlayer.play();
        }, 1000);
        audioPlayer.play();
    }
</script>
<style scoped>
    audio {
        display: none;
    }
</style>

<audio
 bind:this={audioPlayer}
 src="./pixies.wav" 
 controls
/>