---
title: Bouton Drop-Down
description: Le bouton Drop-Down se compose d’un bouton qui affiche une liste déroulante d’éléments s’excluant mutuellement, lorsque l’utilisateur clique dessus.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887b5979d5536b255526789aa541a6f2d1b67d1b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473515"
---
# <a name="drop-down-button"></a>Bouton Drop-Down

Le bouton Drop-Down se compose d’un bouton qui affiche une liste déroulante d’éléments s’excluant mutuellement, lorsque l’utilisateur clique dessus.

-   [Détails](#details)
-   [Propriétés du bouton déroulant](#drop-down-button-properties)
-   [Rubriques connexes](#related-topics)

## <a name="details"></a>Détails

Ce contrôle est utile pour exposer des éléments étroitement liés dans les cas où aucune valeur par défaut évidente n’est disponible et où les éléments individuels peuvent être représentés par une image, du texte, ou les deux.

La capture d’écran suivante illustre le bouton Drop-Down du ruban dans un exemple de ruban.

![capture d’écran d’un contrôle DropDownButton dans un exemple de ruban.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a>Propriétés du bouton Drop-Down

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle bouton Drop-Down.

En règle générale, une Drop-Down propriété de bouton est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle bouton Drop-Down.




| Clé de propriété | Notes | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.<br /> Si tous les éléments enfants sont désactivés, l’infrastructure définit <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> sur false (0). Dans le cas contraire, si un ou plusieurs éléments enfants sont activés, UI_PKEY_Enabled a la valeur true (-1).<blockquote>[!Important]<br />La propriété <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> pour le contrôle de bouton Drop-Down doit être invalidée après l’activation ou la désactivation d’un ou plusieurs éléments enfants. Cela garantit que l’infrastructure interroge la valeur de propriété mise à jour et actualise l’état du contrôle de bouton Drop-Down dans l’interface utilisateur du ruban.</blockquote><br /><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.<blockquote>[!Note]<br />Si la commande associée au contrôle est invalidée via un appel à <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework :: InvalidateUICommand</strong></a>, le Framework interroge cette propriété lorsque <code>UI_INVALIDATIONS_VALUE</code> est passé comme valeur d' <em>indicateurs</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage DropDownButton**](windowsribbon-element-dropdownbutton.md)
</dt> </dl>
