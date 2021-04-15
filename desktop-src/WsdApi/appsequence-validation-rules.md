---
description: AppSequence les informations contenues dans WS-Discovery annonce et les messages de réponse (Hello, messages ProbeMatches et ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Règles de validation AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528593"
---
# <a name="appsequence-validation-rules"></a>Règles de validation AppSequence

AppSequence les informations contenues dans WS-Discovery annonce et les messages de réponse ([Hello](hello-message.md), [messages ProbeMatches](probematches-message.md)et [ResolveMatches](resolvematches-message.md)). Ces informations sont traitées et validées par WSDAPI avant que ces messages ne soient transmis aux composants situés au-dessus de la pile (tels que l’Explorateur réseau ou une application qui appelle WSDAPI).

Le code XML suivant montre un exemple d’élément AppSequence. Le préfixe WSD fait référence à l’espace de noms `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

WSDAPI ignore les messages périmés. Pour chaque périphérique (identifié de façon unique par l’adresse du point de terminaison dans le corps SOAP), WSDAPI ignore les messages avec un MessageNumber AppSequence inférieur au dernier message vu.

WSDAPI ignore les annonces XAddr obsolètes. Si l’ID d’instance de AppSequence est inférieur au dernier InstanceId vu, WSDAPI ignore le XAddrs publié dans le corps SOAP. En outre, si l’InstanceId est le même que le précédent, mais que MetadataVersion est inférieur au dernier MetadataVersion, WSDAPI ignore le XAddrs.

WSDAPI ignore les messages de WS-Discovery dupliqués. Si deux messages WS-Discovery identiques sont envoyés au WSDAPI, seule la première reçue sera traitée. Cela s’applique en général uniquement aux applications qui appellent directement dans les interfaces [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) ou [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles de message d’échange de métadonnées et de découverte](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



