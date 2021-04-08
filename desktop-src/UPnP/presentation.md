---
title: Présentation
description: La présentation est la dernière étape du processus UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839842"
---
# <a name="presentation"></a><span data-ttu-id="96972-103">Présentation</span><span class="sxs-lookup"><span data-stu-id="96972-103">Presentation</span></span>

<span data-ttu-id="96972-104">La présentation est la dernière étape du processus UPnP.</span><span class="sxs-lookup"><span data-stu-id="96972-104">Presentation is the final step in the UPnP process.</span></span> <span data-ttu-id="96972-105">Si un appareil possède une URL pour la présentation, un point de contrôle peut récupérer une page à partir de cette URL et charger la page dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="96972-105">If a device has a URL for presentation, a control point can retrieve a page from this URL and load the page into a browser.</span></span> <span data-ttu-id="96972-106">Selon les fonctionnalités de la page de présentation et de l’appareil, le point de contrôle peut contrôler l’appareil et afficher l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="96972-106">Depending on the capabilities of the presentation page and the device, the control point can control the device and view the status of the device.</span></span>

<span data-ttu-id="96972-107">Le chemin d’accès de la ressource, qui est transmis à [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) pendant l’inscription, est l’emplacement où se trouvent tous les fichiers pertinents pour la présentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="96972-107">The resource path, which is passed to [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) during registration, is where all the files relevant to the presentation of the device are located.</span></span> <span data-ttu-id="96972-108">Les développeurs d’appareils peuvent fournir des pages distinctes pour chaque appareil intégré.</span><span class="sxs-lookup"><span data-stu-id="96972-108">Device developers can provide separate pages for each embedded device.</span></span> <span data-ttu-id="96972-109">L’URL de présentation dans le modèle de description de l’appareil peut être une URL absolue ou une URL relative.</span><span class="sxs-lookup"><span data-stu-id="96972-109">The presentation URL in the device description template can either be an absolute URL or a relative URL.</span></span> <span data-ttu-id="96972-110">Pour les URL relatives, qui sont relatives au chemin d’accès de la ressource, le modèle de description de l’appareil doit contenir un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="96972-110">For relative URLs, which are relative to the resource path, the device description template should contain a file name.</span></span> <span data-ttu-id="96972-111">**IUPnPRegistrar** convertit ce en URL avec l’emplacement réel.</span><span class="sxs-lookup"><span data-stu-id="96972-111">**IUPnPRegistrar** converts this to a URL with the actual location.</span></span> <span data-ttu-id="96972-112">Pour les URL absolues, l’emplacement n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="96972-112">For absolute URLs, the location is not modified.</span></span>

<span data-ttu-id="96972-113">Pour prendre en charge les scripts côté client dans une page de présentation, des informations supplémentaires sont généralement ajoutées à l’URL sous la forme d’une « chaîne de requête ».</span><span class="sxs-lookup"><span data-stu-id="96972-113">To support client side scripts within a presentation page, extra information is normally appended to the URL in the form of a "query string".</span></span> <span data-ttu-id="96972-114">Les informations supplémentaires ajoutées sont l’URL du document de description de l’appareil, ainsi que le UDN de l’appareil ou de l’appareil intégré.</span><span class="sxs-lookup"><span data-stu-id="96972-114">The extra information that is appended is the URL to the device description document, and the UDN of the device or embedded device.</span></span> <span data-ttu-id="96972-115">L’URL de description de l’appareil peut être utilisée pour charger un document de description dans le script, puis contrôler l’appareil par le biais de ses services.</span><span class="sxs-lookup"><span data-stu-id="96972-115">The device description URL can be used to load a description document in the script, and then control the device through its services.</span></span> <span data-ttu-id="96972-116">Le UDN est utilisé pour sélectionner un appareil intégré à partir de l’appareil racine.</span><span class="sxs-lookup"><span data-stu-id="96972-116">The UDN is used to select an embedded device from the root device.</span></span>

<span data-ttu-id="96972-117">Le format de l’URL de présentation modifiée est : l’URL de présentation réelle, un point d’interrogation («  ? »), l’URL de description de l’appareil, un signe plus (« + »), le UDN d’appareil.</span><span class="sxs-lookup"><span data-stu-id="96972-117">The format of the modified presentation URL is: the actual presentation URL, a question mark ("?"), the device description URL, a plus sign ("+"), the device UDN.</span></span> <span data-ttu-id="96972-118">Le point d’interrogation indique le début de la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="96972-118">The question mark denotes the start of the query string.</span></span>

<span data-ttu-id="96972-119">Si l’URL de présentation dans le modèle de description de périphérique était une URL absolue et qu’elle contenait déjà un point d’interrogation («  ? »), les informations supplémentaires ne sont pas ajoutées à l’URL de présentation.</span><span class="sxs-lookup"><span data-stu-id="96972-119">If the presentation URL in the device description template was an absolute URL and it already contained a question mark ("?"), then the extra information is not added to the presentation URL.</span></span>



| <span data-ttu-id="96972-120">Description</span><span class="sxs-lookup"><span data-stu-id="96972-120">Description</span></span>                        | <span data-ttu-id="96972-121">URL</span><span class="sxs-lookup"><span data-stu-id="96972-121">URL</span></span>                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96972-122">Dans le modèle de description de l’appareil</span><span class="sxs-lookup"><span data-stu-id="96972-122">In the device description template</span></span> | <span data-ttu-id="96972-123">**presentationURL** MyDevice.html **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="96972-123">**presentationURL** MyDevice.html **/presentationURL**</span></span>                                                                                              |
| <span data-ttu-id="96972-124">Généré par l’hôte d’appareil</span><span class="sxs-lookup"><span data-stu-id="96972-124">Generated by the device host</span></span>       | <span data-ttu-id="96972-125">**presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ...</span><span class="sxs-lookup"><span data-stu-id="96972-125">**presentationURL**https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394…</span></span> <span data-ttu-id="96972-126">+ UDN **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="96972-126">+ UDN **/presentationURL**</span></span> |



 

<span data-ttu-id="96972-127">Un script côté client peut avoir besoin d’extraire l’URL de description de l’appareil à partir de l’URL de présentation pour charger l’objet [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) .</span><span class="sxs-lookup"><span data-stu-id="96972-127">A client-side script may have to extract the device description URL from the presentation URL to load the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) object.</span></span> <span data-ttu-id="96972-128">Pour ce faire, prenez la chaîne de requête et terminez-la au signe plus (« + »).</span><span class="sxs-lookup"><span data-stu-id="96972-128">This is done by taking the query string, and terminating it at the plus sign ("+").</span></span>


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



<span data-ttu-id="96972-129">Dans le cas d’une page de présentation pour un appareil intégré, des tâches supplémentaires sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="96972-129">In the case of a presentation page for an embedded device, some additional work is required.</span></span> <span data-ttu-id="96972-130">Après avoir chargé le [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), le script doit obtenir la collection de périphériques intégrés, puis sélectionner l’appareil qui correspond au UDN dans la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="96972-130">After loading the [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), the script must obtain the collection of embedded devices, then select the device that matches the UDN in the query string.</span></span> <span data-ttu-id="96972-131">Le script suivant montre comment sélectionner l’appareil intégré pour la page de présentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="96972-131">The following script shows how to select the embedded device for the current presentation page.</span></span> <span data-ttu-id="96972-132">Il suppose que LightDesc est déjà chargé.</span><span class="sxs-lookup"><span data-stu-id="96972-132">It assumes LightDesc is already loaded.</span></span>


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




