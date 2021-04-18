---
description: Les appareils série d’une machine virtuelle sont constitués de contrôleurs série et de ports série. Chaque ordinateur virtuel dispose d’un seul contrôleur série, et chaque contrôleur série a exactement deux ports série.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Classes d’appareils série
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519363"
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



 

 

 




