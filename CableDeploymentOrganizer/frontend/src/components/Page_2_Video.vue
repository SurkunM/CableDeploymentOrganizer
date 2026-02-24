<template>
    <div class="table-container">
        <h2 class="mb-4">Видеонаблюдение</h2>
        <table class="table table-bordered table-hover table-striped text-center">
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
                <item-video-work v-for="(videoWork, index) in videoWorks"
                                 :videoWork="videoWork"
                                 :index="index"
                                 :key="videoWork.id">
                </item-video-work>
            </tbody>
        </table>
    </div>
</template>

<script>
    import ItemVideoWork from "./Item_Video_Work.vue";

    export default {
        components: {
            ItemVideoWork
        },

        data() {
            return {
                videoWorks: [
                    { id: 1, date: "12.12.2026", adress: "Kommunisticheskiy 120", office: "212", description: "videoWorks videoWorks Монтаж монтаж Монтаж монтаж videoWorks монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж Монтаж монтаж ", state: "Выполняеться", author: "Ivanov A.V" },
                    { id: 2, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "videoWork svideo WorksvideoWorksСмонтировапть много много ыфоарыивариуриари арывиарукиаруи ариывраирыфиарыиа", state: "В очереди", author: "Ivanov A.V" },
                    { id: 3, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "videoWork svideo Worksvукиаруи ариывраирыфиарыиа", state: "В очереди", author: "Ivanov A.V" },
                    { id: 4, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "videoWork svideo WorksvideoWи ариывраирыфиарыиа", state: "В очереди", author: "Ivanov A.V" },
                    { id: 5, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "videoWork svideo Worksvного мнорыфиарыиа", state: "В очереди", author: "Ivanov A.V" },
                    { id: 6, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "videoWork svideo Workного ыфоарыивариуриари арывиарукиаруи ариывраирыфиарыиа", state: "В очереди", author: "Ivanov A.V" },
                    { id: 7, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "videoWork svideo WorksvideoWorого много ыфоарыивариуриари арывиарукиаруи ариывраирыфиарыиа", state: "В очереди", author: "Ivanov A.V" },
                    { id: 8, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "videoWork svideo WorksvideoWoго много ыфоарыивариуриари арывиарукиаруи ариывраирыфиарыиа", state: "В очереди", author: "Ivanov A.V" },
                    { id: 9, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "videoWork svideo Woарукиаруи ариывраирыфиарыиа", state: "В очереди", author: "Ivanov A.V" },
                    { id: 10, date: "12.12.2026", adress: "Choros-Gurkina 4", office: "212", description: "videoWork svideoиывраирыфиарыиа", state: "В очереди", author: "Ivanov A.V" }
                ]
            }
        }
    }
</script>