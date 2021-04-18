---
description: Les fonctions de téléphonie étendues sont répertoriées par catégorie dans les tableaux suivants.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Référence des services de téléphonie étendus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519305"
---
# <a name="extended-telephony-services-reference"></a>Référence des services de téléphonie étendus

Les fonctions de téléphonie étendues sont répertoriées par catégorie dans les tableaux suivants.

## <a name="extended-telephony-functions-for-line-devices"></a>Fonctions de téléphonie étendues pour les appareils de ligne



| Fonction                                                   | Description                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | Permet à une application de négocier une version d’extension à utiliser avec le périphérique de ligne spécifié. Asynchrone. |
| [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | Permet aux fournisseurs de services d’accéder aux fonctionnalités spécifiques à l’appareil qui ne sont pas proposées par d’autres fonctions TAPI. Synchronous. |
| [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | Envoie des fonctionnalités de commutateur spécifiques à l’appareil au commutateur. Asynchrone.                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a>Fonctions de téléphonie étendues pour les appareils téléphoniques



| Fonction                                                     | Description                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | Fonction d’échappement spécifique à l’appareil pour autoriser les extensions dépendantes du fournisseur. Asynchrone.                          |
| [**PhoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Permet à une application de négocier une version d’extension à utiliser avec l’appareil téléphonique spécifié. Synchronous. |



 

 

 



