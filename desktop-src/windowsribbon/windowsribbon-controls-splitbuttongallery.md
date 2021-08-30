---
title: Galerie de boutons partagés
description: La bibliothèque de boutons partagés est un contrôle composite qui contient un bouton principal qui expose un seul élément ou une seule commande par défaut, et un bouton secondaire qui, lorsque vous cliquez dessus, affiche le reste de l’élément ou de la collection de commandes dans une liste déroulante mutuellement exclusive.
ms.assetid: c0fcfe72-d2e9-465d-941a-b3832b36b8c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d53bb751f9e734ad4ba7138146fc096e3f45377
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469326"
---
# <a name="split-button-gallery"></a>Galerie de boutons partagés

La bibliothèque de boutons partagés est un contrôle composite qui contient un bouton principal qui expose un seul élément ou une seule commande par défaut, et un bouton secondaire qui, lorsque vous cliquez dessus, affiche le reste de l’élément ou de la collection de commandes dans une liste déroulante mutuellement exclusive.

-   [Détails](#details)
-   [Propriétés de la bibliothèque du bouton partagé](#split-button-gallery-properties)
-   [Rubriques connexes](#related-topics)

## <a name="details"></a>Détails

Ce contrôle est utile pour exposer des éléments étroitement liés dans les cas où une valeur par défaut évidente est disponible et où les éléments individuels peuvent être représentés par une image, du texte, ou les deux.

La capture d’écran suivante illustre la Galerie du bouton partagé du ruban dans Microsoft Paint.

![capture d’écran d’un contrôle splitbuttongallery dans le ruban Microsoft Paint.](images/controls/splitbuttongallery.png)

## <a name="split-button-gallery-properties"></a>Propriétés de la bibliothèque du bouton partagé

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de la Galerie de boutons partagés.

En règle générale, une propriété de la bibliothèque de boutons partagés est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle de Galerie de boutons partagés.




| Clé de propriété | Notes | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(valide uniquement pour une galerie d’éléments)<br /> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.<blockquote>[!Note]<br />Si la commande associée au contrôle est invalidée via un appel à <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework :: InvalidateUICommand</strong></a>, le Framework interroge cette propriété lorsque <code>UI_INVALIDATIONS_VALUE</code> est passé comme valeur d' <em>indicateurs</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Élément de balisage SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)
</dt> <dt>

[Utilisation des galeries](ribbon-controls-galleries.md)
</dt> <dt>

[Exemple de Galerie](windowsribbon-gallerysample.md)
</dt> </dl>

