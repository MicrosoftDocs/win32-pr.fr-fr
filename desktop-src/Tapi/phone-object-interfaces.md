---
description: l’objet Téléphone est l’entité qui représente l’appareil téléphonique réel et tous ses contrôles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Téléphone Interfaces d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e146910b8184f35057843f20ad663e2be21d2c4844852e7cca3939e1e979d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873269"
---
# <a name="phone-object-interfaces"></a>Téléphone Interfaces d’objet

l’objet Téléphone est l’entité qui représente l’appareil téléphonique réel et tous ses contrôles.

les interfaces [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) et [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) ne sont pas directement exposées sur l’objet Téléphone, mais sont étroitement liées et sont répertoriées ici pour des raisons de commodité de référence.



| Interface                                                  | Description                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Autorise l’accès au périphérique téléphonique à un niveau comparable à celui disponible avec l’interface TAPI 2. API *x* C.                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Fournit des méthodes pour le contrôle automatique des tonalités et des anneaux d’un téléphone, et pour la gestion automatique des appels basée sur l’État hookswitch d’un téléphone. |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Récupère la description des événements de téléphone.                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Énumère [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).                                                                                                    |



 

 

 



