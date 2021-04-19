---
title: Élément ENTRYREF
description: L’élément ENTRYREF pointe vers les éléments d’entrée dans un métafichier externe.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Élément ENTRYREF lecteur Windows Media
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520815"
---
# <a name="entryref-element"></a><span data-ttu-id="731e1-104">Élément ENTRYREF</span><span class="sxs-lookup"><span data-stu-id="731e1-104">ENTRYREF Element</span></span>

<span data-ttu-id="731e1-105">L’élément **ENTRYREF** pointe vers les éléments d' **entrée** dans un métafichier externe.</span><span class="sxs-lookup"><span data-stu-id="731e1-105">The **ENTRYREF** element points to the **ENTRY** elements in an external metafile.</span></span>

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="731e1-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="731e1-106">Attributes</span></span>

<span data-ttu-id="731e1-107">**Href** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="731e1-107">**HREF** (required)</span></span>

<span data-ttu-id="731e1-108">URL d’un métafichier référencé.</span><span class="sxs-lookup"><span data-stu-id="731e1-108">URL to a referenced metafile.</span></span>

<span data-ttu-id="731e1-109">**CLIENTBIND**</span><span class="sxs-lookup"><span data-stu-id="731e1-109">**CLIENTBIND**</span></span>

<span data-ttu-id="731e1-110">Cet attribut n'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="731e1-110">This attribute is no longer supported.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="731e1-111">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="731e1-111">Parent/Child Elements</span></span>



| <span data-ttu-id="731e1-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="731e1-112">Hierarchy</span></span>       | <span data-ttu-id="731e1-113">Éléments</span><span class="sxs-lookup"><span data-stu-id="731e1-113">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="731e1-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="731e1-114">Parent elements</span></span> | <span data-ttu-id="731e1-115">**ASX**, **événement**, **répéter**</span><span class="sxs-lookup"><span data-stu-id="731e1-115">**ASX**, **EVENT**, **REPEAT**</span></span> |
| <span data-ttu-id="731e1-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="731e1-116">Child elements</span></span>  | <span data-ttu-id="731e1-117">Aucune</span><span class="sxs-lookup"><span data-stu-id="731e1-117">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="731e1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="731e1-118">Remarks</span></span>

<span data-ttu-id="731e1-119">Cet élément pointe vers le contenu d’un métafichier externe.</span><span class="sxs-lookup"><span data-stu-id="731e1-119">This element points to the contents of an external metafile.</span></span> <span data-ttu-id="731e1-120">Le lecteur Windows Media traite les éléments d' **entrée** du métafichier référencé comme s’ils étaient inclus dans le métafichier principal à la position de l’élément **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="731e1-120">Windows Media Player processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="731e1-121">Toutefois, elle ignore tous les éléments d' **entrée** dans le métafichier référencé dont l’attribut **SKIPIFREF** a la valeur Yes.</span><span class="sxs-lookup"><span data-stu-id="731e1-121">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="731e1-122">Le lecteur Windows Media 7,0, 7,1 et le lecteur Windows Media pour Windows XP ignorent tous les éléments **ENTRYREF** dans le métafichier référencé.</span><span class="sxs-lookup"><span data-stu-id="731e1-122">Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="731e1-123">Par conséquent, les fichiers de conversions peuvent être imbriqués un niveau de profondeur uniquement lors de l’utilisation de ces versions du lecteur.</span><span class="sxs-lookup"><span data-stu-id="731e1-123">Thus, metafiles can only be nested one level deep when using these versions of the Player.</span></span> <span data-ttu-id="731e1-124">Le lecteur Windows Media ignore également l’élément **ASX** dans le fichier référencé avec ses attributs.</span><span class="sxs-lookup"><span data-stu-id="731e1-124">Windows Media Player also ignores the **ASX** element in the referenced file along with its attributes.</span></span> <span data-ttu-id="731e1-125">Le lecteur Windows Media série 9 ou version ultérieure prend en charge l’imbrication de fichiers de permétrage jusqu’à cinq niveaux.</span><span class="sxs-lookup"><span data-stu-id="731e1-125">Windows Media Player 9 Series or later supports nesting metafiles up to five levels deep.</span></span>

<span data-ttu-id="731e1-126">L’URL spécifiée dans l’attribut **href** devient l’URL de base pour toutes les URL relatives dans le métafichier externe.</span><span class="sxs-lookup"><span data-stu-id="731e1-126">The URL specified in the **HREF** attribute becomes the base URL for any relative URLs in the external metafile.</span></span> <span data-ttu-id="731e1-127">Cette URL est utilisée lorsqu’une entrée du métafichier externe est lue et que l’utilisateur l’ajoute à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="731e1-127">This URL is used when an entry from the external metafile is playing and the user adds it to the library.</span></span>

## <a name="examples"></a><span data-ttu-id="731e1-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="731e1-128">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="731e1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="731e1-129">Requirements</span></span>



| <span data-ttu-id="731e1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="731e1-130">Requirement</span></span> | <span data-ttu-id="731e1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="731e1-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="731e1-132">Version</span><span class="sxs-lookup"><span data-stu-id="731e1-132">Version</span></span><br/> | <span data-ttu-id="731e1-133">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="731e1-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="731e1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="731e1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="731e1-135">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="731e1-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="731e1-136">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="731e1-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





