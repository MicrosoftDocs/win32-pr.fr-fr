---
title: Élément Navigate
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’élément Navigate spécifie une URL utilisée par les appels à External. NavigateTaskPaneURL.
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- Élément naviguer dans le lecteur Windows Media
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532246"
---
# <a name="navigate-element"></a><span data-ttu-id="646cb-106">Élément Navigate</span><span class="sxs-lookup"><span data-stu-id="646cb-106">Navigate Element</span></span>

> [!Note]  
> <span data-ttu-id="646cb-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="646cb-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="646cb-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="646cb-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="646cb-109">L’élément **Navigate** spécifie une URL utilisée par les appels à **External. NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="646cb-109">The **Navigate** element specifies a URL used by calls to **External.NavigateTaskPaneURL**.</span></span>

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="646cb-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="646cb-110">Attributes</span></span>



| <span data-ttu-id="646cb-111">Terme</span><span class="sxs-lookup"><span data-stu-id="646cb-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="646cb-112">Description</span><span class="sxs-lookup"><span data-stu-id="646cb-112">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="646cb-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="646cb-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span><br/> | <span data-ttu-id="646cb-114">URL complète de la page Web à laquelle naviguer.</span><span class="sxs-lookup"><span data-stu-id="646cb-114">Fully qualified URL for the webpage to which to navigate.</span></span> <span data-ttu-id="646cb-115">**NavigateTaskPaneURL** peut ajouter une chaîne de requête à cette URL.</span><span class="sxs-lookup"><span data-stu-id="646cb-115">**NavigateTaskPaneURL** can append a query string to this URL.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="646cb-116">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="646cb-116">Parent/Child Elements</span></span>



| <span data-ttu-id="646cb-117">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="646cb-117">Hierarchy</span></span>       | <span data-ttu-id="646cb-118">Élément</span><span class="sxs-lookup"><span data-stu-id="646cb-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="646cb-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="646cb-119">Parent elements</span></span> | <span data-ttu-id="646cb-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="646cb-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="646cb-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="646cb-121">Child elements</span></span>  | <span data-ttu-id="646cb-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="646cb-122">None</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="646cb-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="646cb-123">Requirements</span></span>



| <span data-ttu-id="646cb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="646cb-124">Requirement</span></span> | <span data-ttu-id="646cb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="646cb-125">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="646cb-126">Version</span><span class="sxs-lookup"><span data-stu-id="646cb-126">Version</span></span><br/> | <span data-ttu-id="646cb-127">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="646cb-127">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="646cb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="646cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646cb-129">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="646cb-129">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="646cb-130">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="646cb-130">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="646cb-131">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="646cb-131">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="646cb-132">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="646cb-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





