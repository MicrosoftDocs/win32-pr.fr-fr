---
description: Définit les métadonnées d’hébergement pour l’appareil à implémenter. Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: élément hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994796"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="b9cc3-104">élément hostMetadata</span><span class="sxs-lookup"><span data-stu-id="b9cc3-104">hostMetadata element</span></span>

<span data-ttu-id="b9cc3-105">Définit les métadonnées d’hébergement pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="b9cc3-106">Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).</span><span class="sxs-lookup"><span data-stu-id="b9cc3-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="b9cc3-107">Usage</span><span class="sxs-lookup"><span data-stu-id="b9cc3-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="b9cc3-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="b9cc3-108">Attributes</span></span>

<span data-ttu-id="b9cc3-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b9cc3-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b9cc3-110">Child elements</span></span>



| <span data-ttu-id="b9cc3-111">Élément</span><span class="sxs-lookup"><span data-stu-id="b9cc3-111">Element</span></span>                             | <span data-ttu-id="b9cc3-112">Description</span><span class="sxs-lookup"><span data-stu-id="b9cc3-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9cc3-113">**HBA**</span><span class="sxs-lookup"><span data-stu-id="b9cc3-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="b9cc3-114">Définit les éléments ServiceID et [**types**](types.md) pour l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="b9cc3-115">S’il n’est pas fourni explicitement, WSDAPI ne fournit pas de données par défaut en réponse aux demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="b9cc3-116">**Hébergement**</span><span class="sxs-lookup"><span data-stu-id="b9cc3-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="b9cc3-117">Définit les éléments [**ServiceId**](serviceid.md) et [**types**](types.md) pour les services fournis par cet hôte de service.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="b9cc3-118">Chaque service fourni par cet hôte de service doit disposer de ses propres informations d’élément [**hébergé**](hosted.md) pour s’assurer que le service est correctement publié dans les réponses aux demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b9cc3-119">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b9cc3-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="b9cc3-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b9cc3-120">Parent elements</span></span>



| <span data-ttu-id="b9cc3-121">Élément</span><span class="sxs-lookup"><span data-stu-id="b9cc3-121">Element</span></span>                                                         | <span data-ttu-id="b9cc3-122">Description</span><span class="sxs-lookup"><span data-stu-id="b9cc3-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="b9cc3-123">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="b9cc3-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="b9cc3-124">Décrit l’hôte et les métadonnées hébergées pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b9cc3-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="b9cc3-125">Remarks</span></span>

<span data-ttu-id="b9cc3-126">Les métadonnées d’hébergement apparaissent dans cet élément sous une forme similaire à celle spécifiée dans le profil d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="b9cc3-127">**hostMetadata** est légèrement différent du format décrit dans le profil de l’appareil, car la seule propriété de référence qu’il prend en charge est l’ID du service.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="b9cc3-128">L’élément [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) est utilisé par la suite pour générer une constante C contenant ces informations.</span><span class="sxs-lookup"><span data-stu-id="b9cc3-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="b9cc3-129">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b9cc3-129">Element information</span></span>



| <span data-ttu-id="b9cc3-130">Étiquette</span><span class="sxs-lookup"><span data-stu-id="b9cc3-130">Label</span></span> | <span data-ttu-id="b9cc3-131">Value</span><span class="sxs-lookup"><span data-stu-id="b9cc3-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b9cc3-132">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9cc3-132">Minimum supported system</span></span><br/> | <span data-ttu-id="b9cc3-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9cc3-133">Windows Vista</span></span> |
| <span data-ttu-id="b9cc3-134">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="b9cc3-134">Can be empty</span></span>                        | <span data-ttu-id="b9cc3-135">Non</span><span class="sxs-lookup"><span data-stu-id="b9cc3-135">No</span></span>            |



 

 




