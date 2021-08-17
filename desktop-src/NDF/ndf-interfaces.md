---
title: Interfaces NDF
description: Les interfaces suivantes peuvent être utilisées pour étendre les fonctionnalités des classes d’assistance Microsoft qui sont identifiées comme extensibles.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16ff5dde9246798392903f47370e663e26dd6be7f21252f8791bfee267018b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801949"
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



 

 

 




