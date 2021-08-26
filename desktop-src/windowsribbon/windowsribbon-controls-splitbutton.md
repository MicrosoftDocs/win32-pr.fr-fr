---
title: Bouton partagé
description: Le bouton partagé est un contrôle composite avec lequel l’utilisateur peut sélectionner une valeur par défaut liée à un bouton principal, ou sélectionner dans une liste de valeurs s’excluant mutuellement dans une liste déroulante liée à un bouton secondaire.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066a2275c49ad8d6dd32dd8ce4fd3d89956f204c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473755"
---
# <a name="split-button"></a>Bouton partagé

Le bouton partagé est un contrôle composite avec lequel l’utilisateur peut sélectionner une valeur par défaut liée à un bouton principal, ou sélectionner dans une liste de valeurs s’excluant mutuellement dans une liste déroulante liée à un bouton secondaire.

-   [Introduction](#introduction)
-   [Propriétés du bouton partagé](#split-button-properties)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Ce contrôle est utile pour exposer des éléments étroitement liés dans les cas où une valeur par défaut évidente est disponible et où les éléments individuels peuvent être représentés par une image, du texte, ou les deux.

La capture d’écran suivante illustre le bouton partagé du ruban.

![capture d’écran d’un contrôle SplitButton dans un exemple de ruban.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Propriétés du bouton partagé

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle bouton partagé.

En règle générale, une propriété de bouton partagé est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle bouton partagé.




| Clé de propriété | Notes | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.<br /> Si tous les éléments enfants sont désactivés, l’infrastructure définit <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> sur false (0). Dans le cas contraire, si un ou plusieurs éléments enfants sont activés, UI_PKEY_Enabled a la valeur true (-1).<blockquote>[!Important]<br />La propriété <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> du contrôle de bouton partagé doit être invalidée après l’activation ou la désactivation d’un ou plusieurs éléments enfants. Cela garantit que l’infrastructure interroge la valeur de propriété mise à jour et actualise l’état du contrôle bouton partagé dans l’interface utilisateur du ruban.</blockquote><br /><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Peut uniquement être mis à jour par le biais d’une invalidation. | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage SplitButton**](windowsribbon-element-splitbutton.md)
</dt> </dl>
