<template>
    <div class="code-area">
        <div class="area-left">
            <area-select :level='3' type='text' v-model="selected"></area-select>
        </div>
        <div class="area-right">
            <pre><code>{{selected}}</code></pre>
        </div>
        <div class="original-code" ref="original" v-if="shown">
            <pre><code><span>//返回值是一个数组，分别是省份行政区域文本</span><br /><span>&lt;</span>template<span>&gt;</span><br/>&nbsp;&nbsp;&nbsp;&nbsp;<span>&lt;</span>area-select&nbsp;:level='3' type='text'&nbsp;v-model='selected'&gt;&lt;/area-select&gt;<br/>&lt;</span>/template<span>&gt;</span></code></pre>
        </div>
        <div class="show-code" @click="toggle">
            {{this.shown ? 'Hide Code' : 'Show Code'}}
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                selected: [],
                shown: false
            }
        },
        methods: {
            toggle() {
                this.shown = !this.shown;
            }
        }
    };

</script>