---
title: Tab (infrastructure du ruban Windows)
description: Un onglet contient des groupes de contrôles connexes.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317077"
---
# <a name="tab-windows-ribbon-framework"></a>Tab (infrastructure du ruban Windows)

Un onglet contient des [groupes](windowsribbon-controls-group.md) de contrôles connexes.

-   [Détails](#details)
-   [Propriétés de l’onglet](#tab-properties)
-   [Rubriques connexes](#related-topics)

## <a name="details"></a>Détails

Il existe trois types d’onglets dans l’infrastructure du ruban.



| Type               | Description                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Onglet principal**       | Onglets principaux qui organisent les fonctions par défaut de l’application.                                                                                                                                                                                                                   |
| **Onglet contextuel** | Onglets qui s’affichent au cours de l’état d’un document ou d’un espace de travail spécifique. Par exemple, si un utilisateur sélectionne un type d’objet particulier, tel qu’une image contenue dans l’en-tête d’une table, différents onglets contextuels peuvent s’afficher et exposer les fonctionnalités de la table et de l’image. |
| **Onglet modal**      | Les onglets principaux qui s’affichent pendant un [mode d’application](ribbon-applicationmodes.md)de document ou d’espace de travail spécifique, tels que l’aperçu avant impression.                                                                                                                                        |



 

La capture d’écran suivante montre un onglet principal de Windows 7 Paint.

![capture d’écran qui montre un contrôle d’onglet principal.](images/controls/coretab.png)

## <a name="tab-properties"></a>Propriétés de l’onglet

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle onglet.

En général, une propriété de tabulation est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle Tab.



| Clé de propriété                                                                                     | Notes                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [\_Étiquette de nom de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-label.md)                           | Peut uniquement être mis à jour par le biais d’une invalidation. |
| [KeyTip de l’interface utilisateur \_ \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Peut uniquement être mis à jour par le biais d’une invalidation. |
| [IU \_ \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Peut uniquement être mis à jour par le biais d’une invalidation. |
| [IU \_ \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Peut uniquement être mis à jour par le biais d’une invalidation. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bibliothèque de contrôles de l’infrastructure du ruban Windows](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage Tab**](windowsribbon-element-tab.md)
</dt> </dl>

 

 
