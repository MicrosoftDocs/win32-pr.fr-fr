---
description: Certains serveurs et proxys HTTP requièrent une authentification avant d’autoriser l’accès aux ressources sur Internet. Les fonctions des services HTTP Microsoft Windows (WinHTTP) prennent en charge l’authentification du serveur et du proxy pour les sessions HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Authentification dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dd40e6da1f455e04e24fa740cf4d83da7e0472e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203010"
---
# <a name="authentication-in-winhttp"></a>Authentification dans WinHTTP

Certains serveurs et proxys HTTP requièrent une authentification avant d’autoriser l’accès aux ressources sur Internet. Les fonctions des services HTTP Microsoft Windows (WinHTTP) prennent en charge l’authentification du serveur et du proxy pour les sessions HTTP.

## <a name="about-http-authentication"></a>À propos de l’authentification HTTP

Si l’authentification est requise, l’application HTTP reçoit le code d’état 401 (le serveur nécessite une authentification) ou 407 (le proxy nécessite une authentification). Avec le code d’État, le proxy ou le serveur envoie un ou plusieurs en-têtes Authenticate : WWW-Authenticate (pour l’authentification du serveur) ou Proxy-Authenticate (pour l’authentification du proxy).

Chaque en-tête Authenticate contient un schéma d’authentification pris en charge et, pour les schémas de base et les schémas synthétiques, un domaine. Si plusieurs schémas d’authentification sont pris en charge, le serveur retourne plusieurs en-têtes Authenticate. La valeur de domaine est sensible à la casse et définit un ensemble de serveurs ou de proxys pour lesquels les mêmes informations d’identification sont acceptées. Par exemple, l’en-tête « WWW-Authenticate : Basic domaine = "example" » peut être retourné lorsque l’authentification du serveur est requise. Cet en-tête spécifie que les informations d’identification de l’utilisateur doivent être fournies pour le domaine « example ».

Une application HTTP peut inclure un champ d’en-tête Authorization avec une demande qu’elle envoie au serveur. L’en-tête Authorization contient le schéma d’authentification et la réponse appropriée requise par ce schéma. Par exemple, l’en-tête « Authorization : Basic <username : password> » est ajouté à la demande et envoyé au serveur si le client a reçu l’en-tête de réponse « WWW-Authenticate : Basic Realm = » example «».

> [!Note]  
> Bien qu’elles soient affichées ici sous forme de texte brut, le nom d’utilisateur et le mot de passe sont en fait [*codés en base64*](glossary.md).

 

Il existe deux types généraux de schémas d’authentification :

-   Schéma d’authentification de base, dans lequel le nom d’utilisateur et le mot de passe sont envoyés en texte clair au serveur.

    Le schéma d’authentification de base est basé sur le modèle qu’un client doit identifier lui-même à l’aide d’un nom d’utilisateur et d’un mot de passe pour chaque domaine. Le serveur traite la demande uniquement si la demande est envoyée avec un en-tête d’autorisation qui comprend un nom d’utilisateur et un mot de passe valides.

-   Des schémas de stimulation-réponse, tels que Kerberos, dans lesquels le serveur conteste les [*données d’authentification*](glossary.md)du client. Le client transforme les données avec les informations d’identification de l’utilisateur et renvoie les données transformées au serveur à des fins d’authentification.

    Les schémas de stimulation/réponse permettent une authentification plus sécurisée. Dans un schéma de stimulation/réponse, le nom d’utilisateur et le mot de passe ne sont jamais transmis sur le réseau. Une fois que le client a sélectionné un modèle de stimulation-réponse, le serveur renvoie un code d’état approprié avec un challenge contenant les [*données d’authentification*](glossary.md) de ce schéma. Le client renvoie ensuite la demande avec la réponse appropriée pour obtenir le service demandé. Les schémas de stimulation/réponse peuvent exécuter plusieurs échanges.

Le tableau suivant répertorie les schémas d’authentification pris en charge par WinHTTP, le type d’authentification et une description du schéma.



| Schéma            | Type               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| De base (texte en clair) | De base              | Utilise une chaîne [*encodée en base64*](glossary.md) qui contient le nom d’utilisateur et le mot de passe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest            | Stimulation-réponse | Défis liés à l’utilisation d’une valeur à usage unique (chaîne de données spécifiée par le serveur). Une réponse valide contient une somme de contrôle du nom d’utilisateur, du mot de passe, de la valeur de nonce donnée, du [*verbe http*](glossary.md)et de l’Uniform Resource Identifier (Uri) demandé.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | Stimulation-réponse | Requiert la transformation des [*données d’authentification*](glossary.md) avec les informations d’identification de l’utilisateur pour prouver l’identité. Pour que l’authentification NTLM fonctionne correctement, plusieurs échanges doivent avoir lieu sur la même connexion. Par conséquent, l’authentification NTLM ne peut pas être utilisée si un proxy intermédiaire ne prend pas en charge les connexions persistantes. L’authentification NTLM échoue également si [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) est utilisé avec l’indicateur [**\_ Disable \_ Keep \_ Alive WinHTTP**](option-flags.md) qui désactive la sémantique Keep-Alive.                                                                                                                                                                                                                                       |
| Passport          | Stimulation-réponse | Utilise [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Negotiate         | Stimulation-réponse | Si le serveur et le client utilisent tous deux Windows 2000 ou une version ultérieure, l’authentification Kerberos est utilisée. Sinon, l’authentification NTLM est utilisée. Kerberos est disponible dans les systèmes d’exploitation Windows 2000 et versions ultérieures et est considéré comme plus sécurisé que l’authentification NTLM. Pour que l’authentification par négociation fonctionne correctement, plusieurs échanges doivent avoir lieu sur la même connexion. Par conséquent, l’authentification Negotiate ne peut pas être utilisée si un proxy intermédiaire ne prend pas en charge les connexions persistantes. L’authentification par négociation échoue également si [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) est utilisé avec l’indicateur de [**désactivation de la fonction de \_ \_ maintien \_**](option-flags.md) de l’activité WinHTTP qui désactive la sémantique Keep-Alive. Le schéma d’authentification Negotiate est parfois appelé authentification Windows intégrée. |



 

## <a name="authentication-in-winhttp-applications"></a>Authentification dans les applications WinHTTP

L’interface de programmation d’applications (API) WinHTTP fournit deux fonctions utilisées pour accéder aux ressources Internet lorsque l’authentification est nécessaire : [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) et [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).

Quand une réponse est reçue avec un code d’état 401 ou 407, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) peut être utilisé pour analyser les en-têtes d’authentification afin de déterminer les schémas d’authentification pris en charge et la cible d’authentification. La cible d’authentification est le serveur ou le proxy qui demande l’authentification. **WinHttpQueryAuthSchemes** détermine également le premier schéma d’authentification, à partir des schémas disponibles, en fonction des préférences de schéma d’authentification suggérées par le serveur. Cette méthode de choix d’un schéma d’authentification est le comportement suggéré par [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) permet à une application de spécifier le schéma d’authentification utilisé avec un nom d’utilisateur et un mot de passe valides pour une utilisation sur le serveur ou le proxy cible. Après avoir défini les informations d’identification et renvoyé la demande, les en-têtes nécessaires sont générés et ajoutés automatiquement à la demande. Étant donné que certains schémas d’authentification requièrent plusieurs transactions, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) peut renvoyer l’erreur, erreur WinHTTP de renvoi de \_ \_ \_ demande. Lorsque cette erreur se produit, l’application doit continuer à renvoyer la demande jusqu’à la réception d’une réponse qui ne contient pas de code d’état 401 ou 407. Un code d’état 200 indique que la ressource est disponible et que la demande est réussie. Consultez [**codes d’État http**](http-status-codes.md) pour obtenir des codes d’État supplémentaires qui peuvent être retournés.

Si un schéma d’authentification et des informations d’identification acceptables sont connus avant l’envoi d’une demande au serveur, une application peut appeler [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) avant d’appeler [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Dans ce cas, WinHTTP tente une pré-authentification avec le serveur en fournissant des informations d’identification ou des [*données d’authentification*](glossary.md) dans la demande initiale au serveur. La pré-authentification peut réduire le nombre d’échanges dans le processus d’authentification et, par conséquent, améliorer les performances de l’application.

La pré-authentification peut être utilisée avec les schémas d’authentification suivants :

-   De base-toujours possible.
-   Négocier la résolution dans Kerberos-probablement possible ; la seule exception est lorsque les décalages de temps sont désactivés entre le client et le contrôleur de domaine.
-   (Négocier la résolution dans NTLM)-jamais possible.
-   NTLM-possible dans Windows Server 2008 R2 uniquement.
-   Digest-jamais possible.
-   Passport-jamais possible ; après la stimulation-réponse initiale, WinHTTP utilise des cookies pour se pré-authentifier auprès de Passport.

Une application WinHTTP standard effectue les étapes suivantes afin de gérer l’authentification.

-   Demandez une ressource avec [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) et [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).
-   Vérifiez les en-têtes de réponse avec [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
-   Si un code d’état 401 ou 407 est retourné, indiquant que l’authentification est requise, appelez [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) pour trouver un schéma acceptable.
-   Définissez le schéma d’authentification, le nom d’utilisateur et le mot de passe avec [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).
-   Renvoyez la requête avec le même handle de demande en appelant [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

Les informations d’identification définies par [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) sont utilisées uniquement pour une demande. WinHTTP ne met pas en cache les informations d’identification à utiliser dans d’autres requêtes, ce qui signifie que les applications doivent être écrites pour répondre à plusieurs demandes. Si une connexion authentifiée est réutilisée, les autres demandes peuvent ne pas être renouvelées, mais votre code doit être en mesure de répondre à une demande à tout moment.

### <a name="example-retrieving-a-document"></a>Exemple : extraction d’un document

L’exemple de code suivant tente de récupérer un document spécifié à partir d’un serveur HTTP. Le code d’État est récupéré à partir de la réponse pour déterminer si l’authentification est requise. Si un code d’état 200 est trouvé, le document est disponible. Si le code d’état 401 ou 407 est trouvé, l’authentification est requise avant que le document puisse être récupéré. Pour tout autre code d’État, un message d’erreur s’affiche. Pour obtenir la liste des codes d’État possibles, consultez [**codes d’État http**](http-status-codes.md) .


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a>Stratégie d’ouverture de session automatique

La stratégie de connexion automatique (ouverture de session automatique) détermine le moment où il est acceptable pour WinHTTP d’inclure les informations d’identification par défaut dans une demande. Les informations d’identification par défaut sont le jeton de thread actuel ou le jeton de session, selon que WinHTTP est utilisé en mode synchrone ou asynchrone. Le jeton de thread est utilisé en mode synchrone, et le jeton de session est utilisé en mode asynchrone. Ces informations d’identification par défaut sont souvent le nom d’utilisateur et le mot de passe utilisés pour se connecter à Microsoft Windows.

La stratégie d’ouverture de session automatique a été implémentée pour éviter que ces informations d’identification ne soient utilisées de façon illégale pour l’authentification auprès d’un serveur non approuvé. Par défaut, le niveau de sécurité est défini sur le \_ niveau de sécurité WinHTTP AUTOlogon \_ \_ \_ , ce qui permet d’utiliser les informations d’identification par défaut uniquement pour les requêtes intranet. La stratégie d’ouverture de session automatique s’applique uniquement aux schémas d’authentification NTLM et Negotiate. Les informations d’identification ne sont jamais transmises automatiquement avec d’autres schémas.

La stratégie d’ouverture de session automatique peut être définie à l’aide de la fonction [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l’option WinHTTP de l’indicateur de [**\_ \_ \_ stratégie AutoLogon**](option-flags.md) . Cet indicateur s’applique uniquement au handle de demande. Lorsque la stratégie est définie sur le niveau de sécurité WINHTTP ouverture de la stratégie \_ \_ \_ \_ faible, les informations d’identification par défaut peuvent être envoyées à tous les serveurs. Lorsque la stratégie est définie sur le \_ niveau de sécurité WinHTTP AUTOlogon \_ \_ \_ élevé, les informations d’identification par défaut ne peuvent pas être utilisées pour l’authentification. Il est fortement recommandé d’utiliser l’ouverture de session automatique au niveau du support.

## <a name="stored-user-names-and-passwords"></a>Noms d’utilisateur et mots de passe stockés

Windows XP a introduit le concept de noms d’utilisateurs et de mots de passe stockés. Si les informations d’identification Passport d’un utilisateur sont enregistrées via l' **Assistant Inscription Passport** ou la **boîte de dialogue informations d’identification** standard, elles sont enregistrées dans les noms d’utilisateur et mots de passe stockés. Quand vous utilisez WinHTTP sur Windows XP ou version ultérieure, WinHTTP utilise automatiquement les informations d’identification dans les noms d’utilisateurs et les mots de passe stockés si les informations d’identification ne sont pas définies explicitement. Cela est similaire à la prise en charge des informations d’identification d’ouverture de session par défaut pour NTLM/Kerberos. Toutefois, l’utilisation des informations d’identification Passport par défaut n’est pas soumise aux paramètres de stratégie d’ouverture de session automatique.

 

 



