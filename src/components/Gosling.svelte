<script lang="ts">
  import Ryan from "../assets/ryan.jpg";
  export let result: number;
</script>


<style scoped>
    .gosling {
        flex-grow: 1;
        color: white;
        display: flex;
        width: 100%;
        -webkit-text-stroke-color: black;
    }
    .idk {
        font-size: 3rem;
        text-align: center;
        position: fixed;
        z-index: 999;
        left: 50%;
        transform: translateX(-50%);
        -webkit-text-stroke-width: 2px;
    }
    .ryan {
        flex-shrink: 0;
        width: 100%;
        min-height: 100%;
    }

    .ryan img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    .result {
        position: fixed;
        z-index: 999;
        right: 0;
        bottom: 0;
        padding-right: 1rem;
    }

    .result p {
        font-size: 1rem;
    }

    @media (max-width: 600px) {
        .idk {
            font-size: 2rem;
        }
        .result {
            padding-right: 0.5rem;
        }
        .result p {
            font-size: 10px;
        }
    }
</style>


<div class="gosling">
    <h1 class="idk">i don't know</h1>
    <div class="ryan">
        <img src={Ryan.src} alt="Ryan Gosling" />
    </div>
    <span class="result">
        <p>maybe {result} or something</p>
    </span>
</div>