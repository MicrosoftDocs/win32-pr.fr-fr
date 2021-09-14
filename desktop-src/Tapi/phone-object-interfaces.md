---
description: l’objet Téléphone est l’entité qui représente l’appareil téléphonique réel et tous ses contrôles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Téléphone Interfaces d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011085"
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



 

 

 



