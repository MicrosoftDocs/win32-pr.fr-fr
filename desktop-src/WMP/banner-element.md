---
title: Élément BANNER
description: L’élément BANNER définit une URL vers un fichier graphique qui s’affiche dans le panneau d’affichage.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Élément de bannière lecteur Windows Media
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543873"
---
# <a name="banner-element"></a><span data-ttu-id="888d9-104">Élément BANNER</span><span class="sxs-lookup"><span data-stu-id="888d9-104">BANNER Element</span></span>

<span data-ttu-id="888d9-105">L’élément **Banner** définit une URL vers un fichier graphique qui s’affiche dans le panneau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="888d9-105">The **BANNER** element defines a URL to a graphic file that will appear in the display panel.</span></span>

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a><span data-ttu-id="888d9-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="888d9-106">Attributes</span></span>

<span data-ttu-id="888d9-107">**Href** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="888d9-107">**HREF** (required)</span></span>

<span data-ttu-id="888d9-108">URL d’un fichier graphique affiché dans le panneau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="888d9-108">URL to a graphic file that is displayed in the display panel.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="888d9-109">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="888d9-109">Parent/Child Elements</span></span>



| <span data-ttu-id="888d9-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="888d9-110">Hierarchy</span></span>       | <span data-ttu-id="888d9-111">Éléments</span><span class="sxs-lookup"><span data-stu-id="888d9-111">Elements</span></span>                   |
|-----------------|----------------------------|
| <span data-ttu-id="888d9-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="888d9-112">Parent elements</span></span> | <span data-ttu-id="888d9-113">**ASX**, **entrée**</span><span class="sxs-lookup"><span data-stu-id="888d9-113">**ASX**, **ENTRY**</span></span>         |
| <span data-ttu-id="888d9-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="888d9-114">Child elements</span></span>  | <span data-ttu-id="888d9-115">**abstract**, **moreinfo**</span><span class="sxs-lookup"><span data-stu-id="888d9-115">**ABSTRACT**, **MOREINFO**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="888d9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="888d9-116">Remarks</span></span>

<span data-ttu-id="888d9-117">Cet élément définit une URL vers un fichier graphique qui s’affiche dans le panneau d’affichage du lecteur Windows Media, sous le contenu de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="888d9-117">This element defines a URL to a graphic file that appears in the Windows Media Player display panel, beneath the video content.</span></span> <span data-ttu-id="888d9-118">Si le support est uniquement audio, le graphique de bannière s’affiche de lui-même.</span><span class="sxs-lookup"><span data-stu-id="888d9-118">If the media is audio only, the banner graphic is displayed by itself.</span></span> <span data-ttu-id="888d9-119">Le lecteur Windows Media réserve un espace de 32 pixels de haut en 194 pixels de large (la barre de bannière) du graphique.</span><span class="sxs-lookup"><span data-stu-id="888d9-119">Windows Media Player reserves a space 32 pixels high by 194 pixels wide (the banner bar) for the graphic.</span></span> <span data-ttu-id="888d9-120">Si le graphique défini dans l’URL est plus petit, il s’affiche à sa taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="888d9-120">If the graphic defined in the URL is smaller than that, it displays at its original size.</span></span> <span data-ttu-id="888d9-121">Si le graphique est plus grand que l’espace réservé, le lecteur Windows Media rogne l’image pour l’ajuster à l’espace.</span><span class="sxs-lookup"><span data-stu-id="888d9-121">If the graphic is larger than the reserved space, Windows Media Player will crop the image to fit the space.</span></span>

<span data-ttu-id="888d9-122">Vous pouvez utiliser un élément **abstrait** dans la portée de l’élément **bannière** pour afficher du texte sous la forme d’une info-bulle lorsque l’utilisateur place le pointeur de la souris sur le graphique de la bannière.</span><span class="sxs-lookup"><span data-stu-id="888d9-122">You can use an **ABSTRACT** element within the scope of the **BANNER** element to display text as a ToolTip when the user pauses the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="888d9-123">Un élément **moreinfo** dans un élément **Banner** définit une URL vers laquelle l’utilisateur est tenu quand l’utilisateur clique sur le graphique de bannière.</span><span class="sxs-lookup"><span data-stu-id="888d9-123">A **MOREINFO** element within a **BANNER** element defines a URL to which the user is taken when the user clicks the banner graphic.</span></span> <span data-ttu-id="888d9-124">(L’URL peut être n’importe quel chemin d’accès ou protocole, tel qu’un lien de messagerie électronique, une URL HTTP (Hypertext Transfer Protocol) vers un site Web ou même une commande Microsoft JScript.) Lorsque le pointeur est déplacé au-dessus du graphique, le graphique est gaufré et ressemble à un bouton.</span><span class="sxs-lookup"><span data-stu-id="888d9-124">(The URL can be any path or protocol, such as an email link, a Hypertext Transfer Protocol (HTTP) URL to a website, or even a Microsoft JScript command.) When the pointer is moved over the graphic, the graphic becomes embossed and looks like a button.</span></span>

<span data-ttu-id="888d9-125">Un élément de **bannière** défini pour un élément **ASX** s’affiche pendant la lecture de tous les clips de la playlist.</span><span class="sxs-lookup"><span data-stu-id="888d9-125">A **BANNER** element defined for an **ASX** element displays while all clips in the playlist are playing.</span></span> <span data-ttu-id="888d9-126">Un élément **Banner** défini dans un élément **entry** s’affiche uniquement lors de la diffusion de ce clip et, pendant cette période, remplace les bannières définies dans l’élément **ASX** parent.</span><span class="sxs-lookup"><span data-stu-id="888d9-126">A **BANNER** element defined in an **ENTRY** element displays only while that clip is playing, and during that time overrides any banner defined within the parent **ASX** element.</span></span> <span data-ttu-id="888d9-127">Vous pouvez spécifier la façon dont le lecteur Windows Media réserve de l’espace pour la bannière en définissant l’attribut **BANNERBAR** de l’élément **ASX** .</span><span class="sxs-lookup"><span data-stu-id="888d9-127">You can specify how Windows Media Player reserves space for the banner by setting the **BANNERBAR** attribute of the **ASX** element.</span></span>

<span data-ttu-id="888d9-128">Les images de bannière ne sont pas prises en charge avec les fichiers DRM ou lorsque le lecteur Windows Media est incorporé dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="888d9-128">Banner images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

## <a name="examples"></a><span data-ttu-id="888d9-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="888d9-129">Examples</span></span>

<span data-ttu-id="888d9-130">Voici un exemple d’élément **Banner** sans éléments enfants :</span><span class="sxs-lookup"><span data-stu-id="888d9-130">The following is an example of a **BANNER** element without child elements:</span></span>


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



<span data-ttu-id="888d9-131">Voici un exemple d’élément **Banner** contenant des éléments **abstract** et **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="888d9-131">The following is an example of a **BANNER** element containing **ABSTRACT** and **MOREINFO** elements.</span></span>


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a><span data-ttu-id="888d9-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="888d9-132">Requirements</span></span>



| <span data-ttu-id="888d9-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="888d9-133">Requirement</span></span> | <span data-ttu-id="888d9-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="888d9-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="888d9-135">Version</span><span class="sxs-lookup"><span data-stu-id="888d9-135">Version</span></span><br/> | <span data-ttu-id="888d9-136">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="888d9-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="888d9-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="888d9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888d9-138">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="888d9-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="888d9-139">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="888d9-139">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





