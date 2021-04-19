---
description: Définit les éléments ServiceID, types, PnPXHardwareId et PnPXCompatibleId pour les services définis par l’hôte de service.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: élément hébergé
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536592"
---
# <a name="hosted-element"></a><span data-ttu-id="9a2c4-103">élément hébergé</span><span class="sxs-lookup"><span data-stu-id="9a2c4-103">hosted element</span></span>

<span data-ttu-id="9a2c4-104">Définit les éléments [**ServiceId**](serviceid.md), [**types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)et [**PnPXCompatibleId**](pnpxcompatibleid.md) pour les services définis par l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="9a2c4-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="9a2c4-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="9a2c4-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="9a2c4-106">Attributes</span></span>

<span data-ttu-id="9a2c4-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9a2c4-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9a2c4-108">Child elements</span></span>



| <span data-ttu-id="9a2c4-109">Élément</span><span class="sxs-lookup"><span data-stu-id="9a2c4-109">Element</span></span>                                                 | <span data-ttu-id="9a2c4-110">Description</span><span class="sxs-lookup"><span data-stu-id="9a2c4-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="9a2c4-111">**PnPXCompatibleId**</span><span class="sxs-lookup"><span data-stu-id="9a2c4-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="9a2c4-112">Spécifie l’identificateur compatible PnP-X du service.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="9a2c4-113">**PnPXHardwareId**</span><span class="sxs-lookup"><span data-stu-id="9a2c4-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="9a2c4-114">Spécifie l’identificateur matériel PnP-X du service.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="9a2c4-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="9a2c4-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="9a2c4-116">Définit un identificateur de service pour l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="9a2c4-117">**Types**</span><span class="sxs-lookup"><span data-stu-id="9a2c4-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="9a2c4-118">Définit une liste de noms qualifiés XSD.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="9a2c4-119">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9a2c4-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="9a2c4-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9a2c4-120">Parent elements</span></span>



| <span data-ttu-id="9a2c4-121">Élément</span><span class="sxs-lookup"><span data-stu-id="9a2c4-121">Element</span></span>                                         | <span data-ttu-id="9a2c4-122">Description</span><span class="sxs-lookup"><span data-stu-id="9a2c4-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="9a2c4-123">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="9a2c4-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="9a2c4-124">Métadonnées d’hébergement pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9a2c4-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9a2c4-125">Remarks</span></span>

<span data-ttu-id="9a2c4-126">Chaque service fourni par un hôte de service doit disposer de ses propres informations d’élément **hébergé** pour s’assurer que le service est correctement publié dans les réponses aux demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="9a2c4-127">Les éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) sont facultatifs, mais lorsqu’ils sont utilisés, ils doivent être utilisés ensemble.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="9a2c4-128">S’il en existe un, l’autre doit également être présent.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="9a2c4-129">Si un élément [**PnPXDeviceCategory**](pnpxdevicecategory.md) est présent, au moins un élément **hébergé** doit contenir à la fois des éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="9a2c4-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="9a2c4-130">De même, si des éléments **PnPXHardwareId** et **PnPXCompatibleId** sont présents dans un élément **hébergé** , au moins un élément **PnPXDeviceCategory** doit être présent dans l’élément [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="9a2c4-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="9a2c4-131">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9a2c4-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9a2c4-132">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a2c4-132">Minimum supported system</span></span><br/> | <span data-ttu-id="9a2c4-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a2c4-133">Windows Vista</span></span> |
| <span data-ttu-id="9a2c4-134">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="9a2c4-134">Can be empty</span></span>                        | <span data-ttu-id="9a2c4-135">Non</span><span class="sxs-lookup"><span data-stu-id="9a2c4-135">No</span></span>            |



 

 




