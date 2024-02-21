<template>

</template>

<script lang="ts">
export default {
  setup() {

    type product = {
      name: string,
      price: number,
      quantity: number
    }

    const products: Array<product> = [
      { name: 'Футболка', price: 20, quantity: 2 },
      { name: 'Джинсы', price: 50, quantity: 1 },
      { name: 'Носки', price: 5, quantity: 10 },
      { name: 'Штаны', price: 30, quantity: 1 }
    ];

    const accum = (value:string):string => {
      const valueArr: Array<string> = value.toLowerCase().split('');
      const length:number = valueArr.length;
      let result:string = '';
      if(length) {
        for (let i = 0; i < length; i++) {
          for (let q = 0; q <= i; q++) {
            if (q < 1) result += valueArr[i].toUpperCase();
            else result += valueArr[i];
            if (q === i && i < length - 1) result += '-';
          }
        }
      }
      return result
    }

    const amountOfRevenue = (value: Array<product>):number => {
      let amount:number = 0;
      value.forEach(item => {
        if (item.price && item.quantity) amount += item.price * item.quantity
      });
      return amount
    }

    amountOfRevenue(products);
    accum("abed");
    accum("RqaEzty");
    accum("cwAt");

  }
}

</script>

<style scoped>

</style>