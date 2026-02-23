<template>
    <div class="request-form-container">
        <h2 class="mb-4">Новая заявка</h2>

        <form @submit.prevent="submitForm">
            <div class="mb-3">
                <label for="address" class="form-label">Адрес</label>
                <input type="text"
                       class="form-control"
                       id="address"
                       v-model="formData.address"
                       placeholder="Введите адрес объекта"
                       required>
            </div>

            <div class="mb-3">
                <label for="description" class="form-label">Описание работы</label>
                <textarea class="form-control"
                          id="description"
                          rows="3"
                          v-model="formData.description"
                          placeholder="Опишите, что нужно сделать..."
                          required></textarea>
            </div>

            <div class="row mb-3">
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

                <!-- Автор -->
                <div class="col-md-6">
                    <label for="author" class="form-label">Автор</label>
                    <input type="text"
                           class="form-control"
                           id="author"
                           v-model="formData.author"
                           placeholder="Ваше имя"
                           required>
                </div>
            </div>

            <div class="d-grid gap-2">
                <button type="submit" class="btn btn-primary btn-lg">Отправить заявку</button>
            </div>
        </form>

        <!-- Блок для тестового вывода (можно удалить потом) -->
        <div v-if="submittedData" class="mt-4 p-3 bg-success text-white rounded">
            <h5>Данные отправлены (Тест):</h5>
            <pre>{{ submittedData }}</pre>
        </div>
    </div>
</template>

<script setup>
    import { ref, reactive } from 'vue';

    // Реактивный объект для хранения полей формы
    const formData = reactive({
        address: '',
        description: '',
        status: 'Новая', // Значение по умолчанию
        author: ''
    });

    // Переменная для отображения результата (для теста)
    const submittedData = ref(null);

    const submitForm = () => {
        // 1. Получаем текущую дату и время
        const now = new Date();

        // Форматируем дату в красивый вид (ГГГГ-ММ-ДД ЧЧ:ММ)
        // Можно использовать также toLocaleDateString('ru-RU')
        const currentDate = now.toISOString().slice(0, 10) + ' ' + now.toTimeString().slice(0, 5);

        // 2. Собираем итоговый объект
        const payload = {
            date: currentDate,
            address: formData.address,
            description: formData.description,
            status: formData.status,
            author: formData.author
        };

        // 3. Тут будет логика отправки в Store или на бэкенд
        console.log("Отправка данных:", payload);

        // Для демонстрации сохраняем в переменную, чтобы увидеть на экране
        submittedData.value = payload;

        // Очистка формы (опционально)
        // formData.address = '';
        // formData.description = '';
        // formData.author = '';
    };
</script>

<style scoped>
        /*
      Если вы хотите использовать только Bootstrap, этот блок можно удалить.
      Но я добавил ограничение ширины, чтобы форма не была слишком широкой на больших экранах.
    */
        .request-form-container {
            max-width: 600px;
            margin: 0 auto; /* Центрирование формы */
        }
</style>