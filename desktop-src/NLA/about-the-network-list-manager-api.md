---
title: À propos de l’API du gestionnaire de listes de réseaux
description: À propos de l’API du gestionnaire de listes de réseaux
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675258"
---
# <a name="about-the-network-list-manager-api"></a>À propos de l’API du gestionnaire de listes de réseaux

L’environnement réseau Microsoft Windows permet aux ordinateurs multirésidents de se connecter simultanément à plusieurs réseaux. Il peut y avoir plusieurs réseaux sans fil disponibles, ainsi que des connexions de réseau local et d’accès à distance. Le gestionnaire de listes de réseaux identifie les réseaux disponibles et retourne les données d’attribut réseau à l’application.

L’API du gestionnaire de listes de réseaux interagit avec le service Network List Manager pour identifier et récupérer les propriétés de chaque réseau auquel le PC se connecte. Chaque réseau est identifié de manière unique par une signature réseau basée sur les propriétés identifiables de manière unique de ce réseau. Lorsqu’une application s’inscrit pour les notifications du gestionnaire de liste de réseaux, l’application reçoit des notifications sur la disponibilité de nouvelles connexions réseau ou des modifications apportées aux connexions réseau existantes. Les applications peuvent ajuster leur logique en fonction du réseau auquel elles sont connectées ; la connexion réseau à laquelle ils sont connectés ; ou les propriétés du réseau. Avec ces informations, les applications peuvent affiner leurs actions en fonction des conditions actuelles du réseau.

Windows Vista introduit de nouvelles interfaces qui peuvent être utilisées pour obtenir des informations détaillées sur ces caractéristiques du réseau, et bien plus encore. Avec l’interface [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) , il est facile d’énumérer tous les réseaux ([**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) qu’un ordinateur a jamais vu, ou seulement les réseaux connectés, ou uniquement les réseaux déconnectés. L’interface **INetworkListManager** facilite également l’énumération des interfaces réseau sur un ordinateur.

L’interface [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) est utilisée pour déterminer les propriétés d’une connexion réseau : Name, description, ID, Managed/Authenticated, Connected/Disconnected, et bien plus encore. Il est possible qu’un seul réseau soit connecté à plusieurs interfaces. par conséquent, par le biais d’une interface **iNetwork** , vous pouvez également énumérer les instances de l’interface **iNetwork** utilisée.

L’interface [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) vous indique les propriétés pertinentes d’une interface : ID, Guid, type (géré, authentifié) et État (connecté, déconnecté, v4 local, v4 Internet, V6 local, V6 Internet). La version locale v4 signifie un accès local IPv4 (Internet Protocol version 4). Internet v4 signifie IPv4 avec accès à Internet. IPv6 local et V6 Internet signifiant IPv6.

La racine de l’arborescence d’objets pour l’emplacement réseau est l’interface [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) . Cette interface est implémentée sur la coclasse **CLSID \_ NetworkListManager** . Pour utiliser cette interface, il est nécessaire de créer l’objet com **CLSID \_ NetworkListManager** comme illustré ci-après :


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




