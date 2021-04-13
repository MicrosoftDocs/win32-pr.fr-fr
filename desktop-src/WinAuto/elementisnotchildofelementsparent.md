---
title: ElementIsNotChildOfElementsParent
description: ElementIsNotChildOfElementsParent
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380428"
---
# <a name="elementisnotchildofelementsparent"></a><span data-ttu-id="67238-103">ElementIsNotChildOfElementsParent</span><span class="sxs-lookup"><span data-stu-id="67238-103">ElementIsNotChildOfElementsParent</span></span>

## <a name="text"></a><span data-ttu-id="67238-104">Texte</span><span class="sxs-lookup"><span data-stu-id="67238-104">Text</span></span>

<span data-ttu-id="67238-105">L’élément n’est pas un enfant de son parent</span><span class="sxs-lookup"><span data-stu-id="67238-105">Element is not a child of it's parent</span></span>

## <a name="type"></a><span data-ttu-id="67238-106">Type</span><span class="sxs-lookup"><span data-stu-id="67238-106">Type</span></span>

<span data-ttu-id="67238-107">Error</span><span class="sxs-lookup"><span data-stu-id="67238-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="67238-108">Description</span><span class="sxs-lookup"><span data-stu-id="67238-108">Description</span></span>

<span data-ttu-id="67238-109">Lorsque la méthode [**\_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) est appelée sur l’élément enfant retourné par [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (à l’aide des \_ constantes de navigation NAVDIR firstChild ou NAVDIR \_ LastChild), l’élément parent retourné ne correspond pas à l’élément parent spécifié dans l’appel **accNavigate** .</span><span class="sxs-lookup"><span data-stu-id="67238-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

<span data-ttu-id="67238-110">Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.</span><span class="sxs-lookup"><span data-stu-id="67238-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="67238-111">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="67238-111">Possible causes</span></span>

<span data-ttu-id="67238-112">Implémentation MSAA incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="67238-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67238-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67238-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67238-114">**IAccessible :: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="67238-114">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="67238-115">**IAccessible :: \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="67238-115">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




