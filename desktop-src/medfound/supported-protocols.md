---
description: Protocoles pris en charge
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocoles pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753837"
---
# <a name="supported-protocols"></a><span data-ttu-id="a6d63-103">Protocoles pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6d63-103">Supported Protocols</span></span>

<span data-ttu-id="a6d63-104">Media Foundation prend en charge les protocoles suivants :</span><span class="sxs-lookup"><span data-stu-id="a6d63-104">Media Foundation supports the following protocols:</span></span>

-   <span data-ttu-id="a6d63-105">Protocole RTSP (Real Time Streaming Protocol)</span><span class="sxs-lookup"><span data-stu-id="a6d63-105">Real Time Streaming Protocol (RTSP)</span></span>

    <span data-ttu-id="a6d63-106">RTSP est principalement utilisé pour la diffusion en continu de contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="a6d63-106">RTSP is mainly used for streaming media content.</span></span> <span data-ttu-id="a6d63-107">Il peut utiliser UDP ou TCP comme protocoles de transport.</span><span class="sxs-lookup"><span data-stu-id="a6d63-107">It can use UDP or TCP as transport protocols.</span></span> <span data-ttu-id="a6d63-108">Le protocole UDP est le plus efficace pour la distribution de contenu, car la surcharge de bande passante est inférieure à celle des protocoles basés sur TCP.</span><span class="sxs-lookup"><span data-stu-id="a6d63-108">UDP is the most efficient for content delivery because the bandwidth overhead is less than with TCP-based protocols.</span></span> <span data-ttu-id="a6d63-109">Même si le protocole TCP garantit la remise fiable des paquets, TCP n’est pas adapté aux flux de médias numériques, où l’utilisation efficace de la bande passante est plus importante que les paquets perdus occasionnellement.</span><span class="sxs-lookup"><span data-stu-id="a6d63-109">Even though the TCP protocol ensures reliable packet delivery, TCP is not well suited for digital media streams, where efficient use of bandwidth is more important than occasional lost packets.</span></span>

-   <span data-ttu-id="a6d63-110">Hypertext Transfer Protocol (HTTP)</span><span class="sxs-lookup"><span data-stu-id="a6d63-110">Hypertext Transfer Protocol (HTTP)</span></span>

    <span data-ttu-id="a6d63-111">HTTP utilise TCP et est utilisé par les serveurs Web.</span><span class="sxs-lookup"><span data-stu-id="a6d63-111">HTTP uses TCP and is used by web servers.</span></span> <span data-ttu-id="a6d63-112">Le schéma « httpd:// » indique que la source peut être téléchargée à partir d’un serveur Web.</span><span class="sxs-lookup"><span data-stu-id="a6d63-112">The "httpd://" scheme indicates that the source is downloadable from a web server.</span></span> <span data-ttu-id="a6d63-113">Le protocole HTTP est également utilisé dans le cas de pare-feu, qui sont généralement configurés pour accepter les requêtes HTTP et rejetent généralement d’autres protocoles de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="a6d63-113">HTTP is also used in case of firewalls, which are usually configured to accept HTTP requests and typically reject other streaming protocols.</span></span>

<span data-ttu-id="a6d63-114">L’application peut récupérer les protocoles pris en charge par Media Foundation à l’aide de l’interface [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) .</span><span class="sxs-lookup"><span data-stu-id="a6d63-114">The application can get the protocols supported by Media Foundation by using the [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) interface.</span></span> <span data-ttu-id="a6d63-115">Pour ce faire, l’application doit d’abord récupérer le nombre de protocoles, en appelant [**IMFNetSchemeHandlerConfig :: GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) , puis obtenir le type de protocole en fonction de l’index en appelant [**IMFNetSchemeHandlerConfig :: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span><span class="sxs-lookup"><span data-stu-id="a6d63-115">To do this, the application must first retrieve the number of protocols, by calling [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) and then get the protocol type based on the index by calling [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span></span> <span data-ttu-id="a6d63-116">Cette méthode retourne l’une des valeurs définies dans l’énumération de [**\_ \_ type de protocole MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="a6d63-116">This method returns one of the values defined in the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>

<span data-ttu-id="a6d63-117">L’application peut également récupérer les schémas pris en charge par le programme de résolution source en appelant la fonction [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .</span><span class="sxs-lookup"><span data-stu-id="a6d63-117">The application can also get the schemes supported by the source resolver by calling the [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) function.</span></span>

## <a name="protocol-rollover"></a><span data-ttu-id="a6d63-118">Substitution de protocole</span><span class="sxs-lookup"><span data-stu-id="a6d63-118">Protocol Rollover</span></span>

<span data-ttu-id="a6d63-119">Lorsqu’une application spécifie « mms:// » comme schéma d’URL, le programme de résolution source effectue une opération de *substitution de protocole* .</span><span class="sxs-lookup"><span data-stu-id="a6d63-119">When an application specifies "mms://" as the URL scheme, the source resolver performs a *protocol rollover* operation.</span></span> <span data-ttu-id="a6d63-120">Dans ce processus, le programme de résolution source détermine le meilleur protocole pour la source réseau à utiliser pour obtenir le contenu.</span><span class="sxs-lookup"><span data-stu-id="a6d63-120">In this process, the source resolver determines the best protocol for the network source to use for getting the content.</span></span> <span data-ttu-id="a6d63-121">En général, pour la diffusion de contenu multimédia, RTSP avec UDP (RTSP) est plus efficace que HTTP.</span><span class="sxs-lookup"><span data-stu-id="a6d63-121">Typically, for media steaming, RTSP with UDP (RTSPU) is more efficient than HTTP.</span></span> <span data-ttu-id="a6d63-122">Toutefois, si le contenu est hébergé sur un serveur Web, le protocole HTTP est un meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="a6d63-122">However, if the content is hosted on a web server, HTTP is a better choice.</span></span>

<span data-ttu-id="a6d63-123">La substitution de protocole peut également se produire lorsqu’une tentative d’utilisation du protocole spécifié dans le schéma d’URL échoue.</span><span class="sxs-lookup"><span data-stu-id="a6d63-123">Protocol rollover can also occur when an attempt to use the protocol specified in the URL scheme fails.</span></span> <span data-ttu-id="a6d63-124">Par exemple, un protocole peut échouer lorsqu’un pare-feu bloque les paquets UDP.</span><span class="sxs-lookup"><span data-stu-id="a6d63-124">For example, a protocol can fail when a firewall blocks UDP packets.</span></span> <span data-ttu-id="a6d63-125">Dans ce cas, le programme de résolution source bascule vers HTTP.</span><span class="sxs-lookup"><span data-stu-id="a6d63-125">In this case, the source resolver switches to HTTP.</span></span>

<span data-ttu-id="a6d63-126">La substitution de protocole ne s’applique pas si le schéma d’URL contient un protocole spécifique, tel que « rtspu:// ».</span><span class="sxs-lookup"><span data-stu-id="a6d63-126">Protocol rollover does not apply if the URL scheme contains a specific protocol, such as "rtspu://".</span></span> <span data-ttu-id="a6d63-127">En outre, la substitution n’est pas effectuée si l’authentification échoue ou si le serveur a atteint une limite de connexions client.</span><span class="sxs-lookup"><span data-stu-id="a6d63-127">Also, rollover is not performed if authentication fails or the server has reached a limit of client connections.</span></span> <span data-ttu-id="a6d63-128">Il est recommandé que les applications spécifient le schéma « mms:// » et autorisent le programme de résolution source à sélectionner le meilleur protocole pour le scénario.</span><span class="sxs-lookup"><span data-stu-id="a6d63-128">It is recommended that applications specify the "mms://" scheme and allow the source resolver to select the best protocol for the scenario.</span></span>

<span data-ttu-id="a6d63-129">Le tableau suivant répertorie l’ordre de substitution.</span><span class="sxs-lookup"><span data-stu-id="a6d63-129">The following table lists the rollover order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6d63-130">Schémas autorisés</span><span class="sxs-lookup"><span data-stu-id="a6d63-130">Schemes allowed</span></span></th>
<th><span data-ttu-id="a6d63-131">Ordre de substitution des protocoles</span><span class="sxs-lookup"><span data-stu-id="a6d63-131">Protocol rollover order</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a6d63-132">mms://ou rtsp://</span><span class="sxs-lookup"><span data-stu-id="a6d63-132">mms:// or rtsp://</span></span></td>
<td><span data-ttu-id="a6d63-133">Mise en cache rapide activée :</span><span class="sxs-lookup"><span data-stu-id="a6d63-133">Fast Cache enabled:</span></span><br/>
<ol>
<li><span data-ttu-id="a6d63-134">RTSP avec TCP (RTSPt)</span><span class="sxs-lookup"><span data-stu-id="a6d63-134">RTSP with TCP (RTSPT)</span></span><br/></li>
<li><span data-ttu-id="a6d63-135">RTSP avec UDP (RTSP)</span><span class="sxs-lookup"><span data-stu-id="a6d63-135">RTSP with UDP (RTSPU)</span></span><br/></li>
<li><span data-ttu-id="a6d63-136">Streaming HTTP</span><span class="sxs-lookup"><span data-stu-id="a6d63-136">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="a6d63-137">Téléchargement HTTP (HTTPD)</span><span class="sxs-lookup"><span data-stu-id="a6d63-137">HTTP download (HTTPD)</span></span><br/></li>
</ol>
<span data-ttu-id="a6d63-138">Mise en cache rapide désactivée :</span><span class="sxs-lookup"><span data-stu-id="a6d63-138">Fast Cache disabled:</span></span><br/>
<ol>
<li><span data-ttu-id="a6d63-139">RTSP</span><span class="sxs-lookup"><span data-stu-id="a6d63-139">RTSPU</span></span><br/></li>
<li><span data-ttu-id="a6d63-140">RTSPt</span><span class="sxs-lookup"><span data-stu-id="a6d63-140">RTSPT</span></span><br/></li>
<li><span data-ttu-id="a6d63-141">Streaming HTTP</span><span class="sxs-lookup"><span data-stu-id="a6d63-141">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="a6d63-142">Téléchargement HTTP</span><span class="sxs-lookup"><span data-stu-id="a6d63-142">HTTP Download</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6d63-143">rtspu://</span><span class="sxs-lookup"><span data-stu-id="a6d63-143">rtspu://</span></span></td>
<td><span data-ttu-id="a6d63-144">RTSP</span><span class="sxs-lookup"><span data-stu-id="a6d63-144">RTSPU</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6d63-145">rtspt://</span><span class="sxs-lookup"><span data-stu-id="a6d63-145">rtspt://</span></span></td>
<td><span data-ttu-id="a6d63-146">RTSPt</span><span class="sxs-lookup"><span data-stu-id="a6d63-146">RTSPT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6d63-147"> https://</span><span class="sxs-lookup"><span data-stu-id="a6d63-147">https://</span></span></td>
<td><ol>
<li><span data-ttu-id="a6d63-148">HTTP</span><span class="sxs-lookup"><span data-stu-id="a6d63-148">HTTP</span></span><br/></li>
<li><span data-ttu-id="a6d63-149">HTTPD</span><span class="sxs-lookup"><span data-stu-id="a6d63-149">HTTPD</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6d63-150">httpd://</span><span class="sxs-lookup"><span data-stu-id="a6d63-150">httpd://</span></span></td>
<td><span data-ttu-id="a6d63-151">HTTPD</span><span class="sxs-lookup"><span data-stu-id="a6d63-151">HTTPD</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a><span data-ttu-id="a6d63-152">Récupération du protocole en cours</span><span class="sxs-lookup"><span data-stu-id="a6d63-152">Retrieving the Current Protocol</span></span>

<span data-ttu-id="a6d63-153">Après une opération de substitution de protocole, la source réseau peut utiliser un autre protocole que celui spécifié par l’application dans le schéma d’URL.</span><span class="sxs-lookup"><span data-stu-id="a6d63-153">After a protocol rollover operation, the network source might use a protocol other than the one specified by the application in the URL scheme.</span></span> <span data-ttu-id="a6d63-154">Le résultat de substitution de protocole est disponible pour l’application une fois que la source réseau a établi la connexion avec le serveur multimédia.</span><span class="sxs-lookup"><span data-stu-id="a6d63-154">The protocol rollover result is available to the application after the network source establishes the connection with the media server.</span></span>

<span data-ttu-id="a6d63-155">Pour obtenir le protocole et le transport utilisés pour obtenir le contenu, l’application peut récupérer les valeurs de propriété pour la propriété de [ \_ protocole MFNETSOURCE](mfnetsource-protocol-property.md) et la propriété de [ \_ transport MFNETSOURCE](mfnetsource-transport-property.md) d’un objet **IPropertyStore** à partir de la source réseau.</span><span class="sxs-lookup"><span data-stu-id="a6d63-155">To get the protocol and transport that are used for getting the content, the application can retrieve the property values for the [MFNETSOURCE\_PROTOCOL](mfnetsource-protocol-property.md) property and the [MFNETSOURCE\_TRANSPORT](mfnetsource-transport-property.md) property of an **IPropertyStore** object from the network source.</span></span>

<span data-ttu-id="a6d63-156">Le code suivant montre comment récupérer ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a6d63-156">The following code shows how to get these values.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



<span data-ttu-id="a6d63-157">Dans l’exemple de code précédent, **IPropertyStore :: GetValue** récupère la \_ valeur de protocole MFNETSOURCE, qui est un membre de l’énumération de [**\_ \_ type de protocole MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="a6d63-157">In the preceding example code, **IPropertyStore::GetValue** retrieves the MFNETSOURCE\_PROTOCOL value, which is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span> <span data-ttu-id="a6d63-158">Pour le \_ transport MFNETSOURCE, la valeur est un membre de l’énumération du [**\_ \_ type de transport MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="a6d63-158">For MFNETSOURCE\_TRANSPORT, the value is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>

<span data-ttu-id="a6d63-159">L’application peut également récupérer les mêmes valeurs à l’aide du service MFNETSOURCE \_ Statistics \_ service.</span><span class="sxs-lookup"><span data-stu-id="a6d63-159">Alternately, the application can get the same values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span> <span data-ttu-id="a6d63-160">Pour utiliser ce service, l’application peut appeler la fonction [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer la Banque de propriétés à partir de la source réseau.</span><span class="sxs-lookup"><span data-stu-id="a6d63-160">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store from the network source.</span></span> <span data-ttu-id="a6d63-161">Cette banque de propriétés contient des statistiques réseau dans la propriété [MFNETSOURCE \_ Statistics](mfnetsource-statistics-property.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d63-161">This property store contains network statistics in the [MFNETSOURCE\_STATISTICS](mfnetsource-statistics-property.md) property.</span></span> <span data-ttu-id="a6d63-162">Les valeurs de protocole et de transport peuvent être récupérées en spécifiant \_ l’ID de protocole MFNETSOURCE \_ et \_ \_ l’ID de transport MFNETSOURCE, définis dans l’énumération des [**\_ \_ ID de statistiques MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="a6d63-162">Protocol and transport values can be retrieved by specifying MFNETSOURCE\_PROTOCOL\_ID and MFNETSOURCE\_TRANSPORT\_ID—defined in the [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enumeration.</span></span> <span data-ttu-id="a6d63-163">Le code suivant montre comment récupérer les valeurs de protocole et de transport à l’aide du \_ service MFNETSOURCE Statistics \_ service.</span><span class="sxs-lookup"><span data-stu-id="a6d63-163">The following code shows how to get the protocol and transport values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a><span data-ttu-id="a6d63-164">Activation et désactivation des protocoles</span><span class="sxs-lookup"><span data-stu-id="a6d63-164">Enabling and Disabling Protocols</span></span>

<span data-ttu-id="a6d63-165">L’application peut configurer la source réseau afin que certains protocoles soient ignorés pendant le processus de substitution.</span><span class="sxs-lookup"><span data-stu-id="a6d63-165">The application can configure the network source so that certain protocols are skipped during the rollover process.</span></span> <span data-ttu-id="a6d63-166">Pour ce faire, les propriétés de la source réseau sont utilisées pour désactiver des protocoles spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a6d63-166">To do this, network source properties are used to disable specific protocols.</span></span> <span data-ttu-id="a6d63-167">Le tableau suivant présente les propriétés et les protocoles qu’ils contrôlent.</span><span class="sxs-lookup"><span data-stu-id="a6d63-167">The following table shows the properties and the protocols they control.</span></span>



| <span data-ttu-id="a6d63-168">Propriété</span><span class="sxs-lookup"><span data-stu-id="a6d63-168">Property</span></span>                                                                    | <span data-ttu-id="a6d63-169">Description</span><span class="sxs-lookup"><span data-stu-id="a6d63-169">Description</span></span>                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="a6d63-170">MFNETSOURCE \_ activer \_ http</span><span class="sxs-lookup"><span data-stu-id="a6d63-170">MFNETSOURCE\_ENABLE\_HTTP</span></span>](mfnetsource-enable-http-property.md)           | <span data-ttu-id="a6d63-171">Active ou désactive les protocoles HTTP et HTTPD.</span><span class="sxs-lookup"><span data-stu-id="a6d63-171">Enables or disables HTTP and HTTPD.</span></span>         |
| [<span data-ttu-id="a6d63-172">MFNETSOURCE \_ activer \_ RTSP</span><span class="sxs-lookup"><span data-stu-id="a6d63-172">MFNETSOURCE\_ENABLE\_RTSP</span></span>](mfnetsource-enable-rtsp-property.md)           | <span data-ttu-id="a6d63-173">Active ou désactive RTSP et RTSPt.</span><span class="sxs-lookup"><span data-stu-id="a6d63-173">Enables or disables RTSPU and RTSPT.</span></span>        |
| [<span data-ttu-id="a6d63-174">MFNETSOURCE \_ activer \_ TCP</span><span class="sxs-lookup"><span data-stu-id="a6d63-174">MFNETSOURCE\_ENABLE\_TCP</span></span>](mfnetsource-enable-tcp-property.md)             | <span data-ttu-id="a6d63-175">Active ou désactive le protocole RTSPt.</span><span class="sxs-lookup"><span data-stu-id="a6d63-175">Enables or disables RTSPT.</span></span>                  |
| [<span data-ttu-id="a6d63-176">MFNETSOURCE \_ activer \_ UDP</span><span class="sxs-lookup"><span data-stu-id="a6d63-176">MFNETSOURCE\_ENABLE\_UDP</span></span>](mfnetsource-enable-udp-property.md)             | <span data-ttu-id="a6d63-177">Active ou désactive RTSP.</span><span class="sxs-lookup"><span data-stu-id="a6d63-177">Enables or disables RTSPU.</span></span>                  |
| [<span data-ttu-id="a6d63-178">MFNETSOURCE \_ activer le \_ Téléchargement</span><span class="sxs-lookup"><span data-stu-id="a6d63-178">MFNETSOURCE\_ENABLE\_DOWNLOAD</span></span>](mfnetsource-enable-download-property.md)   | <span data-ttu-id="a6d63-179">Active ou désactive le HTTPD.</span><span class="sxs-lookup"><span data-stu-id="a6d63-179">Enables or disables HTTPD.</span></span>                  |
| [<span data-ttu-id="a6d63-180">MFNETSOURCE \_ activer la \_ diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="a6d63-180">MFNETSOURCE\_ENABLE\_STREAMING</span></span>](mfnetsource-enable-streaming-property.md) | <span data-ttu-id="a6d63-181">Active ou désactive RTSP, RTSPt et HTTP.</span><span class="sxs-lookup"><span data-stu-id="a6d63-181">Enables or disables RTSPU, RTSPT, and HTTP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a6d63-182">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6d63-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6d63-183">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6d63-183">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




