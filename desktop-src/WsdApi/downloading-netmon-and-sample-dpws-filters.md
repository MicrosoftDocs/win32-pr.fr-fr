---
description: Moniteur réseau Microsoft 3 (NetMon) est un analyseur de paquets utilisé pour inspecter le trafic réseau.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Téléchargement de Netmon et des exemples de filtres DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6f92f2680807101a3c82664f4b0b3ae5a877f0d9f5797da9c9c0b6ea2b158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030219"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Téléchargement de Netmon et des exemples de filtres DPWS

Moniteur réseau Microsoft 3 (NetMon) est un analyseur de paquets utilisé pour inspecter le trafic réseau. vous devez télécharger Netmon avant les étapes de dépannage indiquées dans [inspection des suivis réseau pour UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) et [inspecter les traces réseau pour les métadonnées HTTP Exchange](inspecting-network-traces-for-http-metadata-exchange.md) peuvent être suivies. Une fois Netmon téléchargé, vous pouvez utiliser des filtres DPWS pour isoler le trafic concerné.

## <a name="downloading-netmon"></a>Téléchargement de NetMon

Pour télécharger NetMon, accédez à [Moniteur réseau Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) et suivez les instructions. Pour plus d’informations sur NetMon, consultez « informations sur Moniteur réseau 3,0 » dans la base de connaissances de l’aide et du support à l’adresse [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>Exemples de filtres DPWS

Parfois, la résolution des problèmes d’échange de WS-Discovery et de métadonnées doit avoir lieu sur un réseau occupé. Les exemples de filtres peuvent être utilisés pour limiter la sortie Netmon au trafic qui vous intéresse. Pour plus d’informations sur l’utilisation des filtres NetMon, consultez [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

L’exemple suivant montre un filtre qui limite la sortie à tout le trafic de diffusion WS-Discovery.

> [!Note]  
> Ce filtre ne capture pas le trafic des piles qui ne répondent pas aux messages de multidiffusion WS-Discovery qui proviennent du port 3702. Si une telle pile est utilisée, vous devez modifier cet exemple de filtre avant de l’utiliser.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

L’exemple suivant illustre un filtre qui limite la sortie aux messages HTTP envoyés aux piles WSDAPI sur le port par défaut.

> [!Note]  
> Les services peuvent envoyer des messages HTTP pertinents à partir de ports autres que 5357. Si le trafic provenant d’autres ports présente un intérêt, vous devez modifier cet exemple de filtre avant de l’utiliser.

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

L’exemple suivant illustre un filtre qui limite la sortie au trafic de multidiffusion IPv4.

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

L’exemple suivant illustre un filtre qui limite la sortie au trafic de multidiffusion IPv6.

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

Certains filtres peuvent être combinés pour limiter davantage les résultats. L’exemple suivant illustre un filtre qui limite la sortie au trafic de multidiffusion IPv4 WS-Discovery.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

Lorsque ces filtres sont utilisés, le trafic pertinent peut être exclu des résultats Netmon. Une exclusion peut se produire lorsque les services résident sur des ports autres que les ports par défaut (5357/5358) et lorsqu’une pile DPWS ne répond pas aux messages à l’aide du port par défaut. Dans ce cas, les filtres doivent être modifiés avant d’être utilisés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



