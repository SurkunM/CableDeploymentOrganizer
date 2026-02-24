<template>
    <tr>
        <td>{{ lanWork.date }}</td>
        <td>{{ lanWork.adress}}</td>
        <td>{{ lanWork.office}}</td>
        <td>{{ lanWork.description}}</td>
        <td>{{ lanWork.state}}</td>
        <td>{{ lanWork.author}}</td>
        <td class="align-middle">
            <div class="d-flex justify-content-center">
                <button class="btn btn-secondary btn-sm" type="button">
                    Подробнее
                </button>
            </div>
        </td>
    </tr>
</template>

<script>
    export default {
        props: {
            lanWork: {
                type: Object,
                required: true
            },

            index: {
                type: Number,
                required: true
            }
        }
    }
</script>