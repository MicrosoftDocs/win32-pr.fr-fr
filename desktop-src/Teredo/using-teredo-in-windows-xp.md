---
title: Utilisation de Teredo dans Windows XP
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: 'En savoir plus sur : utilisation de Teredo dans Windows XP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29abb2b4056564be29708ceb00742b37d363d7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042764"
---
# <a name="using-teredo-in-windows-xp"></a>Utilisation de Teredo dans Windows XP

Pour utiliser le client Teredo ou le relais spécifique à l’hôte sur des ordinateurs exécutant Windows XP avec Service Pack 1 (SP1) avec le Pack de mise en réseau avancée, Windows XP avec Service Pack 2 (SP2), Windows Server 2003 avec Service Pack 1 (SP1) ou Windows Server 2003 avec Service Pack 2 (SP2), un développeur d’applications doit effectuer les opérations suivantes :

-   Assurez-vous que l’application est compatible avec IPv6 à l’aide des nouveaux éléments de programmation Windows Sockets 2 (fonctions et structures) qui prennent en charge IPv4 et IPv6. Pour plus d’informations, consultez le [Guide IPv6 pour les applications Windows Sockets](../winsock/ipv6-guide-for-windows-sockets-applications-2.md).
-   Activez l’utilisation de Teredo dans votre application en définissant l' \_ \_ option de socket Windows Sockets au niveau de protection IPv6 sur le niveau de protection non \_ \_ restreint. Pour plus d’informations, consultez [utilisation \_ du \_ niveau de protection IPv6](/previous-versions/aa916826(v=msdn.10)). Vous pouvez également définir cette option par le biais de la classe [System .net. sockets](/dotnet/api/system.net.sockets?view=netcore-3.1) .NET Framework.
-   Créez une exception pour le pare-feu Windows afin d’autoriser le trafic Teredo entrant non sollicité. Utilisez les API du [pare-feu Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page) pour créer une exception de port pour le port UDP affecté pour le trafic Teredo. Pour plus d’informations et des exemples détaillant la sécurité requise et les considérations relatives au trafic pour Teredo, voir [utilisation de Teredo](using-teredo.md).

Pour vous assurer que Teredo est disponible pour une utilisation lors de l’exécution de l’application, les développeurs d’applications doivent effectuer les opérations suivantes pendant le processus d’installation de l’application :

-   Installez IPv6 à l’aide de la commande **netsh interface ipv6 install** . Le pare-feu Windows protège l’ordinateur de l’utilisateur contre le trafic IPv6 entrant non sollicité, de la même façon que le trafic IPv4.
-   Activez Teredo avec la commande **netsh interface ipv6 set Teredo client** .

Si vous le souhaitez, vous pouvez vérifier si IPv6 est installé chaque fois que votre application s’exécute et installer IPv6 et activer Teredo si nécessaire. Vous devez également informer l’utilisateur de l’installation D’ipv6 et de l’activation de Teredo.

 

 
