<template>
    <section class="contact-us p-5 bg-success text-white">
        <div class="row">
            <div class="col">
                <div class="card border-0 bg-transparent">
                    <div class="card-header">
                        <h2 class="card-title">📞 تواصل معنا</h2>
                    </div>
                    <div class="card-body text-end">
                        <form @submit.prevent="sendMessage">
                            <div class="mb-3">
                                <label class="text-light" for="name">الاسم:</label>
                                <input type="text" id="name" v-model="name" class="form-control">
                            </div>
                            <div class="mb-3">
                                <label class="text-light" for="email">البريد الإلكتروني:</label>
                                <input type="email" id="email" v-model="email" class="form-control">
                            </div>
                            <div class="mb-3">
                                <label class="text-light" for="message">رسالتك:</label>
                                <textarea id="message" v-model="message" class="form-control"></textarea>
                            </div>
                            <button type="submit" class="btn btn-warning">إرسال الرسالة</button>
                        </form>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card border-0 bg-transparent">
                    <div class="card-body">
                        <h4 class="text-muted"><font-awesome-icon icon="envelope" /> {{ $t('contact_section.email') }}</h4>
                        <h3 class="text-light">{{ ('contact@diamon-arrow.com') }}</h3>
                    </div>
                </div>
                <div class="card border-0 bg-transparent">
                    <div class="card-body">
                        <h4 class="text-muted"><font-awesome-icon icon="phone" /> {{ $t('contact_section.phone') }}</h4>
                        <h3 class="text-light" dir="ltr">{{ ('+249 99 123 1234') }}</h3>
                    </div>
                </div>
                <div class="card border-0 bg-transparent">
                    <div class="card-body">
                        <h4 class="text-muted"><font-awesome-icon icon="location-dot" /> {{ $t('contact_section.address') }}</h4>
                        <h3 class="text-light">{{ ('Khartoum, Sudan') }}</h3>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return { name: "", email: "", message: "" };
    },
    methods: {
        sendMessage() {
            alert(`تم إرسال رسالتك بنجاح، ${this.name}!`);
        }
    }
};
</script>