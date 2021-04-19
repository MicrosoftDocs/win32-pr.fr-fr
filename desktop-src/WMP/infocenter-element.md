---
title: Élément Centre d’informations
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément Centre d’informations
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Élément Centre d’informations lecteur Windows Media
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530418"
---
# <a name="infocenter-element"></a><span data-ttu-id="a490f-105">Élément Centre d’informations</span><span class="sxs-lookup"><span data-stu-id="a490f-105">InfoCenter Element</span></span>

> [!Note]  
> <span data-ttu-id="a490f-106">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="a490f-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a490f-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a490f-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a490f-108">L’élément **Centre** d’informations spécifie l’URL de la page Web que le lecteur Windows Media affiche dans la fonctionnalité d’affichage du centre d’informations de en **cours de lecture** lorsque le magasin en ligne est actif.</span><span class="sxs-lookup"><span data-stu-id="a490f-108">The **InfoCenter** element specifies the URL of the webpage that Windows Media Player displays in the Info Center View feature of **Now Playing** when the online store is active.</span></span>

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="a490f-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="a490f-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="a490f-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="a490f-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="a490f-111">URL de la page Web affichée par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a490f-111">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="a490f-112">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="a490f-112">Parent/Child Elements</span></span>



| <span data-ttu-id="a490f-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="a490f-113">Hierarchy</span></span>       | <span data-ttu-id="a490f-114">Élément</span><span class="sxs-lookup"><span data-stu-id="a490f-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="a490f-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a490f-115">Parent elements</span></span> | <span data-ttu-id="a490f-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="a490f-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="a490f-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a490f-117">Child elements</span></span>  | <span data-ttu-id="a490f-118">Aucune</span><span class="sxs-lookup"><span data-stu-id="a490f-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="a490f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a490f-119">Remarks</span></span>

<span data-ttu-id="a490f-120">L’utilisateur contrôle quand l’affichage du centre d’informations est actif.</span><span class="sxs-lookup"><span data-stu-id="a490f-120">The user controls when Info Center View is active.</span></span>

<span data-ttu-id="a490f-121">Pour récupérer des informations sur l’élément multimédia en cours de lecture, vous devez incorporer une instance du contrôle du lecteur Windows Media dans votre page Web et utiliser le modèle objet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="a490f-121">To retrieve information about the currently playing media item, you must embed an instance of Windows Media Player control in your webpage and use the Player object model.</span></span>

<span data-ttu-id="a490f-122">Le tableau suivant détaille les paramètres envoyés avec la demande d’URL.</span><span class="sxs-lookup"><span data-stu-id="a490f-122">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="a490f-123">D’autres peuvent être présents à des fins de compatibilité héritée.</span><span class="sxs-lookup"><span data-stu-id="a490f-123">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="a490f-124">Nom</span><span class="sxs-lookup"><span data-stu-id="a490f-124">Name</span></span>         | <span data-ttu-id="a490f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a490f-125">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a490f-126">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="a490f-126">*geoid*</span></span>      | <span data-ttu-id="a490f-127">ID d’emplacement géographique Windows.</span><span class="sxs-lookup"><span data-stu-id="a490f-127">Windows geographical location ID.</span></span> <span data-ttu-id="a490f-128">L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="a490f-128">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="a490f-129">*locale*</span><span class="sxs-lookup"><span data-stu-id="a490f-129">*locale*</span></span>     | <span data-ttu-id="a490f-130">ID de paramètres régionaux du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a490f-130">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="a490f-131">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="a490f-131">*userlocale*</span></span> | <span data-ttu-id="a490f-132">ID de paramètres régionaux Windows.</span><span class="sxs-lookup"><span data-stu-id="a490f-132">Windows locale ID.</span></span> <span data-ttu-id="a490f-133">Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="a490f-133">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="a490f-134">*version*</span><span class="sxs-lookup"><span data-stu-id="a490f-134">*version*</span></span>    | <span data-ttu-id="a490f-135">Numéro de version du lecteur Windows Media en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="a490f-135">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a490f-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a490f-136">Requirements</span></span>



| <span data-ttu-id="a490f-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a490f-137">Requirement</span></span> | <span data-ttu-id="a490f-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="a490f-138">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="a490f-139">Version</span><span class="sxs-lookup"><span data-stu-id="a490f-139">Version</span></span><br/> | <span data-ttu-id="a490f-140">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a490f-140">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a490f-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a490f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a490f-142">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="a490f-142">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="a490f-143">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="a490f-143">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="a490f-144">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="a490f-144">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





