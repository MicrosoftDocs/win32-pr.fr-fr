---
description: Si un fichier de configuration automatique de proxy n’a pas été déployé sur le réseau local, WinHttpGetProxyForUrl ne peut pas trouver de serveur proxy.
ms.assetid: a170e63a-8586-47df-af5e-4ee3621795b2
title: Détection sans fichier de configuration automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5ec281c2ef74e2a377cecbd30f16cbc49bd79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414536"
---
# <a name="discovery-without-an-auto-config-file"></a>Détection sans fichier de configuration automatique

Si un fichier de configuration automatique de proxy n’a pas été déployé sur le réseau local, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) ne peut pas trouver de serveur proxy. Si **WinHttpGetProxyForUrl** échoue, il existe plusieurs stratégies de basculement possibles pour obtenir une configuration de proxy viable, en fonction de son environnement d’exécution. Il s’agit notamment de demander le paramètre de proxy via une interface utilisateur, de demander à un utilisateur de stocker la configuration du proxy dans le registre à l’aide de l’utilitaire « ProxyCfg.exe » WinHTTP ou d’utiliser [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) pour vérifier si un serveur proxy est listé dans les paramètres d’Internet Explorer.

Il est possible qu’il n’existe pas de fichier de configuration automatique de proxy car le client dispose d’une connexion Internet directe, par exemple via un fournisseur de services Internet, et n’a pas besoin d’un serveur proxy.

Un serveur proxy peut être requis, en revanche, mais le réseau local ne prend peut-être pas en charge WPAD. Dans ce cas, la configuration du proxy doit être obtenue à partir de l’utilisateur ou trouvée sur l’ordinateur client.

Une application basée sur WinHTTP qui s’exécute dans un environnement serveur de niveau intermédiaire, telle qu’une application COM+ ou ASP, doit s’appuyer sur un administrateur de serveur qui définit une configuration de proxy par défaut dans le registre à l’aide de l’utilitaire « ProxyCfg.exe ». Ces informations de configuration par défaut peuvent ensuite être récupérées à l’aide de la fonction [**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration) , ou simplement en spécifiant l’indicateur de **\_ \_ \_ préconfiguration de type d’accès WinHTTP** dans l’appel [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) .

En revanche, une application WinHTTP s’exécutant sur un ordinateur de bureau client peut tenter d’examiner les paramètres de proxy d’Internet Explorer. [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) remplit une structure de configuration de proxy Internet Explorer de l' [**\_ \_ utilisateur \_ \_ \_ en cours**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) , fournie par l’appelant, avec les paramètres de proxy Internet Explorer de l’utilisateur actuel pour la connexion active (accès à distance, VPN ou LAN). Cette configuration peut indiquer que la détection automatique est utilisée, ou elle peut spécifier une URL pour un fichier de configuration automatique de proxy, ou elle peut spécifier un serveur proxy réel à utiliser, ou une combinaison des trois. Si ces informations incluent une URL PAC ou un serveur proxy, l’application WinHTTP peut essayer de les utiliser.

Vous trouverez un exemple qui utilise les fonctions [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) et [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) dans les exemples WinHTTP du kit de développement logiciel (SDK) de la plateforme.

 

 



