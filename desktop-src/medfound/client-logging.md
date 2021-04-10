---
description: Journalisation du client
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Journalisation du client (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201176"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="8c48a-103">Journalisation du client (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="8c48a-103">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="8c48a-104">La source réseau prend en charge la journalisation du client, ce qui permet au serveur multimédia d’effectuer le suivi de l’activité des clients qui s’y connectent.</span><span class="sxs-lookup"><span data-stu-id="8c48a-104">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="8c48a-105">Les journaux du client permettent à un serveur d’enregistrer les statistiques de connexion, de rendu et de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="8c48a-105">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="8c48a-106">Ces journaux peuvent être utilisés par les fournisseurs de contenu dans divers scénarios, tels que, pour suivre l’utilisation du serveur multimédia et générer la facturation, ou pour fournir un contenu de qualité appropriée en fonction de la vitesse du réseau du client.</span><span class="sxs-lookup"><span data-stu-id="8c48a-106">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="8c48a-107">Un fichier journal contient plusieurs entrées d’événement client.</span><span class="sxs-lookup"><span data-stu-id="8c48a-107">A log file contains several client event entries.</span></span> <span data-ttu-id="8c48a-108">Chaque entrée de journal contient un certain nombre de champs délimités par des espaces.</span><span class="sxs-lookup"><span data-stu-id="8c48a-108">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="8c48a-109">Il existe deux types de journaux client : le *rendu* (lecture) et la *diffusion en continu* (réception).</span><span class="sxs-lookup"><span data-stu-id="8c48a-109">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="8c48a-110">Étant donné que le contenu peut être lu et diffusé simultanément, le client peut envoyer une combinaison des deux types de données de journal.</span><span class="sxs-lookup"><span data-stu-id="8c48a-110">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="8c48a-111">Dans certains cas, deux entrées de journal peuvent exister pour la même session.</span><span class="sxs-lookup"><span data-stu-id="8c48a-111">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="8c48a-112">Par exemple, lorsque la mise en cache rapide est activée, le client peut finir de recevoir le contenu diffusé en continu avant de terminer son rendu.</span><span class="sxs-lookup"><span data-stu-id="8c48a-112">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="8c48a-113">Dans ce cas, les données du journal de diffusion en continu sont envoyées avant les données du journal de rendu.</span><span class="sxs-lookup"><span data-stu-id="8c48a-113">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="8c48a-114">Le client envoie des données de journal au serveur lorsque le client passe d’un état de lecture (lecture, rapide ou rembobinage) à un état de non-lecture (arrêter, suspendre, terminer le flux et début du flux).</span><span class="sxs-lookup"><span data-stu-id="8c48a-114">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="8c48a-115">Lorsque les données d’un journal de rendu sont soumises, une connexion est établie directement sur le serveur multimédia ou sur un serveur proxy configuré.</span><span class="sxs-lookup"><span data-stu-id="8c48a-115">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="8c48a-116">Si le contenu est stocké dans un fichier de cache local temporaire sur l’ordinateur qui exécute le client, le client peut lire un fichier à partir de son cache local et envoyer les données du journal de rendu pour indiquer qu’il a lu le contenu.</span><span class="sxs-lookup"><span data-stu-id="8c48a-116">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="8c48a-117">Dans ce cas, le client lit un fichier à partir de son cache local, l’entrée du journal de rendu ne contient pas de statistiques réseau et le protocole est défini sur cache.</span><span class="sxs-lookup"><span data-stu-id="8c48a-117">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="8c48a-118">Le client envoie des données de journal de diffusion sur le serveur pour indiquer comment le client a reçu le contenu, mais pas comment il a été rendu.</span><span class="sxs-lookup"><span data-stu-id="8c48a-118">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="8c48a-119">Le client peut envoyer le journal de diffusion en continu longtemps avant que le client n’ait terminé le rendu du contenu.</span><span class="sxs-lookup"><span data-stu-id="8c48a-119">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="8c48a-120">Cette rubrique ne fournit pas d’informations sur tous les champs de journal.</span><span class="sxs-lookup"><span data-stu-id="8c48a-120">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="8c48a-121">Pour obtenir une référence complète, consultez [structure des données du journal Windows Media](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span><span class="sxs-lookup"><span data-stu-id="8c48a-121">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="8c48a-122">Configuration des champs du journal</span><span class="sxs-lookup"><span data-stu-id="8c48a-122">Configuring Log Fields</span></span>

<span data-ttu-id="8c48a-123">Media Foundation permet au client de configurer la source réseau à l’aide de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8c48a-123">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="8c48a-124">L’application doit définir les propriétés appropriées dans une banque de propriétés et la passer à l’une des méthodes de programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="8c48a-124">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="8c48a-125">Le programme de résolution source crée la source réseau comme demandé et ouvre une connexion avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="8c48a-125">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="8c48a-126">Si la connexion réussit, le client envoie des informations sur lui-même.</span><span class="sxs-lookup"><span data-stu-id="8c48a-126">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="8c48a-127">Le tableau suivant décrit les champs du journal et les propriétés correspondantes qu’une application peut définir par le biais du programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="8c48a-127">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="8c48a-128">Ces informations ne changent pas au cours de la session.</span><span class="sxs-lookup"><span data-stu-id="8c48a-128">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c48a-129">Champ de journalisation</span><span class="sxs-lookup"><span data-stu-id="8c48a-129">Logging field</span></span></th>
<th><span data-ttu-id="8c48a-130">Description</span><span class="sxs-lookup"><span data-stu-id="8c48a-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c48a-131">c-playerid</span><span class="sxs-lookup"><span data-stu-id="8c48a-131">c-playerid</span></span></td>
<td><span data-ttu-id="8c48a-132">Identification unique du joueur.</span><span class="sxs-lookup"><span data-stu-id="8c48a-132">Unique identification of the player.</span></span> <span data-ttu-id="8c48a-133">Ces informations sont envoyées au début de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8c48a-133">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="8c48a-134">En général, il s’agit d’un GUID du client.</span><span class="sxs-lookup"><span data-stu-id="8c48a-134">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="8c48a-135">Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c48a-135">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="8c48a-136">Le client envoie ces informations au serveur au début de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8c48a-136">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="8c48a-137">Exemple de valeur : &quot; {c579d042-CECC-11D1-bb31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="8c48a-137">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c48a-138">c-playerversion</span><span class="sxs-lookup"><span data-stu-id="8c48a-138">c-playerversion</span></span></td>
<td><span data-ttu-id="8c48a-139">Numéro de version du lecteur qui est envoyé au début de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8c48a-139">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="8c48a-140">Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c48a-140">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="8c48a-141">Le client envoie ces informations au serveur au début de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8c48a-141">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c48a-142">CS (agent utilisateur)</span><span class="sxs-lookup"><span data-stu-id="8c48a-142">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="8c48a-143">Type de navigateur utilisé si le lecteur a été incorporé dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="8c48a-143">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="8c48a-144">Cette valeur peut être définie par le client dans la propriété <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c48a-144">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="8c48a-145">Si le lecteur n’a pas été incorporé, ce champ fait référence à l’agent utilisateur du client qui a généré le journal.</span><span class="sxs-lookup"><span data-stu-id="8c48a-145">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="8c48a-146">Dans ce cas, le client doit définir la propriété <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c48a-146">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="8c48a-147">Le client envoie ces informations au serveur au début de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8c48a-147">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="8c48a-148">Exemple de valeur : &quot; Mozilla/4.0 _ (compatible ; _MSIE_4.01 ; _Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="8c48a-148">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c48a-149">CS (référant)</span><span class="sxs-lookup"><span data-stu-id="8c48a-149">cs(Referer)</span></span></td>
<td><span data-ttu-id="8c48a-150">URL de la page Web dans laquelle le lecteur a été incorporé (s’il a été incorporé).</span><span class="sxs-lookup"><span data-stu-id="8c48a-150">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="8c48a-151">Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c48a-151">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="8c48a-152">Le client envoie ces informations au serveur à la fin de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8c48a-152">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="8c48a-153">Exemple de valeur : &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="8c48a-153">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c48a-154">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="8c48a-154">c-hostexe</span></span></td>
<td><span data-ttu-id="8c48a-155">Pour les entrées de journal du lecteur, le programme hôte (. exe) qui a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="8c48a-155">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="8c48a-156">Par exemple, une page Web dans un navigateur, une applet Microsoft Visual Basic ou un lecteur autonome.</span><span class="sxs-lookup"><span data-stu-id="8c48a-156">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="8c48a-157">Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c48a-157">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="8c48a-158">Le client envoie ces informations au serveur à la fin de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8c48a-158">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="8c48a-159">Exemples de valeurs :</span><span class="sxs-lookup"><span data-stu-id="8c48a-159">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="8c48a-160">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="8c48a-160">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="8c48a-161">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="8c48a-161">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c48a-162">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="8c48a-162">c-hostexever</span></span></td>
<td><span data-ttu-id="8c48a-163">Numéro de version du programme hôte (. exe).</span><span class="sxs-lookup"><span data-stu-id="8c48a-163">Host program (.exe) version number.</span></span> <span data-ttu-id="8c48a-164">Le client peut envoyer ces informations au serveur dans la propriété <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c48a-164">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="8c48a-165">Le client envoie ces informations au serveur à la fin de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8c48a-165">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8c48a-166">L’exemple de code suivant montre comment une application cliente configure la source réseau.</span><span class="sxs-lookup"><span data-stu-id="8c48a-166">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="8c48a-167">Cet exemple définit le champ de Journal « c-hostexe ».</span><span class="sxs-lookup"><span data-stu-id="8c48a-167">This example sets the "c-hostexe" log field.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a><span data-ttu-id="8c48a-168">Récupération des statistiques réseau</span><span class="sxs-lookup"><span data-stu-id="8c48a-168">Retrieving Network Statistics</span></span>

<span data-ttu-id="8c48a-169">Lorsque l’application appelle l’une des méthodes de résolution de source, elle crée la source réseau, définit les propriétés spécifiées dans la Banque de propriétés et ouvre une session avec le serveur multimédia.</span><span class="sxs-lookup"><span data-stu-id="8c48a-169">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="8c48a-170">Outre les informations configurables décrites dans la section précédente, les données supplémentaires sont transférées entre le serveur et le client au début de la session, pendant la diffusion en continu et lorsque la session est fermée.</span><span class="sxs-lookup"><span data-stu-id="8c48a-170">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="8c48a-171">L’application peut récupérer des statistiques réseau à l’aide de l’identificateur de service **MFNETSOURCE \_ Statistics \_ service** .</span><span class="sxs-lookup"><span data-stu-id="8c48a-171">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="8c48a-172">Pour utiliser ce service, l’application peut appeler la fonction [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer la Banque de propriétés qui contient les statistiques réseau dans la propriété [**MFNETSOURCE \_ Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="8c48a-172">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="8c48a-173">Des valeurs spécifiques peuvent être récupérées en fournissant l’identificateur correspondant défini dans l’énumération **MFNETSOURCE \_ Statistics \_ ID** .</span><span class="sxs-lookup"><span data-stu-id="8c48a-173">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="8c48a-174">L’exemple de code suivant montre comment utiliser le service pour récupérer le nombre de paquets reçus par le client.</span><span class="sxs-lookup"><span data-stu-id="8c48a-174">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



<span data-ttu-id="8c48a-175">La liste suivante décrit certains identificateurs de statistiques réseau définis dans [**MFNETSOURCE \_ Statistics \_ ID**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="8c48a-175">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="8c48a-176">Identificateur des statistiques réseau</span><span class="sxs-lookup"><span data-stu-id="8c48a-176">Network statistics identifier</span></span>              | <span data-ttu-id="8c48a-177">Description</span><span class="sxs-lookup"><span data-stu-id="8c48a-177">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c48a-178">**\_ID AVGBANDWIDTHBPS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-178">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="8c48a-179">Bande passante moyenne (en bits par seconde) à laquelle le client a été connecté au serveur.</span><span class="sxs-lookup"><span data-stu-id="8c48a-179">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="8c48a-180">La valeur est calculée sur toute la durée de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8c48a-180">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="8c48a-181">**\_ID BUFFERINGCOUNT \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-181">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="8c48a-182">Nombre de fois où le client met en mémoire tampon lors de la diffusion du flux.</span><span class="sxs-lookup"><span data-stu-id="8c48a-182">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="8c48a-183">**\_ID BYTESRECEIVED \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-183">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="8c48a-184">Nombre d’octets reçus par le client à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="8c48a-184">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="8c48a-185">La valeur n’inclut aucune surcharge ajoutée par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="8c48a-185">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="8c48a-186">Le même contenu diffusé en continu à l’aide de différents protocoles peut aboutir à des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="8c48a-186">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="8c48a-187">**\_ID LINKBANDWIDTH \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-187">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="8c48a-188">Bande passante disponible maximale du client en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="8c48a-188">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="8c48a-189">**\_ID LOSTPACKETS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-189">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="8c48a-190">Nombre de paquets envoyés par le serveur mais perdus pendant la transmission et jamais joués par le client.</span><span class="sxs-lookup"><span data-stu-id="8c48a-190">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="8c48a-191">La valeur n’inclut pas les paquets TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="8c48a-191">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="8c48a-192">**\_ID RECVPACKETS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-192">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="8c48a-193">Nombre de paquets reçus à partir du serveur la valeur n’inclut pas les paquets TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="8c48a-193">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="8c48a-194">**\_ID RECOVEREDBYECCPACKETS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-194">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="8c48a-195">Paquets perdus sur le réseau qui ont été réparés et récupérés au niveau de la couche client.</span><span class="sxs-lookup"><span data-stu-id="8c48a-195">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="8c48a-196">Cette valeur n’inclut pas les paquets TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="8c48a-196">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="8c48a-197">**\_ID RESENDSREQUESTED \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-197">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="8c48a-198">Nombre de demandes effectuées par le client pour recevoir de nouveaux paquets.</span><span class="sxs-lookup"><span data-stu-id="8c48a-198">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="8c48a-199">Cette valeur n’inclut pas les paquets TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="8c48a-199">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="8c48a-200">**\_ID RECOVEREDPACKETS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-200">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="8c48a-201">Nombre de paquets récupérés, car ils ont été renvoyés via UDP.</span><span class="sxs-lookup"><span data-stu-id="8c48a-201">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="8c48a-202">Cette valeur n’inclut pas les paquets TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="8c48a-202">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="8c48a-203">Ce champ contient un zéro, sauf si le client utilise le renvoi UDP.</span><span class="sxs-lookup"><span data-stu-id="8c48a-203">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="8c48a-204">**\_ID BUFFERPROGRESS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c48a-204">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="8c48a-205">Pourcentage de la mémoire tampon de diffusion rempli pendant la mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8c48a-205">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="8c48a-206">**\_ID de protocole MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="8c48a-206">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="8c48a-207">Protocole utilisé pour accéder au flux.</span><span class="sxs-lookup"><span data-stu-id="8c48a-207">Protocol used to access the stream.</span></span> <span data-ttu-id="8c48a-208">Cela peut différer du protocole demandé par le client.</span><span class="sxs-lookup"><span data-stu-id="8c48a-208">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="8c48a-209">**\_ID de transport MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="8c48a-209">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="8c48a-210">Protocole de transport utilisé pour remettre le flux.</span><span class="sxs-lookup"><span data-stu-id="8c48a-210">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="8c48a-211">Il doit s’agir du protocole UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="8c48a-211">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="8c48a-212">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c48a-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c48a-213">Fonctionnalités de la source réseau</span><span class="sxs-lookup"><span data-stu-id="8c48a-213">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="8c48a-214">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c48a-214">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

