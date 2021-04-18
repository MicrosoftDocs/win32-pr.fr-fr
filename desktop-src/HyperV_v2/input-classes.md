---
description: Les périphériques d’entrée utilisateur sont représentés par ces classes. Une machine virtuelle est toujours associée à une instance de chaque classe.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Classes d’entrée
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519594"
---
# <a name="input-classes"></a><span data-ttu-id="64fd3-104">Classes d’entrée</span><span class="sxs-lookup"><span data-stu-id="64fd3-104">Input classes</span></span>

<span data-ttu-id="64fd3-105">Les périphériques d’entrée utilisateur sont représentés par ces classes.</span><span class="sxs-lookup"><span data-stu-id="64fd3-105">The user input devices are represented by these classes.</span></span> <span data-ttu-id="64fd3-106">Une machine virtuelle est toujours associée à une instance de chaque classe.</span><span class="sxs-lookup"><span data-stu-id="64fd3-106">A virtual machine always has one instance of each class associated with it.</span></span> <span data-ttu-id="64fd3-107">Ces appareils ne peuvent pas être ajoutés ou supprimés de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="64fd3-107">These devices may not be added or removed from the virtual machine.</span></span> <span data-ttu-id="64fd3-108">Par conséquent, il n’existe aucune instance de pool de ressources pour les périphériques clavier ou souris.</span><span class="sxs-lookup"><span data-stu-id="64fd3-108">Therefore, there are no resource pool instances for keyboard or mouse devices.</span></span>

<span data-ttu-id="64fd3-109">Les périphériques clavier et souris sont liés à l’ordinateur virtuel via l’Association [**MSVM \_ SystemDevice**](msvm-systemdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="64fd3-109">The keyboard and mouse devices are linked to the virtual machine through the [**Msvm\_SystemDevice**](msvm-systemdevice.md) association.</span></span> <span data-ttu-id="64fd3-110">Un ordinateur virtuel contient à la fois un périphérique PS2 et un périphérique de souris synthétique.</span><span class="sxs-lookup"><span data-stu-id="64fd3-110">A virtual machine contains both a PS2 and a synthetic mouse device.</span></span> <span data-ttu-id="64fd3-111">Un seul périphérique de pointage est actif à la fois.</span><span class="sxs-lookup"><span data-stu-id="64fd3-111">Only one pointing device is active at a time.</span></span>

<span data-ttu-id="64fd3-112">Voici les classes WMI de virtualisation associées à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="64fd3-112">The following are virtualization WMI classes related to input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="64fd3-113">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="64fd3-113">In this section</span></span>



| <span data-ttu-id="64fd3-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="64fd3-114">Topic</span></span>                                                          | <span data-ttu-id="64fd3-115">Description</span><span class="sxs-lookup"><span data-stu-id="64fd3-115">Description</span></span>                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="64fd3-116">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="64fd3-116">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)<br/>             | <span data-ttu-id="64fd3-117">Représente un périphérique clavier.</span><span class="sxs-lookup"><span data-stu-id="64fd3-117">Represents a keyboard device.</span></span><br/>        |
| [<span data-ttu-id="64fd3-118">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="64fd3-118">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)<br/>             | <span data-ttu-id="64fd3-119">Représente un périphérique de souris PS2.</span><span class="sxs-lookup"><span data-stu-id="64fd3-119">Represents a PS2 mouse device.</span></span><br/>       |
| [<span data-ttu-id="64fd3-120">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="64fd3-120">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)<br/> | <span data-ttu-id="64fd3-121">Représente un périphérique de souris synthétique.</span><span class="sxs-lookup"><span data-stu-id="64fd3-121">Represents a synthetic mouse device.</span></span><br/> |



 

 

 




