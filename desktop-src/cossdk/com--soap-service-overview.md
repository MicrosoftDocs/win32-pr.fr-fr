---
description: Utilisation d’un ordinateur par révolution HTTP en permettant aux utilisateurs d’utiliser un navigateur Web pour accéder facilement aux informations sur un serveur distant sur un réseau.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Vue d’ensemble du service SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93ce7d80753f306777d3ac0b77dc46dc4e08d22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514932"
---
# <a name="com-soap-service-overview"></a><span data-ttu-id="a20c6-103">Vue d’ensemble du service SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="a20c6-103">COM+ SOAP Service Overview</span></span>

<span data-ttu-id="a20c6-104">Utilisation d’un ordinateur par révolution HTTP en permettant aux utilisateurs d’utiliser un navigateur Web pour accéder facilement aux informations sur un serveur distant sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="a20c6-104">HTTP revolutionized computer use by allowing people to use a Web browser for easy access to information on a remote server over a network.</span></span> <span data-ttu-id="a20c6-105">Les services Web XML ont à présent révolutionné le développement d’applications en permettant aux applications clientes d’appeler facilement des méthodes à distance sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="a20c6-105">XML web services have now revolutionized application development by allowing client applications to easily call remote methods over a network.</span></span>

<span data-ttu-id="a20c6-106">Il est souvent utile pour une application cliente de pouvoir appeler une méthode implémentée sur un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="a20c6-106">It is often useful for a client application to be able to call a method implemented on a remote server.</span></span> <span data-ttu-id="a20c6-107">Parfois, la méthode utilise des informations volatiles stockées sur le serveur distant (par exemple, une méthode qui retourne le prix actuel du stock correspondant à un symbole de titre donné).</span><span class="sxs-lookup"><span data-stu-id="a20c6-107">Sometimes the method makes use of volatile information stored on the remote server (for example, a method that returns the current price of the stock corresponding to a given ticker symbol).</span></span> <span data-ttu-id="a20c6-108">À d’autres moments, le développeur souhaite pouvoir mettre à niveau l’implémentation des méthodes sans avoir à redéployer toutes les applications qui l’utilisent.</span><span class="sxs-lookup"><span data-stu-id="a20c6-108">At other times, the developer wants the ability to upgrade the methods implementation without having to redeploy all the applications that use it.</span></span>

<span data-ttu-id="a20c6-109">Comme les pages Web, les services Web XML sont accessibles via un serveur Web, par exemple IIS, à l’aide de HTTP.</span><span class="sxs-lookup"><span data-stu-id="a20c6-109">Like webpages, XML web services are accessed via a web server, such as IIS, using HTTP.</span></span> <span data-ttu-id="a20c6-110">Toutefois, au lieu des pages Web encodées en HTML, ces paquets HTTP contiennent les paramètres d’entrée et de sortie des appels à une méthode implémentée sur le serveur, encodé dans SOAP.</span><span class="sxs-lookup"><span data-stu-id="a20c6-110">However, instead of webpages encoded in HTML, these HTTP packets contain the input and output parameters of calls to a method implemented on the server, encoded in SOAP.</span></span>

<span data-ttu-id="a20c6-111">Pour utiliser un service Web XML, vous devez connaître l’URL où le service est exposé et le nom de la méthode que vous souhaitez appeler, et vous devez fournir les paramètres d’entrée à la méthode.</span><span class="sxs-lookup"><span data-stu-id="a20c6-111">To use an XML web service, you need to know the URL where the service is exposed and the name of the method you want to call, and you must provide the input parameters to the method.</span></span> <span data-ttu-id="a20c6-112">[La norme SOAP 1,1](https://www.w3.org/TR/SOAP/) fournit l’exemple suivant d’un paquet http contenant un appel distant à un service Web XML à https://www.stockquoteserver.com/StockQuote , qui retourne le prix actuel du stock correspondant à un symbole de titre donné.</span><span class="sxs-lookup"><span data-stu-id="a20c6-112">[The SOAP 1.1 standard](https://www.w3.org/TR/SOAP/) provides the following example of an HTTP packet containing a remote call to an XML web service at https://www.stockquoteserver.com/StockQuote, which returns the current price of the stock corresponding to a given ticker symbol.</span></span>

``` syntax
POST /StockQuote HTTP/1.1
Host: www.stockquoteserver.com
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn
SOAPAction: "Some-URI"

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<m:GetLastTradePrice xmlns:m="Some-URI">
<symbol>DIS</symbol>
</m:GetLastTradePrice>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="a20c6-113">Comme l’illustre l’exemple précédent, SOAP est une instance XML qui peut être incorporée dans une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="a20c6-113">As the preceding example illustrates, SOAP is an XML instance that can be embedded in an HTTP request.</span></span> <span data-ttu-id="a20c6-114">De même, le résultat est retourné sous la forme d’un paquet HTTP avec une charge utile SOAP, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="a20c6-114">Similarly, the result is returned as an HTTP packet with a SOAP payload, as shown in the following example.</span></span>

``` syntax
HTTP/1.1 200 OK
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding//">
<SOAP-ENV:Body>
<m:GetLastTradePriceResponse xmlns:m="Some-URI">
<Price>34.5</Price>
</m:GetLastTradePriceResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="a20c6-115">Bien qu’il soit utile d’avoir une compréhension de l’infrastructure sous-jacente aux services Web XML, COM+ facilite la création et l’utilisation de services Web XML que vous n’aurez pas souvent à plonger à ce niveau.</span><span class="sxs-lookup"><span data-stu-id="a20c6-115">While it is helpful to have some understanding of the infrastructure that underlies XML web services, COM+ makes it so easy to create and use XML web services that you won't often have to delve to this level.</span></span>

<span data-ttu-id="a20c6-116">Vous pouvez exposer les méthodes dans les interfaces par défaut des composants COM configurés dans n’importe quelle application COM+ en tant que service Web XML.</span><span class="sxs-lookup"><span data-stu-id="a20c6-116">You can expose the methods in the default interfaces of the configured COM components in any COM+ application as an XML web service.</span></span> <span data-ttu-id="a20c6-117">Aucune considération particulière de programmation n’est nécessaire lors de l’écriture des composants, sauf que les méthodes que vous souhaitez exposer doivent se trouver dans l’interface par défaut et que le composant doit être configuré (dans le catalogue COM+ de votre serveur).</span><span class="sxs-lookup"><span data-stu-id="a20c6-117">No special programming considerations are necessary when writing the components, except that the methods you want to expose must be in the default interface and the component must be configured (in your server's COM+ catalog).</span></span> <span data-ttu-id="a20c6-118">Vous n’avez pas besoin d’écrire du code pour communiquer via une interface réseau ou pour analyser le protocole SOAP.</span><span class="sxs-lookup"><span data-stu-id="a20c6-118">You need not write code to communicate via a network interface or to parse SOAP.</span></span> <span data-ttu-id="a20c6-119">Pour obtenir des instructions détaillées sur l’utilisation du service SOAP COM+ pour créer un service Web XML, consultez [création de services Web XML](creating-xml-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="a20c6-119">For detailed instructions about using the COM+ SOAP service to create an XML web service, see [Creating XML Web Services](creating-xml-web-services.md).</span></span>

<span data-ttu-id="a20c6-120">Lorsque vous exposez une application COM+ en tant que service Web XML, des informations détaillées sur la syntaxe de toutes les méthodes disponibles à partir d’un service Web XML sont publiées automatiquement, à l’aide de l’Web Services Description Language (WSDL).</span><span class="sxs-lookup"><span data-stu-id="a20c6-120">When you expose a COM+ application as an XML web service, detailed information about the syntax of all the methods available from an XML web service is published automatically, using the Web Services Description Language (WSDL).</span></span> <span data-ttu-id="a20c6-121">Ces informations sont utilisées par les clients qui utilisent votre service Web XML.</span><span class="sxs-lookup"><span data-stu-id="a20c6-121">This information is used by clients that use your XML web service.</span></span>

<span data-ttu-id="a20c6-122">COM+ vous offre deux moyens d’accéder à un service Web XML distant et de l’utiliser, comme suit :</span><span class="sxs-lookup"><span data-stu-id="a20c6-122">COM+ provides two ways for you to access and use a remote XML web service, as follows:</span></span>

-   <span data-ttu-id="a20c6-123">Le mode WKO ( *bien connu* ) peut être utilisé pour accéder à n’importe quel service Web XML qui publie sa syntaxe à l’aide de WSDL, même si ce service Web XML n’a pas été créé à l’aide de com+ ou même de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a20c6-123">The *well-known object* (WKO) mode can be used to access any XML web service that publishes its syntax using WSDL, even if that XML web service was not created using COM+ or even Microsoft Windows.</span></span>
-   <span data-ttu-id="a20c6-124">Le mode de l' *objet activé* par le client (CAO) peut être utilisé uniquement pour accéder aux services Web XML créés en exposant des applications com+.</span><span class="sxs-lookup"><span data-stu-id="a20c6-124">The *client-activated object* (CAO) mode can be used only to access XML web services created by exposing COM+ applications.</span></span> <span data-ttu-id="a20c6-125">Le mode CAO augmente les performances en utilisant des connexions persistantes, une fonctionnalité qui n’est pas prise en charge par la norme SOAP actuelle.</span><span class="sxs-lookup"><span data-stu-id="a20c6-125">CAO mode increases performance by using persistent connections, a feature not supported by the current SOAP standard.</span></span>

<span data-ttu-id="a20c6-126">Ces deux méthodes permettent aux applications clientes d’appeler des méthodes de services Web XML à distance de manière simple, sans avoir à écrire du code pour communiquer via une interface réseau ou pour analyser SOAP.</span><span class="sxs-lookup"><span data-stu-id="a20c6-126">Both methods allow client applications to call the methods of XML web services remotely in a straightforward fashion, without having to write code to communicate via a network interface or parse SOAP.</span></span> <span data-ttu-id="a20c6-127">Pour plus d’informations sur l’accès aux services Web XML dans les deux modes, consultez [accès aux services Web XML en mode CAO](accessing-xml-web-services-in-cao-mode.md) et [accès aux services Web XML en mode WKO](accessing-xml-web-services-in-wko-mode.md).</span><span class="sxs-lookup"><span data-stu-id="a20c6-127">For details about how to access XML web services in either mode, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md) and [Accessing XML Web Services in WKO Mode](accessing-xml-web-services-in-wko-mode.md).</span></span>

> [!Note]  
> <span data-ttu-id="a20c6-128">COM+ ne prend en charge que la spécification SOAP-RPC, et non la spécification SOAP-Document.</span><span class="sxs-lookup"><span data-stu-id="a20c6-128">COM+ supports only the SOAP-RPC specification, not the SOAP-Document specification.</span></span>

 

<span data-ttu-id="a20c6-129">COM+ facilite grandement l’utilisation des services Web XML en vous permettant d’utiliser des applications COM+ existantes en tant que services Web XML en mode CAO de manière totalement transparente.</span><span class="sxs-lookup"><span data-stu-id="a20c6-129">COM+ makes using XML web services especially easy by allowing you to use existing COM+ applications as XML web services in CAO mode in a completely transparent fashion.</span></span> <span data-ttu-id="a20c6-130">Si vous [exportez](exporting-a-soap-enabled-application.md) une application com+ qui a été exposée en tant que service Web XML à partir de votre serveur, tout client qui [importe](importing-a-soap-enabled-application.md) l’application peut utiliser de manière transparente le service Web XML du serveur chaque fois que l’application importée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a20c6-130">If you [export](exporting-a-soap-enabled-application.md) a COM+ application that has been exposed as an XML web service from your server, any client that [imports](importing-a-soap-enabled-application.md) the application can transparently use the server's XML web service whenever the imported application is used.</span></span> <span data-ttu-id="a20c6-131">Cette fonctionnalité permet de convertir très facilement les applications COM+ existantes en services Web XML et le déploiement de ces services sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="a20c6-131">This facility makes the conversion of existing COM+ applications to XML web services and the deployment of those services over a network very easy.</span></span>

<span data-ttu-id="a20c6-132">L’utilisation des services Web XML présente plusieurs avantages par rapport aux autres implémentations des appels de procédure distante (RPC), y compris les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a20c6-132">Using XML web services has several unique advantages over alternative implementations of remote procedure calls (RPC), including the following:</span></span>

-   <span data-ttu-id="a20c6-133">SOAP est une véritable implémentation de RPC multiplateforme qui augmente l’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="a20c6-133">SOAP is a true cross-platform RPC implementation, which increases interoperability.</span></span>
-   <span data-ttu-id="a20c6-134">Les services Web XML prennent en charge les méthodes avec les paramètres d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="a20c6-134">XML web services support methods with both input and output parameters.</span></span>
-   <span data-ttu-id="a20c6-135">Les services Web XML s’exécutent sur HTTP, ce qui peut généralement pénétrer les pare-feu susceptibles de bloquer d’autres implémentations RPC.</span><span class="sxs-lookup"><span data-stu-id="a20c6-135">XML web services run over HTTP, which can usually penetrate firewalls that might block other RPC implementations.</span></span>
-   <span data-ttu-id="a20c6-136">Lorsqu’un service Web XML est implémenté à l’aide de COM+, le développeur n’a pas à écrire de code spécialisé. Il s’agit d’un énorme avantage par rapport aux autres mécanismes RPC.</span><span class="sxs-lookup"><span data-stu-id="a20c6-136">When an XML web service is implemented using COM+, the developer does not have to write any specialized code; this is a tremendous advantage over alternative RPC mechanisms.</span></span>

> [!Note]  
> <span data-ttu-id="a20c6-137">Les services Web XML ne prennent pas en charge les appels transactionnels asynchrones ou en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="a20c6-137">XML web services do not support asynchronous or transparently transactional calls.</span></span> <span data-ttu-id="a20c6-138">Utilisez le service [composants en file d’attente com+](com--queued-components.md) lorsque vous avez besoin de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a20c6-138">Use the [COM+ Queued Components](com--queued-components.md) service when you require this functionality.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a20c6-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a20c6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a20c6-140">Considérations sur la sécurité du service SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="a20c6-140">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



