<template>
    <div class="row">
        <div class="col-sm-12">
            <h2>Quotes Added</h2>
            <div class="progress">
                <div class="progress">
                    <div
                    class="progress-bar"
                    role="progressbar"
                    aria-valuenow="60"
                    aria-valuemin="0"
                    aria-valuemax="100"
                    :style="'width:' + (quotesLength * 10) + '%'">
                        {{ quotesLength + ' / 10' }}
                    </div>
                </div>
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