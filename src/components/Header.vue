<template>
    <div>
        <h2>Quotes Added</h2>
        <div class="progress-bar">
            <div class="progress" :style="'width:' + (quotesLength * 10) + '%'">
                  {{ quotesLength + ' / 10' }}
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            quotesLength: {
                type: Number,
                required: true
            }
        }
    }
</script>

<style scoped>
    .progress,
    .progress-bar {
        height: 20px;
        border-radius: 5px;
    }

    .progress-bar {
        background-color: #ccc;
        width: 100%;

    }

    .progress {
        background-color: blue;
    }
</style>