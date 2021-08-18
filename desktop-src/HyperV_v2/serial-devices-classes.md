---
description: Les appareils série d’une machine virtuelle sont constitués de contrôleurs série et de ports série. Chaque ordinateur virtuel dispose d’un seul contrôleur série, et chaque contrôleur série a exactement deux ports série.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Classes d’appareils série
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b95a2baaf4bc3dacfddf0e18f6acd88379f958e49fc1ccbd5d6ee5cf49a11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746105"
---
# <a name="serial-devices-classes"></a>Classes d’appareils série

Les appareils série d’une machine virtuelle sont constitués de contrôleurs série et de ports série. Chaque ordinateur virtuel dispose d’un seul contrôleur série, et chaque contrôleur série a exactement deux ports série.

Les paramètres du contrôleur série ne sont pas configurables. par conséquent, aucune instance de données de paramètre n’est associée. En outre, vous ne pouvez pas ajouter ou supprimer des contrôleurs série ou des ports série d’une machine virtuelle. Par conséquent, il n’existe aucune instance de pool de ressources pour les appareils série.

Voici les classes WMI de virtualisation associées aux appareils série.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                      | Description                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSVM \_ SerialController**](msvm-serialcontroller.md)<br/>                         | Représente les fonctionnalités et la gestion du contrôleur série.<br/> |
| [**MSVM \_ SerialPort**](msvm-serialport.md)<br/>                                     | Représente un port série associé au contrôleur série.<br/>      |
| [**MSVM \_ SerialPortOnSerialController**](msvm-serialportonserialcontroller.md)<br/> | Associe un port série à un contrôleur série.<br/>                   |



 

 

 




