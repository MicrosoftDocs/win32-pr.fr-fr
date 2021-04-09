---
description: L’action BindImage lie chaque exécutable ou DLL qui doit être lié aux dll importées par celui-ci.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Action BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864438"
---
# <a name="bindimage-action"></a><span data-ttu-id="3185b-103">Action BindImage</span><span class="sxs-lookup"><span data-stu-id="3185b-103">BindImage Action</span></span>

<span data-ttu-id="3185b-104">L’action BindImage lie chaque exécutable ou DLL qui doit être lié aux dll importées par celui-ci.</span><span class="sxs-lookup"><span data-stu-id="3185b-104">The BindImage action binds each executable or DLL that must be bound to the DLLs imported by it.</span></span> <span data-ttu-id="3185b-105">L’action BindImage agit sur chaque fichier de la table [BindImage](bindimage-table.md) , mais uniquement sur ceux qui doivent être installés localement.</span><span class="sxs-lookup"><span data-stu-id="3185b-105">The BindImage action acts on each file in the [BindImage](bindimage-table.md) table, but only those that are to be installed locally.</span></span> <span data-ttu-id="3185b-106">Le programme d’installation calcule l’adresse virtuelle de chaque fonction importée à partir de toutes les dll, puis enregistre l’adresse virtuelle calculée dans la [*table d’adresses d’importation*](i-gly.md) (IAT) de l’image d’importation.</span><span class="sxs-lookup"><span data-stu-id="3185b-106">The installer computes the virtual address of each function imported from all DLLs, then saves the computed virtual address in the importing image's [*import address table*](i-gly.md) (IAT).</span></span>

<span data-ttu-id="3185b-107">L’action BindImage appelle en interne l’API Windows **BindImageEx** .</span><span class="sxs-lookup"><span data-stu-id="3185b-107">The BindImage Action internally calls the **BindImageEx** Windows API.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3185b-108">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="3185b-108">Sequence Restrictions</span></span>

<span data-ttu-id="3185b-109">L’action BindImage doit venir après l’action [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="3185b-109">The BindImage action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3185b-110">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="3185b-110">ActionData Messages</span></span>



| <span data-ttu-id="3185b-111">Champ</span><span class="sxs-lookup"><span data-stu-id="3185b-111">Field</span></span> | <span data-ttu-id="3185b-112">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="3185b-112">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="3185b-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3185b-113">\[1\]</span></span> | <span data-ttu-id="3185b-114">Identificateur de fichier de l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="3185b-114">File identifier of executable.</span></span> |



 

 

 



