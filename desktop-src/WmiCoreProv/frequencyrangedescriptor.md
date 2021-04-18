---
description: Représente un conteneur pour les caractéristiques d’une plage de fréquences prise en charge.
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: FrequencyRangeDescriptor, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: d18bee8a69fd8663ea54973d6e4e8219f5f74e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543082"
---
# <a name="frequencyrangedescriptor-class"></a><span data-ttu-id="25583-103">FrequencyRangeDescriptor, classe</span><span class="sxs-lookup"><span data-stu-id="25583-103">FrequencyRangeDescriptor class</span></span>

<span data-ttu-id="25583-104">La classe WMI **FrequencyRangeDescriptor** représente un conteneur pour les caractéristiques d’une plage de fréquences prise en charge.</span><span class="sxs-lookup"><span data-stu-id="25583-104">The **FrequencyRangeDescriptor** WMI class represents a container for characteristics of a supported frequency range.</span></span> <span data-ttu-id="25583-105">Les instances de cette classe sont des éléments du tableau **MonitorFreqRanges** dans [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span><span class="sxs-lookup"><span data-stu-id="25583-105">Instances of this class are elements of the **MonitorFreqRanges** array in [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="25583-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25583-106">Syntax</span></span>

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a><span data-ttu-id="25583-107">Membres</span><span class="sxs-lookup"><span data-stu-id="25583-107">Members</span></span>

<span data-ttu-id="25583-108">La classe **FrequencyRangeDescriptor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="25583-108">The **FrequencyRangeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="25583-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="25583-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25583-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="25583-110">Properties</span></span>

<span data-ttu-id="25583-111">La classe **FrequencyRangeDescriptor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="25583-111">The **FrequencyRangeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25583-112">**ActiveHeight**</span><span class="sxs-lookup"><span data-stu-id="25583-112">**ActiveHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-115">Hauteur, en pixels, de l’image active.</span><span class="sxs-lookup"><span data-stu-id="25583-115">Height, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="25583-116">**ActiveWidth**</span><span class="sxs-lookup"><span data-stu-id="25583-116">**ActiveWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-117">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-119">Largeur, en pixels, de l’image active.</span><span class="sxs-lookup"><span data-stu-id="25583-119">Width, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="25583-120">**ConstraintType**</span><span class="sxs-lookup"><span data-stu-id="25583-120">**ConstraintType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-121">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-123">Type de contrainte pour la plage de fréquences.</span><span class="sxs-lookup"><span data-stu-id="25583-123">Constraint type for the frequency range.</span></span>

</dd> <dt>

<span data-ttu-id="25583-124">**MaxHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="25583-124">**MaxHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-127">Dénominateur de synchronisation horizontale maximal.</span><span class="sxs-lookup"><span data-stu-id="25583-127">Maximum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="25583-128">**MaxHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="25583-128">**MaxHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-131">Numérateur de synchronisation horizontal maximal en kilohertz (KHz).</span><span class="sxs-lookup"><span data-stu-id="25583-131">Maximum horizontal sync numerator in kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="25583-132">**MaxPixelRate**</span><span class="sxs-lookup"><span data-stu-id="25583-132">**MaxPixelRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-135">Taux de pixels maximal en Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="25583-135">Maximum pixel rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="25583-136">**MaxVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="25583-136">**MaxVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-139">Dénominateur de synchronisation verticale maximale.</span><span class="sxs-lookup"><span data-stu-id="25583-139">Maximum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="25583-140">**MaxVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="25583-140">**MaxVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-143">Numérateur de synchronisation vertical maximal, en Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="25583-143">Maximum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="25583-144">**MinHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="25583-144">**MinHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-147">Dénominateur de synchronisation horizontale minimal.</span><span class="sxs-lookup"><span data-stu-id="25583-147">Minimum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="25583-148">**MinHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="25583-148">**MinHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-151">Numérateur de synchronisation horizontale minimal dans, kilohertz (KHz).</span><span class="sxs-lookup"><span data-stu-id="25583-151">Minimum horizontal sync numerator in, kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="25583-152">**MinVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="25583-152">**MinVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-153">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-155">Dénominateur de synchronisation verticale minimale.</span><span class="sxs-lookup"><span data-stu-id="25583-155">Minimum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="25583-156">**MinVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="25583-156">**MinVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25583-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25583-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-159">Numérateur de synchronisation verticale minimal, en Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="25583-159">Minimum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="25583-160">**Origine**</span><span class="sxs-lookup"><span data-stu-id="25583-160">**Origin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25583-161">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="25583-161">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="25583-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="25583-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25583-163">Lancé.</span><span class="sxs-lookup"><span data-stu-id="25583-163">Origin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25583-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25583-164">Requirements</span></span>



| <span data-ttu-id="25583-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25583-165">Requirement</span></span> | <span data-ttu-id="25583-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="25583-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25583-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25583-167">Minimum supported client</span></span><br/> | <span data-ttu-id="25583-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25583-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="25583-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25583-169">Minimum supported server</span></span><br/> | <span data-ttu-id="25583-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25583-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="25583-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="25583-171">Namespace</span></span><br/>                | <span data-ttu-id="25583-172">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="25583-172">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="25583-173">MOF</span><span class="sxs-lookup"><span data-stu-id="25583-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25583-174"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25583-174"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="25583-175">DLL</span><span class="sxs-lookup"><span data-stu-id="25583-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25583-176"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25583-176"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25583-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25583-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25583-178">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="25583-178">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




