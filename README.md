# Image Conversation — Parallel Convolution

Ветка создана поверх `feat/sequential_convolution` и содержит вторую задачу: параллельную свёртку одного изображения.

Инкремент относительно последовательной ветки — общий рантайм свёртки и OpenMP-реализации разбиения по строкам, столбцам, пикселям и прямоугольным блокам. Pipeline для массива изображений в этой ветке отсутствует.

## Сборка

```bash
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release -DBUILD_TESTING=OFF
cmake --build build --target app -j
```

## Пример запуска

```bash
./build/app -i input/sea.png -o output/sea.png -f gauss -h 5 -w 5 -p rows
```

Доступные режимы: `rows`, `cols`, `pixels`, `grid`.
