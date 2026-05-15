# Image Conversation

Основная ветка намеренно оставлена минимальной.

Реализации задач разнесены по отдельным веткам:

- `feat/sequential_convolution` — последовательная свёртка.
- `feat/parallel_convolution` — параллельная свёртка поверх последовательной реализации.
- `feat/image_pipepline` — pipeline обработки изображений поверх параллельной реализации.
- `feat/gpgu_pipepline` — pipeline обработки изображений с параллельной реализацией, gpu и hybrid (gpu + cpu)
