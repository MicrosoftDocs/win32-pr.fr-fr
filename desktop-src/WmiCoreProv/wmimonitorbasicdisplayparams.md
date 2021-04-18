---
description: Représente les fonctionnalités d’affichage de base d’un moniteur d’ordinateur.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: WmiMonitorBasicDisplayParams, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536390"
---
# <a name="wmimonitorbasicdisplayparams-class"></a><span data-ttu-id="60164-103">WmiMonitorBasicDisplayParams, classe</span><span class="sxs-lookup"><span data-stu-id="60164-103">WmiMonitorBasicDisplayParams class</span></span>

<span data-ttu-id="60164-104">La classe WMI **WmiMonitorBasicDisplayParams** représente les fonctionnalités d’affichage de base d’un moniteur d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="60164-104">The **WmiMonitorBasicDisplayParams** WMI class represents the basic display features of a computer monitor.</span></span> <span data-ttu-id="60164-105">La valeur de la propriété **VideoInputType** indique si l’analyse est analogique ou numérique.</span><span class="sxs-lookup"><span data-stu-id="60164-105">The value of the **VideoInputType** property indicates whether the monitor is analog or digital.</span></span> <span data-ttu-id="60164-106">Les données de cette classe correspondent aux données dans le bloc paramètres d’affichage de base/fonctionnalités de la norme E-EDID (Enhanced Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA).</span><span class="sxs-lookup"><span data-stu-id="60164-106">Data in this class corresponds to data in the Basic Display Parameters/Features block of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="60164-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60164-107">Syntax</span></span>

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a><span data-ttu-id="60164-108">Membres</span><span class="sxs-lookup"><span data-stu-id="60164-108">Members</span></span>

<span data-ttu-id="60164-109">La classe **WmiMonitorBasicDisplayParams** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="60164-109">The **WmiMonitorBasicDisplayParams** class has these types of members:</span></span>

-   [<span data-ttu-id="60164-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="60164-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60164-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="60164-111">Properties</span></span>

<span data-ttu-id="60164-112">La classe **WmiMonitorBasicDisplayParams** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="60164-112">The **WmiMonitorBasicDisplayParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60164-113">**Actif**</span><span class="sxs-lookup"><span data-stu-id="60164-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60164-114">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60164-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60164-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60164-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60164-116">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="60164-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="60164-117">**DisplayTransferCharacteristic**</span><span class="sxs-lookup"><span data-stu-id="60164-117">**DisplayTransferCharacteristic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60164-118">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="60164-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="60164-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60164-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60164-120">Affichez les caractéristiques de transfert (100 \* gamma-100).</span><span class="sxs-lookup"><span data-stu-id="60164-120">Display transfer characteristic (100\*Gamma-100).</span></span>

</dd> <dt>

<span data-ttu-id="60164-121">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="60164-121">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60164-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60164-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60164-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60164-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60164-124">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="60164-124">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="60164-125">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="60164-125">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="60164-126">**MaxHorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="60164-126">**MaxHorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60164-127">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="60164-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="60164-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60164-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60164-129">Taille maximale de l’image horizontale en centimètres.</span><span class="sxs-lookup"><span data-stu-id="60164-129">Maximum horizontal image size in centimeters.</span></span> <span data-ttu-id="60164-130">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="60164-130">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="60164-131">**MaxVerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="60164-131">**MaxVerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60164-132">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="60164-132">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="60164-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60164-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60164-134">Taille d’image verticale maximale en centimètres.</span><span class="sxs-lookup"><span data-stu-id="60164-134">Maximum vertical image size in centimeters.</span></span> <span data-ttu-id="60164-135">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="60164-135">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="60164-136">**SupportedDisplayFeatures**</span><span class="sxs-lookup"><span data-stu-id="60164-136">**SupportedDisplayFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60164-137">Type de données : **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span><span class="sxs-lookup"><span data-stu-id="60164-137">Data type: **[**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span></span>
</dt> <dt>

<span data-ttu-id="60164-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60164-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60164-139">Affichez les fonctionnalités prises en charge par l’analyse.</span><span class="sxs-lookup"><span data-stu-id="60164-139">Display features supported by the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="60164-140">**VideoInputType**</span><span class="sxs-lookup"><span data-stu-id="60164-140">**VideoInputType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60164-141">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="60164-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="60164-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60164-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60164-143">Type d’entrée vidéo.</span><span class="sxs-lookup"><span data-stu-id="60164-143">Video input type.</span></span>



| <span data-ttu-id="60164-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="60164-144">Value</span></span>                                                                              | <span data-ttu-id="60164-145">Signification</span><span class="sxs-lookup"><span data-stu-id="60164-145">Meaning</span></span>            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="60164-146"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="60164-146"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="60164-147">Analogique</span><span class="sxs-lookup"><span data-stu-id="60164-147">Analog</span></span><br/>  |
| <dl> <span data-ttu-id="60164-148"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="60164-148"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="60164-149">Digital</span><span class="sxs-lookup"><span data-stu-id="60164-149">Digital</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60164-150">Notes</span><span class="sxs-lookup"><span data-stu-id="60164-150">Remarks</span></span>

<span data-ttu-id="60164-151">**MaxHorizontalImageSize** et **MaxVerticalImageSize** représentent les dimensions d’image maximales que le moniteur peut afficher correctement pour l’ensemble des combinaisons de mise en forme et de minutage prises en charge.</span><span class="sxs-lookup"><span data-stu-id="60164-151">**MaxHorizontalImageSize** and **MaxVerticalImageSize** represent the maximum image dimensions that the monitor can correctly display for the entire set of supported timing and format combinations.</span></span> <span data-ttu-id="60164-152">La dimension image maximale est définie par la norme VESA Video image image Definition (VIAD) et est arrondie au centimètre le plus proche.</span><span class="sxs-lookup"><span data-stu-id="60164-152">The maximum image dimension is defined by VESA Video Image Area Definition (VIAD) Standard and is rounded to the nearest centimeter.</span></span> <span data-ttu-id="60164-153">Le système de l’ordinateur hôte peut utiliser ces données pour sélectionner la taille de l’image et les proportions qui permettront un texte correctement mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="60164-153">The host computer system can use this data to select the image size and aspect ratio that will allow properly scaled text.</span></span> <span data-ttu-id="60164-154">Sachez que, si l’un des champs ou les deux sont nuls, le système n’émet aucune supposition quant à la taille d’affichage.</span><span class="sxs-lookup"><span data-stu-id="60164-154">Be aware that, if either or both of these fields are zero, then the system makes no assumptions about the display size.</span></span> <span data-ttu-id="60164-155">Par exemple, la taille d’un affichage de projection peut être indéterminée.</span><span class="sxs-lookup"><span data-stu-id="60164-155">For example, the size of a projection display may be undetermined.</span></span>

## <a name="requirements"></a><span data-ttu-id="60164-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60164-156">Requirements</span></span>



| <span data-ttu-id="60164-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60164-157">Requirement</span></span> | <span data-ttu-id="60164-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="60164-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60164-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60164-159">Minimum supported client</span></span><br/> | <span data-ttu-id="60164-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60164-160">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="60164-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60164-161">Minimum supported server</span></span><br/> | <span data-ttu-id="60164-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60164-162">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="60164-163">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60164-163">Namespace</span></span><br/>                | <span data-ttu-id="60164-164">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="60164-164">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="60164-165">MOF</span><span class="sxs-lookup"><span data-stu-id="60164-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60164-166"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60164-166"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="60164-167">DLL</span><span class="sxs-lookup"><span data-stu-id="60164-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60164-168"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60164-168"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60164-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60164-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60164-170">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="60164-170">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




