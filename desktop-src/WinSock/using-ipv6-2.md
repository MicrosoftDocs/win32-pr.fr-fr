---
description: sur Windows XP plus tard, un nouvel outil de ligne de commande est fourni pour la configuration et la gestion d’IPv4. Cet outil utilise la \# commande &0034 ; netsh interface ip&\# 0034 ; pour la configuration et la gestion d’IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Utilisation d'une adresse IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296615"
---
# <a name="using-ipv6"></a>Utilisation d'une adresse IPv6

sur Windows XP plus tard, un nouvel outil de ligne de commande est fourni pour la configuration et la gestion d’IPv4. Cet outil utilise la commande « netsh interface IP » pour la configuration et la gestion d’IPv4.

sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures, ce nouvel outil en ligne de commande a été amélioré pour prendre en charge la configuration et la gestion d’IPv6. Cet outil amélioré est la commande « netsh interface IPv6 ». Les modifications de configuration effectuées à l’aide des commandes Netsh.exe sont permanentes et ne sont pas perdues lors du redémarrage de l’ordinateur ou du protocole IPv6.

la commande suivante est disponible sur Windows XP avec SP1 et versions ultérieures pour interroger et configurer IPv6 sur un ordinateur local :

-   [Netsh.exe](netsh-exe.md)

avant Windows XP avec Service Pack 1 (SP1), la configuration et la gestion ipv6 utilisaient plusieurs anciens outils en ligne de commande pour configurer et gérer ipv6. À l’aide de ces outils plus anciens, les modifications IPv6 ne sont pas permanentes et sont perdues lorsque l’ordinateur ou le protocole IPv6 a été redémarré.

les commandes plus anciennes suivantes sont disponibles sur Windows XP

-   [Net.exe](net-exe-2.md)
-   [Ipv6.exe](ipv6-exe-2.md)
-   [Ipsec6.exe](ipsec6-exe-2.md)

ces anciens outils étaient également fournis dans la version préliminaire de la technologie IPv6 pour Windows 2000

Les modifications de configuration effectuées à l’aide de ces anciens outils peuvent être conservées en les plaçant sous forme de lignes de commande dans un fichier de script de commande (. cmd) qui est exécuté après le redémarrage de l’ordinateur ou du protocole IPv6. pour réactiver automatiquement les modifications de configuration après le redémarrage, il est possible d’utiliser la Windows tâches planifiées pour exécuter le fichier. cmd au démarrage de l’ordinateur.

ces outils plus anciens ne sont pas fournis sur Windows Server 2003 et versions ultérieures. l’outil « netsh interface ipv6 » est fourni pour la configuration et la gestion d’ipv6 à partir de la ligne de commande sur Windows Server 2003 et versions ultérieures.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Protocole Internet version 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Guide IPv6 pour les Applications Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[version préliminaire de la technologie IPv6 pour Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



