---
title: Button (infrastructure de ruban Windows)
description: Le bouton est un contrôle sur lequel l’utilisateur peut cliquer pour fournir une entrée à une application.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102645"
---
# <a name="button-windows-ribbon-framework"></a>Button (infrastructure de ruban Windows)

Le bouton est un contrôle sur lequel l’utilisateur peut cliquer pour fournir une entrée à une application.

-   [Introduction](#introduction)
-   [Propriétés du bouton](#button-properties)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

La capture d’écran suivante contient trois exemples de l’élément Button du ruban.

![capture d’écran des contrôles Button dans le ruban de Microsoft WordPad.](images/controls/button.png)

## <a name="button-properties"></a>Propriétés du bouton

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle bouton.

En général, une propriété de bouton est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle Button.



| Clé de propriété                                                                                             | Notes                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IU-au-dessus \_ \_ activé](windowsribbon-reference-properties-uipkey-enabled.md)                               | Prend en charge [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [KeyTip de l’interface utilisateur \_ \_](windowsribbon-reference-properties-uipkey-keytip.md)                                 | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [\_Étiquette de nom de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-label.md)                                   | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)             | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ LARGEIMAGE](windowsribbon-reference-properties-uipkey-largeimage.md)                         | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)                         | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bibliothèque de contrôles de l’infrastructure du ruban Windows](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage de bouton**](windowsribbon-element-button.md)
</dt> </dl>

 

 
