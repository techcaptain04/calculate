<!-- create an invisible audio player -->
<script lang="ts">
    export let isPlaying: boolean;
    let audioPlayer: HTMLAudioElement;
    
    $: if (audioPlayer) {
        audioPlayer.currentTime = 1.75;
    }

    $: if (isPlaying) {
        audioPlayer && audioPlayer.play();
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