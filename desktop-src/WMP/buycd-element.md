---
title: Élément BuyCD
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Élément BuyCD lecteur Windows Media
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520903"
---
# <a name="buycd-element"></a><span data-ttu-id="5a2c1-105">Élément BuyCD</span><span class="sxs-lookup"><span data-stu-id="5a2c1-105">BuyCD Element</span></span>

> [!Note]  
> <span data-ttu-id="5a2c1-106">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5a2c1-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5a2c1-108">L’élément **BuyCD** spécifie les URL des pages Web que le lecteur Windows Media affiche lorsque l’utilisateur choisit d’effectuer un achat.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-108">The **BuyCD** element specifies the URLs for webpages that Windows Media Player displays when the user chooses to make a purchase.</span></span>

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="5a2c1-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="5a2c1-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="5a2c1-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="5a2c1-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="5a2c1-111">URL de la page Web que le magasin en ligne affiche pour proposer un CD ou un DVD à acheter dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-111">URL for the webpage that the online store displays to offer a CD or DVD for purchase in Windows Media Player.</span></span>

</dd> <dt>

<span data-ttu-id="5a2c1-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span><span class="sxs-lookup"><span data-stu-id="5a2c1-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span></span>
</dt> <dd>

<span data-ttu-id="5a2c1-113">URL de la page Web que le magasin en ligne affiche pour proposer un CD ou un DVD à acheter dans Windows XP Media Center Edition 2004 Update.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-113">URL for the webpage the online store displays to offer a CD or DVD for purchase in Windows XP Media Center Edition 2004 Update.</span></span>

</dd> <dt>

<span data-ttu-id="5a2c1-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span><span class="sxs-lookup"><span data-stu-id="5a2c1-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span></span>
</dt> <dd>

<span data-ttu-id="5a2c1-115">URL de la page Web que le magasin en ligne affiche pour proposer un CD ou un DVD à acheter dans une fenêtre de navigateur distincte.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-115">URL for the webpage that the online store displays to offer a CD or DVD for purchase in a separate browser window.</span></span> <span data-ttu-id="5a2c1-116">Cette URL est également utilisée par Windows XP Service Pack 2 ou une version ultérieure pour la fonctionnalité **Online Shop for Music** .</span><span class="sxs-lookup"><span data-stu-id="5a2c1-116">This URL is also used by Windows XP Service Pack 2 or later for the **Shop for music online** feature.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="5a2c1-117">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="5a2c1-117">Parent/Child Elements</span></span>



| <span data-ttu-id="5a2c1-118">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="5a2c1-118">Hierarchy</span></span>       | <span data-ttu-id="5a2c1-119">Élément</span><span class="sxs-lookup"><span data-stu-id="5a2c1-119">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="5a2c1-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5a2c1-120">Parent elements</span></span> | <span data-ttu-id="5a2c1-121">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="5a2c1-121">**ServiceInfo**</span></span> |
| <span data-ttu-id="5a2c1-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5a2c1-122">Child elements</span></span>  | <span data-ttu-id="5a2c1-123">Aucune</span><span class="sxs-lookup"><span data-stu-id="5a2c1-123">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="5a2c1-124">Notes</span><span class="sxs-lookup"><span data-stu-id="5a2c1-124">Remarks</span></span>

<span data-ttu-id="5a2c1-125">Quand l’utilisateur clique sur un bouton ou un lien dans le lecteur Windows Media pour acheter un CD ou un DVD, le lecteur envoie la demande d’URL à ServiceTask1 avec des paramètres attachés à l’aide d’un séparateur de chaîne de requête de point d’interrogation ( ?).</span><span class="sxs-lookup"><span data-stu-id="5a2c1-125">When the user clicks a button or link in Windows Media Player to purchase a CD or DVD, the Player sends the URL request to ServiceTask1 with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="5a2c1-126">Le tableau suivant détaille les paramètres envoyés avec la demande d’URL.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-126">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="5a2c1-127">D’autres peuvent être présents à des fins de compatibilité héritée.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-127">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="5a2c1-128">Nom</span><span class="sxs-lookup"><span data-stu-id="5a2c1-128">Name</span></span>         | <span data-ttu-id="5a2c1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a2c1-129">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2c1-130">*Album*</span><span class="sxs-lookup"><span data-stu-id="5a2c1-130">*Album*</span></span>      | <span data-ttu-id="5a2c1-131">Valeur de l’attribut **WM/AlbumTitle** pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-131">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="5a2c1-132">*Peinture*</span><span class="sxs-lookup"><span data-stu-id="5a2c1-132">*Artist*</span></span>     | <span data-ttu-id="5a2c1-133">Valeur de l’attribut **WM/AlbumArtist** , s’il en existe un, ou la valeur de l’attribut **Author** pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-133">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="5a2c1-134">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="5a2c1-134">*geoid*</span></span>      | <span data-ttu-id="5a2c1-135">ID d’emplacement géographique Windows.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-135">Windows geographical location ID.</span></span> <span data-ttu-id="5a2c1-136">L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-136">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="5a2c1-137">*locale*</span><span class="sxs-lookup"><span data-stu-id="5a2c1-137">*locale*</span></span>     | <span data-ttu-id="5a2c1-138">ID de paramètres régionaux du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-138">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="5a2c1-139">*Titre*</span><span class="sxs-lookup"><span data-stu-id="5a2c1-139">*Title*</span></span>      | <span data-ttu-id="5a2c1-140">Valeur de l’attribut **title** pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-140">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="5a2c1-141">*UFID*</span><span class="sxs-lookup"><span data-stu-id="5a2c1-141">*UFID*</span></span>       | <span data-ttu-id="5a2c1-142">Valeur de l’attribut **WM/UniqueFileIdentifier** pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-142">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="5a2c1-143">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="5a2c1-143">*userlocale*</span></span> | <span data-ttu-id="5a2c1-144">ID de paramètres régionaux Windows.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-144">Windows locale ID.</span></span> <span data-ttu-id="5a2c1-145">Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="5a2c1-146">*version*</span><span class="sxs-lookup"><span data-stu-id="5a2c1-146">*version*</span></span>    | <span data-ttu-id="5a2c1-147">Numéro de version du lecteur Windows Media en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

<span data-ttu-id="5a2c1-148">Windows XP Media Center Edition 2004 fournit aux utilisateurs une interface utilisateur conçue pour être affichée à distance.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-148">Windows XP Media Center Edition 2004 provides users with a user interface designed to be viewed at a distance.</span></span> <span data-ttu-id="5a2c1-149">Vous devez créer des pages Web pour le paramètre *MediaCenterURL* à afficher sur de grands écrans.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-149">You should create webpages for the *MediaCenterURL* parameter to be viewed on large displays.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2c1-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a2c1-150">Requirements</span></span>



| <span data-ttu-id="5a2c1-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a2c1-151">Requirement</span></span> | <span data-ttu-id="5a2c1-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a2c1-152">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="5a2c1-153">Version</span><span class="sxs-lookup"><span data-stu-id="5a2c1-153">Version</span></span><br/> | <span data-ttu-id="5a2c1-154">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5a2c1-154">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a2c1-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a2c1-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2c1-156">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="5a2c1-156">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="5a2c1-157">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="5a2c1-157">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="5a2c1-158">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="5a2c1-158">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





