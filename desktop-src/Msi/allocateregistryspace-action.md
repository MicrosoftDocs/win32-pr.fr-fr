---
description: L’action AllocateRegistrySpace garantit que la quantité d’espace disponible dans le registre, spécifiée par la propriété AVAILABLEFREEREG, existe dans le registre.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Action AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521536"
---
# <a name="allocateregistryspace-action"></a><span data-ttu-id="5553f-103">Action AllocateRegistrySpace</span><span class="sxs-lookup"><span data-stu-id="5553f-103">AllocateRegistrySpace Action</span></span>

<span data-ttu-id="5553f-104">L’action AllocateRegistrySpace garantit que la quantité d’espace disponible dans le registre, spécifiée par la propriété [**AVAILABLEFREEREG**](availablefreereg.md) , existe dans le registre.</span><span class="sxs-lookup"><span data-stu-id="5553f-104">The AllocateRegistrySpace action ensures that the amount of free registry space specified by the [**AVAILABLEFREEREG**](availablefreereg.md) property exists in the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="5553f-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="5553f-105">Sequence Restrictions</span></span>

<span data-ttu-id="5553f-106">L’action AllocateRegistrySpace doit être appelée après [InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="5553f-106">The AllocateRegistrySpace action must be called after [InstallInitialize](installinitialize-action.md).</span></span> <span data-ttu-id="5553f-107">Il est recommandé de planifier le AllocateRegistrySpace avant toutes les autres actions pour vous assurer que l’espace disponible dans le Registre est suffisant pour continuer.</span><span class="sxs-lookup"><span data-stu-id="5553f-107">It is advisable to schedule the AllocateRegistrySpace before all other actions to ensure there is enough registry space available to continue.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="5553f-108">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="5553f-108">ActionData Messages</span></span>



| <span data-ttu-id="5553f-109">Champ</span><span class="sxs-lookup"><span data-stu-id="5553f-109">Field</span></span> | <span data-ttu-id="5553f-110">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="5553f-110">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="5553f-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5553f-111">\[1\]</span></span> | <span data-ttu-id="5553f-112">Espace du registre requis en Ko.</span><span class="sxs-lookup"><span data-stu-id="5553f-112">Registry space required in KB.</span></span> |



 

 

 



