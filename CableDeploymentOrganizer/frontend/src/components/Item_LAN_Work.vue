<template>
    <tr>
        <td>{{ lanWork.date }}</td>
        <td>{{ lanWork.adress}}</td>
        <td text-align: justify>{{ lanWork.description}}</td>
        <td>{{ lanWork.state}}</td>
        <td>{{ lanWork.author}}</td>
        <td>
            <div class="d-flex justify-content-center">
                <button class="btn btn-primary me-1" type="button">
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