---
description: Pour afficher une boîte de dialogue qui répertorie les objets de performance et les compteurs définis sur l’ordinateur, appelez la fonction PdhBrowseCounters.
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: Exploration des compteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4bae5ce5ae7a21ae247cf66515f7386b8d0265
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013906"
---
# <a name="browsing-counters"></a>Exploration des compteurs

Pour afficher une boîte de dialogue qui répertorie les objets de performance et les compteurs définis sur l’ordinateur, appelez la fonction [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) . La boîte de dialogue permet à l’utilisateur de parcourir et de sélectionner les compteurs de performances. Vous utilisez la structure de [**\_ navigation PDH \_ DLG \_**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) pour spécifier la configuration de la boîte de dialogue. Par exemple, vous pouvez configurer la boîte de dialogue pour retourner une sélection ou plusieurs sélections.

En entrée, le membre **szReturnPathBuffer** contient l’objet et le compteur de performance par défaut qui sont sélectionnés dans la boîte de dialogue. Lors de la sortie, la mémoire tampon contient l’objet de performance et le compteur sélectionnés par l’utilisateur. Vous pouvez également utiliser le membre **pCallback** pour spécifier une fonction de rappel pour traiter les noms de compteur retournés par la boîte de dialogue.

Notez que cette boîte de dialogue peut retourner \_ la boîte de dialogue PDH \_ annulée si **BSingleCounterPerDialog** a la **valeur false** et que l’utilisateur clique sur le bouton Fermer, votre gestion des erreurs devrait donc en tenir compte.

Pour obtenir un exemple qui utilise la fonction [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) , consultez [exploration des compteurs de performances](browsing-performance-counters.md).

Pour récupérer une liste d’objets de performance sur l’ordinateur, vous pouvez également appeler la fonction [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) . Pour récupérer une liste de compteurs et d’instances pour un objet de performance, appelez la fonction [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) . Vous pouvez également utiliser ces fonctions pour identifier les objets de performance et les compteurs contenus dans un fichier journal. Les appels répétés à **PdhEnumObjectItems** retournent la même liste de compteurs et d’instances jusqu’à ce que vous appeliez **PdhEnumObjects** pour actualiser d’abord la liste des objets de performance. Pour obtenir un exemple qui énumère les objets et les compteurs, consultez [énumération des objets de processus](enumerating-process-objects.md).

## <a name="selecting-the-data-source"></a>Sélection de la source de données

Vous pouvez utiliser [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) conjointement à [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) pour inviter l’utilisateur à choisir si la source de données est en temps réel ou à partir d’un fichier journal, et, s’il s’agit d’un fichier journal, son nom. Si vous ne souhaitez pas que la boîte de dialogue source de données s’affiche, vous pouvez appeler **PdhSelectDataSource** pour afficher uniquement le catalogue de l’Explorateur de fichiers. Pour ce faire, spécifiez \_ \_ l’Explorateur de fichiers des indicateurs PDH \_ \_ uniquement comme deuxième paramètre de l’appel à **PdhSelectDataSource**.

 

 



