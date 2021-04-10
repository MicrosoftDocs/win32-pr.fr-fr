---
title: Interfaces NDF
description: Les interfaces suivantes peuvent être utilisées pour étendre les fonctionnalités des classes d’assistance Microsoft qui sont identifiées comme extensibles.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028483"
---
# <a name="ndf-interfaces"></a>Interfaces NDF

Les interfaces suivantes peuvent être utilisées pour étendre les fonctionnalités des classes d’assistance Microsoft qui sont identifiées comme extensibles. Bien que cette fonctionnalité ne soit pas requise pour la plupart des applications, elle peut fournir des diagnostics et des résolutions plus spécifiques dans certains cas.

> [!Note]  
> Ces interfaces et leurs méthodes associées sont destinées aux développeurs qui implémentent leurs propres classes d’assistance tierces qui étendent les fonctionnalités NDF.

 



| Nom de l'interface                                                 | Description                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | Appelée par l’NDF pour la plupart des activités qui se produisent pendant un diagnostic.                                                     |
| [**INetDiagHelperEx**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | Appelé par l’NDF pour capturer et fournir des informations associées aux diagnostics et à la résolution des problèmes liés au réseau. |
| [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | Appelé par l’NDF pour confirmer qu’il contient des informations requises                                                           |
| [**INetDiagHelperUtilFactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | Réservé pour le système.                                                                                                 |



 

 

 




