---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310150"
---
# <a name="variantnotint-checkrole"></a><span data-ttu-id="565cb-103">VariantNotInt (CheckRole)</span><span class="sxs-lookup"><span data-stu-id="565cb-103">VariantNotInt (CheckRole)</span></span>

## <a name="text"></a><span data-ttu-id="565cb-104">Texte</span><span class="sxs-lookup"><span data-stu-id="565cb-104">Text</span></span>

<span data-ttu-id="565cb-105">La variante retournée par {0} doit être un {1} , mais est un {2} .</span><span class="sxs-lookup"><span data-stu-id="565cb-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="565cb-106">Type</span><span class="sxs-lookup"><span data-stu-id="565cb-106">Type</span></span>

<span data-ttu-id="565cb-107">Error</span><span class="sxs-lookup"><span data-stu-id="565cb-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="565cb-108">Description</span><span class="sxs-lookup"><span data-stu-id="565cb-108">Description</span></span>

<span data-ttu-id="565cb-109">Un élément signale un rôle MSAA non valide.</span><span class="sxs-lookup"><span data-stu-id="565cb-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="565cb-110">Par exemple, la méthode [**obtenir \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) utilisée pour récupérer le rôle MSAA d’un élément doit retourner une valeur entière qui représente l’une des constantes de rôle MSAA, mais qui retourne une autre variante à la place.</span><span class="sxs-lookup"><span data-stu-id="565cb-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method used to retrieve the MSAA role of an element should return an integer value that represents one of the MSAA role constants, but is returning another variant instead.</span></span>

<span data-ttu-id="565cb-111">Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car les éléments peuvent être identifiés incorrectement à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="565cb-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="565cb-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="565cb-112">Possible causes</span></span>

<span data-ttu-id="565cb-113">Un rôle MSAA est défini de manière inappropriée pour l’élément ou son parent.</span><span class="sxs-lookup"><span data-stu-id="565cb-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="565cb-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="565cb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="565cb-115">**IAccessible :: \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="565cb-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="565cb-116">**Rôles d’objet**</span><span class="sxs-lookup"><span data-stu-id="565cb-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




