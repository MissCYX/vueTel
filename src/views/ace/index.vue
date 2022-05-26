<template>
    <div class="content">
        <editor
            ref="editors"
            :content="value"
            :theme="'monokai'"
            :lang="'html'"
            :config="config"
            @change="editorChange"
            :height="100"
        ></editor>
    </div>
</template>
<script>
import Editor from './aceEditor.vue'

export default {
    components: {
        Editor
    },
    data() {
        return {
            value: '',
            config: {
                font_size: 16,
                sql_atom: true
            }
        }
    },
    methods: {
        editorChange(data){
            console.log(data)
        }
    }
}
</script>
<style scoped>
.content{
    width: 100%;
    padding: 20px;
    height: 100%;
    min-height: 200px;
}
</style>



