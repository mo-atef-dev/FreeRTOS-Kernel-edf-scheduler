# About The Project
This project a working implementation of an EDF (Earliest Deadline First) scheduler in FreeRTOS kernal. The project is part of Udacity's Advanced Embedded Systems Nanodegree.

The original FreeRTOS kernal repo can be found [here](https://github.com/FreeRTOS/FreeRTOS-Kernel).

![Udacity](https://img.shields.io/badge/Udacity-grey?style=for-the-badge&logo=udacity&logoColor=15B8E6)

## Uses
FreeRTOS V10.5.0

# License

Distributed under the MIT open source license.

# Usage

Just use this version of the kernal in your project. You can also copy `include/FreeRTOS.h` and `tasks.c` and overwrite them in your project.

For more details on using FreeRTOS in your project, you can check readme of **FreeRTOS kernal** repo [here](https://github.com/FreeRTOS/FreeRTOS-Kernel), or **FreeRTOS** repo [here](https://github.com/FreeRTOS/FreeRTOS).

## Asumptions
The period of the task is the deadline of the task.

## Code
To use the EDF scheduler:
1. Add the `#define configUSE_EDF_SCHEDULER    1` in `FreeRTOSConfig.h` to enable using the EDF scheduler.
2. Use `xTaskPeriodicCreate` function instead of `xTaskCreate` when creating tasks. An error will occur if `xTaskCreate` is used to create tasks while the EDF scheduler is enabled.
3. The task period is then provided (in number of ticks) as a parameter in `xTaskPeriodicCreate`.

# Contact

Mohamed Atef: mohamed.a13121998@gmail.com
