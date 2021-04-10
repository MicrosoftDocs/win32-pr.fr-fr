---
description: Cette rubrique fournit un exemple d’écriture d’un script qui obtient des données via les services HTTP Microsoft Windows (WinHTTP) de façon synchrone ou asynchrone.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Récupération de données à l’aide d’un script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734516cf75f92cc43ab4cb15f22bd97aa803ec33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950917"
---
# <a name="retrieving-data-using-script"></a><span data-ttu-id="d14d3-103">Récupération de données à l’aide d’un script</span><span class="sxs-lookup"><span data-stu-id="d14d3-103">Retrieving Data Using Script</span></span>

<span data-ttu-id="d14d3-104">Cette rubrique fournit un exemple d’écriture d’un script qui obtient des données via les services HTTP Microsoft Windows (WinHTTP) de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d14d3-104">This topic includes an example of how to write a script that obtains data through Microsoft Windows HTTP Services (WinHTTP) either synchronously or asynchronously.</span></span> <span data-ttu-id="d14d3-105">Les concepts présentés dans cet exemple fournissent la base de l’écriture d’applications clientes ou de serveur de couche intermédiaire qui requièrent l’accès aux données à l’aide du protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="d14d3-105">The concepts demonstrated in this example provide the basis for writing client or middle-tier server applications that require access to data using the HTTP protocol.</span></span>

-   [<span data-ttu-id="d14d3-106">Conditions préalables et configuration requise</span><span class="sxs-lookup"><span data-stu-id="d14d3-106">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="d14d3-107">Récupération de données de façon synchrone</span><span class="sxs-lookup"><span data-stu-id="d14d3-107">Retrieving Data Synchronously</span></span>](#retrieving-data-synchronously)
-   [<span data-ttu-id="d14d3-108">Récupération de données de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="d14d3-108">Retrieving Data Asynchronously</span></span>](#retrieving-data-asynchronously)
-   [<span data-ttu-id="d14d3-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d14d3-109">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="d14d3-110">Conditions préalables et configuration requise</span><span class="sxs-lookup"><span data-stu-id="d14d3-110">Prerequisites and Requirements</span></span>

<span data-ttu-id="d14d3-111">Outre les connaissances pratiques de Microsoft JScript, cet exemple nécessite les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d14d3-111">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="d14d3-112">Version actuelle du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d14d3-112">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="d14d3-113">L’outil de configuration de proxy pour établir les paramètres de proxy pour les services HTTP Microsoft Windows (WinHTTP), si votre connexion à Internet s’effectue via un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="d14d3-113">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="d14d3-114">Pour plus d’informations, consultez [ProxyCfg.exe, un outil de configuration de proxy](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="d14d3-114">For more information, see [ProxyCfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md).</span></span>
-   <span data-ttu-id="d14d3-115">Une bonne connaissance de la terminologie et des concepts relatifs au [réseau](network-terminology.md) .</span><span class="sxs-lookup"><span data-stu-id="d14d3-115">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="d14d3-116">Récupération de données de façon synchrone</span><span class="sxs-lookup"><span data-stu-id="d14d3-116">Retrieving Data Synchronously</span></span>

<span data-ttu-id="d14d3-117">**Pour créer un script qui obtient le texte d’une page Web de façon synchrone, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="d14d3-117">**To create a script that obtains the text from a Web page synchronously, do the following:**</span></span>

1.  <span data-ttu-id="d14d3-118">Ouvrez un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="d14d3-118">Open a text editor.</span></span>
2.  <span data-ttu-id="d14d3-119">Copiez le code suivant dans l’éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="d14d3-119">Copy the following code into the text editor.</span></span>

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  <span data-ttu-id="d14d3-120">Enregistrez le fichier en tant que « Retrieve.js ».</span><span class="sxs-lookup"><span data-stu-id="d14d3-120">Save the file as "Retrieve.js".</span></span>
4.  <span data-ttu-id="d14d3-121">À partir d’une invite de commandes, tapez « cscript Retrieve.js » et appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="d14d3-121">From a command prompt, type "cscript Retrieve.js" and press ENTER.</span></span>

<span data-ttu-id="d14d3-122">Vous avez maintenant un script qui utilise un objet [**WinHttpRequest**](winhttprequest.md) pour obtenir le code source HTML de la page Web à l’adresse https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="d14d3-122">You now have a script that uses a [**WinHttpRequest**](winhttprequest.md) object to obtain the HTML source code for the Web page at https://www.microsoft.com.</span></span> <span data-ttu-id="d14d3-123">Vous devrez peut-être attendre quelques secondes avant que le code n’apparaisse.</span><span class="sxs-lookup"><span data-stu-id="d14d3-123">You might have to wait several seconds for the code to appear.</span></span>

<span data-ttu-id="d14d3-124">L’application contient une seule fonction, « getText ».</span><span class="sxs-lookup"><span data-stu-id="d14d3-124">The application contains only one function, "getText".</span></span> <span data-ttu-id="d14d3-125">La première ligne du script crée l’objet [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="d14d3-125">The first line of the script creates the [**WinHttpRequest**](winhttprequest.md) object.</span></span>


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



<span data-ttu-id="d14d3-126">Lorsque le moteur JScript rencontre cette ligne, il crée une instance de cet objet.</span><span class="sxs-lookup"><span data-stu-id="d14d3-126">When the JScript engine encounters this line, it creates an instance of this object.</span></span> <span data-ttu-id="d14d3-127">Si vous recevez le message d’erreur « le composant ActiveX ne peut pas créer d’objet », sur cette ligne, il est probable que le WinHttp.dll n’a pas été correctement inscrit ou qu’il n’est pas présent sur le système.</span><span class="sxs-lookup"><span data-stu-id="d14d3-127">If you get the error message, "ActiveX component can't create object", on this line, most likely the WinHttp.dll was not properly registered or is not present on the system.</span></span>

<span data-ttu-id="d14d3-128">La ligne suivante du script appelle la méthode [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="d14d3-128">The next line of the script calls the [**Open**](iwinhttprequest-open.md) method.</span></span>


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



<span data-ttu-id="d14d3-129">Trois paramètres spécifient le [*verbe http*](glossary.md) à utiliser, le nom de la ressource et s’il faut utiliser WinHTTP de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d14d3-129">Three parameters specify which [*HTTP verb*](glossary.md) to use, the name of the resource, and whether to use WinHTTP synchronously or asynchronously.</span></span> <span data-ttu-id="d14d3-130">Dans cet exemple, la méthode utilise le *verbe http*« obtenir » pour obtenir des données à partir de https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="d14d3-130">In this example, the method is using the *HTTP verb*"GET" to obtain data from https://www.microsoft.com.</span></span> <span data-ttu-id="d14d3-131">La spécification de la **valeur false** pour le dernier paramètre détermine que la transaction se produit de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="d14d3-131">Specifying **FALSE** for the last parameter determines that the transaction occurs synchronously.</span></span> <span data-ttu-id="d14d3-132">La méthode [**Open**](iwinhttprequest-open.md) n’établit pas de connexion à la ressource, car le nom peut le supposer.</span><span class="sxs-lookup"><span data-stu-id="d14d3-132">The [**Open**](iwinhttprequest-open.md) method does not establish a connection to the resource as the name might imply.</span></span> <span data-ttu-id="d14d3-133">Au lieu de cela, il initialise les structures de données internes qui maintiennent les informations sur la session, la connexion et la demande.</span><span class="sxs-lookup"><span data-stu-id="d14d3-133">Rather, it initializes the internal data structures that maintain information about the session, connection, and request.</span></span>

<span data-ttu-id="d14d3-134">La méthode [**Send**](iwinhttprequest-send.md) assemble les en-têtes de requête et envoie la demande.</span><span class="sxs-lookup"><span data-stu-id="d14d3-134">The [**Send**](iwinhttprequest-send.md) method assembles the request headers and sends the request.</span></span> <span data-ttu-id="d14d3-135">En cas d’appel en mode synchrone, la méthode [**Send**](iwinhttprequest-send.md) attend également une réponse avant d’autoriser l’application à continuer.</span><span class="sxs-lookup"><span data-stu-id="d14d3-135">When called in synchronous mode, the [**Send**](iwinhttprequest-send.md) method also waits for a response before allowing the application to continue.</span></span>


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



<span data-ttu-id="d14d3-136">Après l’envoi de la demande, le script retourne la valeur de la propriété [**responseText**](iwinhttprequest-responsetext.md) de l’objet [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="d14d3-136">After sending the request, the script returns the value of the [**ResponseText**](iwinhttprequest-responsetext.md) property of the [**WinHttpRequest**](winhttprequest.md) object.</span></span> <span data-ttu-id="d14d3-137">Cette propriété contient le corps d’entité de la réponse, dans ce cas, la source d’un document.</span><span class="sxs-lookup"><span data-stu-id="d14d3-137">This property contains the entity body of the response, in this case, the source of a document.</span></span>


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



<span data-ttu-id="d14d3-138">L’exécution du script s’interrompt pendant que l’intégralité du texte de la ressource est récupérée.</span><span class="sxs-lookup"><span data-stu-id="d14d3-138">Execution of the script pauses while the entire text of the resource is retrieved.</span></span> <span data-ttu-id="d14d3-139">Le texte de la ressource est retourné à partir de la fonction et affiché.</span><span class="sxs-lookup"><span data-stu-id="d14d3-139">The resource text is returned from the function and displayed.</span></span>

<span data-ttu-id="d14d3-140">L’objet [**WinHttpRequest**](winhttprequest.md) garantit que toutes les ressources internes qui sont allouées pour la transaction http sont libérées.</span><span class="sxs-lookup"><span data-stu-id="d14d3-140">The [**WinHttpRequest**](winhttprequest.md) object ensures that any internal resources that are allocated for the HTTP transaction are released.</span></span>

## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="d14d3-141">Récupération de données de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="d14d3-141">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="d14d3-142">La récupération de données de façon asynchrone à l’aide de WinHTTP est très similaire à la récupération de données de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="d14d3-142">Retrieving data asynchronously using WinHTTP is very similar to retrieving data synchronously.</span></span> <span data-ttu-id="d14d3-143">Modifiez le script de la section précédente en effectuant deux petites modifications.</span><span class="sxs-lookup"><span data-stu-id="d14d3-143">Modify the script from the previous section by making two small changes.</span></span>

1.  <span data-ttu-id="d14d3-144">Définissez le troisième paramètre de la méthode [**Open**](iwinhttprequest-open.md) sur « true » au lieu de « false » pour spécifier que les méthodes WinHTTP doivent être exécutées de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d14d3-144">Set the third parameter of the [**Open**](iwinhttprequest-open.md) method to "true" instead of "false" to specify that WinHTTP methods should be performed asynchronously.</span></span>
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  <span data-ttu-id="d14d3-145">Appelez la méthode [**WaitForResponse**](iwinhttprequest-waitforresponse.md) avant d’accéder à la propriété [**responseText**](iwinhttprequest-responsetext.md) pour vous assurer que l’intégralité de la réponse a été reçue.</span><span class="sxs-lookup"><span data-stu-id="d14d3-145">Invoke the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method before accessing the [**ResponseText**](iwinhttprequest-responsetext.md) property to ensure that the entire response has been received.</span></span>
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

<span data-ttu-id="d14d3-146">Le principal avantage de l’utilisation de WinHTTP de manière asynchrone dans le script est que la méthode [**Send**](iwinhttprequest-send.md) est retournée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d14d3-146">The main advantage to using WinHTTP asynchronously in script is that the [**Send**](iwinhttprequest-send.md) method returns immediately.</span></span> <span data-ttu-id="d14d3-147">La requête est préparée et envoyée par un thread de travail.</span><span class="sxs-lookup"><span data-stu-id="d14d3-147">The request is prepared and sent by a worker thread.</span></span> <span data-ttu-id="d14d3-148">Cela permet à votre application d’effectuer d’autres tâches pendant qu’elle attend la réponse.</span><span class="sxs-lookup"><span data-stu-id="d14d3-148">This enables your application to do other things while it is waiting for the response.</span></span> <span data-ttu-id="d14d3-149">Avant de tenter d’accéder à la réponse, assurez-vous que l’intégralité de la réponse a été reçue en appelant la méthode [**WaitForResponse**](iwinhttprequest-waitforresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="d14d3-149">Before attempting to access the response, ensure that the entire response has been received by calling the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method.</span></span> <span data-ttu-id="d14d3-150">Sinon, une erreur peut se produire.</span><span class="sxs-lookup"><span data-stu-id="d14d3-150">Otherwise an error can occur.</span></span>

<span data-ttu-id="d14d3-151">La méthode [**WaitForResponse**](iwinhttprequest-waitforresponse.md) peut également être utilisée pour spécifier une valeur de délai d’attente pour la transaction.</span><span class="sxs-lookup"><span data-stu-id="d14d3-151">The [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method can also be used to specify a time-out value for the transaction.</span></span> <span data-ttu-id="d14d3-152">Un paramètre facultatif vous permet de spécifier la valeur du délai d’attente en secondes.</span><span class="sxs-lookup"><span data-stu-id="d14d3-152">An optional parameter enables you to specify the time-out value in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d14d3-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d14d3-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d14d3-154">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="d14d3-154">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="d14d3-155">Demande de commentaires HTTP/1.1 (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="d14d3-155">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



