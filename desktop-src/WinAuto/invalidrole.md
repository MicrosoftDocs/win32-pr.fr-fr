---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510602"
---
# <a name="invalidrole"></a><span data-ttu-id="b770e-103">InvalidRole</span><span class="sxs-lookup"><span data-stu-id="b770e-103">InvalidRole</span></span>

## <a name="text"></a><span data-ttu-id="b770e-104">Texte</span><span class="sxs-lookup"><span data-stu-id="b770e-104">Text</span></span>

<span data-ttu-id="b770e-105">Le entier retourné par la fonction obtenir \_ accRole n’est pas une constante Role valide, système de rôle IE \_\_\*</span><span class="sxs-lookup"><span data-stu-id="b770e-105">The int returned from get\_accRole is not a valid role constant, ie ROLE\_SYSTEM\_\*</span></span>

## <a name="type"></a><span data-ttu-id="b770e-106">Type</span><span class="sxs-lookup"><span data-stu-id="b770e-106">Type</span></span>

<span data-ttu-id="b770e-107">Error</span><span class="sxs-lookup"><span data-stu-id="b770e-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="b770e-108">Description</span><span class="sxs-lookup"><span data-stu-id="b770e-108">Description</span></span>

<span data-ttu-id="b770e-109">Un élément signale un rôle MSAA non valide.</span><span class="sxs-lookup"><span data-stu-id="b770e-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="b770e-110">Par exemple, la méthode [**obtenir \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) retourne une valeur entière qui n’est pas mappée à une constante de rôle d’objet valide (par exemple, ListItem de système de rôle \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="b770e-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method returns an integer value that does not map to a valid object role constant (such as ROLE\_SYSTEM\_LISTITEM).</span></span>

<span data-ttu-id="b770e-111">Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car les éléments peuvent être identifiés incorrectement à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b770e-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="b770e-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="b770e-112">Possible causes</span></span>

<span data-ttu-id="b770e-113">Un rôle MSAA est défini de manière inappropriée pour l’élément ou son parent.</span><span class="sxs-lookup"><span data-stu-id="b770e-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b770e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b770e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b770e-115">**IAccessible :: \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="b770e-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="b770e-116">**Rôles d’objet**</span><span class="sxs-lookup"><span data-stu-id="b770e-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




