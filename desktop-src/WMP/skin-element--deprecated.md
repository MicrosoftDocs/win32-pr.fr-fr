---
title: Élément SKIN (déconseillé)
description: Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Élément SKIN (déconseillé) lecteur Windows Media
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537772"
---
# <a name="skin-element-deprecated"></a><span data-ttu-id="a61aa-104">Élément SKIN (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="a61aa-104">SKIN Element (deprecated)</span></span>

<span data-ttu-id="a61aa-105">Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a61aa-105">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="a61aa-106">L’élément **Skin** spécifie une URL vers une bordure.</span><span class="sxs-lookup"><span data-stu-id="a61aa-106">The **SKIN** element specifies a URL to a border.</span></span>

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="a61aa-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="a61aa-107">Attributes</span></span>

<span data-ttu-id="a61aa-108">**Href** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="a61aa-108">**HREF** (required)</span></span>

<span data-ttu-id="a61aa-109">URL d’un fichier de bordure compressé avec l’extension de nom de fichier. WMZ.</span><span class="sxs-lookup"><span data-stu-id="a61aa-109">URL for a compressed border file with a file name extension .wmz.</span></span> <span data-ttu-id="a61aa-110">Pour le lecteur Windows Media série 9 ou version ultérieure, cette valeur peut référencer uniquement les fichiers de bordure sur le disque dur de l’utilisateur situé dans le même répertoire que la sélection de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="a61aa-110">For Windows Media Player 9 Series or later, this value can reference only border files on the user's hard disk located in the same directory as the metafile playlist.</span></span> <span data-ttu-id="a61aa-111">Consultez l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="a61aa-111">See the example code.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="a61aa-112">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="a61aa-112">Parent/Child Elements</span></span>



| <span data-ttu-id="a61aa-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="a61aa-113">Hierarchy</span></span>       | <span data-ttu-id="a61aa-114">Éléments</span><span class="sxs-lookup"><span data-stu-id="a61aa-114">Elements</span></span> |
|-----------------|----------|
| <span data-ttu-id="a61aa-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a61aa-115">Parent elements</span></span> | <span data-ttu-id="a61aa-116">**ASX**</span><span class="sxs-lookup"><span data-stu-id="a61aa-116">**ASX**</span></span>  |
| <span data-ttu-id="a61aa-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a61aa-117">Child elements</span></span>  | <span data-ttu-id="a61aa-118">Aucune</span><span class="sxs-lookup"><span data-stu-id="a61aa-118">None</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="a61aa-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a61aa-119">Remarks</span></span>

<span data-ttu-id="a61aa-120">L’élément **Skin** est utilisé pour créer une bordure, qui est similaire à une apparence, mais qui est affichée dans la zone de **lecture à présent** du lecteur Windows Media en mode complet.</span><span class="sxs-lookup"><span data-stu-id="a61aa-120">The **SKIN** element is used to create a border, which is similar to a skin but is displayed in the **Now Playing** area of the full mode Windows Media Player.</span></span> <span data-ttu-id="a61aa-121">L’élément **Skin** est utilisé uniquement pour les bordures, qui apparaissent dans le lecteur Windows Media en mode complet, et non pour les skins standard, qui remplacent entièrement le mode compact du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a61aa-121">The **SKIN** element is used only for borders, which appear inside the full mode Windows Media Player, and not for regular skins, which entirely replace the compact mode Windows Media Player.</span></span>

<span data-ttu-id="a61aa-122">Dans un package de téléchargement Windows Media (avec l’extension de nom de fichier. WMD), l’élément **Skin** permet à une bordure d’avoir du contenu et d’établir un lien vers d’autres sites.</span><span class="sxs-lookup"><span data-stu-id="a61aa-122">In a Windows Media Download Package (with a .wmd file name extension), the **SKIN** element enables a border to have content and link to other sites.</span></span> <span data-ttu-id="a61aa-123">Le package de téléchargement Windows Media est un fichier compressé qui contient un fichier de bordure et un métafichier Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a61aa-123">The Windows Media Download Package is a compressed file that contains a border file and a Windows Media metafile.</span></span> <span data-ttu-id="a61aa-124">Le fichier de bordure (avec l’extension de nom de fichier. WMZ) est compressé et comprend un fichier de définition d’apparence (avec l’extension de nom de fichier. WMS).</span><span class="sxs-lookup"><span data-stu-id="a61aa-124">The border file (with a .wmz file name extension) is compressed, and includes a skin definition file (with a .wms file name extension).</span></span>

<span data-ttu-id="a61aa-125">Un élément **Skin** a trois composants :</span><span class="sxs-lookup"><span data-stu-id="a61aa-125">A **SKIN** element has three components:</span></span>

-   <span data-ttu-id="a61aa-126">Une apparence</span><span class="sxs-lookup"><span data-stu-id="a61aa-126">A skin</span></span>
-   <span data-ttu-id="a61aa-127">Du contenu</span><span class="sxs-lookup"><span data-stu-id="a61aa-127">Some content</span></span>
-   <span data-ttu-id="a61aa-128">Un métafichier</span><span class="sxs-lookup"><span data-stu-id="a61aa-128">A metafile</span></span>

<span data-ttu-id="a61aa-129">Les habillages fournis avec les packages de téléchargement Windows Media doivent être de forme rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="a61aa-129">Skins included with Windows Media Download Packages must be rectangular in shape.</span></span> <span data-ttu-id="a61aa-130">La création de bordures avec des apparences qui ne sont pas rectangulaires peut produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="a61aa-130">Creating borders with skins that are not rectangular may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="a61aa-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="a61aa-131">Examples</span></span>


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a><span data-ttu-id="a61aa-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a61aa-132">Requirements</span></span>



| <span data-ttu-id="a61aa-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a61aa-133">Requirement</span></span> | <span data-ttu-id="a61aa-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a61aa-134">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="a61aa-135">Version</span><span class="sxs-lookup"><span data-stu-id="a61aa-135">Version</span></span><br/> | <span data-ttu-id="a61aa-136">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="a61aa-136">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a61aa-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a61aa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a61aa-138">**Bordures du lecteur Windows Media (déconseillée)**</span><span class="sxs-lookup"><span data-stu-id="a61aa-138">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="a61aa-139">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a61aa-139">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="a61aa-140">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a61aa-140">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





