---
title: Élément LOGURL
description: L’élément LOGURL indique au lecteur Windows Media de soumettre toutes les données de journal à l’URL spécifiée.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Élément LOGURL lecteur Windows Media
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526072"
---
# <a name="logurl-element"></a><span data-ttu-id="a8cbd-104">Élément LOGURL</span><span class="sxs-lookup"><span data-stu-id="a8cbd-104">LOGURL Element</span></span>

<span data-ttu-id="a8cbd-105">L’élément **LOGURL** indique au lecteur Windows Media de soumettre toutes les données de journal à l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-105">The **LOGURL** element instructs Windows Media Player to submit any log data to the specified URL.</span></span>

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="a8cbd-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="a8cbd-106">Attributes</span></span>

<span data-ttu-id="a8cbd-107">**Href** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="a8cbd-107">**HREF** (required)</span></span>

<span data-ttu-id="a8cbd-108">URL d’un hôte capable de traiter les demandes de journalisation.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-108">URL to a host that is able to process logging requests.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="a8cbd-109">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="a8cbd-109">Parent/Child Elements</span></span>



| <span data-ttu-id="a8cbd-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="a8cbd-110">Hierarchy</span></span>       | <span data-ttu-id="a8cbd-111">Éléments</span><span class="sxs-lookup"><span data-stu-id="a8cbd-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="a8cbd-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a8cbd-112">Parent elements</span></span> | <span data-ttu-id="a8cbd-113">**ASX**, **entrée**</span><span class="sxs-lookup"><span data-stu-id="a8cbd-113">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="a8cbd-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8cbd-114">Child elements</span></span>  | <span data-ttu-id="a8cbd-115">Aucune</span><span class="sxs-lookup"><span data-stu-id="a8cbd-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="a8cbd-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a8cbd-116">Remarks</span></span>

<span data-ttu-id="a8cbd-117">L’élément **LOGURL** permet à une sélection de métafichier client d’envoyer des informations de journalisation supplémentaires à des serveurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-117">The **LOGURL** element enables a client metafile playlist to send additional logging information to specified servers.</span></span> <span data-ttu-id="a8cbd-118">Les informations de journalisation sont automatiquement envoyées au serveur d’origine d’une sélection quand elle est ouverte et à chaque **LOGURL** spécifié pour l’élément **ASX** , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-118">Logging information is automatically sent to the origin server of a playlist when it is opened and to each **LOGURL** specified for the **ASX** element, if any are present.</span></span> <span data-ttu-id="a8cbd-119">Les informations de journalisation sont également envoyées à chaque **LOGURL** spécifié pour un élément d' **entrée** lorsque cette entrée est atteinte.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-119">Logging information is also sent to each **LOGURL** specified for an **ENTRY** element when that entry is reached.</span></span> <span data-ttu-id="a8cbd-120">L’URL spécifiée dans l’attribut **href** d’un élément **LOGURL** doit être l’adresse d’un hôte qui est en mesure de traiter les demandes de journalisation.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-120">The URL specified in the **HREF** attribute of a **LOGURL** element must be the address of a host that is able to process logging requests.</span></span> <span data-ttu-id="a8cbd-121">L’URL peut être n’importe quelle URL HTTP valide.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-121">The URL can be any valid HTTP URL.</span></span> <span data-ttu-id="a8cbd-122">L’URL peut également indiquer l’emplacement d’un script CGI.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-122">The URL can also indicate the location of a CGI script.</span></span>

<span data-ttu-id="a8cbd-123">Les seuls protocoles valides pour un élément **LOGURL** sont HTTP et HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-123">The only valid protocols for a **LOGURL** element are HTTP and HTTPS.</span></span>

<span data-ttu-id="a8cbd-124">Un élément **LOGURL** dans la portée d’un élément **ASX** est uniquement applicable au métafichier dans lequel il réside, que ce métafichier soit référencé ou non à partir d’un autre métafichier.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-124">A **LOGURL** element within the scope of an **ASX** element is applicable only to the metafile in which it resides, regardless of whether that metafile is referenced from another metafile.</span></span> <span data-ttu-id="a8cbd-125">Un élément **LOGURL** force l’envoi de données de journal pour tout le contenu diffusé en continu à partir de son étendue définie et uniquement pour le contenu diffusé en continu à partir de son étendue définie.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-125">A **LOGURL** element forces the submission of log data for all content streamed from within its defined scope and only for content streamed from within its defined scope.</span></span> <span data-ttu-id="a8cbd-126">Les données de journal sont envoyées au serveur d’origine et à toutes les URL listées dans chaque élément **LOGURL** de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-126">Log data will be submitted to the origin server and to all URLs listed in every **LOGURL** element in scope.</span></span> <span data-ttu-id="a8cbd-127">Les données de journal ne sont envoyées qu’une seule fois à chaque URL de la liste, même si la même URL est listée plusieurs fois dans une étendue donnée.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-127">Log data will be submitted only once to each listed URL, even if the same URL is listed more than once in a given scope.</span></span> <span data-ttu-id="a8cbd-128">La répétition d’une **entrée** entraînerait une autre soumission aux URL listées.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-128">A repeat of an **ENTRY** would result in another submission to the listed URLs.</span></span>

<span data-ttu-id="a8cbd-129">Il n’existe aucune limite quant au nombre d’éléments **LOGURL** dans une sélection de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-129">There is no limit to the number of **LOGURL** elements in a metafile playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="a8cbd-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="a8cbd-130">Examples</span></span>


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



<span data-ttu-id="a8cbd-131">Voici des exemples d’URL valides.</span><span class="sxs-lookup"><span data-stu-id="a8cbd-131">The following are examples of valid URLs.</span></span>

<span data-ttu-id="a8cbd-132">URL d’une application ISAPI :</span><span class="sxs-lookup"><span data-stu-id="a8cbd-132">URL of an ISAPI application:</span></span>


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



<span data-ttu-id="a8cbd-133">URL d’un script CGI :</span><span class="sxs-lookup"><span data-stu-id="a8cbd-133">URL of a CGI script:</span></span>


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



<span data-ttu-id="a8cbd-134">Une URL HTTP valide :</span><span class="sxs-lookup"><span data-stu-id="a8cbd-134">A valid HTTP URL:</span></span>


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a><span data-ttu-id="a8cbd-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8cbd-135">Requirements</span></span>



| <span data-ttu-id="a8cbd-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8cbd-136">Requirement</span></span> | <span data-ttu-id="a8cbd-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8cbd-137">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="a8cbd-138">Version</span><span class="sxs-lookup"><span data-stu-id="a8cbd-138">Version</span></span><br/> | <span data-ttu-id="a8cbd-139">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="a8cbd-139">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8cbd-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8cbd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8cbd-141">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a8cbd-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="a8cbd-142">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a8cbd-142">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





