# angular
Заметки

Производительность:
Каледдарь, 365 элементов с динамическими классами.
Измерил средние (за 10 раз) интервалы создания элементов с [ngClass] и class="{{}}". 43.1 милисекунды против 27.5

class="{{  (day && !day.disabled) ? 'calendar__day' : 'calendar__day-disabled'}} {{isHover(day,i)}}" - 27.5ms

[ngClass]="[(day && !day.disabled) ? 'calendar__day' : 'calendar__day-disabled',  isHover(day,i)]" - 43.1ms
