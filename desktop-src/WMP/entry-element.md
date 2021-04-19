---
title: Élément ENTRy
description: L’élément ENTRy spécifie un fichier Windows Media à afficher sous forme de clip.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Élément d’entrée Windows Media Player
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537686"
---
# <a name="entry-element"></a><span data-ttu-id="493b1-104">Élément ENTRy</span><span class="sxs-lookup"><span data-stu-id="493b1-104">ENTRY Element</span></span>

<span data-ttu-id="493b1-105">L’élément **entry** spécifie un fichier Windows Media à afficher sous forme de clip.</span><span class="sxs-lookup"><span data-stu-id="493b1-105">The **ENTRY** element specifies a Windows Media file to render as a clip.</span></span>

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a><span data-ttu-id="493b1-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="493b1-106">Attributes</span></span>

<span data-ttu-id="493b1-107">**CLIENTSKIP**</span><span class="sxs-lookup"><span data-stu-id="493b1-107">**CLIENTSKIP**</span></span>

<span data-ttu-id="493b1-108">Valeur indiquant si l’utilisateur peut avancer au-delà du clip.</span><span class="sxs-lookup"><span data-stu-id="493b1-108">Value indicating whether the user can skip forward past the clip.</span></span>

<span data-ttu-id="493b1-109">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="493b1-109">Possible values include the following.</span></span>



| <span data-ttu-id="493b1-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="493b1-110">Value</span></span> | <span data-ttu-id="493b1-111">Description</span><span class="sxs-lookup"><span data-stu-id="493b1-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="493b1-112">YES</span><span class="sxs-lookup"><span data-stu-id="493b1-112">YES</span></span>   | <span data-ttu-id="493b1-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="493b1-113">Default.</span></span> <span data-ttu-id="493b1-114">L’utilisateur peut avancer au-delà du clip.</span><span class="sxs-lookup"><span data-stu-id="493b1-114">User can skip forward past the clip.</span></span> |
| <span data-ttu-id="493b1-115">Non</span><span class="sxs-lookup"><span data-stu-id="493b1-115">NO</span></span>    | <span data-ttu-id="493b1-116">L’utilisateur ne peut pas avancer au-delà du clip.</span><span class="sxs-lookup"><span data-stu-id="493b1-116">User cannot skip forward past the clip.</span></span>       |



 

<span data-ttu-id="493b1-117">**SKIPIFREF**</span><span class="sxs-lookup"><span data-stu-id="493b1-117">**SKIPIFREF**</span></span>

<span data-ttu-id="493b1-118">Valeur indiquant si le lecteur Windows Media doit ignorer ce clip lorsque l’élément d' **entrée** est inclus dans un deuxième métafichier par le biais de l’utilisation d’un élément **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="493b1-118">Value indicating whether Windows Media Player should skip this clip when the **ENTRY** element is included in a second metafile through the use of an **ENTRYREF** element.</span></span>

<span data-ttu-id="493b1-119">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="493b1-119">Possible values include the following.</span></span>



| <span data-ttu-id="493b1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="493b1-120">Value</span></span> | <span data-ttu-id="493b1-121">Description</span><span class="sxs-lookup"><span data-stu-id="493b1-121">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="493b1-122">YES</span><span class="sxs-lookup"><span data-stu-id="493b1-122">YES</span></span>   | <span data-ttu-id="493b1-123">Le lecteur Windows Media ignore cette entrée, si elle est référencée par l’intermédiaire d’un élément **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="493b1-123">Windows Media Player will ignore this entry, if referenced through an **ENTRYREF** element.</span></span> |
| <span data-ttu-id="493b1-124">Non</span><span class="sxs-lookup"><span data-stu-id="493b1-124">NO</span></span>    | <span data-ttu-id="493b1-125">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="493b1-125">Default.</span></span> <span data-ttu-id="493b1-126">Le lecteur Windows Media n’ignore pas cette entrée.</span><span class="sxs-lookup"><span data-stu-id="493b1-126">Windows Media Player will not ignore this entry.</span></span>                                   |



 

## <a name="parentchild-elements"></a><span data-ttu-id="493b1-127">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="493b1-127">Parent/Child Elements</span></span>



| <span data-ttu-id="493b1-128">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="493b1-128">Hierarchy</span></span>       | <span data-ttu-id="493b1-129">Éléments</span><span class="sxs-lookup"><span data-stu-id="493b1-129">Elements</span></span>                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="493b1-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="493b1-130">Parent elements</span></span> | <span data-ttu-id="493b1-131">**ASX**, **événement**, **répéter**</span><span class="sxs-lookup"><span data-stu-id="493b1-131">**ASX**, **EVENT**, **REPEAT**</span></span>                                                                                                                                                               |
| <span data-ttu-id="493b1-132">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="493b1-132">Child elements</span></span>  | <span data-ttu-id="493b1-133">**abstrait**, **auteur**, **bannière**, **base**, **Copyright**, **Duration**, **ENDMARKER**, **moreinfo**, **param**, **PREVIEWDURATION**, **ref**, **STARTMARKER**, **StartTime**, **title**</span><span class="sxs-lookup"><span data-stu-id="493b1-133">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **DURATION**, **ENDMARKER**, **MOREINFO**, **PARAM**, **PREVIEWDURATION**, **REF**, **STARTMARKER**, **STARTTIME**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="493b1-134">Notes</span><span class="sxs-lookup"><span data-stu-id="493b1-134">Remarks</span></span>

<span data-ttu-id="493b1-135">Cet élément est la construction fondamentale dans un métafichier Windows Media.</span><span class="sxs-lookup"><span data-stu-id="493b1-135">This element is the fundamental construct in a Windows Media metafile.</span></span> <span data-ttu-id="493b1-136">L’élément **entry** et ses attributs associés définissent des méta-informations pour une seule pièce logique de contenu, appelée clip.</span><span class="sxs-lookup"><span data-stu-id="493b1-136">The **ENTRY** element and its associated attributes define meta-information for a single, logical piece of content, called a clip.</span></span> <span data-ttu-id="493b1-137">Les éléments enfants dans la portée d’un élément d' **entrée** définissent le contenu multimédia pour que le lecteur Windows Media ouvre (**ref**), des informations sur le clip que le lecteur Windows Media affiche sous forme de texte (**auteur**, **Copyright**, **titre**) et d’autres paramètres liés au clip.</span><span class="sxs-lookup"><span data-stu-id="493b1-137">Child elements within the scope of an **ENTRY** element define media content for Windows Media Player to open (**REF**), information about the clip that Windows Media Player will display as text (**AUTHOR**, **COPYRIGHT**, **TITLE**), and other settings related to the clip.</span></span> <span data-ttu-id="493b1-138">L’élément enfant **ref** lie le contenu à diffuser en continu pour l’élément d' **entrée** parent.</span><span class="sxs-lookup"><span data-stu-id="493b1-138">The **REF** child element links the content to be streamed for the parent **ENTRY** element.</span></span> <span data-ttu-id="493b1-139">Bien que le script ne s’arrête pas, l' **entrée** n’a pas de sens sans un enfant **ref** .</span><span class="sxs-lookup"><span data-stu-id="493b1-139">Though the script will not break, the **ENTRY** is meaningless without a **REF** child.</span></span>

<span data-ttu-id="493b1-140">Si la valeur de l’attribut **CLIENTSKIP** est non, l’utilisateur ne peut pas avancer au-delà de la partie de contenu définie par l’élément **entry** .</span><span class="sxs-lookup"><span data-stu-id="493b1-140">If the value of the **CLIENTSKIP** attribute is NO, the user cannot skip forward past the piece of content defined by the **ENTRY** element.</span></span> <span data-ttu-id="493b1-141">Cela ne fonctionne pas si l’élément **ref** enfant fait référence à un autre métafichier.</span><span class="sxs-lookup"><span data-stu-id="493b1-141">This does not work if the child **REF** element references another metafile.</span></span> <span data-ttu-id="493b1-142">Les sous-fichiers imbriqués doivent être référencés à l’aide de l’élément **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="493b1-142">Nested metafiles should be referenced using the **ENTRYREF** element.</span></span>

<span data-ttu-id="493b1-143">L’attribut **SKIPIFREF** se rapporte uniquement aux éléments d' **entrée** inclus dans un deuxième métafichier par le biais de l’utilisation d’un élément **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="493b1-143">The **SKIPIFREF** attribute pertains only to **ENTRY** elements that are included in a second metafile through the use of an **ENTRYREF** element.</span></span> <span data-ttu-id="493b1-144">L’élément **ENTRYREF** référence un autre métafichier pour l’inclusion logique dans le fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="493b1-144">The **ENTRYREF** element references another metafile for logical inclusion in the current file.</span></span> <span data-ttu-id="493b1-145">Si la valeur de l’attribut **SKIPIFREF** pour un élément d' **entrée** du fichier de métafichier référencé est oui, le lecteur Windows Media ignore cette entrée extraite et passe à l’élément d' **entrée** suivant, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="493b1-145">If the value of the **SKIPIFREF** attribute for an **ENTRY** element from the referenced metafile file is YES, Windows Media Player ignores this pulled-in entry, and moves on to the next **ENTRY** element, if any.</span></span> <span data-ttu-id="493b1-146">L’élément d' **entrée** suivant peut être l’entrée suivante dans le fichier d’origine, ou l’entrée suivante dans le métafichier référencé dans l’élément **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="493b1-146">The next **ENTRY** element can be the next entry in the original file, or the next entry in the metafile referenced in the **ENTRYREF** element.</span></span>

## <a name="examples"></a><span data-ttu-id="493b1-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="493b1-147">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="493b1-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="493b1-148">Requirements</span></span>



| <span data-ttu-id="493b1-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="493b1-149">Requirement</span></span> | <span data-ttu-id="493b1-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="493b1-150">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="493b1-151">Version</span><span class="sxs-lookup"><span data-stu-id="493b1-151">Version</span></span><br/> | <span data-ttu-id="493b1-152">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="493b1-152">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="493b1-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="493b1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="493b1-154">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="493b1-154">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="493b1-155">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="493b1-155">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





