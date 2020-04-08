---
layout: post
title: STM32 unique device IDs
---

Today I learnt that a 96-bit unique device ID is factory-coded into STM32 microcontrollers. 
These device IDs can be used for anything from serial numbers to security keys. 
However, one might need a device id with less bits - Enter the STM32 system hardware driver, **stm32l0xx_hw.c**.

The driver contains a **HW_GetUniqueId( uint8_t *id )** function(which takes as input, a pointer to an array that will contain the ID number) to generator an 8-element array of 32-bit integers which can be used as required to generate a unique id of up to 64-bit. This can of course be extended to obtain any integer with any number of bits up to 96.

My use case was to generate a unique LoRa device EUI for the Nucleo-L073RZ MCU + Semtech SX1272MB2xAS LoRa® extension board. The device EUI is necessary for the setup and connection of the node device to a gateway connected to The Things Network(TTN).
