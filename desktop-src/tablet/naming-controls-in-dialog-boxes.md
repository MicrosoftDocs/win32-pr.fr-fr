---
description: Lorsque vous utilisez les boîtes de dialogue Microsoft Windows, vous devez étiqueter tous les contrôles pour faciliter la fonctionnalité vocale. La boîte de dialogue Exécuter suivante affiche une étiquette de contrôle de texte statique pour une zone de liste déroulante. Le texte statique se termine par un signe deux-points.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Nommer des contrôles dans les boîtes de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565160"
---
# <a name="naming-controls-in-dialog-boxes"></a>Nommer des contrôles dans les boîtes de dialogue

Lorsque vous utilisez les boîtes de dialogue Microsoft Windows, vous devez étiqueter tous les contrôles pour faciliter la fonctionnalité vocale. La boîte de dialogue **exécuter** suivante affiche une étiquette de contrôle de texte statique pour une zone de liste déroulante. Le texte statique se termine par un signe deux-points.

![capture d’écran montrant la boîte de dialogue Exécuter](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

Il existe deux types de contrôles :

-   Les contrôles qui ont leurs légendes comme propriété de ce contrôle, tels que les boutons de commande et les cases à cocher. Les aides à l’accessibilité n’ont aucun problème pour identifier ces contrôles tant que la légende est correctement définie.
-   Les contrôles qui n’ont pas leurs propres légendes, tels que les contrôles d’édition, les zones de liste et les affichages de liste, doivent être étiquetés à l’aide de contrôles de texte statique distincts. Pour plus d’informations sur les contrôles qui n’ont pas leurs propres légendes, consultez [contrôles sans propriétés de légende](controls-without-caption-properties.md).

Plusieurs techniques peuvent être utilisées pour surmonter les situations dans lesquelles les contrôles n’ont pas leurs propres légendes, mais elles ne sont effectives que pour les fenêtres qui sont affichées par le gestionnaire de boîtes de dialogue standard (SDM). Toutes les autres fenêtres doivent exposer les noms et les relations entre les contrôles en prenant explicitement en charge Microsoft Active Accessibility. Pour plus d’informations sur Active Accessibility, consultez la section [accessibilité](/windows/desktop/accessibility) de MSDN Library.

 

 
