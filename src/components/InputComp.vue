<template>
    <div class="card">
        <div class="card-body">
            <textarea class="form-control" v-model="input"></textarea>
            <button class="btn btn-outline-info my-2" @click="sendPost()">Click</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "InputComp",
    data: () => {
        return {
            input:"",
        }
    },
    methods: {
        sendPost() {
            this.$emit("send-post", this.input);
        }
    }
}
</script>