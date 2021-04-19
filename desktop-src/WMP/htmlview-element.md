---
title: Élément HTMLView
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’élément HTMLView spécifie l’URL de base d’une page Web HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Élément HTMLView lecteur Windows Media
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545926"
---
# <a name="htmlview-element"></a><span data-ttu-id="b99a1-106">Élément HTMLView</span><span class="sxs-lookup"><span data-stu-id="b99a1-106">HTMLView Element</span></span>

> [!Note]  
> <span data-ttu-id="b99a1-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="b99a1-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b99a1-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b99a1-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b99a1-109">L’élément **HTMLView** spécifie l’URL de base d’une page Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="b99a1-109">The **HTMLView** element specifies the base URL of an HTMLView webpage.</span></span>

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="b99a1-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="b99a1-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="b99a1-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="b99a1-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="b99a1-112">URL de base de la page Web HTMLView affichée par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b99a1-112">Base URL for the HTMLView webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="b99a1-113">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="b99a1-113">Parent/Child Elements</span></span>



| <span data-ttu-id="b99a1-114">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b99a1-114">Hierarchy</span></span>       | <span data-ttu-id="b99a1-115">Élément</span><span class="sxs-lookup"><span data-stu-id="b99a1-115">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="b99a1-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b99a1-116">Parent elements</span></span> | <span data-ttu-id="b99a1-117">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b99a1-117">**ServiceInfo**</span></span> |
| <span data-ttu-id="b99a1-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b99a1-118">Child elements</span></span>  | <span data-ttu-id="b99a1-119">Aucune</span><span class="sxs-lookup"><span data-stu-id="b99a1-119">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="b99a1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b99a1-120">Remarks</span></span>

<span data-ttu-id="b99a1-121">Vous pouvez utiliser cet élément pour intégrer la fonctionnalité HTMLView à votre magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="b99a1-121">You can use this element to integrate the HTMLView feature with your online store.</span></span> <span data-ttu-id="b99a1-122">Si le domaine de l’URL spécifiée par le magasin en ligne actuel correspond à celui de la page Web HTMLView, le commutateur à **présent** se produit sans intervention de l’utilisateur et le contenu de HTMLView est affiché.</span><span class="sxs-lookup"><span data-stu-id="b99a1-122">If the domain of the URL specified by the current online store matches the one for the HTMLView webpage, the switch to **Now Playing** happens without user intervention and the HTMLView content is displayed.</span></span> <span data-ttu-id="b99a1-123">Dans le cas contraire, le lecteur Windows Media demande à l’utilisateur l’autorisation d’afficher le contenu HTMLView.</span><span class="sxs-lookup"><span data-stu-id="b99a1-123">Otherwise, Windows Media Player prompts the user for permission to show the HTMLView content.</span></span>

<span data-ttu-id="b99a1-124">Par exemple, si l’URL de la page Web HTMLView est https://www.proseware.com/html/HTMLView.htm et que l’URL de l’attribut **BaseURL** est spécifiée en tant que https://www.proseware.com , la page Web HTMLView s’affiche sans demander confirmation à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b99a1-124">For example, if the URL for the HTMLView webpage is https://www.proseware.com/html/HTMLView.htm and the URL for the **BaseURL** attribute is specified as https://www.proseware.com, the HTMLView webpage displays without prompting the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="b99a1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b99a1-125">Requirements</span></span>



| <span data-ttu-id="b99a1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b99a1-126">Requirement</span></span> | <span data-ttu-id="b99a1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b99a1-127">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="b99a1-128">Version</span><span class="sxs-lookup"><span data-stu-id="b99a1-128">Version</span></span><br/> | <span data-ttu-id="b99a1-129">Lecteur Windows Media 10 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b99a1-129">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b99a1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b99a1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b99a1-131">**Affichage des pages Web dans le lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b99a1-131">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="b99a1-132">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="b99a1-132">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="b99a1-133">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="b99a1-133">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="b99a1-134">**Élément PARAM**</span><span class="sxs-lookup"><span data-stu-id="b99a1-134">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="b99a1-135">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b99a1-135">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





