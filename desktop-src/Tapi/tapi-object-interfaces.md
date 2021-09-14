---
description: L’objet TAPI est l’objet principal pour TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfaces d’objet TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416314"
---
# <a name="tapi-object-interfaces"></a>Interfaces d’objet TAPI

L' [objet TAPI](tapi-object.md) est l’objet principal pour TAPI 3.

L’interface [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) n’est pas directement exposée sur l’objet TAPI, mais est étroitement liée à celle-ci et est répertoriée ici pour des raisons de commodité de référence.



| Interfaces                                                 | Description                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | Interface TAPI principale 3.                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | Dérive de [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); fournit des méthodes supplémentaires qui prennent en charge les appareils téléphoniques.                                                         |
| [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | Interface sortante utilisée pour recevoir des informations asynchrones sur les événements TAPI 3.                                                                       |
| [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | Fournit une interface d’entrée dans les contrôles de centre d’appels.                                                                                                 |
| [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Fournit des méthodes pour récupérer des informations concernant les événements d’objet TAPI.                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Étend [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); fournit une méthode pour récupérer un pointeur vers l’objet Phone qui a provoqué l’événement d’objet TAPI. |



 

 

 
