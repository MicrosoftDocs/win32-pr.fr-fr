---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311524"
---
# <a name="elementhasnoname"></a><span data-ttu-id="73af6-103">ElementHasNoName</span><span class="sxs-lookup"><span data-stu-id="73af6-103">ElementHasNoName</span></span>

## <a name="text"></a><span data-ttu-id="73af6-104">Texte</span><span class="sxs-lookup"><span data-stu-id="73af6-104">Text</span></span>

<span data-ttu-id="73af6-105">L’élément n’a pas de nom</span><span class="sxs-lookup"><span data-stu-id="73af6-105">Element has no name</span></span>

## <a name="type"></a><span data-ttu-id="73af6-106">Type</span><span class="sxs-lookup"><span data-stu-id="73af6-106">Type</span></span>

<span data-ttu-id="73af6-107">Error</span><span class="sxs-lookup"><span data-stu-id="73af6-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="73af6-108">Description</span><span class="sxs-lookup"><span data-stu-id="73af6-108">Description</span></span>

<span data-ttu-id="73af6-109">Un élément n’a pas de nom.</span><span class="sxs-lookup"><span data-stu-id="73af6-109">An element does not have a name.</span></span> <span data-ttu-id="73af6-110">Par exemple, l’élément n’a pas d’accName implémenté et une chaîne vide est retournée lorsque la méthode [**\_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) est utilisée pour récupérer le nom MSAA de l’élément.</span><span class="sxs-lookup"><span data-stu-id="73af6-110">For example, the element does not have accName implemented and an empty string is returned when the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method is used to retrieve the MSAA name of the element.</span></span>

<span data-ttu-id="73af6-111">Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un élément peut être mal identifié à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="73af6-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="73af6-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="73af6-112">Possible causes</span></span>

-   <span data-ttu-id="73af6-113">L’élément ou son parent n’a aucun nom ou étiquette.</span><span class="sxs-lookup"><span data-stu-id="73af6-113">The element or its parent has no name or label.</span></span>
-   <span data-ttu-id="73af6-114">Un [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) qui suggère que l’élément a un nom est assigné à l’élément.</span><span class="sxs-lookup"><span data-stu-id="73af6-114">The element is assigned an [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) that suggests the element have a name.</span></span>
-   <span data-ttu-id="73af6-115">L’élément qui a le focus ne doit pas recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="73af6-115">The element that has focus should not receive focus.</span></span> <span data-ttu-id="73af6-116">Par exemple, une étiquette ou un contrôle désactivé.</span><span class="sxs-lookup"><span data-stu-id="73af6-116">For example, a label or a disabled control.</span></span>
-   <span data-ttu-id="73af6-117">Un contrôle invisible a reçu le focus.</span><span class="sxs-lookup"><span data-stu-id="73af6-117">An invisible control has received focus.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73af6-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73af6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73af6-119">**IAccessible :: \_ accName**</span><span class="sxs-lookup"><span data-stu-id="73af6-119">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="73af6-120">Propriété Name</span><span class="sxs-lookup"><span data-stu-id="73af6-120">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




