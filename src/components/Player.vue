<template>
    <li class="item --add">
        <i class="fas fa-user-circle"></i>
        <span class="item__data --name">
            <span>{{name.first}}</span>
            <span>{{name.last}}</span>
        </span>
        <span class="item__data --team"></span>
        <a class="item__delete --team" role="button">
            <i class="fas fa-trash-alt"></i>
        </a>
    </li>
</template>

<script>
export default {
    name: "Player",
    props: {
        name: Object,
    }
}
</script>

<style>

</style>
