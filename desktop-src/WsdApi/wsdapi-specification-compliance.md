---
description: l’API WSDAPI (web services on devices) assure la prise en charge du profil des appareils pour les services web (DPWS) sur Windows Vista, ce qui permet la communication des services web (WS) entre les ordinateurs basés sur Windows et les périphériques connectés au réseau.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Conformité de la spécification WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dcf649d8d2771d17f24e983a739c0119a0fe8af67f70b706ba35bcddec20d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991389"
---
# <a name="wsdapi-specification-compliance"></a>Conformité de la spécification WSDAPI

l’API WSDAPI (web services on devices) assure la prise en charge du [profil des appareils pour les services web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) sur Windows Vista, ce qui permet la communication des services web (WS) entre les ordinateurs basés sur Windows et les périphériques connectés au réseau. DPWS assemble des spécifications WS de base, telles que [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)et [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), et les améliore ou les limite pour fournir un ensemble de fonctionnalités de base pour les appareils à ressources restreintes. Cette spécification de base contient les fonctionnalités requises, telles que la possibilité de décrire les propriétés de l’appareil via des métadonnées et des fonctionnalités facultatives, telles que la possibilité de rejeter des messages spécifiques pour des raisons de sécurité.

l’implémentation du WSDAPI dans Windows Vista est la première version de la prise en charge explicite de DPWS, et est une implémentation non managée de DPWS qui est distincte et distincte des autres implémentations de Services Web (telles que le [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) ou [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).

les rubriques suivantes présentent un intérêt pour les fabricants de périphériques et les autres implémenteurs d’appareils qui créent des appareils qui interagissent avec les clients et hôtes wsdapi basés sur Windows sans utiliser wsdapi. Ces rubriques décrivent l’implémentation de WSDAPI par rapport aux spécifications sous-jacentes. Elles couvrent l’implémentation des fonctionnalités requises, des fonctionnalités facultatives et des fonctionnalités supplémentaires non définies dans la spécification.

-   [Conformité de la spécification DPWS](dpws-specification-compliance.md)
-   [Conformité de la spécification WS-Discovery](ws-discovery-specification-compliance.md)
-   [Conformité des spécifications WS-MetadataExchange et WS-Transfer](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Fonctionnalités de WS-Discovery supplémentaires](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement de périphérique WSD](wsd-device-development.md)
</dt> <dt>

[Recommandations de l’implémentation des appareils WSD](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
