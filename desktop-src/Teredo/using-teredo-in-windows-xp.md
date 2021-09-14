---
title: utilisation de Teredo dans Windows XP
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: 'en savoir plus sur : utilisation de Teredo dans Windows XP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29abb2b4056564be29708ceb00742b37d363d7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095625"
---
# <a name="using-teredo-in-windows-xp"></a>utilisation de Teredo dans Windows XP

pour utiliser le client Teredo ou le relais spécifique à l’hôte sur des ordinateurs exécutant Windows xp avec service pack 1 (sp1) avec le Pack de mise en réseau avancée, Windows XP avec service pack 2 (sp2), Windows server 2003 avec service pack 1 (sp1) ou Windows server 2003 avec service pack 2 (sp2), un développeur d’applications doit effectuer les opérations suivantes :

-   assurez-vous que l’application est compatible avec IPv6 en utilisant les nouveaux éléments de programmation de Windows sockets 2 (fonctions et structures) qui prennent en charge à la fois IPv4 et IPv6. pour plus d’informations, consultez le [Guide IPv6 pour les Applications Windows sockets](../winsock/ipv6-guide-for-windows-sockets-applications-2.md).
-   activez l’utilisation de Teredo dans votre application en définissant le niveau de \_ protection IPV6 \_ Windows option de socket sockets sur le niveau de protection non \_ \_ restreint. Pour plus d’informations, consultez [utilisation \_ du \_ niveau de protection IPv6](/previous-versions/aa916826(v=msdn.10)). vous pouvez également définir cette option par le biais de la classe [System .net. sockets](/dotnet/api/system.net.sockets?view=netcore-3.1) .NET Framework.
-   créez une exception pour le pare-feu Windows pour autoriser le trafic Teredo entrant non sollicité. utilisez les api de [pare-feu Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page) pour créer une exception de port pour le port UDP affecté pour le trafic Teredo. Pour plus d’informations et des exemples détaillant la sécurité requise et les considérations relatives au trafic pour Teredo, voir [utilisation de Teredo](using-teredo.md).

Pour vous assurer que Teredo est disponible pour une utilisation lors de l’exécution de l’application, les développeurs d’applications doivent effectuer les opérations suivantes pendant le processus d’installation de l’application :

-   Installez IPv6 à l’aide de la commande **netsh interface ipv6 install** . Windows Le pare-feu protège l’ordinateur de l’utilisateur contre le trafic IPv6 entrant non sollicité, de la même façon que le trafic IPv4.
-   Activez Teredo avec la commande **netsh interface ipv6 set Teredo client** .

Si vous le souhaitez, vous pouvez vérifier si IPv6 est installé chaque fois que votre application s’exécute et installer IPv6 et activer Teredo si nécessaire. Vous devez également informer l’utilisateur de l’installation D’ipv6 et de l’activation de Teredo.

 

 
