---
description: Microsoft Windows HTTP Services (WinHTTP) vous offre une interface de haut niveau prise en charge par le serveur aux protocoles HTTP/2 et 1,1 Internet.
ms.assetid: 8337f699-3ec0-4397-acc2-6dc813f7542d
title: À propos de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19df8ac8073cfca4fd74fd5d024712cc3fc59c770c3d9ad0ab1386bc0642d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570289"
---
# <a name="about-winhttp"></a>À propos de WinHTTP

> [!NOTE]
> pour les conteneurs d’applications et les services système depuis Windows 10, la version 1709, HTTP/2 (voir [RFC7540](https://tools.ietf.org/html/rfc7540)) est activée par défaut.

Microsoft Windows HTTP Services (WinHTTP) vous offre une interface de haut niveau prise en charge par le serveur aux protocoles HTTP/2 et 1,1 Internet. WinHTTP est conçu pour être utilisé principalement dans les scénarios basés sur le serveur par les applications serveur qui communiquent avec les serveurs HTTP.

[WinInet](/windows/desktop/WinInet/portal) a été conçu comme une plateforme cliente http pour les applications de bureau interactives. WinINet affiche une interface utilisateur pour certaines opérations, telles que la collecte des informations d’identification de l’utilisateur. Toutefois, WinHTTP gère ces opérations par programme. Les applications serveur qui requièrent des services clients HTTP doivent utiliser WinHTTP au lieu de WinINet. Pour plus d’informations, consultez [Portage d’applications WinInet vers WinHTTP](porting-wininet-applications-to-winhttp.md).

WinHTTP est également conçu pour être utilisé dans les services système et les applications clientes basées sur HTTP. Toutefois, les [applications à utilisateur](/windows/desktop/WinInet/portal)unique qui requièrent des fonctionnalités de protocole FTP, la persistance des cookies, la mise en cache, la gestion automatique des boîtes de dialogue des informations d’identification, la compatibilité d’Internet Explorer ou la prise en charge des plateformes de niveau inférieur,

Cette interface est accessible à partir de C/C++ à l’aide de l’interface de programmation d’applications (API) WinHTTP, ou à l’aide des interfaces [**IWinHttpRequest**](iwinhttprequest-interface.md) et [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) . winhttp est également accessible à partir de script et Microsoft Visual Basic par le biais de l’objet WinHTTP. Pour plus d’informations et pour obtenir une description des différentes fonctions, consultez la référence des fonctions WinHTTP pour le langage spécifique.

à partir de Windows 8, WinHTTP fournit des api pour activer les connexions à l’aide du [protocole websocket](https://tools.ietf.org/html/rfc6455)l, par exemple [**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend) et [**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive).

> [!Caution]  
> WinHTTP n’est pas réentrant, sauf pendant le rappel d’achèvement asynchrone. Autrement dit, lorsqu’un thread a un appel en attente pour l’une des fonctions WinHTTP telles que WinHttpSendRequest, WinHttpReceiveResponse, WinHttpQueryDataAvailable, WinHttpSendData ou WinHttpWriteData, il ne doit jamais appeler WinHTTP une deuxième fois jusqu’à ce que le premier appel soit terminé. Un autre scénario sous lequel un deuxième appel peut se produire est le suivant : si une application met en file d’attente un appel de procédure asynchrone (APC) vers le thread qui appelle WinHTTP, et si WinHTTP exécute une attente alertable en interne, l’APC peut s’exécuter. Si la routine APC se produit également pour appeler WinHTTP, elle réentre l’API WinHTTP et l’état interne de WinHTTP peut être endommagé.

## <a name="winhttp-51-features"></a>Fonctionnalités WinHTTP 5,1

Les fonctionnalités suivantes ont été ajoutées à la version 5,1 de WinHTTP :

-   Prise en charge D’ipv6.
-   Fonctionnalités du proxy.
-   Protocole HTTP/1.0, y compris la prise en charge des connexions Keep-Alive (persistant) et des cookies de session.
-   Prise en charge du transfert mémorisé en bloc HTTP/1.1 pour les réponses HTTP.
-   Regroupement persistant des connexions anonymes entre les sessions.
-   Fonctionnalité SSL (Secure Sockets Layer) (SSL), y compris les certificats clients. Les protocoles SSL pris en charge sont les suivants : SSL 2,0, SSL 3,0 et TLS (Transport Layer Security) 1,0.
-   Prise en charge de l’authentification serveur et proxy, y compris la prise en charge intégrée de Microsoft Passport 1,4 et du package Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md) .
-   Gestion automatique des redirections, sauf si elles sont supprimées.
-   Interface scriptable en plus de l’API.
-   Utilitaire de suivi pour aider à résoudre les problèmes.

Un certain nombre de fonctionnalités [WinInet](/windows/desktop/WinInet/portal) ne sont pas prises en charge dans WinHTTP, notamment la mise en cache des URL et les cookies persistants, le proxy automatique, la numérotation automatique, la prise en charge hors connexion et le protocole FTP (FTP).

Pour plus d’informations sur les modifications introduites dans la version 5,1, voir [What’s New in WinHTTP 5,1](what-s-new-in-winhttp-5-1.md).

## <a name="getting-started-with-winhttp"></a>Prise en main avec WinHTTP

Pour plus d’informations sur WinHTTP, consultez les rubriques suivantes.

* [WinInet et WinHTTP](/windows/desktop/wininet/wininet-vs-winhttp) comparent les deux technologies pour accéder à http.
* Les [versions WinHTTP](winhttp-versions.md) décrivent l’historique des versions de WinHTTP.
* [Nouveautés de winhttp 5,1](what-s-new-in-winhttp-5-1.md) décrit les modifications et les nouvelles fonctionnalités de WinHTTP 5,1.
* La [terminologie réseau](network-terminology.md) décrit des concepts et une terminologie utiles relatifs à la mise en réseau en général et au protocole http en particulier.
* Le [choix d’une interface WinHTTP](choosing-a-winhttp-interface.md) décrit l’API C/C++ et l’interface com pour WinHTTP.
* [Considérations sur la sécurité WinHTTP](winhttp-security-considerations.md) décrit les problèmes de sécurité à prendre en compte lors de l’utilisation de WinHTTP.
* [Portage d’applications WinInet vers WinHTTP](porting-wininet-applications-to-winhttp.md) décrit comment modifier vos applications [WinInet](/windows/desktop/WinInet/portal) existantes pour utiliser l’API WinHTTP.
