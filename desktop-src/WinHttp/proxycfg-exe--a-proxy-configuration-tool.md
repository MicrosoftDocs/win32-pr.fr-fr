---
description: Cette rubrique explique l’utilisation de l’outil de configuration de proxy des services HTTP Microsoft Windows (WinHTTP), &\# 0034 ; ProxyCfg.exe&\# 0034 ;.
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Outils de configuration de proxy Netsh.exe et ProxyCfg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a33e832d324a5863652673b8e25725fba72e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524826"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a>Outils de configuration de proxy Netsh.exe et ProxyCfg.exe

* * Windows Vista et Windows Server 2008 : * *

ProxyCfg.exe est déconseillé. Elle est remplacée par les commandes [Netsh.exe WinHTTP](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)) .

Cette rubrique explique l’utilisation de l’outil de configuration de proxy [Microsoft Windows http services (WinHTTP)](about-winhttp.md) , « ProxyCfg.exe ».

Il existe deux façons d’accéder aux serveurs http et HTTPs (Secure Hypertext Transfer Protocol) via un proxy à l’aide des services HTTP Microsoft Windows (WinHTTP). Tout d’abord, vous pouvez spécifier des paramètres de proxy à partir de votre application WinHTTP. Deuxièmement, vous pouvez spécifier des paramètres de proxy par défaut en dehors de votre application à l’aide de l’utilitaire de configuration de proxy situé dans le répertoire% windir% \\ system32.

Vous pouvez définir par programmation les données de proxy à partir de votre application ou de votre script. Si vous écrivez une application à l’aide de l’API WinHTTP, utilisez l’une des deux techniques suivantes pour modifier les paramètres de proxy.

-   Utilisez la fonction [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) . Spécifiez le type d’accès dans le deuxième paramètre, le nom du proxy dans le troisième paramètre et une liste de contournement dans le quatrième paramètre. L’exemple suivant montre comment la fonction [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) peut être utilisée pour définir des données de proxy.

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   Utilisez la fonction [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) . L’indicateur de [**\_ \_ proxy de l’option WinHTTP**](option-flags.md) vous permet de spécifier des paramètres de proxy avec une structure d' [**\_ \_ informations de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) . L’exemple de code suivant montre comment la fonction [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) peut être utilisée pour définir des données de proxy.

    ``` syntax
    WINHTTP_PROXY_INFO proxyInfo;
    proxyInfo.dwAccessType = WINHTTP_ACCESS_TYPE_NAMED_PROXY;
    proxyInfo.lpszProxy = L"proxy_name";
    proxyInfo.lpszProxyBypass = L"<local>";
        
    // Set the proxy information for this session.
    WinHttpSetOption( hSession, 
                      WINHTTP_OPTION_PROXY, 
                      &proxyInfo, 
                      sizeof(proxyInfo));
    ```

Si vous écrivez un script ou une application à l’aide de l’objet [**WinHttpRequest**](winhttprequest.md) , utilisez la technique suivante pour modifier les paramètres du proxy.

-   Utilisez la méthode [**SetProxy**](iwinhttprequest-setproxy.md) . Spécifiez le type d’accès dans le premier paramètre, le nom du proxy dans le deuxième paramètre et une liste de contournement dans le troisième paramètre. L’exemple suivant montre comment la méthode [**SetProxy**](iwinhttprequest-setproxy.md) peut être utilisée dans un script pour définir des données de proxy.

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

Pour spécifier les paramètres par défaut et éliminer la nécessité d’utiliser la méthode [**SetProxy**](iwinhttprequest-setproxy.md) ou la fonction [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , utilisez l’utilitaire de configuration du proxy. À l’aide de cet utilitaire, vous pouvez spécifier que votre application accède à un réseau directement, par le biais d’un proxy ou par le biais d’une combinaison d’accès direct et par proxy, en spécifiant une liste de contournement. Lorsque vous utilisez l’API WinHTTP, l’outil de configuration de proxy détermine uniquement les paramètres lorsque vous transmettez l’indicateur **\_ \_ \_ par défaut du type d’accès WinHTTP** à l’API [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) . L’objet [**WinHttpRequest**](winhttprequest.md) utilise les paramètres de l’outil de configuration du proxy par défaut.

Les paramètres de proxy pour WinHTTP ne sont pas les paramètres de proxy pour Microsoft Internet Explorer. Vous ne pouvez pas configurer les paramètres de proxy pour WinHTTP dans le panneau de configuration Microsoft Windows. L’utilisation de l’utilitaire de configuration de proxy WinHTTP ne modifie pas les paramètres que vous utilisez pour Internet Explorer.

> [!Note]  
> Si vous essayez d’ouvrir et d’envoyer une requête HTTP à l’aide de WinHTTP et que les paramètres du proxy sont incorrects, une erreur se produit.

 

## <a name="command-line-parameters"></a>Paramètres de ligne de commande

Le tableau suivant répertorie les paramètres de ligne de commande disponibles pour une utilisation avec l’outil ProxyCfg.exe.



| Paramètre | Description                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| aucun      | Quand aucun paramètre n’est spécifié, les paramètres de proxy WinHTTP actuels sont affichés.                                                                                                                                                                                                                                                                                                                                               |
| ?         | Les informations d’aide s’affichent.                                                                                                                                                                                                                                                                                                                                                                                                    |
| d         | Spécifie que les applications WinHTTP accèdent directement au réseau, sans proxy.                                                                                                                                                                                                                                                                                                                                                 |
| p         | Spécifie le serveur proxy. Vous pouvez également spécifier une liste facultative de serveurs accessibles sans proxy.                                                                                                                                                                                                                                                                                                                   |
| u         | Spécifie que les applications WinHTTP utilisent les paramètres de proxy de l’utilisateur actuel pour Internet Explorer. Ce paramètre ne fonctionne pas si Internet Explorer détecte automatiquement les paramètres du proxy ou s’il utilise une URL de configuration automatique pour définir les informations du proxy.                                                                                                                                                      |
| i         | Spécifie que les applications WinHTTP utilisent les paramètres de proxy de l’utilisateur actuel pour Internet Explorer. Cela ne fonctionne que si ProxyCfg.exe n’a pas été utilisé précédemment. Si ProxyCfg.exe est installé, spécifiez que le paramètre de ligne de commande « u » utilise les paramètres manuels. Ce paramètre ne fonctionne pas si Internet Explorer détecte automatiquement les paramètres du proxy ou s’il utilise une URL de configuration automatique pour définir les informations du proxy. |



 

Vous pouvez spécifier des proxies dans une chaîne délimitée par des espaces. Les listes de proxy peuvent contenir le numéro de port utilisé pour accéder au proxy. Pour répertorier un proxy pour un protocole spécifique, la chaîne doit respecter le format, <protocol> = https://<\_ nom du proxy>. Les protocoles valides sont HTTP et HTTPs. Par exemple, pour répertorier un proxy HTTP, une chaîne valide est http = https://http\_proxy\_name:80 , où \_ nom du proxy http \_ est le nom du serveur proxy et 80 est le numéro de port que vous devez utiliser pour accéder au proxy. Si le proxy utilise le numéro de port par défaut pour ce protocole, vous pouvez omettre le numéro de port. Si un nom de proxy est listé par lui-même, vous pouvez l’utiliser comme proxy par défaut pour tous les protocoles qui n’ont pas de proxy spécifié. Par exemple, http = https://http\_proxy other \_ proxy utilise \_ le proxy HTTP pour toutes les opérations http, tandis que le protocole HTTPS utilise le proxy nommé Other \_ proxy.

Vous pouvez répertorier les adresses IP ou les noms d’hôte connus localement dans la liste de contournement du proxy. Cette liste peut contenir des caractères génériques, tels que « \* », qui obligent l’application à contourner le serveur proxy pour les adresses qui correspondent au modèle spécifié, par exemple « \* . Microsoft.com » ou « \* . org ». Les caractères génériques doivent être les caractères les plus à gauche de la liste. Par exemple \* , « AAA ». n’est pas pris en charge. Pour répertorier plusieurs adresses et noms d'hôtes, séparez-les par des espaces ou des points-virgules dans la chaîne de contournement de proxy. Si vous spécifiez la <local> macro, la fonction ignore tout nom d’hôte qui ne contient pas de point.

> [!WARNING]
> Après l’exécution de Proxycfg.exe, vous ne pouvez pas restaurer les paramètres de proxy précédents. Toutefois, vous pouvez supprimer les paramètres du proxy entièrement.

 

## <a name="usage"></a>Utilisation

Pour utiliser l’outil de configuration de proxy, ouvrez une fenêtre d’invite de commandes et exécutez l’utilitaire de configuration de proxy avec les paramètres de ligne de commande appropriés. La section suivante fournit des exemples de syntaxe.

## <a name="example-syntax"></a>Exemple de syntaxe

### <a name="example-1-use-a-proxy-only-for-external-resources"></a>Exemple 1 : utiliser un proxy uniquement pour les ressources externes

Voici l’utilisation la plus courante pour Proxycfg.exe. Cette commande spécifie que les serveurs HTTP et HTTPs sont accessibles via le serveur proxy nommé « \_ serveur proxy », à l’exception des noms d’hôte qui ne contiennent pas de point.

**proxycfg-p \_ serveur proxy « <local> »**

### <a name="example-2-use-a-proxy-for-all-resources"></a>Exemple 2 : utiliser un proxy pour toutes les ressources

L’exemple suivant spécifie que les serveurs HTTP et HTTPs sont accessibles par le biais du serveur proxy nommé « \_ serveur proxy ». Aucune liste de contournement n’est spécifiée.

**serveur proxy proxycfg-p \_**

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a>Exemple 3 : utiliser un proxy différent pour sécuriser les ressources

L’exemple suivant spécifie que les serveurs HTTP sont accessibles via le proxy proxy HTTP et que les \_ serveurs https sont accessibles par le biais du proxy HTTPS \_ . Les sites intranet locaux et tout site dans le \* domaine. Microsoft.com ignorent le proxy.

**proxycfg-p "http = http \_ proxy HTTPS = proxy HTTPS \_ " " <local> ; \* . microsoft.com»**

## <a name="removing-proxycfgexe"></a>Suppression de ProxyCfg.exe

Après avoir utilisé l’outil de configuration de proxy, vous ne pouvez pas restaurer vos paramètres de proxy d’origine. Toutefois, si nécessaire, vous pouvez supprimer les paramètres de Registre créés par l’utilitaire. Pour supprimer les entrées de Registre créées par ProxyCfg.exe, vous devez supprimer la valeur **WinHttpSettings** de la clé de Registre suivante.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings** \\ **connections** \\ **WinHttpSettings**

La suppression de la valeur *WinHttpSettings* supprime toutes les configurations de proxy.

## <a name="proxycfgexe-and-authentication"></a>ProxyCfg.exe et authentification

L’utilitaire de configuration du proxy définit la stratégie d’authentification par défaut. Étant donné que vous ne devez pas effectuer d’authentification NTLM avec des ordinateurs hôtes non approuvés, par défaut, l’authentification NTLM se produit automatiquement uniquement avec les hôtes de la liste de contournement du proxy. S’il n’existe aucun proxy, vous pouvez toujours utiliser ProxyCfg.exe pour spécifier une liste de contournement des hôtes auxquels vous faites confiance pour effectuer l’authentification NTLM. Un nom de proxy est requis lors de l’utilisation de ProxyCfg.exe à cet effet, mais vous pouvez utiliser n’importe quelle chaîne valide à la place d’un nom de proxy réel.

Pour plus d’informations sur la stratégie de connexion automatique, consultez [stratégie d’ouverture de session automatique](authentication-in-winhttp.md).

 

 
