---
title: Élément REF
description: L’élément REF spécifie une URL pour le contenu multimédia numérique.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Élément REF lecteur Windows Media
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528098"
---
# <a name="ref-element"></a><span data-ttu-id="472e4-104">Élément REF</span><span class="sxs-lookup"><span data-stu-id="472e4-104">REF Element</span></span>

<span data-ttu-id="472e4-105">L’élément **ref** spécifie une URL pour le contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="472e4-105">The **REF** element specifies a URL for digital media content.</span></span>

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a><span data-ttu-id="472e4-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="472e4-106">Attributes</span></span>

<span data-ttu-id="472e4-107">**Href** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="472e4-107">**HREF** (required)</span></span>

<span data-ttu-id="472e4-108">URL d’un contenu multimédia pris en charge par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="472e4-108">URL to any piece of media content supported by Windows Media Player.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="472e4-109">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="472e4-109">Parent/Child Elements</span></span>



| <span data-ttu-id="472e4-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="472e4-110">Hierarchy</span></span>       | <span data-ttu-id="472e4-111">Éléments</span><span class="sxs-lookup"><span data-stu-id="472e4-111">Elements</span></span>                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="472e4-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="472e4-112">Parent elements</span></span> | <span data-ttu-id="472e4-113">**MENTION**</span><span class="sxs-lookup"><span data-stu-id="472e4-113">**ENTRY**</span></span>                                                                        |
| <span data-ttu-id="472e4-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="472e4-114">Child elements</span></span>  | <span data-ttu-id="472e4-115">**Duration**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **StartTime**</span><span class="sxs-lookup"><span data-stu-id="472e4-115">**DURATION**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="472e4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="472e4-116">Remarks</span></span>

<span data-ttu-id="472e4-117">Cet élément spécifie une URL pour un élément de contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="472e4-117">This element specifies a URL for a piece of media content.</span></span> <span data-ttu-id="472e4-118">L’URL peut pointer vers n’importe quel type de média pris en charge, à l’aide de n’importe quel protocole pris en charge par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="472e4-118">The URL can point to any media type supported, using any protocol supported by Windows Media Player.</span></span>

<span data-ttu-id="472e4-119">Les types de médias pris en charge incluent des images fixes, telles que des images. gif et. jpg et des fichiers Flash, avec l’extension de nom de fichier. swf.</span><span class="sxs-lookup"><span data-stu-id="472e4-119">The media types supported include still images such as .gif and .jpg images and Flash files with an .swf file name extension.</span></span> <span data-ttu-id="472e4-120">Ces types de médias sont utiles pour inclure du contenu publicitaire dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="472e4-120">These media types are useful for including advertising content within a playlist.</span></span> <span data-ttu-id="472e4-121">Avec les fichiers image et les fichiers Flash qui s’exécutent dans une boucle, vous devez également spécifier la durée d’affichage de l’élément multimédia en incluant un élément **Duration** dans l’élément **ref** .</span><span class="sxs-lookup"><span data-stu-id="472e4-121">With image files and Flash files that play in a loop, you must also specify the amount of time to display the media item by including a **DURATION** element within the **REF** element.</span></span> <span data-ttu-id="472e4-122">Si vous souhaitez qu’une image continue à s’afficher pendant que l’entrée suivante dans la playlist est mise en mémoire tampon, incluez un élément **param** dans l’élément **entry** , affectez à son attribut **Name** la valeur ShowWhileBuffering et affectez à son attribut **value la valeur** true.</span><span class="sxs-lookup"><span data-stu-id="472e4-122">If you want an image to continue displaying while the next entry in the playlist is buffered, include a **PARAM** element within the **ENTRY** element, set its **name** attribute to ShowWhileBuffering, and set its **value** attribute to true.</span></span>

<span data-ttu-id="472e4-123">Pour référencer du contenu sur un CD ou un DVD qui l’autorise, les protocoles wmpcd et wmpdvd sont fournis.</span><span class="sxs-lookup"><span data-stu-id="472e4-123">To reference content on a CD or a DVD that allows it, the wmpcd and wmpdvd protocols are provided.</span></span> <span data-ttu-id="472e4-124">Par exemple, si vous affectez à l’attribut **href** la valeur « wmpdvd://f/5/3 », le chapitre 3 du titre 5 est lu sur un DVD, mais uniquement si le DVD a été créé pour l’autoriser.</span><span class="sxs-lookup"><span data-stu-id="472e4-124">For example, setting the **HREF** attribute to "wmpdvd://f/5/3" will play chapter 3 of title 5 on a DVD, but only if the DVD has been authored to allow it.</span></span>

<span data-ttu-id="472e4-125">Les applications qui ouvrent des médias numériques derrière un pare-feu bénéficient de meilleures performances lors de l’ouverture des éléments multimédias si l’adresse est spécifiée à l’aide du nom DNS (Domain Name Server) au lieu de l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="472e4-125">Applications that open digital media from behind a firewall will have better performance when opening the media items if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="472e4-126">L’utilisation la plus courante de cet élément est la substitution d’URL.</span><span class="sxs-lookup"><span data-stu-id="472e4-126">The most common use of this element is for URL rollover.</span></span> <span data-ttu-id="472e4-127">Si le lecteur Windows Media ne parvient pas à ouvrir un élément multimédia défini dans un élément **ref** , il essaie l’URL dans l’élément **ref** suivant.</span><span class="sxs-lookup"><span data-stu-id="472e4-127">If Windows Media Player is unable to open a piece of media defined in a **REF** element, it tries the URL in the next **REF** element.</span></span> <span data-ttu-id="472e4-128">Une fois que le lecteur Windows Media a ouvert le contenu multimédia à partir d’une URL définie dans l’étendue d’un élément d' **entrée** , il ignore les balises **ref** suivantes dans cet élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="472e4-128">Once Windows Media Player opens media content from a URL defined within the scope of one **ENTRY** element, it ignores subsequent **REF** tags within that **ENTRY** element.</span></span> <span data-ttu-id="472e4-129">À la fin de la lecture de la partie de contenu, le lecteur Windows Media passe à l’élément d' **entrée** suivant, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="472e4-129">After the piece of content is done playing, Windows Media Player moves on to the next **ENTRY** element, if any.</span></span>

-   <span data-ttu-id="472e4-130">**Important** Une fois que le lecteur Windows Media a établi une connexion à un élément de contenu référencé, il ignore tous les autres éléments **ref** de cette **entrée**, que la connexion se termine normalement ou anormalement.</span><span class="sxs-lookup"><span data-stu-id="472e4-130">**Important** Once Windows Media Player establishes a connection to a referenced piece of content, it ignores all other **REF** elements in that **ENTRY**, whether the connection terminates normally or abnormally.</span></span>

<span data-ttu-id="472e4-131">Si l’élément multimédia référencé est un fichier image, l’élément **Duration** doit être utilisé pour spécifier l’heure d’affichage de l’image.</span><span class="sxs-lookup"><span data-stu-id="472e4-131">If the media item referenced is an image file, the **DURATION** element must be used to specify the display time for the image.</span></span>

<span data-ttu-id="472e4-132">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="472e4-132">**Note**</span></span>

<span data-ttu-id="472e4-133">Toute tentative de lecture d’un média Flash qui comprend du son avec le premier frame peut produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="472e4-133">Attempting to play Flash media that includes sound with the first frame may yield unexpected results.</span></span> <span data-ttu-id="472e4-134">Vous devez créer un contenu Flash pour qu’il émette un son commençant à ne pas être antérieur à la deuxième image.</span><span class="sxs-lookup"><span data-stu-id="472e4-134">You should author Flash content to play sound starting no earlier than the second frame.</span></span>

## <a name="examples"></a><span data-ttu-id="472e4-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="472e4-135">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="472e4-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="472e4-136">Requirements</span></span>



| <span data-ttu-id="472e4-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="472e4-137">Requirement</span></span> | <span data-ttu-id="472e4-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="472e4-138">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="472e4-139">Version</span><span class="sxs-lookup"><span data-stu-id="472e4-139">Version</span></span><br/> | <span data-ttu-id="472e4-140">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="472e4-140">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="472e4-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="472e4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472e4-142">**Protocoles et types de fichiers pris en charge**</span><span class="sxs-lookup"><span data-stu-id="472e4-142">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> <dt>

[<span data-ttu-id="472e4-143">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="472e4-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="472e4-144">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="472e4-144">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





