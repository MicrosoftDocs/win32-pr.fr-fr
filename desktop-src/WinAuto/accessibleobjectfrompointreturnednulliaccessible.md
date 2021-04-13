---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c5807fa04f69271f2a2d38e7014b1cd17d4eaa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311230"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a><span data-ttu-id="146ef-103">AccessibleObjectFromPointReturnedNullIAccessible</span><span class="sxs-lookup"><span data-stu-id="146ef-103">AccessibleObjectFromPointReturnedNullIAccessible</span></span>

## <a name="text"></a><span data-ttu-id="146ef-104">Texte</span><span class="sxs-lookup"><span data-stu-id="146ef-104">Text</span></span>

<span data-ttu-id="146ef-105">AccessibleObjectFromPoint ( {0} , {1} ) a retourné la valeur null</span><span class="sxs-lookup"><span data-stu-id="146ef-105">AccessibleObjectFromPoint({0}, {1}) returned null</span></span>

## <a name="type"></a><span data-ttu-id="146ef-106">Type</span><span class="sxs-lookup"><span data-stu-id="146ef-106">Type</span></span>

<span data-ttu-id="146ef-107">Error</span><span class="sxs-lookup"><span data-stu-id="146ef-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="146ef-108">Description</span><span class="sxs-lookup"><span data-stu-id="146ef-108">Description</span></span>

<span data-ttu-id="146ef-109">L’adresse de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’élément d’interface utilisateur obtenue pour les coordonnées données est null.</span><span class="sxs-lookup"><span data-stu-id="146ef-109">The address of the UI element's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface obtained for the given coordinates is NULL.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="146ef-110">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="146ef-110">Possible causes</span></span>

-   <span data-ttu-id="146ef-111">L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.</span><span class="sxs-lookup"><span data-stu-id="146ef-111">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="146ef-112">Implémentation MSAA incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="146ef-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="146ef-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="146ef-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="146ef-114">Navigation via le test de positionnement et l’emplacement à l’écran</span><span class="sxs-lookup"><span data-stu-id="146ef-114">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[<span data-ttu-id="146ef-115">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="146ef-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




