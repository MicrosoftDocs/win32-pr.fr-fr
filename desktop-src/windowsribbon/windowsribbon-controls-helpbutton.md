---
title: Bouton aide
description: Le bouton aide est un contrôle sur lequel l’utilisateur peut cliquer pour afficher le système d’aide de l’application.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941009"
---
# <a name="help-button"></a><span data-ttu-id="2f4e0-103">Bouton aide</span><span class="sxs-lookup"><span data-stu-id="2f4e0-103">Help Button</span></span>

<span data-ttu-id="2f4e0-104">Le bouton aide est un contrôle sur lequel l’utilisateur peut cliquer pour afficher le système d’aide de l’application.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-104">The Help Button is a control that the user can click to display the application help system.</span></span>

-   [<span data-ttu-id="2f4e0-105">Détails</span><span class="sxs-lookup"><span data-stu-id="2f4e0-105">Details</span></span>](#details)
-   [<span data-ttu-id="2f4e0-106">Propriétés du bouton aide</span><span class="sxs-lookup"><span data-stu-id="2f4e0-106">Help Button Properties</span></span>](#help-button-properties)
-   [<span data-ttu-id="2f4e0-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f4e0-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="2f4e0-108">Détails</span><span class="sxs-lookup"><span data-stu-id="2f4e0-108">Details</span></span>

<span data-ttu-id="2f4e0-109">La capture d’écran suivante illustre le bouton aide du ruban.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-109">The following screen shot illustrates the Ribbon Help Button.</span></span>

![capture d’écran montrant le bouton aide.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a><span data-ttu-id="2f4e0-111">Propriétés du bouton aide</span><span class="sxs-lookup"><span data-stu-id="2f4e0-111">Help Button Properties</span></span>

<span data-ttu-id="2f4e0-112">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de bouton d’aide.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Help Button control.</span></span>

<span data-ttu-id="2f4e0-113">En général, une propriété de bouton d’aide est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="2f4e0-113">Typically, a Help Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="2f4e0-114">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="2f4e0-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="2f4e0-115">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="2f4e0-116">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="2f4e0-117">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="2f4e0-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="2f4e0-118">Le tableau suivant répertorie les clés de propriété associées au contrôle bouton d’aide.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-118">The following table lists the property keys that are associated with the Help Button control.</span></span>



| <span data-ttu-id="2f4e0-119">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="2f4e0-119">Property Key</span></span>                                                                                     | <span data-ttu-id="2f4e0-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2f4e0-120">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="2f4e0-121">KeyTip de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="2f4e0-121">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="2f4e0-122">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-122">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="2f4e0-123">\_Étiquette de nom de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="2f4e0-123">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="2f4e0-124">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-124">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="2f4e0-125">IU \_ \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="2f4e0-125">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="2f4e0-126">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-126">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="2f4e0-127">IU \_ \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="2f4e0-127">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="2f4e0-128">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="2f4e0-128">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2f4e0-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f4e0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f4e0-130">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="2f4e0-130">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="2f4e0-131">**Élément HelpButton**</span><span class="sxs-lookup"><span data-stu-id="2f4e0-131">**HelpButton element**</span></span>](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 