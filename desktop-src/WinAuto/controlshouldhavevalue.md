---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196937"
---
# <a name="controlshouldhavevalue"></a><span data-ttu-id="261ef-103">ControlShouldHaveValue</span><span class="sxs-lookup"><span data-stu-id="261ef-103">ControlShouldHaveValue</span></span>

## <a name="text"></a><span data-ttu-id="261ef-104">Texte</span><span class="sxs-lookup"><span data-stu-id="261ef-104">Text</span></span>

<span data-ttu-id="261ef-105">Un contrôle avec le rôle {0} doit avoir une valeur, mais obtenir \_ accValue n’est pas implémenté</span><span class="sxs-lookup"><span data-stu-id="261ef-105">A control with role of {0} should have a value but get\_accValue is not implemented</span></span>

## <a name="type"></a><span data-ttu-id="261ef-106">Type</span><span class="sxs-lookup"><span data-stu-id="261ef-106">Type</span></span>

<span data-ttu-id="261ef-107">Error</span><span class="sxs-lookup"><span data-stu-id="261ef-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="261ef-108">Description</span><span class="sxs-lookup"><span data-stu-id="261ef-108">Description</span></span>

<span data-ttu-id="261ef-109">Un élément ne fournit pas de valeur comme prévu en fonction du rôle MSAA attribué, ce qui implique que l’élément n’a pas la méthode [**\_ accValue obtenue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) .</span><span class="sxs-lookup"><span data-stu-id="261ef-109">An element does not supply a value as expected based on the assigned MSAA role, implying that the element does not have the [**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) method implemented.</span></span> <span data-ttu-id="261ef-110">Par exemple, les rôles MSAA suivants doivent tous fournir une valeur.</span><span class="sxs-lookup"><span data-stu-id="261ef-110">For example, the following MSAA roles should all supply a value.</span></span>

-   <span data-ttu-id="261ef-111">\_ComboBox système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="261ef-111">ROLE\_SYSTEM\_COMBOBOX</span></span>
-   <span data-ttu-id="261ef-112">\_adresse IP du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="261ef-112">ROLE\_SYSTEM\_IPADDRESS</span></span>
-   <span data-ttu-id="261ef-113">\_lien système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="261ef-113">ROLE\_SYSTEM\_LINK</span></span>
-   <span data-ttu-id="261ef-114">système de rôle \_ \_ OUTLINEITEM</span><span class="sxs-lookup"><span data-stu-id="261ef-114">ROLE\_SYSTEM\_OUTLINEITEM</span></span>
-   <span data-ttu-id="261ef-115">\_PROGRESSBAR du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="261ef-115">ROLE\_SYSTEM\_PROGRESSBAR</span></span>
-   <span data-ttu-id="261ef-116">\_curseur système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="261ef-116">ROLE\_SYSTEM\_SLIDER</span></span>
-   <span data-ttu-id="261ef-117">\_SPINBUTTON du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="261ef-117">ROLE\_SYSTEM\_SPINBUTTON</span></span>
-   <span data-ttu-id="261ef-118">\_ScrollBar système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="261ef-118">ROLE\_SYSTEM\_SCROLLBAR</span></span>
-   <span data-ttu-id="261ef-119">\_texte du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="261ef-119">ROLE\_SYSTEM\_TEXT</span></span>

<span data-ttu-id="261ef-120">Ce problème est un problème pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un élément ayant une valeur intrinsèque doit pouvoir signaler cette valeur à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="261ef-120">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because an element that has an intrinsic value must be able to report that value to a user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="261ef-121">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="261ef-121">Possible causes</span></span>

<span data-ttu-id="261ef-122">Un rôle MSAA est défini de manière inappropriée pour l’élément ou son parent.</span><span class="sxs-lookup"><span data-stu-id="261ef-122">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="261ef-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="261ef-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="261ef-124">**IAccessible :: \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="261ef-124">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="261ef-125">**Rôles d’objet**</span><span class="sxs-lookup"><span data-stu-id="261ef-125">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




