---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104558968"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a><span data-ttu-id="8e366-103">AccNavigate \_ ReturnedElementWithIncorrectParent</span><span class="sxs-lookup"><span data-stu-id="8e366-103">AccNavigate\_ReturnedElementWithIncorrectParent</span></span>

## <a name="text"></a><span data-ttu-id="8e366-104">Texte</span><span class="sxs-lookup"><span data-stu-id="8e366-104">Text</span></span>

<span data-ttu-id="8e366-105">Appel de accNavigate ((Live Search), 0, NAVDIR \_ firstChild) qui a renvoyé (x-gadget:///gadget.html) a retourné le parent incorrect ( \[ null \] ) et non (Live Search)</span><span class="sxs-lookup"><span data-stu-id="8e366-105">Calling accNavigate((Live Search), 0, NAVDIR\_FIRSTCHILD) which returned (x-gadget:///gadget.html) returned the incorrect parent(\[NULL\]) and not (Live Search)</span></span>

## <a name="type"></a><span data-ttu-id="8e366-106">Type</span><span class="sxs-lookup"><span data-stu-id="8e366-106">Type</span></span>

<span data-ttu-id="8e366-107">Error</span><span class="sxs-lookup"><span data-stu-id="8e366-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="8e366-108">Description</span><span class="sxs-lookup"><span data-stu-id="8e366-108">Description</span></span>

<span data-ttu-id="8e366-109">Lorsque la méthode [**\_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) est appelée sur l’élément enfant retourné par [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (à l’aide des \_ constantes de navigation NAVDIR firstChild ou NAVDIR \_ LastChild), l’élément parent retourné ne correspond pas à l’élément parent spécifié dans l’appel **accNavigate** .</span><span class="sxs-lookup"><span data-stu-id="8e366-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

![exemple d’implémentation MSAA non valide qui retourne un élément parent incorrect.](images/accchecker-invalid-msaa-parent.png)

<span data-ttu-id="8e366-111">Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.</span><span class="sxs-lookup"><span data-stu-id="8e366-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="8e366-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="8e366-112">Possible causes</span></span>

<span data-ttu-id="8e366-113">Implémentation MSAA incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="8e366-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e366-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e366-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e366-115">**IAccessible :: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="8e366-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="8e366-116">**IAccessible :: \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="8e366-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




