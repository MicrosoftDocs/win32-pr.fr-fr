---
description: L’interface IUpdateSession3 définit les méthodes suivantes.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Méthodes IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112159"
---
# <a name="iupdatesession3-methods"></a>Méthodes IUpdateSession3

L’interface [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) définit les méthodes suivantes.



| Méthode                                                                           | Description                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpdateServiceManager**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | Retourne un pointeur vers une interface [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) pour la session.                                                                                                                                                                                                                |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | Retourne un pointeur vers une interface [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) . L’interface contient des enregistrements d’événements correspondants sur l’ordinateur. Cela amène la méthode [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) à interroger de manière synchrone l’ordinateur sur l’historique des événements de mise à jour. |



 

Pour plus d’informations sur les membres hérités par cette interface, consultez les interfaces suivantes :

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



