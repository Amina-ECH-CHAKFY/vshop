<template>
    <div style="display: flex; align-items: flex-start; padding: 20px; gap: 20px;">
        <div>
            <img :src="imageUrl" alt="product_image" style="width: 300px; height: auto; object-fit: cover;" />
        </div>
        <div>
            <h1 style="margin-bottom: 10px;">{{ product.title }}</h1>
            <p style="margin-bottom: 20px; color: gray;">{{ product.description }}</p>
            <p><strong>Prix : </strong>{{ product.price }} €</p>
            <p><strong>Quantité en stock : </strong>{{ product.quantity }}</p>
            <p><strong>Catégorie : </strong>{{ product.category?.name || 'Non spécifiée' }}</p>
            <p><strong>Marque : </strong>{{ product.brand?.name || 'Non spécifiée' }}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        product: {
            type: Object,
            required: true,
        },
        imageUrl: {
            type: String,
            required: false,
        }
    },
};
</script>
