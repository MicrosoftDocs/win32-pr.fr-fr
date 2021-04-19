---
description: Pour les commandes que vous pouvez utiliser dans Windows Vista et versions ultérieures pour configurer les paramètres de proxy et de suivi pour Windows HTTP, consultez commandes netsh pour Windows Hypertext Transfer Protocol (WINHTTP).
ms.assetid: 81f6b25e-ea14-4dbd-a715-926db7cf90e7
title: Utilisation des outils WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e402962dc34cbf654fa8db49f96b86e7406a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536115"
---
# <a name="using-winhttp-tools"></a>Utilisation des outils WinHTTP

Pour les commandes que vous pouvez utiliser dans Windows Vista et versions ultérieures pour configurer les paramètres de proxy et de suivi pour Windows HTTP, consultez [commandes netsh pour Windows Hypertext Transfer Protocol (WinHTTP)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)).

**Windows Server 2003 et versions antérieures :** Plusieurs outils sont disponibles pour vous aider à écrire et à déboguer vos applications. Elles sont expliquées dans les rubriques suivantes :

-   [WinHttpCfg.exe, un outil de configuration de certificat](winhttpcertcfg-exe--a-certificate-configuration-tool.md) permet aux administrateurs d’installer et de configurer des certificats clients dans n’importe quel [*magasin de certificats*](glossary.md) accessible par le compte IWAM (Internet Server Web Application Manager). L’outil élimine également la nécessité d’effectuer des opérations spéciales pour les comptes, tels que le compte IWAM, pour accéder à des certificats lors de l’utilisation de pages d’Active Server (ASP).
-   Les [outils de configuration de proxyNetsh.exe ou ProxyCfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) peuvent être utilisés pour configurer des serveurs proxy avec les services http Microsoft Windows (WinHTTP).
-   [WinHttpTraceCfg, un outil de configuration de trace](winhttptracecfg-exe--a-trace-configuration-tool.md) offre la possibilité d’analyser les fonctions WinHTTP et le trafic réseau correspondant. Le débogage d’applications qui utilisent des protocoles de transmission chiffrés, tels que les SSL (Secure Sockets Layer) (SSL), empêche la détection de paquets au niveau de la couche de transport réseau et nécessite la possibilité d’intercepter le trafic entre le client et le serveur après qu’il a été déchiffré. La fonction de trace WinHTTP offre une gamme de fonctionnalités permettant d’intercepter le flux de trafic entre le client et le serveur.

 

 
