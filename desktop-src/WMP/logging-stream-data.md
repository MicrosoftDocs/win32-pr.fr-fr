---
title: Journalisation des données de flux
description: Journalisation des données de flux
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Sélections de métafichiers Windows Media, journalisation des données de flux
- sélections, journalisation des données de flux
- sélections de métafichiers, journalisation des données de flux
- Sélections de métafichiers Windows Media, journalisation des données de flux
- sélections, journalisation des données de flux
- sélections de métafichiers, journalisation des données de flux
- journalisation des données de flux
- journalisation des données de flux
- Lecteur Windows Media, journalisation des données de flux
- Lecteur Windows Media, journalisation des données de diffusion en continu
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100813"
---
# <a name="logging-stream-data"></a><span data-ttu-id="0046d-113">Journalisation des données de flux</span><span class="sxs-lookup"><span data-stu-id="0046d-113">Logging Stream Data</span></span>

<span data-ttu-id="0046d-114">Les informations journalisées peuvent être acquises et utilisées pour déterminer le comportement de la visionneuse, par exemple, la fréquence à laquelle un flux est affiché, ou si un utilisateur spécifique a affiché un flux et la durée de la qualité.</span><span class="sxs-lookup"><span data-stu-id="0046d-114">Logged information can be acquired and used to determine viewer behavior, for example, how often a stream is viewed, or if a specific user viewed a stream and for how long at what quality.</span></span>

<span data-ttu-id="0046d-115">Les informations de journalisation sont automatiquement envoyées au serveur d’origine de la sélection.</span><span class="sxs-lookup"><span data-stu-id="0046d-115">Logging information is automatically sent to the server from which the playlist originated.</span></span> <span data-ttu-id="0046d-116">Vous pouvez également envoyer des informations de journalisation à des serveurs supplémentaires, y compris des serveurs Web que vous utilisez exclusivement pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="0046d-116">You can also send logging information to additional servers, including web servers you use exclusively for logging.</span></span> <span data-ttu-id="0046d-117">Pour ce faire, utilisez l’élément **LOGURL** , en spécifiant une URL valide pour l’attribut **href** .</span><span class="sxs-lookup"><span data-stu-id="0046d-117">To do this, use the **LOGURL** element, specifying a valid URL for the **HREF** attribute.</span></span> <span data-ttu-id="0046d-118">Vous pouvez inclure des éléments **LOGURL** comme enfants de l’élément **ASX** et comme enfants d’éléments d' **entrée** individuels.</span><span class="sxs-lookup"><span data-stu-id="0046d-118">You can include **LOGURL** elements as children of the **ASX** element and as children of individual **ENTRY** elements.</span></span> <span data-ttu-id="0046d-119">Lorsque la sélection est ouverte pour la première fois, les informations de journalisation sont envoyées au serveur d’origine et à chaque URL spécifiée dans **LOGURL** Children de l’élément **ASX** .</span><span class="sxs-lookup"><span data-stu-id="0046d-119">When the playlist is first opened, logging information is sent to the origin server and to each URL specified in **LOGURL** children of the **ASX** element.</span></span> <span data-ttu-id="0046d-120">Ensuite, lorsque chaque entrée est atteinte, les informations de journalisation spécifiques à cette entrée sont envoyées à chaque URL spécifiée dans **LOGURL** Children de l’élément **entry** .</span><span class="sxs-lookup"><span data-stu-id="0046d-120">Then, as each entry is reached, logging information specific to that entry is sent to each URL specified in **LOGURL** children of the **ENTRY** element.</span></span>

<span data-ttu-id="0046d-121">Le kit de développement logiciel (SDK) Windows Media format prend en charge l’élément **LOGURL** via l’interface **IWMSReaderNetworkConfig** et les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0046d-121">The Windows Media Format SDK supports the **LOGURL** element through the **IWMSReaderNetworkConfig** interface and the following methods:</span></span>


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



<span data-ttu-id="0046d-122">En plus des informations qui sont journalisées automatiquement, une sélection de métafichiers peut consigner des informations personnalisées à l’aide de l’élément **param** .</span><span class="sxs-lookup"><span data-stu-id="0046d-122">In addition to the information that is automatically logged, a metafile playlist can log custom information through the use of the **PARAM** element.</span></span> <span data-ttu-id="0046d-123">Pour utiliser l’élément **param** de cette manière, définissez l’attribut **Name** sur « log : » suivi d’un nom de champ de journal et d’un espace de noms XML facultatif, séparé du nom de champ par un autre signe deux-points («  : »).</span><span class="sxs-lookup"><span data-stu-id="0046d-123">To use the **PARAM** element in this way, set the **NAME** attribute to "log:" followed by a log field name and an optional XML namespace separated from the field name by another colon (":").</span></span> <span data-ttu-id="0046d-124">Tout ce qui suit le deuxième signe deux-points est traité comme un espace de noms, donc le nom du champ ne doit pas contenir de deux-points.</span><span class="sxs-lookup"><span data-stu-id="0046d-124">Everything after the second colon is treated as a namespace, so the field name should not contain a colon.</span></span>

<span data-ttu-id="0046d-125">Le champ de journal spécifié dans l’attribut **Name** est défini sur la valeur de l’attribut **value** .</span><span class="sxs-lookup"><span data-stu-id="0046d-125">The log field specified in the **NAME** attribute is set to the value of the **VALUE** attribute.</span></span> <span data-ttu-id="0046d-126">Si le journal ne contient pas déjà un champ portant le nom spécifié, il sera ajouté.</span><span class="sxs-lookup"><span data-stu-id="0046d-126">If the log does not already contain a field with the specified name, it will be added.</span></span>

<span data-ttu-id="0046d-127">**Exemple de code**</span><span class="sxs-lookup"><span data-stu-id="0046d-127">**Example Code**</span></span>


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a><span data-ttu-id="0046d-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0046d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0046d-129">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="0046d-129">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0046d-130">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0046d-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




