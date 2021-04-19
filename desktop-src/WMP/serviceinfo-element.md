---
title: Élément ServiceInfo
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’élément ServiceInfo est l’élément principal du document ServiceInfo.xml.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Élément ServiceInfo lecteur Windows Media
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543800"
---
# <a name="serviceinfo-element"></a><span data-ttu-id="fdb13-106">Élément ServiceInfo</span><span class="sxs-lookup"><span data-stu-id="fdb13-106">ServiceInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="fdb13-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="fdb13-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fdb13-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fdb13-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fdb13-109">L’élément **serviceInfo** est l’élément principal du document ServiceInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="fdb13-109">The **ServiceInfo** element is the main element for the ServiceInfo.xml document.</span></span>

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a><span data-ttu-id="fdb13-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="fdb13-110">Attributes</span></span>



| <span data-ttu-id="fdb13-111">Terme</span><span class="sxs-lookup"><span data-stu-id="fdb13-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="fdb13-112">Description</span><span class="sxs-lookup"><span data-stu-id="fdb13-112">Description</span></span>                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb13-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (facultatif)</span><span class="sxs-lookup"><span data-stu-id="fdb13-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)</span></span><br/> | <span data-ttu-id="fdb13-114">Version du fichier ServiceInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="fdb13-114">Version of the ServiceInfo.xml file.</span></span> <span data-ttu-id="fdb13-115">La version 1,00 est prise en charge pour le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fdb13-115">Version 1.00 is supported for Windows Media Player.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="fdb13-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Clé** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="fdb13-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Key** (required)</span></span><br/>                 | <span data-ttu-id="fdb13-117">Chaîne de clé de service qui identifie de façon unique le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="fdb13-117">The service key string that uniquely identifies the online store.</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="fdb13-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span><span class="sxs-lookup"><span data-stu-id="fdb13-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span></span><br/>                 | <span data-ttu-id="fdb13-119">Indique si le magasin en ligne est un magasin de type 1.</span><span class="sxs-lookup"><span data-stu-id="fdb13-119">Indicates whether the online store is a type 1 store.</span></span> <span data-ttu-id="fdb13-120">La valeur « true » indique que le magasin est un magasin de type 1.</span><span class="sxs-lookup"><span data-stu-id="fdb13-120">A value of "true" indicates that the store is a type 1 store.</span></span> <span data-ttu-id="fdb13-121">La valeur « false » indique que le magasin n’est pas un magasin de type 1 ; autrement dit, il s’agit d’un magasin de type 2.</span><span class="sxs-lookup"><span data-stu-id="fdb13-121">A value of "false" indicates that the store is not a type 1 store; that is, it is a type 2 store.</span></span> <span data-ttu-id="fdb13-122">La valeur par défaut est « false ».</span><span class="sxs-lookup"><span data-stu-id="fdb13-122">The default value is "false".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="fdb13-123">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="fdb13-123">Parent/Child Elements</span></span>



| <span data-ttu-id="fdb13-124">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="fdb13-124">Hierarchy</span></span>       | <span data-ttu-id="fdb13-125">Élément</span><span class="sxs-lookup"><span data-stu-id="fdb13-125">Element</span></span>                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb13-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fdb13-126">Parent elements</span></span> | <span data-ttu-id="fdb13-127">Aucun</span><span class="sxs-lookup"><span data-stu-id="fdb13-127">None</span></span>                                                                                                                                                                               |
| <span data-ttu-id="fdb13-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fdb13-128">Child elements</span></span>  | <span data-ttu-id="fdb13-129">**AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **image**, **Centre** d’informations, **installer**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="fdb13-129">**AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **InfoCenter**, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fdb13-130">Notes</span><span class="sxs-lookup"><span data-stu-id="fdb13-130">Remarks</span></span>

<span data-ttu-id="fdb13-131">Le tableau suivant détaille les paramètres envoyés avec la demande d’URL.</span><span class="sxs-lookup"><span data-stu-id="fdb13-131">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="fdb13-132">D’autres peuvent être présents à des fins de compatibilité héritée.</span><span class="sxs-lookup"><span data-stu-id="fdb13-132">Others may be present for legacy compatibility purposes.</span></span> <span data-ttu-id="fdb13-133">La requête inclut également tous les paramètres que vous avez spécifiés à l’aide du paramètre de ligne de commande ServiceExtra du programme d’installation du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fdb13-133">The request will also include any parameters you specified using the ServiceExtra command-line parameter of Windows Media Player setup.</span></span>



| <span data-ttu-id="fdb13-134">Nom</span><span class="sxs-lookup"><span data-stu-id="fdb13-134">Name</span></span>         | <span data-ttu-id="fdb13-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdb13-135">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb13-136">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="fdb13-136">*geoid*</span></span>      | <span data-ttu-id="fdb13-137">ID d’emplacement géographique Windows.</span><span class="sxs-lookup"><span data-stu-id="fdb13-137">Windows geographical location ID.</span></span> <span data-ttu-id="fdb13-138">L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="fdb13-138">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="fdb13-139">*locale*</span><span class="sxs-lookup"><span data-stu-id="fdb13-139">*locale*</span></span>     | <span data-ttu-id="fdb13-140">ID de paramètres régionaux du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fdb13-140">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="fdb13-141">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="fdb13-141">*userlocale*</span></span> | <span data-ttu-id="fdb13-142">ID de paramètres régionaux Windows.</span><span class="sxs-lookup"><span data-stu-id="fdb13-142">Windows locale ID.</span></span> <span data-ttu-id="fdb13-143">Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="fdb13-143">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="fdb13-144">*version*</span><span class="sxs-lookup"><span data-stu-id="fdb13-144">*version*</span></span>    | <span data-ttu-id="fdb13-145">Numéro de version du lecteur Windows Media en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="fdb13-145">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="fdb13-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdb13-146">Requirements</span></span>



| <span data-ttu-id="fdb13-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdb13-147">Requirement</span></span> | <span data-ttu-id="fdb13-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdb13-148">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="fdb13-149">Version</span><span class="sxs-lookup"><span data-stu-id="fdb13-149">Version</span></span><br/> | <span data-ttu-id="fdb13-150">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fdb13-150">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fdb13-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdb13-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb13-152">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="fdb13-152">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="fdb13-153">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="fdb13-153">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="fdb13-154">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="fdb13-154">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





