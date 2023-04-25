<template >
  <body class="bg-gray-400 m-0 sm:m-5" >
    <div class="bg-gray-300 sm:h-full md:h-screen border-solid border-black border-2 " >
      <h2 class="bg-gray-600  text-slate-100 text-3xl flex justify-center font-medium p-4"> List Of Products</h2>
      <div class=" grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 justify-items-center text-xl ">
        <ul v-for="product in products" :key="product.name" class="p-5 ">
          <li >Category : {{ product.category }}</li>
          <li>Name : {{ product.name }}</li>
          <li>Price : {{ product.price }}</li>
          <img :src="product.imageUrl" :alt="product.name" width="220">
        </ul>
      </div>
    </div>
  </body>
</template>

<script setup>

  const data = [
    {
      a1: "Phone",
      b1: "Apple iPhone 13",
      c1: 999,
      d1: "https://shop.unicornstore.in/uploads/images/full/10bb152089499515e46bbdfaba61ac9e.png"
    },
    {
      a1: "Laptop",
      b1: "Dell XPS 15",
      c1: 1499,
      d1: "https://i.dell.com/is/image/DellContent//content/dam/images/products/laptops-and-2-in-1s/xps/15-7590-touch/xp7590t-cnb-00055rf110-gy.psd?fmt=png-alpha&pscan=auto&scl=1&hei=402&wid=402&qlt=100,1&resMode=sharp2&size=402,402&chrss=full"
    }
  ]
    /*absured keys with proper keys
      a1: category
      b1: name
      c1: price
      d1: imageUrl
    */  
    //Displaying with proper keys
    
  const products = computed(() => {
    return data.map(item => {
      return {
        category : item.a1,
        name : item.b1,
        price : item.c1,
        imageUrl: item.d1
      }
    })    
  })    
</script>