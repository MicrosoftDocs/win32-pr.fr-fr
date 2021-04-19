---
title: Gestion de l’authentification
description: Certains proxys et serveurs requièrent une authentification avant d’accorder l’accès aux ressources sur Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82d8cd93f1010c71560d856793ad06d8bc5d9d5
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380853"
---
# <a name="handling-authentication"></a>Gestion de l’authentification

Certains proxys et serveurs requièrent une authentification avant d’accorder l’accès aux ressources sur Internet. Les fonctions WinINet prennent en charge l’authentification du serveur et du proxy pour les sessions http. L’authentification des serveurs FTP doit être gérée par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . Actuellement, l’authentification de la passerelle FTP n’est pas prise en charge.

## <a name="about-http-authentication"></a>À propos de l’authentification HTTP

Si l’authentification est requise, l’application cliente reçoit un code d’état 401, si le serveur requiert une authentification, ou 407, si le proxy requiert une authentification. Avec le code d’État, le proxy ou le serveur envoie un ou plusieurs en-têtes de réponse d’authentification (Proxy-Authenticate (pour l’authentification du proxy) ou WWW-Authenticate (pour l’authentification du serveur).

Chaque en-tête de réponse Authenticate contient un schéma d’authentification disponible et un domaine. Si plusieurs schémas d’authentification sont pris en charge, le serveur retourne plusieurs en-têtes de réponse d’authentification. La valeur de domaine est sensible à la casse et définit un espace de protection sur le proxy ou le serveur. Par exemple, l’en-tête « WWW-Authenticate : Basic Realm = » exemple «» est un exemple d’en-tête retourné lorsque l’authentification du serveur est requise.

L’application cliente qui a envoyé la demande peut s’authentifier en incluant un champ d’en-tête d’autorisation avec la requête. L’en-tête Authorization contient le schéma d’authentification et la réponse appropriée requis par ce schéma. Par exemple, l’en-tête « Authorization : Basic \<username:password> » est ajouté à la demande et renvoyé au serveur si le client a reçu l’en-tête de réponse d’authentification « www-Authenticate : Basic Realm = » example «».

Il existe deux types généraux de schémas d’authentification :

-   Schéma d’authentification de base, où le nom d’utilisateur et le mot de passe sont envoyés en texte clair au serveur.
-   Les schémas de stimulation-réponse, qui permettent un format de stimulation/réponse.

Le schéma d’authentification de base est basé sur le modèle qu’un client doit s’authentifier avec un nom d’utilisateur et un mot de passe pour chaque domaine. Le serveur traite la demande s’il est renvoyé avec un en-tête d’autorisation qui comprend un nom d’utilisateur et un mot de passe valides.

Les schémas de stimulation/réponse permettent une authentification plus sécurisée. Si une demande nécessite une authentification à l’aide d’un modèle de stimulation-réponse, le code d’État et les en-têtes d’authentification appropriés sont retournés au client. Le client doit ensuite renvoyer la demande avec un Negotiate. Le serveur renvoie un code d’état approprié avec un défi, et le client a alors besoin de renvoyer la demande avec la réponse appropriée pour obtenir le service demandé.

Le tableau suivant répertorie les schémas d’authentification, le type d’authentification, la DLL qui les prend en charge et une description du schéma.



| Schéma                                    | Type               | DLL                  | Description                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| De base (texte en clair)                         | basic              | Wininet.dll          | Utilise une chaîne encodée en base64 qui contient le nom d’utilisateur et le mot de passe.                                                                                                                                                                                                                                                                             |
| Digest                                    | stimulation-réponse | Digest.dll           | Un schéma de stimulation/réponse qui est le défi de l’utilisation d’une valeur à usage unique (chaîne de données spécifiée par le serveur). Une réponse valide contient une somme de contrôle du nom d’utilisateur, du mot de passe, de la valeur nonce donnée, de la méthode HTTP et de l’Uniform Resource Identifier (URI) demandé. La prise en charge de l’authentification Digest a été introduite dans Microsoft Internet Explorer 5. |
| NT LAN Manager (NTLM)                     | stimulation-réponse | Winsspi.dll          | Un modèle de stimulation-réponse qui fonde le défi sur le nom d’utilisateur.                                                                                                                                                                                                                                                                             |
| Réseau Microsoft (MSN)                   | stimulation-réponse | Msnsspc.dll          | Schéma d’authentification de The Microsoft Network.                                                                                                                                                                                                                                                                                                     |
| Authentification par mot de passe distribué (DPA) | stimulation-réponse | Msapsspc.dll         | Similaire à l’authentification MSN et est également utilisé par le réseau Microsoft.                                                                                                                                                                                                                                                                           |
| Authentification par mot de passe distant (RPA)    | CompuServe         | Rpawinet.dll, da.dll | Schéma d’authentification CompuServe. Pour plus d’informations, consultez les [spécifications du mécanisme RPA](https://www.compuserve.com/).                                                                                                                                                                                                    |



 

Pour tout autre chose que l’authentification de base, les clés de Registre doivent être configurées en plus de l’installation de la DLL appropriée.

Si l’authentification est requise, l’indicateur de maintien de la [ \_ \_ \_ connexion à l’indicateur Internet](api-flags.md) doit être utilisé dans l’appel à [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). L’indicateur de maintien de la connexion à l' \_ indicateur Internet \_ \_ est requis pour NTLM et d’autres types d’authentification afin de maintenir la connexion lors de l’exécution du processus d’authentification. Si la connexion n’est pas maintenue, le processus d’authentification doit être redémarré avec le proxy ou le serveur.

Les fonctions [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) et [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) s’exécutent correctement, même lorsque l’authentification est requise. La différence est que les données retournées dans les fichiers d’en-tête et [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) recevront une page HTML informant l’utilisateur du code d’État.

### <a name="registering-authentication-keys"></a>Inscription des clés d’authentification

\_ \_ La préconfiguration de type ouvert Internet \_ examine les valeurs de Registre **ProxyEnable**, **ProxyServer** et **ProxyOverride**. Ces valeurs se trouvent sous **HKEY \_ Current \_ User** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.

Pour les schémas d’authentification autres que Basic, une clé doit être ajoutée au Registre sous **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. Une valeur **DWORD** , **Flags**, doit être définie avec la valeur appropriée. La liste suivante affiche les valeurs possibles pour la valeur **Flags** .

-   Contexte unique des indicateurs d’authentification du plug-in \_ \_ \_ \_ \_ par \_ tcpip (valeur = 0x01)

    Chaque socket TCP/IP (Transmission Control Protocol/Internet Protocol) contient un contexte différent. Dans le cas contraire, un nouveau contexte est passé pour chaque modèle d’URL de domaine ou de bloc.

-   Les \_ indicateurs d’authentification de plug-in \_ \_ peuvent \_ gérer \_ l’interface utilisateur (valeur = 0x02)

    Cette DLL peut gérer ses propres entrées utilisateur.

-   Les \_ indicateurs d’authentification de plug-in \_ \_ \_ ne peuvent gérer \_ aucun \_ passwd (valeur = 0x04)

    Cette DLL peut être en capacité d’effectuer une authentification sans inviter l’utilisateur à entrer un mot de passe.

-   Indicateurs d’authentification du plug-in \_ \_ \_ non \_ domaine (valeur = 0x08)

    Cette DLL n’utilise pas de chaîne de domaine http standard. Toutes les données qui semblent être un domaine sont des données spécifiques au schéma.

-   Indicateurs d’authentification du plug-in \_ \_ \_ Keep \_ Alive \_ non \_ requis (valeur = 0x10)

    Cette DLL ne requiert pas de connexion permanente pour sa séquence de stimulation/réponse.

Par exemple, pour ajouter l’authentification NTLM, vous devez ajouter la clé NTLM à la sécurité du logiciel de l' **\_ \_ ordinateur local** de la \\  \\ **sécurité Microsoft** \\ **Internet Explorer** \\ . Sous **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM**, la valeur de chaîne, **DLLFile** et une valeur **DWORD** , **Flags**, doit être ajoutée. **DLLFile** doit avoir la valeur Winsspi.dll et les **indicateurs** doivent avoir la valeur 0x08.

### <a name="server-authentication"></a>Authentification du serveur

Lorsqu’un serveur reçoit une demande qui requiert une authentification, le serveur renvoie un message de code d’état 401. Dans ce message, le serveur doit inclure un ou plusieurs en-têtes de réponse WWW-Authenticate. Ces en-têtes incluent les méthodes d’authentification disponibles sur le serveur. WinINet choisit la première méthode qu’il reconnaît.

L’authentification de base offre une sécurité faible, sauf si le canal est tout d’abord chiffré avec SSL ou PCT.

La fonction [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) peut être utilisée pour obtenir les données de nom d’utilisateur et de mot de passe de l’utilisateur, ou une interface utilisateur personnalisée peut être conçue pour obtenir les données.

Une interface personnalisée peut utiliser la fonction [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) pour définir les valeurs de [ \_ \_ mot de passe](option-flags.md) de l’option Internet et de l' [ \_ option \_ Internet](option-flags.md) , puis renvoyer la demande au serveur.

### <a name="proxy-authentication"></a>Authentification proxy

Lorsqu’un client tente d’utiliser un proxy qui requiert une authentification, le proxy renvoie un message de code d’État 407 au client. Dans ce message, le proxy doit inclure un ou plusieurs en-têtes de réponse Proxy-Authenticate. Ces en-têtes incluent les méthodes d’authentification disponibles à partir du proxy. WinINet choisit la première méthode qu’il reconnaît.

La fonction [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) peut être utilisée pour obtenir les données de nom d’utilisateur et de mot de passe de l’utilisateur, ou une interface utilisateur personnalisée peut être conçue.

Une interface personnalisée peut utiliser la fonction [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) pour définir le [ \_ \_ \_ mot de passe de l’option Internet](option-flags.md) et les valeurs du [ \_ \_ \_ nom d’utilisateur du proxy](option-flags.md) de l’option Internet, puis renvoyer la demande au proxy.

Si aucun nom d’utilisateur et mot de passe de proxy n’est défini, WinINet tente d’utiliser le nom d’utilisateur et le mot de passe pour le serveur. Ce comportement permet aux clients d’implémenter la même interface utilisateur personnalisée que celle utilisée pour gérer l’authentification du serveur.

## <a name="handling-http-authentication"></a>Gestion de l’authentification HTTP

L’authentification HTTP peut être gérée à l’aide de [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) ou d’une fonction personnalisée qui utilise [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) ou qui ajoute ses propres en-têtes d’authentification. [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) peut examiner les en-têtes associés à un handle [**HINTERNET**](appendix-a-hinternet-handles.md) pour rechercher les erreurs masquées, telles que les codes d’état d’un proxy ou d’un serveur. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) peut être utilisée pour définir le nom d’utilisateur et le mot de passe du proxy et du serveur. Pour l’authentification MSN et DPA, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) doit être utilisé pour définir le nom d’utilisateur et le mot de passe.

Pour toute fonction personnalisée qui ajoute ses propres WWW-Authenticate ou Proxy-Authenticate en-têtes, l’indicateur [Internet \_ Flag \_ no \_ auth](api-flags.md) doit être défini pour désactiver l’authentification.

L’exemple suivant montre comment [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) peut être utilisé pour gérer l’authentification http.


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



Dans l’exemple, dwErrorCode est utilisé pour stocker toutes les erreurs associées à l’appel à [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) se termine correctement, même si le proxy ou le serveur requiert une authentification. Lorsque le \_ \_ filtre de l’interface utilisateur erreur \_ des indicateurs pour les \_ \_ Erreurs est passé à [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), la fonction vérifie les en-têtes pour les erreurs masquées. Ces erreurs masquées incluent toutes les demandes d’authentification. [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) affiche la boîte de dialogue appropriée pour inviter l’utilisateur à entrer les données nécessaires. Les indicateurs de l' \_ \_ interface utilisateur erreur indicateurs \_ \_ Générer \_ les données et indicateurs \_ erreur \_ de modification des indicateurs d’interface utilisateur \_ \_ \_ doivent également être passés à [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), de sorte que la fonction construit la structure de données appropriée pour l’erreur et stocke les résultats de la boîte de dialogue dans le handle [**HINTERNET**](appendix-a-hinternet-handles.md) .

L’exemple de code suivant montre comment l’authentification peut être gérée à l’aide de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 