---
description: Pour faciliter la configuration des paramètres de proxy, WinHTTP 5,1 implémente le protocole WPAD (Web Proxy Auto-Discovery), également appelé « proxy automatique ».
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: Prise en charge d’AutoProxy WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26584bd0b1809f3866ed42adc7198275f40f991c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013155"
---
# <a name="winhttp-autoproxy-support"></a>Prise en charge d’AutoProxy WinHTTP

Pour faciliter la configuration des paramètres de proxy, WinHTTP 5,1 implémente le protocole WPAD (Web Proxy Auto-Discovery), également appelé « proxy automatique ».

## <a name="overview-of-autoproxy"></a>Vue d’ensemble d’AutoProxy

Les applications et les composants qui utilisent WinHTTP pour envoyer des requêtes HTTP doivent s’assurer que la configuration du proxy est correctement définie. À moins que le client dispose d’une connexion Internet directe, une requête HTTP doit normalement être envoyée via un serveur proxy Web qui connecte le réseau local du client à Internet (par exemple, c’est souvent le cas pour les clients Web sur un réseau local d’entreprise). Pour les applications basées sur un serveur, la configuration du proxy est normalement gérée par l’administrateur du serveur à l’aide de l’utilitaire de ProxyCfg.exe WinHTTP. L’administrateur du serveur connaît le nom du serveur proxy à l’avance et utilise ProxyCfg.exe pour enregistrer ce paramètre dans le registre où WinHTTP peut le Rechercher. Toutefois, le fait de demander aux utilisateurs finaux du bureau client de configurer manuellement les paramètres de proxy WinHTTP pose problème. L’utilisateur final peut ne pas connaître le nom du serveur proxy ; demander à l’utilisateur final d’exécuter l’utilitaire de ProxyCfg.exe peut être une charge de support pour une organisation. Pour prendre en charge une expérience utilisateur optimale, une application cliente Web doit déterminer la configuration du proxy sans intervention de l’utilisateur.

Pour faciliter la configuration des paramètres de proxy pour les applications basées sur WinHTTP, WinHTTP implémente désormais le [protocole WPAD (Web Proxy Auto-Discovery)](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01), souvent appelé « *proxy* automatique ». Il s’agit du même protocole que celui que les navigateurs Web implémentent pour découvrir automatiquement la configuration du proxy sans obliger l’utilisateur final à spécifier un serveur proxy manuellement. cette fonctionnalité est disponible à partir de la version 5,1 de WinHTTP dans Windows 2000 service pack 3, Windows XP service pack 1 et Windows Server 2003. Notez que, bien que Microsoft Internet Explorer et Microsoft WinHTTP prennent en charge WPAD, la spécification n’a jamais progressé au-delà de la phase « Internet-Draft » et a expiré le 2001 mai.

Le protocole WPAD fonctionne comme suit :

1.  À l’aide des protocoles réseau DHCP et/ou DNS, l’URL d’un fichier de configuration automatique de proxy (PAC) est découverte. L’URL identifie un fichier PAC sur le réseau local du client. WinHTTP prend en charge uniquement les URL PAC « http : » et « https : ». elle ne prend pas en charge, par exemple, les URL « file : ».
2.  Le fichier PAC est téléchargé et éventuellement mis en cache sur l’ordinateur du client. Le fichier PAC est un script exécutable qui génère une liste d’un ou plusieurs serveurs proxy en fonction d’un nom d’hôte cible et d’une URL. WinHTTP ne prend en charge que les fichiers PAC ECMAScript.
3.  Sur chaque requête HTTP, le code de script PAC est exécuté, avec le nom d’hôte et l’URL de la requête HTTP transmis comme paramètres. WinHTTP s’attend à ce que le code de script PAC contienne une fonction appelée **FindProxyForURL**, sous la forme :
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    Cette fonction calcule une liste d’un ou plusieurs serveurs proxy qui peuvent être utilisés par le client HTTP pour transmettre la demande. Si le script PAC détermine que le client HTTP peut atteindre le serveur cible directement sans passer par un serveur proxy, il indique cela à l’aide d’une valeur de retour spéciale.

## <a name="autoproxy-topics"></a>Rubriques relatives à la connexion AutoProxy

-   [Fonctions de proxy AutoProxy WinHTTP](winhttp-autoproxy-api.md)
-   [Détection sans fichier de configuration automatique](discovery-without-an-auto-config-file.md)
-   [Problèmes liés au proxy AutoProxy dans WinHTTP](autoproxy-issues-in-winhttp.md)
-   [Définition des configurations du proxy WinInet dans WinHTTP](setting-wininet-proxy-configurations-in-winhttp.md)
-   [Cache du proxy AutoProxy](autoproxy-cache.md)
-   [Extensions IPv6 du format de fichier de configuration automatique du navigateur](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



