<template>
    <div class="table-container">
        <h2 class="mb-4 ms-1">Локальная сеть</h2>
        <table class="table table-bordered table-hover table-striped text-center table-fixed">
            <thead class="table-dark">
                <tr>
                     <th style="width: 5%;">Дата</th>
                    <th style="width: 15%;">Адрес</th>
                    <th style="width: 10%;">Кабинет</th>
                    <th style="width: 40%;">Описание работы</th>
                    <th style="width: 10%;">Состояние</th>
                    <th style="width: 10%;">Автор</th>
                    <th style="width: 10%;">Подробнее</th>
                </tr>
            </thead>
            <tbody>
                <item-lan-work v-for="(lanWork, index) in lanWorks"
                               :lanWork="lanWork"
                               :index="index"
                               :key="lanWork.id">
                </item-lan-work>
            </tbody>
        </table>
    </div>
</template>

<script>
    import ItemLanWork from "./Item_LAN_Work.vue";

    export default {
        components: {
            ItemLanWork
        },

        data() {
            return {
                lanWorks: [
                    { id: 1, date: "12.12.2026", adress: "Kommunisticheskiy 120", office: "212", description: "Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж ", state: "Выполняеться", author: "Ivanov A.V" },
                    { id: 2, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "Смонтировапть много много ыфоарыивариуриари арывиарукиаруи ариывраирыфиарыиа", state: "В очереди", author: "Ivanov A.V" }
                ]
            }
        }
    }
</script>