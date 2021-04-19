---
description: Définit les métadonnées d’hébergement pour l’appareil à implémenter. Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: élément hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524466"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="a5a39-104">élément hostMetadata</span><span class="sxs-lookup"><span data-stu-id="a5a39-104">hostMetadata element</span></span>

<span data-ttu-id="a5a39-105">Définit les métadonnées d’hébergement pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="a5a39-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="a5a39-106">Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).</span><span class="sxs-lookup"><span data-stu-id="a5a39-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="a5a39-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="a5a39-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="a5a39-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="a5a39-108">Attributes</span></span>

<span data-ttu-id="a5a39-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a5a39-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a5a39-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a5a39-110">Child elements</span></span>



| <span data-ttu-id="a5a39-111">Élément</span><span class="sxs-lookup"><span data-stu-id="a5a39-111">Element</span></span>                             | <span data-ttu-id="a5a39-112">Description</span><span class="sxs-lookup"><span data-stu-id="a5a39-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5a39-113">**HBA**</span><span class="sxs-lookup"><span data-stu-id="a5a39-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="a5a39-114">Définit les éléments ServiceID et [**types**](types.md) pour l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="a5a39-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="a5a39-115">S’il n’est pas fourni explicitement, WSDAPI ne fournit pas de données par défaut en réponse aux demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a5a39-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="a5a39-116">**Hébergement**</span><span class="sxs-lookup"><span data-stu-id="a5a39-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="a5a39-117">Définit les éléments [**ServiceId**](serviceid.md) et [**types**](types.md) pour les services fournis par cet hôte de service.</span><span class="sxs-lookup"><span data-stu-id="a5a39-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="a5a39-118">Chaque service fourni par cet hôte de service doit disposer de ses propres informations d’élément [**hébergé**](hosted.md) pour s’assurer que le service est correctement publié dans les réponses aux demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a5a39-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="a5a39-119">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a5a39-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="a5a39-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a5a39-120">Parent elements</span></span>



| <span data-ttu-id="a5a39-121">Élément</span><span class="sxs-lookup"><span data-stu-id="a5a39-121">Element</span></span>                                                         | <span data-ttu-id="a5a39-122">Description</span><span class="sxs-lookup"><span data-stu-id="a5a39-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="a5a39-123">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="a5a39-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="a5a39-124">Décrit l’hôte et les métadonnées hébergées pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a5a39-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a5a39-125">Notes</span><span class="sxs-lookup"><span data-stu-id="a5a39-125">Remarks</span></span>

<span data-ttu-id="a5a39-126">Les métadonnées d’hébergement apparaissent dans cet élément sous une forme similaire à celle spécifiée dans le profil d’appareil.</span><span class="sxs-lookup"><span data-stu-id="a5a39-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="a5a39-127">**hostMetadata** est légèrement différent du format décrit dans le profil de l’appareil, car la seule propriété de référence qu’il prend en charge est l’ID du service.</span><span class="sxs-lookup"><span data-stu-id="a5a39-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="a5a39-128">L’élément [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) est utilisé par la suite pour générer une constante C contenant ces informations.</span><span class="sxs-lookup"><span data-stu-id="a5a39-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="a5a39-129">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a5a39-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="a5a39-130">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5a39-130">Minimum supported system</span></span><br/> | <span data-ttu-id="a5a39-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5a39-131">Windows Vista</span></span> |
| <span data-ttu-id="a5a39-132">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="a5a39-132">Can be empty</span></span>                        | <span data-ttu-id="a5a39-133">Non</span><span class="sxs-lookup"><span data-stu-id="a5a39-133">No</span></span>            |



 

 




