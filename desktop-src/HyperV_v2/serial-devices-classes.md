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
# <a name="serial-devices-classes"></a><span data-ttu-id="24924-104">Classes d’appareils série</span><span class="sxs-lookup"><span data-stu-id="24924-104">Serial devices classes</span></span>

<span data-ttu-id="24924-105">Les appareils série d’une machine virtuelle sont constitués de contrôleurs série et de ports série.</span><span class="sxs-lookup"><span data-stu-id="24924-105">The serial devices in a virtual machine consist of serial controllers and serial ports.</span></span> <span data-ttu-id="24924-106">Chaque ordinateur virtuel dispose d’un seul contrôleur série, et chaque contrôleur série a exactement deux ports série.</span><span class="sxs-lookup"><span data-stu-id="24924-106">Each virtual machine has exactly one serial controller, and each serial controller has exactly two serial ports.</span></span>

<span data-ttu-id="24924-107">Les paramètres du contrôleur série ne sont pas configurables. par conséquent, aucune instance de données de paramètre n’est associée.</span><span class="sxs-lookup"><span data-stu-id="24924-107">The settings for the serial controller are not configurable; therefore, there is no setting data instance associated with it.</span></span> <span data-ttu-id="24924-108">En outre, vous ne pouvez pas ajouter ou supprimer des contrôleurs série ou des ports série d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="24924-108">Also, you cannot add or remove serial controllers or serial ports from a virtual machine.</span></span> <span data-ttu-id="24924-109">Par conséquent, il n’existe aucune instance de pool de ressources pour les appareils série.</span><span class="sxs-lookup"><span data-stu-id="24924-109">Therefore, there are no resource pool instances for serial devices.</span></span>

<span data-ttu-id="24924-110">Voici les classes WMI de virtualisation associées aux appareils série.</span><span class="sxs-lookup"><span data-stu-id="24924-110">The following are virtualization WMI classes related to serial devices.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="24924-111">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="24924-111">In this section</span></span>



| <span data-ttu-id="24924-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="24924-112">Topic</span></span>                                                                                      | <span data-ttu-id="24924-113">Description</span><span class="sxs-lookup"><span data-stu-id="24924-113">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="24924-114">**MSVM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="24924-114">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)<br/>                         | <span data-ttu-id="24924-115">Représente les fonctionnalités et la gestion du contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="24924-115">Represents the capabilities and management of the serial controller.</span></span><br/> |
| [<span data-ttu-id="24924-116">**MSVM \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="24924-116">**Msvm\_SerialPort**</span></span>](msvm-serialport.md)<br/>                                     | <span data-ttu-id="24924-117">Représente un port série associé au contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="24924-117">Represents a serial port associated with the serial controller.</span></span><br/>      |
| [<span data-ttu-id="24924-118">**MSVM \_ SerialPortOnSerialController**</span><span class="sxs-lookup"><span data-stu-id="24924-118">**Msvm\_SerialPortOnSerialController**</span></span>](msvm-serialportonserialcontroller.md)<br/> | <span data-ttu-id="24924-119">Associe un port série à un contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="24924-119">Associates a serial port with a serial controller.</span></span><br/>                   |



 

 

 




