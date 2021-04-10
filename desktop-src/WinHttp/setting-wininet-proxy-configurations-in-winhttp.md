---
description: Les applications qui portent à partir de WinINet vers WinHTTP peuvent avoir besoin d’utiliser les mêmes paramètres de proxy autorécupérables sous WinINet ou Internet Explorer (IE).
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: Définition des configurations du proxy WinINet dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91306f6591e0aab0f96fa010ee2a83d3f32c8fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953046"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>Définition des configurations du proxy WinINet dans WinHTTP

## <a name="setting-automatic-proxy-on-winhttp-51"></a>Définition du proxy automatique sur WinHTTP 5,1

Les applications qui portent à partir de WinINet vers WinHTTP peuvent avoir besoin d’utiliser les mêmes paramètres de proxy autorécupérables sous WinINet ou Internet Explorer (IE). L’API WinHTTP version 5,1 peut récupérer et utiliser ces paramètres de proxy. En général, WinHTTP spécifie les serveurs proxy et proxy de contournement par session lors de la création de la session. Ces paramètres peuvent être remplacés par demande.

Pour utiliser la même configuration de proxy que WinINet ou IE, le client WinHTTP doit définir des paramètres de proxy pour la session. En outre, si IE ou WinINet sont configurés pour utiliser le protocole WPAD (Web Proxy Auto-Discovery), le client WinHTTP qui utilise ces paramètres doit définir des paramètres de proxy pour chaque demande. Les sections suivantes décrivent comment spécifier les paramètres de proxy pour une session et une demande :

-   [Définition de la configuration du proxy sur une session](#setting-the-proxy-configuration-on-a-session)
-   [Définition de la configuration du proxy sur une demande unique](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>Définition de la configuration du proxy sur une session

## <a name="the-application-is-running-on-a-user-account"></a>L’application est en cours d’exécution sur un compte d’utilisateur

Avant la création d’une session, l’application appelle [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) pour obtenir les paramètres du proxy IE. L’application doit s’exécuter en tant que compte d’utilisateur pour obtenir ces paramètres. Le paramètre *pProxyConfig* est un pointeur vers une structure de [**\_ \_ \_ \_ \_ configuration de proxy Internet Explorer de l’utilisateur courant WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) qui contient le nom du proxy (*LpszProxy*) et les serveurs de contournement du proxy (*lpszProxyBypass*). Le nom du proxy et les valeurs de contournement du proxy de la structure de **\_ \_ \_ \_ \_ configuration du proxy IE de l’utilisateur actuel** sont ensuite utilisés pour initialiser la session WinHTTP. La session est initialisée en appelant [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) avec les paramètres *pwszProxyName* et *pwszProxyBypass* obtenus à partir des membres **lpszProxy** et **lpszProxyBypass** de la structure de **\_ \_ \_ \_ \_ configuration du proxy IE de l’utilisateur actuel WinHTTP** .

## <a name="the-application-is-running-as-a-service"></a>L’application s’exécute en tant que service

L’application doit s’assurer que les paramètres du Registre pour un utilisateur individuel sont chargés dans le registre avant d’appeler [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). Si ces paramètres ne sont pas chargés dans le registre, **WinHttpGetIEProxyConfigForCurrentUser** ne peut pas obtenir les paramètres du proxy. Les paramètres du Registre pour un utilisateur individuel peuvent être chargés dans le registre en appelant la fonction **LoadUserProfile** . Si le chargement des paramètres du registre de l’utilisateur n’est pas une option, l’application peut appeler [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) avec le **\_ \_ \_ \_ proxy par défaut du type d’accès WinHTTP** spécifié dans le paramètre *dwAcessType* . La spécification du proxy par défaut dans l’appel à **WinHttpOpen** indique à l’API WinHTTP de récupérer le jeu de configuration du proxy à l’aide de l’utilitaire de [**proxycfg.exe**](proxycfg-exe--a-proxy-configuration-tool.md) WinHTTP. Une fois que les paramètres du Registre pour un utilisateur individuel ont été chargés, l’application suit les étapes décrites dans [l’application s’exécute sur un compte d’utilisateur](#the-application-is-running-on-a-user-account) pour définir le nom du proxy et les serveurs de contournement du proxy.

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>Définition de la configuration du proxy sur une demande unique

Avant la création de la session, l’application appelle [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) pour déterminer si WinInet et IE sont configurés pour utiliser WPAD. **WinHttpGetIEProxyConfigForCurrentUser** retourne la structure de [**\_ \_ \_ \_ \_ configuration du proxy IE de l’utilisateur actuel WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) qui contient le membre **fAutoDetect** . La valeur **true** pour ce membre indique que le protocole WPAD est utilisé et que le membre **LPSZAUTOCONFIGURL** contient l’URL WPAD.

## <a name="automatic-proxy-configuration-is-used"></a>La configuration automatique du proxy est utilisée

Si WPAD est utilisé, l’application appelle [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) pour récupérer le proxy de la demande. Le paramètre *lpwszUrl* contient l’URL à laquelle la demande est envoyée, et le paramètre *pAutoProxyOptions* contient un pointeur vers la structure ([**\_ \_ options AutoProxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)) qui contient les options du proxy AutoProxy. L’application initialise la structure **des \_ \_ options de proxy automatique WinHTTP** avec les paramètres retournés à partir de la structure de [**\_ \_ \_ \_ \_ configuration du proxy IE de l’utilisateur actuel WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) dans l’appel à [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). L’indicateur d’URL de configuration du PROXY automatique WinHTTP est spécifié dans le membre **dwFlags** de la structure des **options de \_ proxy \_ automatique WinHTTP** et le membre **lpszAutoconfigUrl** contient l’URL de configuration automatique du proxy de la structure de configuration **\_ \_ \_** de **\_ \_ \_ \_ \_ proxy d’utilisateur active WinHTTP** . La fonction **WinHttpGetProxyForUrl** retourne le nom du proxy et la liste de contournement du proxy dans les membres **lpszProxy** et **lpszProxyBypass** de la structure d' [**\_ \_ informations du proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) .

Une fois que le proxy pour la requête est obtenu à partir de [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), l’application crée la demande avec [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) est alors appelé pour définir le proxy pour la demande en spécifiant le handle de requête dans le paramètre *hInternet* . Le paramètre *valeur dwOption* dans l’appel à **WinHttpSetOption** doit avoir la valeur **WinHTTP \_ option \_ proxy** et le paramètre *lpBuffer* est un pointeur vers une structure d' [**\_ \_ informations proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) qui contient le proxy et le contournement du proxy à utiliser pour la requête.

## <a name="automatic-proxy-configuration-is-not-used"></a>La configuration automatique du proxy n’est pas utilisée

Si l’appel à [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) indique que le proxy AutoProxy n’est pas utilisé, l’application peut simplement créer la demande avec [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). La configuration du proxy est la même pour l’ensemble de la session et les modifications par demande ne sont pas nécessaires.

 

 



