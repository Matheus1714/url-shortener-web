<template>
    <div class="card-wrapper">
        <slot></slot>
    </div>
</template>

<style scoped>
  .card-wrapper{
    min-width: 20rem;
    height: 30rem;

    padding: 2rem;
    border-radius: 4px;

    background: var(--card-color);

    box-shadow: 0 0 4px var(--purple),
                0 0 8px var(--purple),
                0 0 16px var(--purple),
                0 0 32px var(--purple);
    
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  @media (width < 700px) {
    .card-wrapper{
      min-width: 100%;
    }
  }
</style>