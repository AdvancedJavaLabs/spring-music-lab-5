# Лабораторная работа: Автоматизация тестирования Spring Music с использованием Selenium

## Цели работы

- Освоить основы автоматизации тестирования веб-приложений с помощью Selenium WebDriver.
- Научиться применять паттерн Page Object для организации кода автотестов.
- На практике реализовать автоматические тесты для CRUD-функционала веб-приложения.

---

## Задание

### 1. Подготовка

- Соберите и запустите приложение локально:
  ```bash
  ./gradlew bootRun

### 2. Основная часть

* Протестируйте базовые сценарии работы приложения с помощью Selenium/JUnit
* Напишите автотесты, покрывающие следующие сценарии:
  * Добавление нового альбома:
    * Откройте главную страницу.
    * Перейдите к форме добавления альбома.
    * Заполните поля (используйте валидные данные), сохраните альбом.
    * Проверьте, что альбом появился в списке.
  * Редактирование альбома:
    * Найдите альбом из предыдущего шага.
    * Перейдите на его страницу редактирования.
    * Измените одно из полей (например, название альбома), сохраните изменения.
    * Проверьте, что изменения отобразились в списке.
  * Удаление альбома:
    * Найдите изменённый альбом.
    * Удалите его.
    * Проверьте, что альбом исчез из списка.
### 3. Требования к оформлению

* Для каждой страницы реализуйте отдельный Page Object класс.
* Каждый автотест должен быть независимым (используйте аннотации @Before/@After для подготовки и очистки данных).
* В коде тестов должны использоваться только методы Page Object-ов, а не прямые обращения к элементам через WebDriver.
