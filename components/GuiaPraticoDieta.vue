<template>
  <div class="min-h-screen">
    <!-- Hero Section -->
    <section class="container mx-auto px-4 py-16 text-center">
      <h1 class="text-4xl md:text-6xl font-bold mb-6">Guia Prático de Dieta para Iniciantes na Musculação</h1>
      <p class="text-xl md:text-2xl mb-8">Transforme sua alimentação e otimize seus treinos</p>
      <button
        class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
        QUERO COMPRAR AGORA!
      </button>
    </section>

    <!-- Features Section -->
    <section class="bg-gray-800 py-16">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold mb-8 text-center">Tudo que você terá acesso:</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div v-for="(feature, index) in features" :key="index" class="bg-gray-700 p-6 rounded-lg">
            <component :is="feature.icon" class="w-12 h-12 mb-4 text-green-500" />
            <h3 class="text-xl font-semibold mb-2">{{ feature.title }}</h3>
            <p>{{ feature.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- About Author Section -->
    <section class="container mx-auto px-4 py-16">
      <h2 class="text-3xl font-bold mb-8 text-center">VOCÊ VAI APRENDER COM QUEM SABE!</h2>
      <div class="flex flex-col md:flex-row items-center">
        <img src="https://www.gravatar.com/avatar/2c7d99fe281ecd3bcd65ab915bac6dd5?s=300" alt="Saulo Alves"
          class="rounded-full w-64 h-64 object-cover mb-8 md:mb-0 md:mr-8" />
        <div>
          <h3 class="text-2xl font-semibold mb-4">Saulo Alves</h3>
          <p class="mb-4">Nutricionista, Bacharel em Direito, acadêmico de Educação Física e pós-graduado em Docência no
            Ensino Superior, Bodybuilding e Coaching.</p>
          <p>Com mais de seis anos de experiência como atleta de fisiculturismo e Coach, mais de 3000 pacientes, alunos
            e vidas mudadas. Ele já conquistou como treinador mais de 23 títulos overall e mais de 150 pódios em
            competições com seus atletas.</p>
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section class="bg-gray-800 py-16">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold mb-8 text-center">Veja o que meus pacientes estão dizendo sobre mim:</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div v-for="(testimonial, index) in testimonials" :key="index" class="bg-gray-700 p-6 rounded-lg">
            <p class="mb-4">{{ testimonial.content }}</p>
            <p class="font-semibold">- {{ testimonial.name }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing Section -->
    <section class="container mx-auto px-4 py-16 text-center">
      <h2 class="text-3xl font-bold mb-8">Você leva tudo isso por apenas:</h2>
      <p class="text-2xl mb-4">de R$ 57,90 por:</p>
      <p class="text-5xl font-bold mb-4">5X R$ 6,98</p>
      <p class="mb-8">ou à vista por 34,90</p>
      <button
        class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full text-lg transition duration-300 ease-in-out transform hover:scale-105">
        QUERO COMPRAR AGORA!
      </button>
      <p class="mt-4 text-sm">Ambiente 100% seguro</p>
    </section>

    <!-- FAQ Section -->
    <section class="bg-gray-800 py-16">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold mb-8 text-center">Perguntas frequentes</h2>
        <div class="space-y-4">
          <div v-for="(faq, index) in faqs" :key="index" class="bg-gray-700 p-6 rounded-lg">
            <h3 class="text-xl font-semibold mb-2">{{ faq.question }}</h3>
            <p>{{ faq.answer }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 py-8">
      <div class="container mx-auto px-4 text-center">
        <p class="mb-4">CRN: 18186</p>
        <p class="mb-4">Copyright 2025. Todos os direitos reservados.</p>
        <div class="flex justify-center space-x-4 mb-4">
          <a href="#" class="text-white hover:text-green-500">
            <InstagramIcon />
          </a>
          <a href="#" class="text-white hover:text-green-500">
            <FacebookIcon />
          </a>
        </div>
        <p>Rua Padre Pedro Ribeiro, 120 - Salesianos, Juazeiro do Norte - CE, 63050-017</p>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { BookOpenIcon, DumbbellIcon, ScaleIcon, AppleIcon, PillIcon, ActivityIcon, InstagramIcon, FacebookIcon } from 'lucide-vue-next'

const features = ref([
  { icon: BookOpenIcon, title: 'Dieta Flexível', description: 'Balanço calórico, calcular suas necessidades calóricas, melhorar seus resultados com base nas suas calorias.' },
  { icon: AppleIcon, title: 'Como se alimentar', description: 'Proteínas, carboidratos, gorduras, fibras, micro e macronutrientes.' },
  { icon: PillIcon, title: 'Suplementação', description: 'Quando e porque usar suplemento, principais tipos de suplementos, whey e creatina.' },
  { icon: ScaleIcon, title: 'Manipulação de dieta', description: 'Ganhar peso, perder peso, bulking e cutting (Noções básicas).' },
  { icon: DumbbellIcon, title: 'Treinamento Físico', description: 'Musculação, estrutura do treino, quando mudar o treino e volume do treino.' },
  { icon: ActivityIcon, title: 'Resultados', description: 'Acompanhe sua evolução e alcance seus objetivos.' },
])

const testimonials = ref([
  { name: 'João Silva', content: 'O guia do Saulo transformou minha abordagem à musculação. Recomendo!' },
  { name: 'Maria Oliveira', content: 'Finalmente entendi como balancear minha dieta. Resultados incríveis!' },
  { name: 'Pedro Santos', content: 'As dicas de suplementação fizeram toda a diferença no meu treino.' },
])

const faqs = ref([
  { question: 'Como funciona o prazo de entrega?', answer: 'O e-book é entregue instantaneamente após a confirmação do pagamento.' },
  { question: 'Posso pagar por boleto ou pix?', answer: 'Sim, oferecemos diversas formas de pagamento, incluindo boleto e pix.' },
  { question: 'Como acessar o produto?', answer: 'Você receberá um e-mail com as instruções de acesso após a compra.' },
  { question: 'Consigo ter resultados com o E-book?', answer: 'Sim! Seguindo as orientações do guia, você terá uma base sólida para alcançar seus objetivos na musculação.' },
])
</script>