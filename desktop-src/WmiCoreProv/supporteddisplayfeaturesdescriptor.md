---
description: Représente les fonctionnalités d’affichage prises en charge de l’analyse.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: SupportedDisplayFeaturesDescriptor, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524510"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a><span data-ttu-id="aee02-103">SupportedDisplayFeaturesDescriptor, classe</span><span class="sxs-lookup"><span data-stu-id="aee02-103">SupportedDisplayFeaturesDescriptor class</span></span>

<span data-ttu-id="aee02-104">Le **SupportedDisplayFeaturesDescriptor** représente les fonctionnalités d’affichage prises en charge de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="aee02-104">The **SupportedDisplayFeaturesDescriptor** represents the supported display features of the monitor.</span></span> <span data-ttu-id="aee02-105">Les informations contenues dans cette classe correspondent aux données de la définition d’entrée vidéo de la norme E-EDID (Extended Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA).</span><span class="sxs-lookup"><span data-stu-id="aee02-105">The information in this class corresponds to data in the Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee02-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aee02-106">Syntax</span></span>

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a><span data-ttu-id="aee02-107">Membres</span><span class="sxs-lookup"><span data-stu-id="aee02-107">Members</span></span>

<span data-ttu-id="aee02-108">La classe **SupportedDisplayFeaturesDescriptor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aee02-108">The **SupportedDisplayFeaturesDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="aee02-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aee02-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aee02-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aee02-110">Properties</span></span>

<span data-ttu-id="aee02-111">La classe **SupportedDisplayFeaturesDescriptor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="aee02-111">The **SupportedDisplayFeaturesDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aee02-112">**ActiveOffSupported**</span><span class="sxs-lookup"><span data-stu-id="aee02-112">**ActiveOffSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee02-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aee02-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aee02-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aee02-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee02-115">Prise en charge d’une alimentation active et très faible.</span><span class="sxs-lookup"><span data-stu-id="aee02-115">Support for active off and very low power.</span></span> <span data-ttu-id="aee02-116">L’affichage consomme moins d’énergie lorsqu’il reçoit un signal de minutage qui est en dehors de la plage de fonctionnement active déclarée.</span><span class="sxs-lookup"><span data-stu-id="aee02-116">The display consumes less power when it receives a timing signal that is outside the declared active operating range.</span></span> <span data-ttu-id="aee02-117">L’affichage est rétabli en mode de fonctionnement normal si le signal de minutage revient à la plage de fonctionnement normale.</span><span class="sxs-lookup"><span data-stu-id="aee02-117">The display will revert to normal operation if the timing signal returns to the normal operating range.</span></span> <span data-ttu-id="aee02-118">Les signaux de synchronisation en dehors de la plage de fonctionnement normale ne sont pas des signaux de synchronisation ou aucun signal.</span><span class="sxs-lookup"><span data-stu-id="aee02-118">Examples of timing signals outside the normal operating range are no sync signals or no DE signal.</span></span>

</dd> <dt>

<span data-ttu-id="aee02-119">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="aee02-119">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee02-120">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="aee02-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aee02-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aee02-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee02-122">Type d’affichage de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="aee02-122">Type of display for the monitor.</span></span> <span data-ttu-id="aee02-123">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="aee02-123">The following table lists possible values.</span></span>



| <span data-ttu-id="aee02-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee02-124">Value</span></span>                                                                              | <span data-ttu-id="aee02-125">Signification</span><span class="sxs-lookup"><span data-stu-id="aee02-125">Meaning</span></span>                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="aee02-126"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="aee02-126"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="aee02-127">Affichage monochrome/nuances de gris</span><span class="sxs-lookup"><span data-stu-id="aee02-127">Monochrome/grayscale display</span></span><br/> |
| <dl> <span data-ttu-id="aee02-128"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="aee02-128"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="aee02-129">Affichage des couleurs RVB</span><span class="sxs-lookup"><span data-stu-id="aee02-129">RGB color display</span></span><br/>            |
| <dl> <span data-ttu-id="aee02-130"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="aee02-130"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="aee02-131">Affichage des couleurs non RVB</span><span class="sxs-lookup"><span data-stu-id="aee02-131">Non-RGB multicolor display</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="aee02-132">**GTFSupported**</span><span class="sxs-lookup"><span data-stu-id="aee02-132">**GTFSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee02-133">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aee02-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aee02-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aee02-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee02-135">Indique si l’affichage est pris en charge par GTF.</span><span class="sxs-lookup"><span data-stu-id="aee02-135">Indicates whether the display has GTF support.</span></span> <span data-ttu-id="aee02-136">Si la **valeur est true**, l’affichage prend en charge les minutages basés sur la norme GTF à l’aide des valeurs de paramètre GTF par défaut.</span><span class="sxs-lookup"><span data-stu-id="aee02-136">If **True**, the display supports timings based on the GTF standard using default GTF parameter values.</span></span>

</dd> <dt>

<span data-ttu-id="aee02-137">**HasPreferredTimingMode**</span><span class="sxs-lookup"><span data-stu-id="aee02-137">**HasPreferredTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee02-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aee02-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aee02-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aee02-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee02-140">Indique si l’affichage a un mode de minutage préféré.</span><span class="sxs-lookup"><span data-stu-id="aee02-140">Indicates whether the display has has a preferred timing mode.</span></span> <span data-ttu-id="aee02-141">Si la **valeur est true**, le premier bloc de synchronisation détaillé contient le mode de minutage préféré du moniteur.</span><span class="sxs-lookup"><span data-stu-id="aee02-141">If **True**, the first detailed timing block contains the preferred timing mode of the monitor.</span></span> <span data-ttu-id="aee02-142">L’utilisation du mode de minutage préféré est requise par EDID v. 1.3 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="aee02-142">Use of preferred timing mode is required by EDID v.1.3 and higher.</span></span>

</dd> <dt>

<span data-ttu-id="aee02-143">**sRGBSupported**</span><span class="sxs-lookup"><span data-stu-id="aee02-143">**sRGBSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee02-144">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aee02-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aee02-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aee02-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee02-146">Si la **valeur est true**, l’affichage prend en charge sRVB.</span><span class="sxs-lookup"><span data-stu-id="aee02-146">If **True**, the display supports sRGB.</span></span>

</dd> <dt>

<span data-ttu-id="aee02-147">**StandbySupported**</span><span class="sxs-lookup"><span data-stu-id="aee02-147">**StandbySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee02-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aee02-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aee02-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aee02-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee02-150">Indique si l’affichage prend en charge la mise en veille de la gestion de l’alimentation de l’affichage VESA (DPMS).</span><span class="sxs-lookup"><span data-stu-id="aee02-150">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) standby.</span></span> <span data-ttu-id="aee02-151">Si la **valeur est true**, la mise en veille DPMS est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="aee02-151">If **True**, DPMS standby is supported.</span></span>

</dd> <dt>

<span data-ttu-id="aee02-152">**SuspendSupported**</span><span class="sxs-lookup"><span data-stu-id="aee02-152">**SuspendSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee02-153">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aee02-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aee02-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aee02-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee02-155">Indique si l’affichage prend en charge l’interruption de la gestion de l’alimentation de l’affichage VESA (DPMS).</span><span class="sxs-lookup"><span data-stu-id="aee02-155">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) suspend.</span></span> <span data-ttu-id="aee02-156">Si la **valeur est true**, DPMS suspend est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="aee02-156">If **True**, DPMS suspend is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aee02-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aee02-157">Requirements</span></span>



| <span data-ttu-id="aee02-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aee02-158">Requirement</span></span> | <span data-ttu-id="aee02-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee02-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aee02-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aee02-160">Minimum supported client</span></span><br/> | <span data-ttu-id="aee02-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee02-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aee02-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aee02-162">Minimum supported server</span></span><br/> | <span data-ttu-id="aee02-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aee02-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aee02-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aee02-164">Namespace</span></span><br/>                | <span data-ttu-id="aee02-165">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="aee02-165">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="aee02-166">MOF</span><span class="sxs-lookup"><span data-stu-id="aee02-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aee02-167"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aee02-167"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="aee02-168">DLL</span><span class="sxs-lookup"><span data-stu-id="aee02-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aee02-169"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee02-169"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee02-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aee02-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee02-171">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="aee02-171">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




