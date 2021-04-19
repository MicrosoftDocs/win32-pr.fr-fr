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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529856"
---
# <a name="authentication-using-script"></a><span data-ttu-id="9ccf8-103">Authentification à l’aide d’un script</span><span class="sxs-lookup"><span data-stu-id="9ccf8-103">Authentication Using Script</span></span>

<span data-ttu-id="9ccf8-104">Cette section montre comment écrire un script qui utilise l’objet [**WinHttpRequest**](winhttprequest.md) pour accéder aux données à partir d’un serveur qui requiert l’authentification http.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-104">This section demonstrates how to write script that uses the [**WinHttpRequest**](winhttprequest.md) object to access data from a server that requires HTTP authentication.</span></span>

-   [<span data-ttu-id="9ccf8-105">Conditions préalables et configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ccf8-105">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="9ccf8-106">Accès à un site Web avec l’authentification</span><span class="sxs-lookup"><span data-stu-id="9ccf8-106">Accessing a Web Site With Authentication</span></span>](#accessing-a-web-site-with-authentication)
-   [<span data-ttu-id="9ccf8-107">Vérification des codes d’État</span><span class="sxs-lookup"><span data-stu-id="9ccf8-107">Checking the Status Codes</span></span>](#checking-the-status-codes)
-   [<span data-ttu-id="9ccf8-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ccf8-108">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="9ccf8-109">Conditions préalables et configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ccf8-109">Prerequisites and Requirements</span></span>

<span data-ttu-id="9ccf8-110">Outre les connaissances pratiques de Microsoft JScript, cet exemple nécessite les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9ccf8-110">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="9ccf8-111">Version actuelle du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-111">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="9ccf8-112">L’outil de configuration de proxy pour établir les paramètres de proxy pour les services HTTP Microsoft Windows (WinHTTP), si votre connexion à Internet s’effectue via un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-112">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="9ccf8-113">Pour plus d’informations [ , consultezProxycfg.exe, un outil de configuration de proxy](proxycfg-exe--a-proxy-configuration-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="9ccf8-113">See [Proxycfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md) for more information.</span></span>
-   <span data-ttu-id="9ccf8-114">Une bonne connaissance de la terminologie et des concepts relatifs au [réseau](network-terminology.md) .</span><span class="sxs-lookup"><span data-stu-id="9ccf8-114">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="accessing-a-web-site-with-authentication"></a><span data-ttu-id="9ccf8-115">Accès à un site Web avec l’authentification</span><span class="sxs-lookup"><span data-stu-id="9ccf8-115">Accessing a Web Site With Authentication</span></span>

<span data-ttu-id="9ccf8-116">**Pour créer un script illustrant l’authentification, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="9ccf8-116">**To create a script that demonstrates authentication, do the following:**</span></span>

1.  <span data-ttu-id="9ccf8-117">Ouvrez un éditeur de texte tel que le bloc-notes Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-117">Open a text editor such as Microsoft Notepad.</span></span>
2.  <span data-ttu-id="9ccf8-118">Copiez le code suivant dans l’éditeur de texte après avoir remplacé « \[ authenticationSite \] » par le texte approprié pour spécifier l’URL d’un site qui requiert l’authentification http.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-118">Copy the following code into the text editor after replacing "\[authenticationSite\]" with the appropriate text to specify the URL of a site that requires HTTP authentication.</span></span>

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

    

3.  <span data-ttu-id="9ccf8-119">Enregistrez le fichier en tant que « Auth.js ».</span><span class="sxs-lookup"><span data-stu-id="9ccf8-119">Save the file as "Auth.js".</span></span>
4.  <span data-ttu-id="9ccf8-120">À partir d’une invite de commandes, tapez « cscript Auth.js » et appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-120">From a command prompt, type "cscript Auth.js" and press ENTER.</span></span>

<span data-ttu-id="9ccf8-121">Vous disposez maintenant d’un programme qui demande une ressource de deux manières différentes.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-121">You now have a program that requests a resource two different ways.</span></span> <span data-ttu-id="9ccf8-122">La première méthode demande la ressource sans fournir d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-122">The first method requests the resource without supplying credentials.</span></span> <span data-ttu-id="9ccf8-123">Un code d’état 401 est retourné pour indiquer que le serveur requiert une authentification.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-123">A 401 status code is returned to indicate that the server requires authentication.</span></span> <span data-ttu-id="9ccf8-124">Les en-têtes de réponse sont également affichés et doivent ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="9ccf8-124">The response headers are also displayed and should look similar to the following:</span></span>

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

<span data-ttu-id="9ccf8-125">Bien que la réponse indique que l’accès à la ressource a été refusé, elle retourne toujours plusieurs en-têtes qui fournissent des informations sur la ressource.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-125">Although the response indicates that access to the resource was denied, it still returns several headers that provide some information about the resource.</span></span> <span data-ttu-id="9ccf8-126">L’en-tête nommé « WWW-Authenticate » indique que le serveur requiert une authentification pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-126">The header named "WWW-Authenticate" indicates that the server requires authentication for this resource.</span></span> <span data-ttu-id="9ccf8-127">S’il existait un en-tête nommé « Proxy-Authenticate », cela signifie que le serveur proxy requiert une authentification.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-127">If there was a header named "Proxy-Authenticate", it would indicate that the proxy server requires authentication.</span></span> <span data-ttu-id="9ccf8-128">Chaque en-tête Authenticate contient un schéma d’authentification disponible et parfois un domaine.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-128">Each authenticate header contains an available authentication scheme and sometimes a realm.</span></span> <span data-ttu-id="9ccf8-129">La valeur de domaine est sensible à la casse et définit un ensemble de serveurs ou de proxys pour lesquels les mêmes informations d’identification doivent être acceptées.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-129">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials should be accepted.</span></span>

<span data-ttu-id="9ccf8-130">Deux en-têtes sont nommés « WWW-Authenticate », ce qui signifie que plusieurs schémas d’authentification sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-130">There are two headers named "WWW-Authenticate", which indicate that multiple authentication schemes are supported.</span></span> <span data-ttu-id="9ccf8-131">Si vous appelez la méthode [**getResponseHeader**](iwinhttprequest-getresponseheader.md) pour rechercher des en-têtes « www-Authenticate », la méthode retourne uniquement le contenu du premier en-tête de ce nom.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-131">If you call the [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) method to find "WWW-Authenticate" headers, the method only returns the contents of the first header of that name.</span></span> <span data-ttu-id="9ccf8-132">Dans ce cas, elle retourne la valeur « NTLM ».</span><span class="sxs-lookup"><span data-stu-id="9ccf8-132">In this case, it returns a value of "NTLM".</span></span> <span data-ttu-id="9ccf8-133">Pour vous assurer que toutes les occurrences d’un en-tête sont traitées, utilisez la méthode [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-133">To ensure that all occurrences of a header are processed, use the [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) method instead.</span></span>

<span data-ttu-id="9ccf8-134">Le deuxième appel de méthode demande la même ressource, mais fournit d’abord les informations d’identification d’authentification en appelant la méthode [**SetCredentials**](iwinhttprequest-setcredentials.md) .</span><span class="sxs-lookup"><span data-stu-id="9ccf8-134">The second method call requests the same resource, but first supplies authentication credentials by calling the [**SetCredentials**](iwinhttprequest-setcredentials.md) method.</span></span> <span data-ttu-id="9ccf8-135">La section de code suivante montre comment cette méthode est utilisée.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-135">The following section of code shows how this method is used.</span></span>


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



<span data-ttu-id="9ccf8-136">Cette méthode définit le nom d’utilisateur sur « UserName », le mot de passe « Password » et indique que les informations d’identification d’autorisation s’appliquent au serveur de ressources.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-136">This method sets the user name to "UserName", the password to "Password", and indicates that the authorization credentials apply to the resource server.</span></span> <span data-ttu-id="9ccf8-137">Les informations d’identification d’authentification peuvent également être envoyées à un proxy.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-137">Authentication credentials can also be sent to a proxy.</span></span>

<span data-ttu-id="9ccf8-138">Lorsque les informations d’identification sont fournies, le serveur renvoie un code d’état 200 qui indique que le document peut être récupéré.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-138">When credentials are supplied, the server returns a 200 status code that indicates that the document can be retrieved.</span></span>

## <a name="checking-the-status-codes"></a><span data-ttu-id="9ccf8-139">Vérification des codes d’État</span><span class="sxs-lookup"><span data-stu-id="9ccf8-139">Checking the Status Codes</span></span>

<span data-ttu-id="9ccf8-140">L’exemple précédent est une instruction, mais elle nécessite que l’utilisateur fournisse explicitement des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-140">The previous example is instructional, but it requires that the user explicitly supply credentials.</span></span> <span data-ttu-id="9ccf8-141">Une application qui fournit des informations d’identification lorsque cela est nécessaire et qui ne fournit pas d’informations d’identification lorsqu’elle n’est pas nécessaire est plus utile.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-141">An application that supplies credentials when it is necessary and does not supply credentials when it is not necessary is more useful.</span></span> <span data-ttu-id="9ccf8-142">Pour implémenter une fonctionnalité qui effectue cette action, vous devez modifier votre exemple pour examiner le code d’état retourné avec la réponse.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-142">To implement a feature that does this, you must modify your example to examine the status code returned with the response.</span></span>

<span data-ttu-id="9ccf8-143">Pour obtenir la liste complète des codes d’État possibles, ainsi que des descriptions, consultez [**codes d’État http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9ccf8-143">For a complete list of possible status codes, along with descriptions, see [**HTTP Status Codes**](http-status-codes.md).</span></span> <span data-ttu-id="9ccf8-144">Toutefois, pour cet exemple, vous ne devriez rencontrer qu’un seul des trois codes.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-144">For this example, however, you should encounter only one of three codes.</span></span> <span data-ttu-id="9ccf8-145">Le code d’état 200 indique qu’une ressource est disponible et qu’elle est envoyée avec la réponse.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-145">A status code of 200 indicates that a resource is available and is being sent with the response.</span></span> <span data-ttu-id="9ccf8-146">Le code d’état 401 indique que le serveur requiert une authentification.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-146">A status code of 401 indicates that the server requires authentication.</span></span> <span data-ttu-id="9ccf8-147">Le code d’État 407 indique que le proxy requiert une authentification.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-147">A status code of 407 indicates that the proxy requires authentication.</span></span>

<span data-ttu-id="9ccf8-148">Modifiez l’exemple que vous avez créé dans la dernière section en remplaçant la fonction « getText2 » par le code suivant (remplacez « \[ authenticationSite \] » par votre propre texte pour spécifier l’URL d’un site qui requiert l’authentification http) :</span><span class="sxs-lookup"><span data-stu-id="9ccf8-148">Modify the example you created in the last section by replacing the "getText2" function with the following code (replace "\[authenticationSite\]" with your own text to specifies the URL of a site that requires HTTP authentication):</span></span>


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



<span data-ttu-id="9ccf8-149">Une fois encore, enregistrez et exécutez le fichier.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-149">Again, save and run the file.</span></span> <span data-ttu-id="9ccf8-150">La deuxième méthode récupère toujours le document, mais fournit uniquement des informations d’identification si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-150">The second method still retrieves the document, but it only provides credentials when required.</span></span> <span data-ttu-id="9ccf8-151">La fonction « getText2 » exécute les méthodes [**Open**](iwinhttprequest-open.md) et [**Send**](iwinhttprequest-send.md) comme si l’authentification n’était pas requise.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-151">The "getText2" function executes the [**Open**](iwinhttprequest-open.md) and [**Send**](iwinhttprequest-send.md) methods as if authentication was not required.</span></span> <span data-ttu-id="9ccf8-152">L’État est récupéré avec la propriété [**Status**](iwinhttprequest-status.md) et une instruction switch répond au code d’État qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-152">The status is retrieved with the [**Status**](iwinhttprequest-status.md) property and a switch statement responds to the resulting status code.</span></span> <span data-ttu-id="9ccf8-153">Si l’État est 401 (le serveur nécessite une authentification) ou 407 (le proxy requiert une authentification), la méthode [**Open**](iwinhttprequest-open.md) est exécutée à nouveau.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-153">If the status is 401 (server requires authentication) or 407 (proxy requires authentication), the [**Open**](iwinhttprequest-open.md) method is executed again.</span></span> <span data-ttu-id="9ccf8-154">Elle est suivie par la méthode [**SetCredentials**](iwinhttprequest-setcredentials.md) , qui définit le nom d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-154">This is followed by the [**SetCredentials**](iwinhttprequest-setcredentials.md) method, which sets the user name and password.</span></span> <span data-ttu-id="9ccf8-155">Le code repasse ensuite à la méthode [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="9ccf8-155">The code then loops back to the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="9ccf8-156">Si, après trois tentatives, la ressource ne peut pas être récupérée avec succès, la fonction arrête l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9ccf8-156">If, after three attempts, the resource cannot be successfully retrieved, then the function stops execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ccf8-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ccf8-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ccf8-158">Authentification dans WinHTTP</span><span class="sxs-lookup"><span data-stu-id="9ccf8-158">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="9ccf8-159">WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="9ccf8-159">WinHttpRequest</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="9ccf8-160">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="9ccf8-160">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)
</dt> <dt>

[<span data-ttu-id="9ccf8-161">Demande de commentaires HTTP/1.1 (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="9ccf8-161">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



