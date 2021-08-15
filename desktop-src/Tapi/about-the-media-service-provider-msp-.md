---
description: Un fournisseur de services multimédia (MSP) TAPI 3 permet à une application un contrôle considérable sur les supports pour un mécanisme de transport particulier.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: À propos du fournisseur de services multimédia (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f6113fa6c5fcceddaf379894d5680cbdccccec5be228041967dabb11fcc2caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872922"
---
# <a name="about-the-media-service-provider-msp"></a>À propos du fournisseur de services multimédia (MSP)

Un fournisseur de services multimédia (MSP) TAPI 3 permet à une application un contrôle considérable sur les supports pour un mécanisme de transport particulier. Un MSP existe toujours associé à un fournisseur de services de téléphonie (TSP). Tout comme un TSP est une couche d’abstraction pour le contrôle d’appel, le MSP contrôle les médias sans avoir besoin de codage spécifique à l’appareil. Pour obtenir un exemple de communication MSP/TSP, consultez [vue d’ensemble du fournisseur de services TAPI](./tapi-service-provider-overview.md).

Un MSP permet le contrôle multimédia via l’utilisation d’interfaces de terminal, de flux et de sous-flux spéciales définies par l’interface TAPI. Le diagramme dans [à propos des contrôles d’appel et des médias](about-call-and-media-controls.md) illustre la façon dont ces interfaces apparaissent dans une application TAPI 3.

En outre, un MSP peut implémenter des [interfaces privées spécifiques au fournisseur](provider-specific-interfaces.md), que l’interface TAPI regroupera sur les objets standard exposés à une application. par exemple, microsoft IPConf MSP, qui est installé avec microsoft Windows 2000, implémente l’interface [**ITParticipant**](itparticipant.md) , qui fournit des contrôles pour les membres individuels d’une conférence.

La rubrique suivante décrit brièvement les MSP qui peuvent être installés avec un système d’exploitation Microsoft. Pour plus d’informations sur la configuration et l’utilisation, consultez le kit de ressources pour la plateforme cible.

D’autres fournisseurs de services multimédias tiers peuvent être écrits pour des protocoles particuliers ou pour des appareils physiques. L' [interface MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-.md) décrit les interfaces qui doivent être implémentées pour permettre à un MSP d’interagir avec les composants de Microsoft Telephony.

 

 
