---
title: Groupe d’onglets
description: Un groupe d’onglets est un contrôle contextuel qui est masqué ou affiché au moment de l’exécution, en fonction de l’état d’un document ou d’un espace de travail. Le groupe d’onglets contient un ensemble de contrôles d’onglet liés au contexte.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316008"
---
# <a name="tab-group"></a>Groupe d’onglets

Un groupe d’onglets est un contrôle contextuel qui est masqué ou affiché au moment de l’exécution, en fonction de l’état d’un document ou d’un espace de travail. Le groupe d’onglets contient un ensemble de contrôles d' [onglet](windowsribbon-controls-tab.md) liés au contexte.

-   [Détails](#details)
-   [Propriétés du groupe d’onglets](#tab-group-properties)
-   [Rubriques connexes](#related-topics)

## <a name="details"></a>Détails

En règle générale, un groupe d’onglets s’affiche au cours d’États d’un document ou d’un espace de travail spécifique, par exemple lorsqu’un utilisateur sélectionne un type d’objet particulier. Par exemple, la sélection d’une image contenue dans l’en-tête d’une table peut nécessiter l’affichage de différents onglets contextuels qui exposent les fonctionnalités de la table et de l’image.

> [!IMPORTANT]
> Un groupe d’onglets ne prend pas en charge les [modes d’application](ribbon-applicationmodes.md). Toutefois, les contrôles d' [onglet](windowsribbon-controls-tab.md) individuels au sein d’un groupe d’onglets peuvent.

 

La capture d’écran suivante montre un [onglet](windowsribbon-controls-tab.md) contextuel de Windows 7 Paint.

![capture d’écran qui montre un contrôle d’onglet contextuel.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a>Propriétés du groupe d’onglets

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de groupe d’onglets.

En règle générale, une propriété de groupe d’onglets est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle de groupe d’onglets.



| Clé de propriété                                                                                     | Notes                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IU \_ \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md)     | Prend en charge [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [KeyTip de l’interface utilisateur \_ \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [\_Étiquette de nom de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-label.md)                           | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bibliothèque de contrôles de l’infrastructure du ruban Windows](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage TabGroup**](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 