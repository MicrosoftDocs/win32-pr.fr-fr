---
description: L’action ResolveSource détermine l’emplacement de la source et définit la propriété SourceDir si la source n’a pas encore été résolue.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Action ResolveSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530189"
---
# <a name="resolvesource-action"></a><span data-ttu-id="482c6-103">Action ResolveSource</span><span class="sxs-lookup"><span data-stu-id="482c6-103">ResolveSource Action</span></span>

<span data-ttu-id="482c6-104">L’action ResolveSource détermine l’emplacement de la source et définit la propriété [**SourceDir**](sourcedir.md) si la source n’a pas encore été résolue.</span><span class="sxs-lookup"><span data-stu-id="482c6-104">The ResolveSource action determines the location of the source and sets the [**SourceDir**](sourcedir.md) property if the source has not been resolved yet.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="482c6-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="482c6-105">Sequence Restrictions</span></span>

<span data-ttu-id="482c6-106">L’action ResolveSource doit venir après l' [action CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="482c6-106">The ResolveSource action must come after the [CostInitialize action](costinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="482c6-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="482c6-107">ActionData Messages</span></span>

<span data-ttu-id="482c6-108">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="482c6-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="482c6-109">Notes</span><span class="sxs-lookup"><span data-stu-id="482c6-109">Remarks</span></span>

<span data-ttu-id="482c6-110">L’action ResolveSource doit être appelée avant d’utiliser la propriété [**SourceDir**](sourcedir.md) dans une expression.</span><span class="sxs-lookup"><span data-stu-id="482c6-110">The ResolveSource action must be called before using the [**SourceDir**](sourcedir.md) property in any expression.</span></span> <span data-ttu-id="482c6-111">Elle doit également être appelée avant la tentative de récupération de la valeur de la propriété **SourceDir** à l’aide de [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="482c6-111">It must also be called before attempting to retrieve the value of the **SourceDir** property using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="482c6-112">L’action ResolveSource ne doit pas être exécutée quand la source n’est pas disponible, comme c’est le cas lors de la désinstallation de l’application.</span><span class="sxs-lookup"><span data-stu-id="482c6-112">The ResolveSource action should not be executed when the source is unavailable, as it may be when uninstalling the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="482c6-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="482c6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="482c6-114">Résilience source</span><span class="sxs-lookup"><span data-stu-id="482c6-114">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



