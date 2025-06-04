<template>
    <section class="investment-opportunities p-5">
        <h2 class="text-center investment-label">💰 فرص الاستثمار المتاحة</h2>
        <div class="row">
            <div v-for="opportunity in investments" :key="opportunity.id" class="col-md-4">
                <div class="card">
                    <img :src="require('@/' + opportunity.image)" class="card-img-top recapt-image" alt="Investment">
                    <div class="card-body">
                        <h5 class="card-title">{{ opportunity.title }}</h5>
                        <p class="card-text">{{ opportunity.description }}</p>
                        <button class="btn btn-success">المزيد من التفاصيل</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
.recapt-image {
    height: 220px;
}
</style>

<script>
export default {
    data() {
        return {
            investments: [
                {
                    id: 1,
                    title: "مشروع الزراعة العضوية",
                    description: "استثمر في المزارع العضوية الصديقة للبيئة، بعائد سنوي يصل إلى 12%.",
                    image: "assets/images/farming.jpg"
                },
                {
                    id: 2,
                    title: "التكنولوجيا الزراعية الذكية",
                    description: "الاستثمار في أنظمة الزراعة الذكية لزيادة الإنتاج وتقليل التكاليف.",
                    image: "assets/images/technofarm.jpg"
                },
                {
                    id: 3,
                    title: "مشاريع الأسمدة و مكافحة الآفات ",
                    description: "الاستثمار في الأسمدة العضوية و أساليب المكافحة الحديثة الآفات لحصاد أكثر وفرة و جودة",
                    image: "assets/images/defend.jpg"
                }
            ]
        };
    }
};
</script>