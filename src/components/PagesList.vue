<template>
    <h4>Pages</h4>
    <table class="table table-striped table-hover">
        <thead>
            <tr>
                <th>Title</th>
                <th>Title</th>
                <th>Title</th>

            </tr>
        </thead>
        <tbody>
            <tr
            v-for="(page, index) in $pages.getAllPages()"
            >
            <td>{{ page.pageTitle}}</td>
            <td>{{ page.link.text}}</td>
            <td>{{ page.published ? 'yes' : 'no'}}</td>

            </tr>
        </tbody>
    </table>
</template>

<script setup>
import {ref, reactive} from 'vue';

const counter = ref(0);

function click(){
    counter.value ++;
    console.log(counter);
}

// function setup(){
//     return {
//         counter,
//         click
//     }
// }
// export default{
//     data(){
//         return {
//             counter : 0
//         };
//     },
//     methods: {
//         click(){
//             this.counter ++;
//         }
//     }
// }
</script>