---
description: L’API WSDAPI (Web Services on Devices) assure la prise en charge du profil des appareils pour les services Web (DPWS) sous Windows Vista, qui permet la communication des services Web (WS) entre les ordinateurs Windows et les périphériques connectés au réseau.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Conformité de la spécification WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202992"
---
# <a name="wsdapi-specification-compliance"></a>Conformité de la spécification WSDAPI

L’API WSDAPI (Web Services on Devices) assure la prise en charge du [profil des appareils pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) sous Windows Vista, qui permet la communication des services Web (WS) entre les ordinateurs Windows et les périphériques connectés au réseau. DPWS assemble des spécifications WS de base, telles que [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)et [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), et les améliore ou les limite pour fournir un ensemble de fonctionnalités de base pour les appareils à ressources restreintes. Cette spécification de base contient les fonctionnalités requises, telles que la possibilité de décrire les propriétés de l’appareil via des métadonnées et des fonctionnalités facultatives, telles que la possibilité de rejeter des messages spécifiques pour des raisons de sécurité.

L’implémentation du WSDAPI dans Windows Vista est la première version de la prise en charge explicite de DPWS, et est une implémentation non managée de DPWS qui est distincte et distincte des autres implémentations de services Web (telles que le [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) ou [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).

Les rubriques suivantes présentent un intérêt pour les fabricants de périphériques et les autres implémenteurs d’appareils qui créent des appareils qui interagissent avec les clients et hôtes WSDAPI basés sur Windows sans utiliser WSDAPI. Ces rubriques décrivent l’implémentation de WSDAPI par rapport aux spécifications sous-jacentes. Elles couvrent l’implémentation des fonctionnalités requises, des fonctionnalités facultatives et des fonctionnalités supplémentaires non définies dans la spécification.

-   [Conformité de la spécification DPWS](dpws-specification-compliance.md)
-   [Conformité de la spécification WS-Discovery](ws-discovery-specification-compliance.md)
-   [Conformité des spécifications WS-MetadataExchange et WS-Transfer](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Fonctionnalités de WS-Discovery supplémentaires](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement de périphérique WSD](wsd-device-development.md)
</dt> <dt>

[Recommandations en matière d’implémentation des appareils WSD](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
