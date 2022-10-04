<template>
  <div>
    <Html class="h-full bg-gray-100">
        <Body>
          <div class="flex flex-col h-screen">
            <header>
              <TheTitle />
            </header>
            <main class="flex-grow">
              <slot />
            </main>
            <TheFooter></TheFooter>
          </div>
        </Body>
    </Html>
  </div>
</template>
      