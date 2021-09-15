---
description: Cette section montre comment écrire un script qui utilise l’objet WinHttpRequest pour accéder aux données à partir d’un serveur qui requiert l’authentification HTTP.
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: Authentification à l’aide d’un script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d33b8042cd1fd15d46e15dfb3624e0d3b4a885b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519373"
---
# <a name="authentication-using-script"></a>Authentification à l’aide d’un script

Cette section montre comment écrire un script qui utilise l’objet [**WinHttpRequest**](winhttprequest.md) pour accéder aux données à partir d’un serveur qui requiert l’authentification http.

-   [Conditions préalables et configuration requise](#prerequisites-and-requirements)
-   [Accès à un site Web avec l’authentification](#accessing-a-web-site-with-authentication)
-   [Vérification des codes d’État](#checking-the-status-codes)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites-and-requirements"></a>Conditions préalables et configuration requise

outre les connaissances pratiques de Microsoft JScript, cet exemple nécessite les éléments suivants :

-   version actuelle du kit de développement logiciel (SDK) Microsoft Windows.
-   l’outil de configuration de proxy pour établir les paramètres de proxy pour les Services HTTP Microsoft Windows (WinHTTP), si votre connexion à Internet s’effectue via un serveur proxy. Pour plus d’informations [ , consultezProxycfg.exe, un outil de configuration de proxy](proxycfg-exe--a-proxy-configuration-tool.md) .
-   Une bonne connaissance de la terminologie et des concepts relatifs au [réseau](network-terminology.md) .

## <a name="accessing-a-web-site-with-authentication"></a>Accès à un site Web avec l’authentification

**Pour créer un script illustrant l’authentification, procédez comme suit :**

1.  ouvrez un éditeur de texte tel que Microsoft Bloc-notes.
2.  Copiez le code suivant dans l’éditeur de texte après avoir remplacé « \[ authenticationSite \] » par le texte approprié pour spécifier l’URL d’un site qui requiert l’authentification http.

    ```VB
    // Load the WinHttpRequest object.
    var WinHttpReq = 
              new ActiveXObject("WinHttp.WinHttpRequest.5.1");

    function getText1( )
    {
      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false;

      // Send a request to the server and wait for a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "No Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText);
      WScript.Echo( WinHttpReq.GetAllResponseHeaders);
      WScript.Echo( );
    };

    function getText2( )
    {
      // HttpRequest SetCredentials flags
      HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;

      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false );

      // Set credentials for server.
      WinHttpReq.SetCredentials( "User Name", 
                                 "Password",
                                 HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

      // It might also be necessary to supply credentials 
      // to the proxy if you connect to the Internet 
      // through a proxy that requires authentication.

      // Send a request to the server and wait for 
      // a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
      WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
      WScript.Echo( );
    };

    getText1( );
    getText2( );
    ```

    

3.  Enregistrez le fichier en tant que « Auth.js ».
4.  À partir d’une invite de commandes, tapez « cscript Auth.js » et appuyez sur entrée.

Vous disposez maintenant d’un programme qui demande une ressource de deux manières différentes. La première méthode demande la ressource sans fournir d’informations d’identification. Un code d’état 401 est retourné pour indiquer que le serveur requiert une authentification. Les en-têtes de réponse sont également affichés et doivent ressembler à ce qui suit :

``` syntax
Connection: Keep-Alive
Content-Length: 0
Date: Fri, 27 Apr 2001 01:47:18 GMT
Content-Type: text/html
Server: Microsoft-IIS/5.0
WWW-Authenticate: NTLM
WWW-Authenticate: Negotiate
Cache-control: private
```

Bien que la réponse indique que l’accès à la ressource a été refusé, elle retourne toujours plusieurs en-têtes qui fournissent des informations sur la ressource. L’en-tête nommé « WWW-Authenticate » indique que le serveur requiert une authentification pour cette ressource. S’il existait un en-tête nommé « Proxy-Authenticate », cela signifie que le serveur proxy requiert une authentification. Chaque en-tête Authenticate contient un schéma d’authentification disponible et parfois un domaine. La valeur de domaine est sensible à la casse et définit un ensemble de serveurs ou de proxys pour lesquels les mêmes informations d’identification doivent être acceptées.

Deux en-têtes sont nommés « WWW-Authenticate », ce qui signifie que plusieurs schémas d’authentification sont pris en charge. Si vous appelez la méthode [**getResponseHeader**](iwinhttprequest-getresponseheader.md) pour rechercher des en-têtes « www-Authenticate », la méthode retourne uniquement le contenu du premier en-tête de ce nom. Dans ce cas, elle retourne la valeur « NTLM ». Pour vous assurer que toutes les occurrences d’un en-tête sont traitées, utilisez la méthode [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) à la place.

Le deuxième appel de méthode demande la même ressource, mais fournit d’abord les informations d’identification d’authentification en appelant la méthode [**SetCredentials**](iwinhttprequest-setcredentials.md) . La section de code suivante montre comment cette méthode est utilisée.


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



Cette méthode définit le nom d’utilisateur sur « UserName », le mot de passe « Password » et indique que les informations d’identification d’autorisation s’appliquent au serveur de ressources. Les informations d’identification d’authentification peuvent également être envoyées à un proxy.

Lorsque les informations d’identification sont fournies, le serveur renvoie un code d’état 200 qui indique que le document peut être récupéré.

## <a name="checking-the-status-codes"></a>Vérification des codes d’État

L’exemple précédent est une instruction, mais elle nécessite que l’utilisateur fournisse explicitement des informations d’identification. Une application qui fournit des informations d’identification lorsque cela est nécessaire et qui ne fournit pas d’informations d’identification lorsqu’elle n’est pas nécessaire est plus utile. Pour implémenter une fonctionnalité qui effectue cette action, vous devez modifier votre exemple pour examiner le code d’état retourné avec la réponse.

Pour obtenir la liste complète des codes d’État possibles, ainsi que des descriptions, consultez [**codes d’État http**](http-status-codes.md). Toutefois, pour cet exemple, vous ne devriez rencontrer qu’un seul des trois codes. Le code d’état 200 indique qu’une ressource est disponible et qu’elle est envoyée avec la réponse. Le code d’état 401 indique que le serveur requiert une authentification. Le code d’État 407 indique que le proxy requiert une authentification.

Modifiez l’exemple que vous avez créé dans la dernière section en remplaçant la fonction « getText2 » par le code suivant (remplacez « \[ authenticationSite \] » par votre propre texte pour spécifier l’URL d’un site qui requiert l’authentification http) :


```VB
function getText2() {
  WScript.Echo( "Credentials: " );

  // HttpRequest SetCredentials flags.
  HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
  HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

  // Specify the target resource.
  var targURL = "https://[authenticationSite]";
  WinHttpReq.open( "GET", targURL, false );

  var Done = false;
  var Attempts = 0;
  do
  {
    // Keep track of the number of request attempts.
    Attempts++;

    // Send a request to the server and wait for a response.
    WinHttpReq.send( );

    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status)
    {
      // A 200 status indicates that the resource was retrieved.
      case 200:
        Done = true;
        break;

      // A 401 status indicates that the server 
      // requires authentication.
      case 401:
        WScript.Echo( "Requires Server UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the server.
        WinHttpReq.SetCredentials( "User Name", 
                             "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        break;

      // A 407 status indicates that the proxy 
      // requires authentication.
      case 407:
        WScript.Echo( "Requires Proxy UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the proxy.
        WinHttpReq.SetCredentials( "User Name", 
                              "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_PROXY );
        break;
    }
  } while( ( !Done ) && ( Attempts < 3 ) );

  // Display the results of the request.
  WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
  WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
  WScript.Echo( );
};
```



Une fois encore, enregistrez et exécutez le fichier. La deuxième méthode récupère toujours le document, mais fournit uniquement des informations d’identification si nécessaire. La fonction « getText2 » exécute les méthodes [**Open**](iwinhttprequest-open.md) et [**Send**](iwinhttprequest-send.md) comme si l’authentification n’était pas requise. L’État est récupéré avec la propriété [**Status**](iwinhttprequest-status.md) et une instruction switch répond au code d’État qui en résulte. Si l’État est 401 (le serveur nécessite une authentification) ou 407 (le proxy requiert une authentification), la méthode [**Open**](iwinhttprequest-open.md) est exécutée à nouveau. Elle est suivie par la méthode [**SetCredentials**](iwinhttprequest-setcredentials.md) , qui définit le nom d’utilisateur et le mot de passe. Le code repasse ensuite à la méthode [**Send**](iwinhttprequest-send.md) . Si, après trois tentatives, la ressource ne peut pas être récupérée avec succès, la fonction arrête l’exécution.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification dans WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[WinHttpRequest](winhttprequest.md)
</dt> <dt>

[**SetCredentials**](iwinhttprequest-setcredentials.md)
</dt> <dt>

[Demande de commentaires HTTP/1.1 (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



