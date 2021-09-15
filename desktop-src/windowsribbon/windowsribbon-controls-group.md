---
title: groupe (Windows Framework du ruban)
description: Le groupe organise les commandes et les contrôles associés au sein d’un onglet.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c153f8cd9d1fc0d2d2bdbaabab0b2e15e099e50d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525229"
---
# <a name="group-windows-ribbon-framework"></a>groupe (Windows Framework du ruban)

Le groupe organise les commandes et les contrôles associés au sein d’un [onglet](windowsribbon-controls-tab.md).

-   [Détails](#details)
-   [Propriétés de groupe](#group-properties)
-   [Rubriques connexes](#related-topics)

## <a name="details"></a>Détails

La capture d’écran suivante illustre le contrôle du groupe de ruban.

![capture d’écran avec légendes montrant un groupe.](images/controls/group.png)

## <a name="group-properties"></a>Propriétés de groupe

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de groupe.

En règle générale, une propriété de groupe est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle de groupe.




| Clé de propriété | Notes | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Peut uniquement être mis à jour par le biais d’une invalidation.<blockquote>[!Note]<br />L’infrastructure requiert que la valeur de <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> pour un contrôle de groupe commence par la lettre Z majuscule. Si la valeur fournie par l’application dans la méthode de rappel <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler :: UpdateProperty</strong></a> ne commence pas par la lettre Z, cette valeur est ignorée et une valeur est générée par l’infrastructure à la place. La valeur du Framework est la lettre Z suivie d’une valeur numérique commençant à 1 et qui s’incrémente séquentiellement, selon les besoins, pour les contrôles de groupe suivants (Z1, Z2,..., ZX).</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
</dt> <dt>

[**élément Group**](windowsribbon-element-group.md)
</dt> </dl>

