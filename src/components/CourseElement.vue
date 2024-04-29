<template>
    <div class="flex gap-x-6 items-center">
        <div class="flex gap-x-6 items-center">
            <div class="w-40 h-40 rounded-full bg-[#767478] relative">
                <div class="w-36 h-36 rounded-full bg-white/80 blur-xl absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2"></div>
                <p class="font-Galindo text-white text-5xl absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">
                    1
                </p>
            </div>
            <div class="inline-block w-0 h-0 border-y-[20px]  border-solid border-y-transparent border-l-[40px] border-white blur-sm"></div>
        </div>
        <div>
            <slot></slot>
        </div>
    </div>
</template>