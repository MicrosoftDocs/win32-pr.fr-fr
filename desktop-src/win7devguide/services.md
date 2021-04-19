---
title: Services (Guide du développeur Windows 7)
description: Windows 7 offre une plateforme puissante, hautement extensible et gérable pour la création et l’intégration des services Web et des applications futures. Windows 7 offre à la fois des API de code managé et des API natives pour la création et l’exécution de services Web.
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aab84cbb522f21b9a09a85d80ef25bf1c858baf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106527562"
---
# <a name="services-windows-7-developer-guide"></a>Services (Guide du développeur Windows 7)

Windows 7 offre une plateforme puissante, hautement extensible et gérable pour la création et l’intégration des services Web et des applications futures.

Windows 7 offre à la fois des API de code managé et des API natives pour la création et l’exécution de services Web. Une série de nouvelles fonctionnalités s’appuient sur une nouvelle couche d’extensibilité qui permet aux développeurs d’étendre toutes les API, en code natif ou au sein de l’infrastructure de Microsoft .NET.

Windows 7 permet également aux développeurs de tirer parti des fonctionnalités améliorées de mise en cache et de recherche. Grâce à ces améliorations, les développeurs peuvent récupérer des données plus rapidement et réduire l’utilisation de la bande passante réseau.

## <a name="windows-web-services"></a>Services Web Windows

Avec les [services Web Windows](/windows/desktop/wsw/portal), vous pouvez créer des applications qui communiquent facilement avec un ordinateur local ou un service Web distant. Windows Web services est une implémentation de code natif de SOAP et fournit une communication réseau de base en prenant en charge un large éventail de protocoles de la famille de services Web (*WS*). Windows Web services est un pair à [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) (*WCF*, services Web de code géré) et fournit un sous-ensemble de fonctionnalités *WCF* hautes performances. Windows Web services offre les avantages suivants :

-   Possibilité de générer des services Web en code natif en C/C++ dans le client et le serveur Windows.
-   Intégration étendue aux services [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) .
-   La possibilité de générer des services Web avec un temps de démarrage minimal.
-   La possibilité de créer des services basés sur la famille *WS* de protocoles et de normes *W3C* .
-   La possibilité d’utiliser des services Web dans des environnements à ressources restreintes.

Pour plus d’informations, consultez [API des services Web Windows](../wsw/portal.md) et [implémenter des services Web avec l’API des services Web Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI).

## <a name="distributed-routing-table"></a>Table de routage distribuée

Windows 7 simplifie la création d’applications d’égal à égal sophistiquées, telles que des systèmes de fichiers distribués et des réseaux de distribution de contenu, avec la [table de routage distribuée](/windows/desktop/P2PSdk/distributed-routing-table-api-reference). La table de routage distribuée fournit un mécanisme sécurisé et évolutif pour la publication et la recherche de clés dans un système d’égal à égal. Il peut être utilisé pour créer des tables de hachage distribuées et construire des topologies pour les réseaux de superposition. (Voir [API table de routage distribué](../p2psdk/distributed-routing-table-api.md).)

## <a name="windows-branchcache"></a>**Windows BranchCache**

Windows 7 améliore la réactivité des applications entre les serveurs centraux et les ordinateurs des succursales. Dans les réseaux actuels, la communication entre les serveurs centraux et les succursales est souvent encombrée, ce qui a pour conséquence une baisse des performances des applications dans la filiale. Avec Windows BranchCache, les clients peuvent récupérer des données à partir d’autres clients dans leur propre branche qui ont déjà téléchargé les données, au lieu d’avoir à récupérer les données sur des serveurs distants. Par conséquent, le trafic lié aux liaisons de réseau étendu (WAN) diminue et la réactivité des applications est améliorée. Le cache conserve une copie de tout le contenu demandé par les clients de la succursale et s’assure que seuls les clients autorisés par le serveur de contenu peuvent accéder aux données demandées, tout en préservant le chiffrement de bout en bout des données.

Windows BranchCache est déjà intégré à HTTP et au protocole SMB (Server Message Block). Si une application utilise WindowsAPIs pour l’un de ces protocoles, Windows BranchCache peut aider à augmenter les performances de cette application sur Windows 7 sans y apporter de modifications.

Si votre application récupère les mêmes données plusieurs fois à partir d’un serveur via une liaison de réseau étendu et n’est pas optimisée automatiquement à l’aide de Windows 7, il est facile d’utiliser les BranchCacheAPIs Windows pour optimiser votre application afin qu’elle fonctionne plus rapidement sur Windows 7 et réponde à vos utilisateurs de succursales.

Ces nouvelles fonctionnalités permettent de réduire le trafic WAN et la latence tout en garantissant la conformité avec les exigences de sécurité. (Voir [distribution d’homologue](../p2psdk/peer-distribution.md).)

 

 
