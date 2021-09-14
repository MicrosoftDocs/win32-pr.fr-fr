---
title: Bouton aide
description: Le bouton aide est un contrôle sur lequel l’utilisateur peut cliquer pour afficher le système d’aide de l’application.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234803"
---
# <a name="help-button"></a>Bouton aide

Le bouton aide est un contrôle sur lequel l’utilisateur peut cliquer pour afficher le système d’aide de l’application.

-   [Détails](#details)
-   [Propriétés du bouton aide](#help-button-properties)
-   [Rubriques connexes](#related-topics)

## <a name="details"></a>Détails

La capture d’écran suivante illustre le bouton aide du ruban.

![capture d’écran montrant le bouton aide.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>Propriétés du bouton aide

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de bouton d’aide.

En général, une propriété de bouton d’aide est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle bouton d’aide.



| Clé de propriété                                                                                     | Notes                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [KeyTip de l’interface utilisateur \_ \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Peut uniquement être mis à jour par le biais d’une invalidation. |
| [\_Étiquette de nom de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-label.md)                           | Peut uniquement être mis à jour par le biais d’une invalidation. |
| [IU \_ \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Peut uniquement être mis à jour par le biais d’une invalidation. |
| [IU \_ \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Peut uniquement être mis à jour par le biais d’une invalidation. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément HelpButton**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 