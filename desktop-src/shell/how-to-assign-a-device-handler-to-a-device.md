---
description: Illustre le processus d’ajout d’un gestionnaire d’appareils à un appareil.
title: Comment affecter un gestionnaire d’appareils à un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16db6a39406e3d8ba7cd8b497e12883685b80d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973179"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Comment affecter un gestionnaire d’appareils à un appareil

Illustre le processus d’ajout d’un gestionnaire d’appareils à un appareil.

## <a name="instructions"></a>Instructions


Pour affecter un gestionnaire d’appareils à un appareil, sous la sous-clé des paramètres de l' **appareil** de l’instance de l’appareil, ajoutez une valeur de type **reg \_ SZ** nommée **DeviceHandlers**. L’entrée de données pour cette valeur est le nom du gestionnaire d’appareils.

Voici un exemple d’entrée pour un \_ appareil 0031 fictif 059&PID \_ .

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceHandlers = MyDeviceHandler
```

Les gestionnaires d’appareils peuvent également être affectés à l’aide des paramètres de [classe](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) d’appareil ou de [groupe](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) d’appareils.

 

 



