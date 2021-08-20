---
description: Voici un guide pas à pas de la programmation à l’aide de l’interface de programmation d’applications (API) d’assistance IP. Il est conçu pour vous permettre de comprendre les fonctions d’assistance IP de base et les structures de données, et comment elles fonctionnent ensemble.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Prise en main avec l’assistance IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134ca2df12a7d2d2cbd2d0a64f1da07c8aeecd4980fea791bfc19ca018cd87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014157"
---
# <a name="getting-started-with-ip-helper"></a>Prise en main avec l’assistance IP

Voici un guide pas à pas de la programmation à l’aide de l’interface de programmation d’applications (API) d’assistance IP. Il est conçu pour vous permettre de comprendre les fonctions d’assistance IP de base et les structures de données, et comment elles fonctionnent ensemble.

L’application utilisée pour l’illustration est une application d’assistance IP très basique. vous trouverez des exemples de code plus avancés dans les exemples inclus dans le kit de développement logiciel (SDK) de Microsoft Windows.

La première étape est la même pour la plupart des applications d’assistance IP.

-   [Création d’une application d’assistance IP de base](creating-a-basic-ip-helper-application.md)

Les sections suivantes décrivent les étapes restantes pour créer cette application d’assistance IP de base.

-   [Récupération d’informations à l’aide de GetNetworkParams](retrieving-information-using-getnetworkparams.md)
-   [Gestion des cartes réseau à l’aide de GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)
-   [Gestion des interfaces à l’aide de GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)
-   [Gestion des adresses IP à l’aide de GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)
-   [Gestion des baux DHCP à l’aide de IpReleaseAddress et IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [Gestion des adresses IP à l’aide de AddIPAddress et DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [Récupération d’informations à l’aide de GetIpStatistics](retrieving-information-using-getipstatistics.md)
-   [Récupération d’informations à l’aide de GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Le code source complet de cet exemple d’assistance IP de base.

-   [Code source complet de l’application d’assistance IP](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a>Exemples avancés d’assistance IP

plusieurs exemples plus avancés d’assistance IP sont inclus dans le kit de développement logiciel (SDK) de Microsoft Windows. par défaut, l’exemple de code source de l’assistance IP est installé par le SDK Windows disponible pour Windows 7 dans le répertoire suivant :

*C : \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ NetDs \\ IPHelp*

Les exemples plus avancés répertoriés ci-dessous se trouvent dans les répertoires suivants :

-   EnableRouter

    Ce répertoire contient un exemple qui montre comment utiliser les fonctions d’assistance IP [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) et [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) pour activer et désactiver le transfert IPv4 sur l’ordinateur local.

-   iparp

    Ce répertoire contient un exemple de programme qui montre comment utiliser les fonctions d’assistance IP pour afficher et manipuler des entrées dans la table ARP IPv4 sur l’ordinateur local.

-   ipchange

    Ce répertoire contient un exemple de programme qui montre comment utiliser les fonctions d’assistance IP pour modifier par programmation une adresse IP pour une carte réseau spécifique sur votre ordinateur. Ce programme montre également comment récupérer les informations de configuration IP d’une carte réseau existante.

-   IPConfig

    Ce répertoire contient un exemple de programme qui montre comment récupérer par programme des informations de configuration IPv4 similaires à l’utilitaire IPCONFIG.EXE. Il montre comment utiliser les fonctions [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) et [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) . Notez que la fonction **GetAdaptersInfo** récupère uniquement les informations IPv4.

-   IPRenew

    Ce répertoire contient un exemple de programme qui montre comment libérer par programmation et renouveler des adresses IPv4 obtenues par le biais de DHCP. Ce programme montre également comment récupérer des informations de configuration de carte réseau existantes.

-   IPRoute

    Ce répertoire contient un exemple de programme qui montre comment utiliser les fonctions d’assistance IP pour manipuler la table de routage IPv4.

-   ipstat

    Ce répertoire contient un exemple de programme qui montre comment utiliser les fonctions d’assistance IP pour afficher les connexions IPv4 pour un protocole. Par défaut, les statistiques sont indiquées pour IP, ICMP, TCP et UDP.

-   NetInfo

    ce répertoire contient un exemple de programme qui montre comment utiliser les nouvelles api d’assistance IP introduites dans Windows Vista et versions ultérieures pour afficher/modifier les informations d’adresse et d’interface pour IPv4 et IPv6.

 

 



