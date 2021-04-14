---
title: NullParent
description: NullParent
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765217f8d2d46645358d590c5a93310b04da01b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309869"
---
# <a name="nullparent"></a><span data-ttu-id="a6d94-103">NullParent</span><span class="sxs-lookup"><span data-stu-id="a6d94-103">NullParent</span></span>

## <a name="text"></a><span data-ttu-id="a6d94-104">Texte</span><span class="sxs-lookup"><span data-stu-id="a6d94-104">Text</span></span>

<span data-ttu-id="a6d94-105">Les éléments parents ont la valeur NULL</span><span class="sxs-lookup"><span data-stu-id="a6d94-105">Elements parent is NULL</span></span>

## <a name="type"></a><span data-ttu-id="a6d94-106">Type</span><span class="sxs-lookup"><span data-stu-id="a6d94-106">Type</span></span>

<span data-ttu-id="a6d94-107">Error</span><span class="sxs-lookup"><span data-stu-id="a6d94-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="a6d94-108">Description</span><span class="sxs-lookup"><span data-stu-id="a6d94-108">Description</span></span>

<span data-ttu-id="a6d94-109">La valeur NULL est retournée lorsque la méthode [**\_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) est appelée sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="a6d94-109">NULL is returned when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the element.</span></span> <span data-ttu-id="a6d94-110">La méthode **obtenir \_ accParent** doit retourner la valeur NULL uniquement lorsqu’elle est appelée sur l’élément racine de la cible de vérification.</span><span class="sxs-lookup"><span data-stu-id="a6d94-110">The **get\_accParent** method should return NULL only when called on the root element of the verification target.</span></span>

<span data-ttu-id="a6d94-111">Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.</span><span class="sxs-lookup"><span data-stu-id="a6d94-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a6d94-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="a6d94-112">Possible causes</span></span>

<span data-ttu-id="a6d94-113">Implémentation MSAA incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="a6d94-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6d94-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6d94-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6d94-115">**IAccessible :: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="a6d94-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="a6d94-116">**IAccessible :: \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="a6d94-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




