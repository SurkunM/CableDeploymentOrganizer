<template>
    <tr>
        <td>{{ videoWork.date }}</td>
        <td>{{ videoWork.adress}}</td>
        <td>{{ videoWork.office}}</td>
        <td>{{ videoWork.description}}</td>
        <td>{{ videoWork.state}}</td>
        <td>{{ videoWork.author}}</td>
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
            videoWork: {
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