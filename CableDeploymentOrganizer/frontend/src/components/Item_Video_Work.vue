<template>
    <tr>
        <td>{{ videoWork.date }}</td>
        <td>{{ videoWork.adress}}</td>
        <td text-align: justify>{{ videoWork.description}}</td>
        <td>{{ videoWork.state}}</td>
        <td>{{ videoWork.author}}</td>
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