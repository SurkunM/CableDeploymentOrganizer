<template>
    <form @submit.prevent="submitForm">
        <textarea></textarea>
        <input />

        <!-- Состояние -->
        <div class="col-md-6">
            <label for="status" class="form-label">Состояние</label>
            <select class="form-select" id="status" v-model="formData.status">
                <option value="Новая">Новая</option>
                <option value="В работе">В работе</option>
                <option value="Ожидание запчастей">Ожидание запчастей</option>
                <option value="Выполнено">Выполнено</option>
            </select>
        </div>
    </form>
</template>