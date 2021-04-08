---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675662"
---
# <a name="accnameshouldnotcontainrole"></a><span data-ttu-id="a2d70-103">AccNameShouldNotContainRole</span><span class="sxs-lookup"><span data-stu-id="a2d70-103">AccNameShouldNotContainRole</span></span>

## <a name="text"></a><span data-ttu-id="a2d70-104">Texte</span><span class="sxs-lookup"><span data-stu-id="a2d70-104">Text</span></span>

<span data-ttu-id="a2d70-105">Le nom de l’élément ( {0} ) ne doit pas contenir le texte du rôle de l’élément ( {1} )</span><span class="sxs-lookup"><span data-stu-id="a2d70-105">Element's Name ({0}) should not contain the text of the Element's Role ({1})</span></span>

## <a name="type"></a><span data-ttu-id="a2d70-106">Type</span><span class="sxs-lookup"><span data-stu-id="a2d70-106">Type</span></span>

<span data-ttu-id="a2d70-107">Avertissement</span><span class="sxs-lookup"><span data-stu-id="a2d70-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="a2d70-108">Description</span><span class="sxs-lookup"><span data-stu-id="a2d70-108">Description</span></span>

<span data-ttu-id="a2d70-109">Le nom d’un élément intègre son rôle MSAA ou le type de contrôle UIA.</span><span class="sxs-lookup"><span data-stu-id="a2d70-109">The name of an element incorporates its MSAA role or UIA control type.</span></span> <span data-ttu-id="a2d70-110">Par exemple, cet avertissement peut se produire si la méthode [**\_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , qui est utilisée pour récupérer le nom MSAA d’un élément, retourne la valeur \_ « \_ ScrollBar système Role \_ \* ».</span><span class="sxs-lookup"><span data-stu-id="a2d70-110">For example, this warning can occur if the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method—which is used to retrieve the MSAA name of an element—returns "ROLE\_SYSTEM\_SCROLLBAR\_\*".</span></span>

<span data-ttu-id="a2d70-111">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car le rôle est lu deux fois, ou il peut être non significatif ou non intuitif pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a2d70-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the role will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a2d70-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="a2d70-112">Possible causes</span></span>

-   <span data-ttu-id="a2d70-113">Un nom ou une étiquette n’est pas assigné à l’élément ou à son parent.</span><span class="sxs-lookup"><span data-stu-id="a2d70-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="a2d70-114">L’élément ou son parent a un nom par défaut qui n’a pas été révisé à un nom convivial.</span><span class="sxs-lookup"><span data-stu-id="a2d70-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="a2d70-115">Par exemple, bouton 1.</span><span class="sxs-lookup"><span data-stu-id="a2d70-115">For example, button1.</span></span>
-   <span data-ttu-id="a2d70-116">Un développeur ne sait pas que les lecteurs d’écran lisent les noms.</span><span class="sxs-lookup"><span data-stu-id="a2d70-116">A developer is not aware that screen readers read names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2d70-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2d70-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d70-118">**IAccessible :: \_ accName**</span><span class="sxs-lookup"><span data-stu-id="a2d70-118">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="a2d70-119">Propriété Name</span><span class="sxs-lookup"><span data-stu-id="a2d70-119">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




