---
description: Appareils mobiles Windows prend en charge les propriétés de tâche suivantes.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Propriétés de la tâche (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539186"
---
# <a name="task-properties"></a><span data-ttu-id="8c341-103">Propriétés de la tâche</span><span class="sxs-lookup"><span data-stu-id="8c341-103">Task Properties</span></span>

<span data-ttu-id="8c341-104">Appareils mobiles Windows prend en charge les propriétés de tâche suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c341-104">Windows Portable Devices supports the following task properties.</span></span>



| <span data-ttu-id="8c341-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="8c341-105">Property</span></span>                         | <span data-ttu-id="8c341-106">VarType</span><span class="sxs-lookup"><span data-stu-id="8c341-106">VarType</span></span>        | <span data-ttu-id="8c341-107">Description</span><span class="sxs-lookup"><span data-stu-id="8c341-107">Description</span></span>                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c341-108">**propriétaire de la \_ tâche wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8c341-108">**WPD\_TASK\_OWNER**</span></span>             | <span data-ttu-id="8c341-109">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="8c341-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="8c341-110">Propriétaire de la tâche.</span><span class="sxs-lookup"><span data-stu-id="8c341-110">The owner of the task.</span></span>                                                                      |
| <span data-ttu-id="8c341-111">**pourcentage d’achèvement de la \_ tâche wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8c341-111">**WPD\_TASK\_PERCENT\_COMPLETE**</span></span> | <span data-ttu-id="8c341-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8c341-112">**VT\_UI4**</span></span>    | <span data-ttu-id="8c341-113">Nombre compris entre 0 et 100 qui spécifie le mode de réalisation de la tâche.</span><span class="sxs-lookup"><span data-stu-id="8c341-113">A number between 0 and 100 that specifies how complete the task is.</span></span>                         |
| <span data-ttu-id="8c341-114">**Date du rappel de la \_ tâche wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8c341-114">**WPD\_TASK\_REMINDER\_DATE**</span></span>    | <span data-ttu-id="8c341-115">**\_Date VT**</span><span class="sxs-lookup"><span data-stu-id="8c341-115">**VT\_DATE**</span></span>   | <span data-ttu-id="8c341-116">Valeur qui spécifie quand un rappel doit être envoyé pour effectuer la tâche, si elle n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="8c341-116">A value that specifies when a reminder should be sent to perform the task, if not complete.</span></span> |
| <span data-ttu-id="8c341-117">**État de la \_ tâche wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8c341-117">**WPD\_TASK\_STATUS**</span></span>            | <span data-ttu-id="8c341-118">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="8c341-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="8c341-119">Description de la chaîne de l’état de la tâche, par exemple, « en cours ».</span><span class="sxs-lookup"><span data-stu-id="8c341-119">A string description of the status of the task, for example, "In Progress".</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="8c341-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c341-120">Requirements</span></span>



| <span data-ttu-id="8c341-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c341-121">Requirement</span></span> | <span data-ttu-id="8c341-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c341-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c341-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c341-123">Header</span></span><br/> | <dl> <span data-ttu-id="8c341-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c341-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c341-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c341-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c341-126">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="8c341-126">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




