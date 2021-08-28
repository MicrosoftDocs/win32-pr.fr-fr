---
title: Activation des fonctionnalités Internet
description: Avant d’utiliser les fonctions WinINet, l’application doit tenter d’établir une connexion à Internet à l’aide de la fonction InternetAttemptConnect.
ms.assetid: 80747c0d-5a09-4ffa-a0ca-b051b82acbf8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f4780b508059c088e2948829662171fd6df46f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885493"
---
# <a name="enabling-internet-functionality"></a>Activation des fonctionnalités Internet

Avant d’utiliser les fonctions WinINet, l’application doit tenter d’établir une connexion à Internet à l’aide de la fonction [**InternetAttemptConnect**](/windows/desktop/api/Wininet/nf-wininet-internetattemptconnect) . Cette fonction appelle la boîte de dialogue d’accès à distance pour établir une connexion à Internet ou vérifier si une connexion existe déjà. Si cette fonction échoue, l’application peut passer en mode hors connexion, ce qui lui permet d’accéder aux informations mises en cache lors des connexions précédentes à Internet.

Utilisez la fonction [**InternetCheckConnection**](/windows/desktop/api/Wininet/nf-wininet-internetcheckconnectiona) pour vérifier la connexion à Internet. Elle tente d’effectuer un test ping sur le serveur désigné par l’URL transmise à la fonction. Si l’indicateur \_ de \_ connexion de force ICC \_ est défini et que l’URL est **null**, la fonction vérifie s’il existe une entrée dans la base de données du serveur pour le serveur le plus proche. S’il en existe un, la fonction exécute une commande ping sur ce serveur.

Ensuite, utilisez la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) pour définir les caractéristiques de la connexion Internet que l’application cliente utilise. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) crée le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) racine qui est utilisé pour établir des sessions [http](http-sessions.md)[FTP](ftp-sessions.md) . [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) ne teste pas la connexion à Internet pour vérifier que les caractéristiques transmises à la fonction sont correctes.

Utilisez la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pour créer une session spécifique. [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Initialise une session pour le site spécifié à l’aide des arguments qui lui sont passés et crée un handle [**HINTERNET**](appendix-a-hinternet-handles.md) qui est une branche du handle racine. [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) n’essaie pas d’accéder ou d’établir une connexion au site spécifié, sauf dans le cas d’une session FTP. Les fonctions [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)et [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) utilisent le descripteur créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pour établir une connexion au site spécifié.

## <a name="using-internetopen"></a>Utilisation de InternetOpen

Pour activer une connexion à Internet, vous devez créer un descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) racine à l’aide de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Informations sur l’agent utilisateur (l’application appelant les fonctions Internet), le type d’accès à Internet, les noms de proxy, les hôtes et les adresses qui contournent le proxy, et le comportement est passé à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="setting-the-user-agent"></a>Configuration de l’agent utilisateur

L’application appelante doit fournir une chaîne qui contient le nom de l’application ou de l’entité qui accède à Internet au paramètre *lpszAgent* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Cette chaîne est utilisée comme agent utilisateur dans le protocole HTTP. Par exemple, Microsoft Internet Explorer utilise « Microsoft Internet Explorer ».

### <a name="setting-access-types"></a>Définition des types d’accès

[**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) prend en charge trois types d’accès :

-   Utilisez \_ \_ le type Open Internet \_ direct si le système sur lequel l’application s’exécute utilise une connexion directe à Internet. Les paramètres *lpszProxyName* et *lpszProxyBypass* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) ne sont pas utilisés et doivent avoir la valeur **null**.
-   Utilisez \_ \_ le proxy de type Internet Open \_ si le système sur lequel l’application s’exécute utilise un ou plusieurs serveurs proxy pour accéder à Internet. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) utilise les serveurs proxy indiqués par *lpszProxyName* et contourne le proxy pour tous les noms d’hôte ou adresses IP spécifiés par *lpszProxyBypass*.
-   Utilisez \_ \_ \_ la préconfiguration du type ouvert sur Internet pour indiquer à votre application d’extraire la configuration du Registre. C’est généralement le meilleur choix, car la plupart des applications, y compris les navigateurs Web, utilisent cette option.

\_ \_ La préconfiguration de type ouvert Internet \_ examine les valeurs de Registre **ProxyEnable**, **ProxyServer** et **ProxyOverride**. ces valeurs se trouvent sous « HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Paramètres ».

Si **ProxyEnable** est égal à zéro, l’application utilise le \_ type Open Internet \_ \_ direct. Dans le cas contraire, l’application utilise \_ \_ le proxy de type ouvert Internet \_ et utilise les informations **ProxyServer** et **ProxyOverride** .

Les fonctions WinINet prennent en charge les proxys de type SOCKS uniquement si Internet Explorer est installé. L’installation d’Internet Explorer comprend le fichier Wsock32n.dll, qui est nécessaire pour prendre en charge les proxys SOCKS. Wsock32n.dll n’est pas redistribuable.

### <a name="listing-proxy-servers"></a>Liste des serveurs proxy

WinINet reconnaît deux types de proxies : les proxys de type CERN (HTTP uniquement) et les proxys FTP TIS (FTP uniquement). Si Internet Explorer est installé, WinINet prend également en charge les proxys de type SOCKS. [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) suppose, par défaut, que le proxy spécifié est un proxy CERN. Si le type d’accès est défini sur INTERNET \_ Open \_ type direct ou sur la \_ \_ \_ \_ préconfiguration de type Open Internet, le paramètre *LpszProxyName* de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) doit avoir la valeur **null**. Dans le cas contraire, la valeur transmise à *lpszProxyName* doit contenir les proxies dans une chaîne délimitée par des espaces. Les listes de proxy peuvent contenir le numéro de port utilisé pour accéder au proxy.

Pour répertorier un proxy pour un protocole spécifique, la chaîne doit respecter le format « » &lt; protocole de protocole &gt; &lt; &gt; ://<nom du proxy \_> « ». Les protocoles valides sont HTTP, HTTPs et FTP. Par exemple, pour répertorier un proxy FTP, une chaîne valide serait « » ftp = ftp://FTP \_ proxy \_ Name : 21 " », où FTP \_ proxy \_ Name est le nom du proxy FTP et 21 le numéro de port qui doit être utilisé pour accéder au proxy. Si le proxy utilise le numéro de port par défaut pour ce protocole, le numéro de port peut être omis. Si un nom de proxy est listé par lui-même, il est utilisé comme proxy par défaut pour tous les protocoles qui n’ont pas de proxy spécifique spécifié. Par exemple, « http = https://http\_proxy other » utilise \_ un proxy HTTP pour toutes les opérations http, tandis que tous les autres protocoles utiliseraient other.

Par défaut, la fonction suppose que le proxy spécifié par *lpszProxyName* est un proxy CERN. Une application peut spécifier plusieurs proxys, y compris des proxies différents pour les différents protocoles. Par exemple, si vous spécifiez «"ftp = ftp://FTP-GW HTTP = https://jericho:99 proxy" ", les demandes FTP sont effectuées via le proxy FTP-GW, qui écoute le port 21, et les requêtes http sont effectuées via un proxy CERN appelé Jéricho, qui écoute le port 99. Sinon, les requêtes HTTP sont effectuées via le proxy CERN appelé proxy, qui écoute le port 80. Notez que si l’application utilise uniquement FTP, par exemple, elle n’a pas besoin de spécifier « » ftp = ftp://FTP-GW : 21 " ». Il peut spécifier simplement «« FTP-GW »». Une application est uniquement requise pour spécifier les noms de protocole si elle utilise plusieurs protocoles par handle renvoyé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="listing-the-proxy-bypass"></a>Affichage du contournement du proxy

Les noms d’hôtes ou adresses IP qui ne doivent pas être envoyés au proxy peuvent être répertoriés dans la liste de contournement du proxy. Cette liste peut contenir des caractères génériques, « \* », qui obligent l’application à contourner le serveur proxy pour les adresses qui correspondent au modèle spécifié. Pour répertorier plusieurs adresses et noms d’hôtes, séparez-les par des points-virgules dans la chaîne de contournement du proxy. Si la &lt; macro « locale &gt; » est spécifiée, la fonction contourne le proxy pour tout nom d’hôte qui ne contient pas de point.

Par défaut, WinINet contournera le proxy pour les demandes qui utilisent les noms d’hôte « localhost », « Loopback », « 127.0.0.1 » ou « \[ :: 1 \] ». Ce comportement existe parce qu’un serveur proxy distant ne résout généralement pas correctement ces adresses.

**Internet Explorer 9 :** Vous pouvez supprimer l’ordinateur local de la liste de contournement du proxy à l’aide de la macro « <-loopback> ».

L’exemple suivant montre des exemples d’appels à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) à l’aide de différentes chaînes de contournement du proxy. Les commentaires au-dessus de chaque appel décrivent l’effet de la chaîne de contournement sur les noms d’hôte qui sont accessibles à partir du handle [**HINTERNET**](appendix-a-hinternet-handles.md) qu’elle crée.


```C++
HINTERNET hInternetRoot;

/* bypass the proxy for any host name that does not 
    contain a period */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("<local>"), 0);

/* bypass the proxy for any host name that starts with the 
    letters "ms" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("ms*"), 0);

/* bypass the proxy for any host name that contains "int", 
    such as "internet" and "painter" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("*int*"), 0);

/* bypass the proxy for the host name "example" and any 
    host name that contains "test" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("example *test*"), 0);

/* Disable the loopback proxy bypass for localhost */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("127.0.0.1:8888"),TEXT("<-loopback>"), 0);
```



## <a name="using-internetconnect"></a>Utilisation de InternetConnect

Pour commencer une session, la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) doit créer un handle à partir du handle racine retourné par la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) . [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) définit l’adresse du serveur, le numéro de port, le nom d’utilisateur, le mot de passe et le type de service.

[**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilise le handle [**HINTERNET**](appendix-a-hinternet-handles.md) racine créé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) pour établir un handle de session. Si l' [indicateur \_ \_ Async de l’indicateur Internet](api-flags.md) a été défini dans l’appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), l’appel à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) doit inclure une valeur de contexte différente de zéro.

Le nom du serveur peut contenir soit le nom d’hôte (par exemple, « www.servername.com »), soit le numéro d’adresse IP du site au format décimal avec points ASCII (par exemple, « 10.0.1.45 »).

Le port du serveur est le numéro de port TCP/IP (Transmission Control Protocol/Internet Protocol) auquel se connecter sur le serveur. [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilise le port par défaut pour le type de service sélectionné si la \_ valeur de numéro de port Internet non valide \_ \_ est utilisée. Les tableaux suivants contiennent les valeurs par défaut du port du serveur pour WinINet.




| Valeur | Signification | 
|-------|---------|
| INTERNET_DEFAULT_FTP_PORT | Utilisez le port par défaut pour les serveurs FTP (port 21). | 
| INTERNET_DEFAULT_GOPHER_PORT | Utilisez le port par défaut pour les serveurs Gopher (port 70).<blockquote>[!Note]<br />Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</blockquote><br /> | 
| INTERNET_DEFAULT_HTTP_PORT | Utilisez le port par défaut pour les serveurs http (port 80). | 
| INTERNET_DEFAULT_HTTPS_PORT | Utilisez le port par défaut pour les serveurs HTTPS (port 443). | 
| INTERNET_DEFAULT_SOCKS_PORT | Utilisez le port par défaut pour les serveurs de pare-feu SOCKS (port 1080). | 




 

### <a name="defining-the-user-name-and-password"></a>Définition du nom d’utilisateur et du mot de passe

La valeur de *lpszUsername* est l’adresse d’une chaîne terminée par le caractère **null** qui contient le nom de l’utilisateur qui se connecte. Si ce paramètre a la **valeur null**, la fonction utilise une valeur par défaut appropriée, à l’exception de http. Un paramètre **null** dans http entraîne le renvoi d’une erreur par le serveur. Pour le protocole FTP, la valeur par défaut est Anonymous.

La valeur de *lpszPassword* est l’adresse d’une chaîne terminée par le caractère **null** qui contient le mot de passe de connexion. Si *lpszUsername* et *lpszPassword* ont tous les deux la **valeur null**, la fonction utilise le mot de passe anonyme par défaut. Dans le cas de FTP, le mot de passe anonyme par défaut est le nom de messagerie de l’utilisateur. Si *lpszUsername* n’a pas la **valeur null** et que *lpszPassword* a la **valeur null**, la fonction utilise un mot de passe vide. Il existe quatre paramètres possibles de *lpszUsername* et *lpszPassword*, qui produisent les comportements indiqués dans le tableau suivant.



| *lpszUsername*      | *lpszPassword*      | Nom d’utilisateur envoyé au serveur FTP | Mot de passe envoyé au serveur FTP |
|---------------------|---------------------|------------------------------|-----------------------------|
| **NULL**            | **NULL**            | façon                  | Nom de messagerie de l’utilisateur           |
| Chaîne non **null** | **NULL**            | *lpszUsername*               | ""                          |
| **NULL**            | Chaîne non **null** | ERROR                        | ERROR                       |
| Chaîne non **null** | Chaîne non **null** | *lpszUsername*               | *lpszPassword*              |



 

Ces informations peuvent être modifiées à l’aide des fonctions [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) et [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) . [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) modifie les valeurs de nom d’utilisateur et de mot de passe, tandis que [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) affiche une boîte de dialogue qui demande le nom d’utilisateur et le mot de passe appropriés.

### <a name="defining-the-session"></a>Définition de la session

Pour définir la session en cours d’établissement, définissez le type de service, les indicateurs et la valeur de contexte pour [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

Deux types de service sont disponibles pour [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta): Internet \_ service \_ FTP et Internet \_ service \_ http. Le \_ \_ protocole http du service Internet est utilisé pour les sessions HTTP et HTTPS.

[Internet \_ FLAG \_ passive](api-flags.md) est le seul indicateur spécifique au service utilisé par les fonctions WinInet. Cet indicateur peut être défini lorsque le type de service est INTERNET \_ service \_ FTP afin d’utiliser la sémantique FTP passive.

Pour toutes les opérations synchrones, la valeur de *dwContext* doit être définie sur zéro. Si des opérations asynchrones ont été établies en définissant l’indicateur de l' [ \_ indicateur \_ Async Internet](api-flags.md) dans l’appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), une valeur différente de zéro doit être fournie pour *dwContext*. Pour plus d’informations sur les opérations asynchrones, consultez [Configuration des opérations asynchrones](common-functions.md).

Pour les sessions FTP, [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) tente d’établir une connexion au serveur sur Internet. Pour les sessions HTTP, [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) n’établit pas de connexion tant qu’une autre fonction n’a pas tenté d’obtenir des informations à partir du serveur.

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

