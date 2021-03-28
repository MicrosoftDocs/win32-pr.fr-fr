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
# <a name="how-to-assign-a-device-handler-to-a-device"></a><span data-ttu-id="c5ed4-103">Comment affecter un gestionnaire d’appareils à un appareil</span><span class="sxs-lookup"><span data-stu-id="c5ed4-103">How to Assign a Device Handler to a Device</span></span>

<span data-ttu-id="c5ed4-104">Illustre le processus d’ajout d’un gestionnaire d’appareils à un appareil.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-104">Illustrates the process for adding a device handler to a device.</span></span>

## <a name="instructions"></a><span data-ttu-id="c5ed4-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="c5ed4-105">Instructions</span></span>


<span data-ttu-id="c5ed4-106">Pour affecter un gestionnaire d’appareils à un appareil, sous la sous-clé des paramètres de l' **appareil** de l’instance de l’appareil, ajoutez une valeur de type **reg \_ SZ** nommée **DeviceHandlers**.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-106">To assign a device handler to a device, under the **Device Parameters** subkey of the device instance, add a value of type **REG\_SZ** named **DeviceHandlers**.</span></span> <span data-ttu-id="c5ed4-107">L’entrée de données pour cette valeur est le nom du gestionnaire d’appareils.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-107">The data entry for this value is the name of the device handler.</span></span>

<span data-ttu-id="c5ed4-108">Voici un exemple d’entrée pour un \_ appareil 0031 fictif 059&PID \_ .</span><span class="sxs-lookup"><span data-stu-id="c5ed4-108">The following is an example entry for a fictitious Vid\_059&Pid\_0031 device.</span></span>

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

<span data-ttu-id="c5ed4-109">Les gestionnaires d’appareils peuvent également être affectés à l’aide des paramètres de [classe](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) d’appareil ou de [groupe](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) d’appareils.</span><span class="sxs-lookup"><span data-stu-id="c5ed4-109">Device handlers can also be assigned by using [device group](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) or [device class](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) settings.</span></span>

 

 



