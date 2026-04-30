# Image Conversation — Sequential Convolution

Ветка содержит первую задачу: последовательную свёртку одного изображения.

В составе ветки оставлены фильтры, загрузка/сохранение изображения, CLI, тестовые изображения и тесты последовательной реализации. Параллельная свёртка, thread pool и pipeline здесь намеренно отсутствуют, чтобы diff относительно `main` показывал только первую задачу.

## Сборка

```bash
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release -DBUILD_TESTING=OFF
cmake --build build --target app -j
```

## Пример запуска

```bash
./build/app -i input/sea.png -o output/sea.png -f gauss -h 5 -w 5 -s
```

## Тесты

```bash
cmake -S . -B build-tests -DCMAKE_BUILD_TYPE=Debug -DBUILD_TESTING=ON
cmake --build build-tests -j
ctest --test-dir build-tests --output-on-failure
```
