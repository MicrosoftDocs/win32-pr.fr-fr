---
description: Définit les métadonnées du fabricant et du modèle pour l’appareil à implémenter. Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: élément thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872bcdfcf3f93bfc8fe307684c31cdebb2000b05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995336"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="30a7e-104">élément thisModelMetadata</span><span class="sxs-lookup"><span data-stu-id="30a7e-104">thisModelMetadata element</span></span>

<span data-ttu-id="30a7e-105">Définit les métadonnées du fabricant et du modèle pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="30a7e-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="30a7e-106">Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).</span><span class="sxs-lookup"><span data-stu-id="30a7e-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="30a7e-107">Usage</span><span class="sxs-lookup"><span data-stu-id="30a7e-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="30a7e-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="30a7e-108">Attributes</span></span>

<span data-ttu-id="30a7e-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="30a7e-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="30a7e-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="30a7e-110">Child elements</span></span>



| <span data-ttu-id="30a7e-111">Élément</span><span class="sxs-lookup"><span data-stu-id="30a7e-111">Element</span></span>                                                     | <span data-ttu-id="30a7e-112">Description</span><span class="sxs-lookup"><span data-stu-id="30a7e-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30a7e-113">**fécule**</span><span class="sxs-lookup"><span data-stu-id="30a7e-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="30a7e-114">Nom du fabricant.</span><span class="sxs-lookup"><span data-stu-id="30a7e-114">Name of the manufacturer.</span></span> <span data-ttu-id="30a7e-115">Au moins un [**fabricant**](manufacturer.md) ou [**manufacturerLS**](manufacturerls.md) doit être présent dans les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="30a7e-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="30a7e-116">**manufacturerLS**</span><span class="sxs-lookup"><span data-stu-id="30a7e-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="30a7e-117">Version localisée du nom du fabricant.</span><span class="sxs-lookup"><span data-stu-id="30a7e-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="30a7e-118">**manufacturerURL**</span><span class="sxs-lookup"><span data-stu-id="30a7e-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="30a7e-119">Adresse URL du fabricant.</span><span class="sxs-lookup"><span data-stu-id="30a7e-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="30a7e-120">**modelName**</span><span class="sxs-lookup"><span data-stu-id="30a7e-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="30a7e-121">Nom de l'unité.</span><span class="sxs-lookup"><span data-stu-id="30a7e-121">Name of the device.</span></span> <span data-ttu-id="30a7e-122">Au moins l’un des [**modelname**](modelname.md) ou [**modelNameLS**](modelnamels.md) doit être présent dans les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="30a7e-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="30a7e-123">**modelNameLS**</span><span class="sxs-lookup"><span data-stu-id="30a7e-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="30a7e-124">Version localisée du nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="30a7e-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="30a7e-125">**modelNumber**</span><span class="sxs-lookup"><span data-stu-id="30a7e-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="30a7e-126">Numéro de modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="30a7e-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="30a7e-127">**modelURL**</span><span class="sxs-lookup"><span data-stu-id="30a7e-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="30a7e-128">Adresse URL du modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="30a7e-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="30a7e-129">**PnPXDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="30a7e-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="30a7e-130">Catégorie PnP-X à laquelle appartient l’appareil.</span><span class="sxs-lookup"><span data-stu-id="30a7e-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="30a7e-131">**presentationURL**</span><span class="sxs-lookup"><span data-stu-id="30a7e-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="30a7e-132">Adresse URL des données de présentation du modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="30a7e-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="30a7e-133">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="30a7e-133">Child element sequence</span></span>

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a><span data-ttu-id="30a7e-134">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="30a7e-134">Parent elements</span></span>



| <span data-ttu-id="30a7e-135">Élément</span><span class="sxs-lookup"><span data-stu-id="30a7e-135">Element</span></span>                                     | <span data-ttu-id="30a7e-136">Description</span><span class="sxs-lookup"><span data-stu-id="30a7e-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="30a7e-137">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="30a7e-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="30a7e-138">Élément racine d’un fichier de script XML du générateur de code WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="30a7e-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="30a7e-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="30a7e-139">Remarks</span></span>

<span data-ttu-id="30a7e-140">Les métadonnées du fabricant correspondent à la section des métadonnées du fabricant décrite dans le profil de l’appareil (pour plus d’informations, consultez le profil de l’appareil).</span><span class="sxs-lookup"><span data-stu-id="30a7e-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="30a7e-141">Le nom du fabricant ou au moins une version localisée du nom du fabricant doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="30a7e-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="30a7e-142">Le nom du modèle ou au moins une version localisée du nom du modèle doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="30a7e-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="30a7e-143">L’élément [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) est ensuite utilisé pour générer une constante C contenant ces informations.</span><span class="sxs-lookup"><span data-stu-id="30a7e-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="30a7e-144">Si un élément [**PnPXDeviceCategory**](pnpxdevicecategory.md) est présent, au moins un élément [**hébergé**](hosted.md) doit contenir à la fois des éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="30a7e-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="30a7e-145">De même, si des éléments **PnPXHardwareId** et **PnPXCompatibleId** sont présents dans un élément **hébergé** , un élément **PnPXDeviceCategory** doit être présent dans l’élément **thisModelMetadata** .</span><span class="sxs-lookup"><span data-stu-id="30a7e-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="30a7e-146">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="30a7e-146">Element information</span></span>



| <span data-ttu-id="30a7e-147">Étiquette</span><span class="sxs-lookup"><span data-stu-id="30a7e-147">Label</span></span> | <span data-ttu-id="30a7e-148">Value</span><span class="sxs-lookup"><span data-stu-id="30a7e-148">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="30a7e-149">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30a7e-149">Minimum supported system</span></span><br/> | <span data-ttu-id="30a7e-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30a7e-150">Windows Vista</span></span> |
| <span data-ttu-id="30a7e-151">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="30a7e-151">Can be empty</span></span>                        | <span data-ttu-id="30a7e-152">Non</span><span class="sxs-lookup"><span data-stu-id="30a7e-152">No</span></span>            |



 

 




