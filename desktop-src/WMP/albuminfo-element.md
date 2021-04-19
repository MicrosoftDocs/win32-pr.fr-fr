---
title: Élément AlbumInfo
description: L’élément AlbumInfo spécifie l’URL de la page Web que le lecteur Windows Media affiche lorsque l’utilisateur choisit d’afficher plus d’informations sur un élément multimédia particulier.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Élément AlbumInfo lecteur Windows Media
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523641"
---
# <a name="albuminfo-element"></a><span data-ttu-id="98d87-104">Élément AlbumInfo</span><span class="sxs-lookup"><span data-stu-id="98d87-104">AlbumInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="98d87-105">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="98d87-105">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="98d87-106">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="98d87-106">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="98d87-107">L’élément **AlbumInfo** spécifie l’URL de la page Web que le lecteur Windows Media affiche lorsque l’utilisateur choisit d’afficher plus d’informations sur un élément multimédia particulier.</span><span class="sxs-lookup"><span data-stu-id="98d87-107">The **AlbumInfo** element specifies the URL for the webpage that Windows Media Player displays when the user chooses to view more information about a particular media item.</span></span>

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a><span data-ttu-id="98d87-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="98d87-108">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="98d87-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="98d87-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="98d87-110">URL de la page Web affichée par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="98d87-110">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="98d87-111">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="98d87-111">Parent/Child Elements</span></span>



| <span data-ttu-id="98d87-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="98d87-112">Hierarchy</span></span>       | <span data-ttu-id="98d87-113">Élément</span><span class="sxs-lookup"><span data-stu-id="98d87-113">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="98d87-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="98d87-114">Parent elements</span></span> | <span data-ttu-id="98d87-115">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="98d87-115">**ServiceInfo**</span></span> |
| <span data-ttu-id="98d87-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="98d87-116">Child elements</span></span>  | <span data-ttu-id="98d87-117">Aucune</span><span class="sxs-lookup"><span data-stu-id="98d87-117">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="98d87-118">Notes</span><span class="sxs-lookup"><span data-stu-id="98d87-118">Remarks</span></span>

<span data-ttu-id="98d87-119">Quand l’utilisateur clique sur un bouton dans le lecteur Windows Media pour afficher des informations supplémentaires sur un élément multimédia particulier, le lecteur envoie la demande d’URL avec des paramètres attachés à l’aide d’un séparateur de chaîne de requête de point d’interrogation ( ?).</span><span class="sxs-lookup"><span data-stu-id="98d87-119">When the user clicks a button in Windows Media Player to view additional information about a particular media item, the Player sends the URL request with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="98d87-120">Le tableau suivant détaille les paramètres envoyés avec la demande d’URL.</span><span class="sxs-lookup"><span data-stu-id="98d87-120">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="98d87-121">D’autres peuvent être présents à des fins de compatibilité héritée.</span><span class="sxs-lookup"><span data-stu-id="98d87-121">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="98d87-122">Nom</span><span class="sxs-lookup"><span data-stu-id="98d87-122">Name</span></span>         | <span data-ttu-id="98d87-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="98d87-123">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d87-124">*Album*</span><span class="sxs-lookup"><span data-stu-id="98d87-124">*Album*</span></span>      | <span data-ttu-id="98d87-125">Valeur de l’attribut **WM/AlbumTitle** pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="98d87-125">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="98d87-126">*Peinture*</span><span class="sxs-lookup"><span data-stu-id="98d87-126">*Artist*</span></span>     | <span data-ttu-id="98d87-127">Valeur de l’attribut **WM/AlbumArtist** , s’il en existe un, ou la valeur de l’attribut **Author** pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="98d87-127">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="98d87-128">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="98d87-128">*geoid*</span></span>      | <span data-ttu-id="98d87-129">ID d’emplacement géographique Windows.</span><span class="sxs-lookup"><span data-stu-id="98d87-129">Windows geographical location ID.</span></span> <span data-ttu-id="98d87-130">L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="98d87-130">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="98d87-131">*locale*</span><span class="sxs-lookup"><span data-stu-id="98d87-131">*locale*</span></span>     | <span data-ttu-id="98d87-132">ID de paramètres régionaux du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="98d87-132">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="98d87-133">*Titre*</span><span class="sxs-lookup"><span data-stu-id="98d87-133">*Title*</span></span>      | <span data-ttu-id="98d87-134">Valeur de l’attribut **title** pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="98d87-134">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="98d87-135">*UFID*</span><span class="sxs-lookup"><span data-stu-id="98d87-135">*UFID*</span></span>       | <span data-ttu-id="98d87-136">Valeur de l’attribut **WM/UniqueFileIdentifier** pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="98d87-136">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="98d87-137">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="98d87-137">*userlocale*</span></span> | <span data-ttu-id="98d87-138">ID de paramètres régionaux Windows.</span><span class="sxs-lookup"><span data-stu-id="98d87-138">Windows locale ID.</span></span> <span data-ttu-id="98d87-139">Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="98d87-139">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="98d87-140">*version*</span><span class="sxs-lookup"><span data-stu-id="98d87-140">*version*</span></span>    | <span data-ttu-id="98d87-141">Numéro de version du lecteur Windows Media en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="98d87-141">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="98d87-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98d87-142">Requirements</span></span>



| <span data-ttu-id="98d87-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98d87-143">Requirement</span></span> | <span data-ttu-id="98d87-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="98d87-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="98d87-145">Version</span><span class="sxs-lookup"><span data-stu-id="98d87-145">Version</span></span><br/> | <span data-ttu-id="98d87-146">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="98d87-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98d87-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98d87-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d87-148">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="98d87-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="98d87-149">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="98d87-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="98d87-150">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="98d87-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





