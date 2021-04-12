---
description: Contient des éléments de descripteur de mode pour le tableau MonitorSourceModes dans la classe WmiMonitorListedSupportedSourceModes.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: VideoModeDescriptor, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320346"
---
# <a name="videomodedescriptor-class"></a><span data-ttu-id="d32f0-103">VideoModeDescriptor, classe</span><span class="sxs-lookup"><span data-stu-id="d32f0-103">VideoModeDescriptor class</span></span>

<span data-ttu-id="d32f0-104">La classe WMI **VideoModeDescriptorVideo** contient des éléments de descripteur de mode pour le tableau **MonitorSourceModes** dans la classe [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) .</span><span class="sxs-lookup"><span data-stu-id="d32f0-104">The **VideoModeDescriptorVideo** WMI class contains mode descriptor elements for the **MonitorSourceModes** array in the [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) class.</span></span> <span data-ttu-id="d32f0-105">Ces éléments incluent des fonctionnalités de surveillance telles que la fréquence de rafraîchissement, les caractéristiques des pixels ou la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="d32f0-105">These elements include monitor features such as refresh rate, pixel characteristics, or image size.</span></span> <span data-ttu-id="d32f0-106">La classe **VideoModeDescriptorVideo** contient des informations qui sont un sur-ensemble des données disponibles à partir de blocs de synchronisation établis, standard et détaillés.</span><span class="sxs-lookup"><span data-stu-id="d32f0-106">The **VideoModeDescriptorVideo** class contains information that is a superset of the data available from established, standard, and detailed timing blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="d32f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d32f0-107">Syntax</span></span>

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a><span data-ttu-id="d32f0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d32f0-108">Members</span></span>

<span data-ttu-id="d32f0-109">La classe **VideoModeDescriptor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d32f0-109">The **VideoModeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="d32f0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d32f0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d32f0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d32f0-111">Properties</span></span>

<span data-ttu-id="d32f0-112">La classe **VideoModeDescriptor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d32f0-112">The **VideoModeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d32f0-113">**CompositePolarityType**</span><span class="sxs-lookup"><span data-stu-id="d32f0-113">**CompositePolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-114">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d32f0-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-116">Type de polarité composite.</span><span class="sxs-lookup"><span data-stu-id="d32f0-116">Composite polarity type.</span></span> <span data-ttu-id="d32f0-117">Il s’agit de la polarité des impulsions de synchronisation horizontale en dehors de la synchronisation verticale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-117">This is polarity of horizontal sync pulses outside of vertical sync.</span></span>



| <span data-ttu-id="d32f0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d32f0-118">Value</span></span>                                                                              | <span data-ttu-id="d32f0-119">Signification</span><span class="sxs-lookup"><span data-stu-id="d32f0-119">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d32f0-120"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-120"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d32f0-121">La polarité composite est positive.</span><span class="sxs-lookup"><span data-stu-id="d32f0-121">Composite polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d32f0-122"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-122"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="d32f0-123">La polarité composite est négative.</span><span class="sxs-lookup"><span data-stu-id="d32f0-123">Composite polarity is negative.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d32f0-124"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-124"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="d32f0-125">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="d32f0-125">Not applicable.</span></span> <span data-ttu-id="d32f0-126">Le type de synchronisation de signal doit être numérique composite.</span><span class="sxs-lookup"><span data-stu-id="d32f0-126">The signal sync type must be digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d32f0-127">**HorizontalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="d32f0-127">**HorizontalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-130">Nombre de pixels actifs horizontalement.</span><span class="sxs-lookup"><span data-stu-id="d32f0-130">Number of horizontally active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-131">**HorizontalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="d32f0-131">**HorizontalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-132">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-134">Nombre de pixels à blanc horizontal</span><span class="sxs-lookup"><span data-stu-id="d32f0-134">Number of horizontally blanking pixels</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-135">**HorizontalBorder**</span><span class="sxs-lookup"><span data-stu-id="d32f0-135">**HorizontalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-136">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-138">Bordure horizontale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-138">Horizontal border.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-139">**HorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="d32f0-139">**HorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-142">Taille de l’image horizontale en millimètres (mm).</span><span class="sxs-lookup"><span data-stu-id="d32f0-142">Horizontal image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-143">**HorizontalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="d32f0-143">**HorizontalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-144">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d32f0-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-146">Type de polarité horizontale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-146">Horizontal polarity type.</span></span>



| <span data-ttu-id="d32f0-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="d32f0-147">Value</span></span>                                                                              | <span data-ttu-id="d32f0-148">Signification</span><span class="sxs-lookup"><span data-stu-id="d32f0-148">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d32f0-149"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-149"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d32f0-150">La polarité horizontale est positive.</span><span class="sxs-lookup"><span data-stu-id="d32f0-150">Horizontal polarity is positive.</span></span><br/>                               |
| <dl> <span data-ttu-id="d32f0-151"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-151"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="d32f0-152">La polarité horizontale est négative.</span><span class="sxs-lookup"><span data-stu-id="d32f0-152">Horizontal polarity is negative.</span></span><br/>                               |
| <dl> <span data-ttu-id="d32f0-153"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-153"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="d32f0-154">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="d32f0-154">Not applicable.</span></span> <span data-ttu-id="d32f0-155">Le type de synchronisation de signal doit être séparé par un numérique.</span><span class="sxs-lookup"><span data-stu-id="d32f0-155">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d32f0-156">**HorizontalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="d32f0-156">**HorizontalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-157">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-159">Dénominateur du taux de rafraîchissement horizontal.</span><span class="sxs-lookup"><span data-stu-id="d32f0-159">Horizontal refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-160">**HorizontalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="d32f0-160">**HorizontalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-161">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-163">Numérateur du taux de rafraîchissement horizontal en Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="d32f0-163">Horizontal refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-164">**HorizontalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="d32f0-164">**HorizontalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-167">Décalage de synchronisation horizontale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-167">Horizontal sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-168">**HorizontalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="d32f0-168">**HorizontalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-169">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-171">Largeur d’impulsion de synchronisation horizontale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-171">Horizontal sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-172">**IsInterlaced**</span><span class="sxs-lookup"><span data-stu-id="d32f0-172">**IsInterlaced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-173">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d32f0-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-175">Indique si le mode d’affichage est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="d32f0-175">Indicates whether the display mode is interlaced.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-176">**IsSerrationRequired**</span><span class="sxs-lookup"><span data-stu-id="d32f0-176">**IsSerrationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-177">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d32f0-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-179">Indique le type de serration requis, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d32f0-179">Indicates what type of serration is required, if appropriate.</span></span>



| <span data-ttu-id="d32f0-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="d32f0-180">Value</span></span>                                                                              | <span data-ttu-id="d32f0-181">Signification</span><span class="sxs-lookup"><span data-stu-id="d32f0-181">Meaning</span></span>                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d32f0-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d32f0-183">Le contrôleur doit fournir une synchronisation horizontale pendant la synchronisation verticale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-183">Controller shall supply horizontal sync during vertical sync.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d32f0-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="d32f0-185">Le contrôleur ne doit pas fournir de synchronisation horizontale pendant la synchronisation verticale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-185">Controller shall not supply horizontal sync during vertical sync.</span></span><br/>                             |
| <dl> <span data-ttu-id="d32f0-186"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-186"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="d32f0-187">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="d32f0-187">Not applicable.</span></span> <span data-ttu-id="d32f0-188">Le type de synchronisation de signal doit être bipolaire, composite analogique ou composite numérique.</span><span class="sxs-lookup"><span data-stu-id="d32f0-188">The signal sync type must be bipolar, analog composite, or digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d32f0-189">**IsSyncOnRGB**</span><span class="sxs-lookup"><span data-stu-id="d32f0-189">**IsSyncOnRGB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-190">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d32f0-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-192">Indique les lignes de signal vidéo à synchroniser, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d32f0-192">Indicates which video signal lines should be synchronized, if appropriate.</span></span>



| <span data-ttu-id="d32f0-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="d32f0-193">Value</span></span>                                                                              | <span data-ttu-id="d32f0-194">Signification</span><span class="sxs-lookup"><span data-stu-id="d32f0-194">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d32f0-195"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-195"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d32f0-196">L’impulsion de synchronisation doit apparaître sur les 3 lignes de signal vidéo.</span><span class="sxs-lookup"><span data-stu-id="d32f0-196">Sync pulse should appear on all 3 video signal lines.</span></span><br/>                  |
| <dl> <span data-ttu-id="d32f0-197"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-197"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="d32f0-198">L’impulsion de synchronisation doit apparaître uniquement sur la ligne de signal vidéo verte.</span><span class="sxs-lookup"><span data-stu-id="d32f0-198">Sync pulse should only appear on the green video signal line.</span></span><br/>          |
| <dl> <span data-ttu-id="d32f0-199"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-199"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="d32f0-200">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="d32f0-200">Not applicable.</span></span> <span data-ttu-id="d32f0-201">Le type de synchronisation de signal doit être composite analogique bipolaire.</span><span class="sxs-lookup"><span data-stu-id="d32f0-201">The signal sync type must be bipolar analog composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d32f0-202">**PixelClockRate**</span><span class="sxs-lookup"><span data-stu-id="d32f0-202">**PixelClockRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-203">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d32f0-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-205">Fréquence d’horloge en Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="d32f0-205">Pixel clock rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-206">**StereoModeType**</span><span class="sxs-lookup"><span data-stu-id="d32f0-206">**StereoModeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-207">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d32f0-207">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-209">Type de mode stéréo.</span><span class="sxs-lookup"><span data-stu-id="d32f0-209">Stereo mode type.</span></span> <span data-ttu-id="d32f0-210">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="d32f0-210">The following table lists the possible values.</span></span>



| <span data-ttu-id="d32f0-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="d32f0-211">Value</span></span>                                                                              | <span data-ttu-id="d32f0-212">Signification</span><span class="sxs-lookup"><span data-stu-id="d32f0-212">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="d32f0-213"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-213"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d32f0-214">Pas de stéréo.</span><span class="sxs-lookup"><span data-stu-id="d32f0-214">No stereo.</span></span><br/>                                               |
| <dl> <span data-ttu-id="d32f0-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-215"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="d32f0-216">Champ stéréo séquentiel avec image de droite sur synchronisation stéréo.</span><span class="sxs-lookup"><span data-stu-id="d32f0-216">Field sequential stereo with right image on stereo sync.</span></span><br/> |
| <dl> <span data-ttu-id="d32f0-217"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-217"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="d32f0-218">Champ stéréo séquentiel avec image de gauche sur synchronisation stéréo.</span><span class="sxs-lookup"><span data-stu-id="d32f0-218">Field sequential stereo with left image on stereo sync.</span></span><br/>  |
| <dl> <span data-ttu-id="d32f0-219"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-219"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="d32f0-220">Stéréo entrelacée bidirectionnelle avec image de droite sur les lignes paires.</span><span class="sxs-lookup"><span data-stu-id="d32f0-220">2-way Interleaved Stereo with Right Image on Even Lines.</span></span><br/> |
| <dl> <span data-ttu-id="d32f0-221"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-221"><dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="d32f0-222">Stéréo entrelacée bidirectionnelle avec image de gauche sur les lignes paires.</span><span class="sxs-lookup"><span data-stu-id="d32f0-222">2-way Interleaved Stereo with Left Image on Even Lines.</span></span><br/>  |
| <dl> <span data-ttu-id="d32f0-223"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-223"><dt>5 (0x5)</dt></span></span> </dl> | <span data-ttu-id="d32f0-224">Stéréo entrelacée à 4 voies.</span><span class="sxs-lookup"><span data-stu-id="d32f0-224">4-way Interleaved Stereo.</span></span><br/>                                |
| <dl> <span data-ttu-id="d32f0-225"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-225"><dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="d32f0-226">Stéréo entrelacée côte à côte.</span><span class="sxs-lookup"><span data-stu-id="d32f0-226">Side-by-Side Interleaved Stereo.</span></span><br/>                         |



 

</dd> <dt>

<span data-ttu-id="d32f0-227">**SyncSignalType**</span><span class="sxs-lookup"><span data-stu-id="d32f0-227">**SyncSignalType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-228">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d32f0-228">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-230">Type de synchronisation de signal.</span><span class="sxs-lookup"><span data-stu-id="d32f0-230">Signal sync type.</span></span> <span data-ttu-id="d32f0-231">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="d32f0-231">The following table lists the possible values.</span></span>



| <span data-ttu-id="d32f0-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="d32f0-232">Value</span></span>                                                                              | <span data-ttu-id="d32f0-233">Signification</span><span class="sxs-lookup"><span data-stu-id="d32f0-233">Meaning</span></span>                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="d32f0-234"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-234"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d32f0-235">Composite analogique</span><span class="sxs-lookup"><span data-stu-id="d32f0-235">Analog Composite</span></span><br/>         |
| <dl> <span data-ttu-id="d32f0-236"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-236"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="d32f0-237">Composite analogique bipolaire</span><span class="sxs-lookup"><span data-stu-id="d32f0-237">Bipolar Analog Composite</span></span><br/> |
| <dl> <span data-ttu-id="d32f0-238"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-238"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="d32f0-239">Composite numérique</span><span class="sxs-lookup"><span data-stu-id="d32f0-239">Digital Composite</span></span><br/>        |
| <dl> <span data-ttu-id="d32f0-240"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-240"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="d32f0-241">Séparation numérique</span><span class="sxs-lookup"><span data-stu-id="d32f0-241">Digital Separate</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="d32f0-242">**VerticalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="d32f0-242">**VerticalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-243">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-245">Nombre de pixels actifs verticalement.</span><span class="sxs-lookup"><span data-stu-id="d32f0-245">Number of vertically active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-246">**VerticalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="d32f0-246">**VerticalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-247">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-249">Nombre de pixels à espacement horizontal.</span><span class="sxs-lookup"><span data-stu-id="d32f0-249">Number of vertically blanking pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-250">**VerticalBorder**</span><span class="sxs-lookup"><span data-stu-id="d32f0-250">**VerticalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-251">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-253">Bordure verticale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-253">Vertical border.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-254">**VerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="d32f0-254">**VerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-255">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-257">Taille de l’image verticale en millimètres (mm).</span><span class="sxs-lookup"><span data-stu-id="d32f0-257">Vertical image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-258">**VerticalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="d32f0-258">**VerticalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-259">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d32f0-259">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-261">Type de polarité verticale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-261">Vertical polarity type.</span></span>



| <span data-ttu-id="d32f0-262">Valeur</span><span class="sxs-lookup"><span data-stu-id="d32f0-262">Value</span></span>                                                                              | <span data-ttu-id="d32f0-263">Signification</span><span class="sxs-lookup"><span data-stu-id="d32f0-263">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d32f0-264"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-264"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d32f0-265">La polarité verticale est positive.</span><span class="sxs-lookup"><span data-stu-id="d32f0-265">Vertical polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d32f0-266"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-266"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="d32f0-267">La polarité verticale est négative</span><span class="sxs-lookup"><span data-stu-id="d32f0-267">Vertical polarity is negative</span></span><br/>                                  |
| <dl> <span data-ttu-id="d32f0-268"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-268"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="d32f0-269">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="d32f0-269">Not applicable.</span></span> <span data-ttu-id="d32f0-270">Le type de synchronisation de signal doit être séparé par un numérique.</span><span class="sxs-lookup"><span data-stu-id="d32f0-270">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d32f0-271">**VerticalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="d32f0-271">**VerticalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-272">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-274">Dénominateur de la fréquence d’actualisation verticale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-274">Vertical refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-275">**VerticalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="d32f0-275">**VerticalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-276">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-278">Numérateur de fréquence d’actualisation verticale en Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="d32f0-278">Vertical refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-279">**VerticalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="d32f0-279">**VerticalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-280">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-282">Décalage de synchronisation verticale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-282">Vertical sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-283">**VerticalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="d32f0-283">**VerticalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-284">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d32f0-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-286">Largeur d’impulsion de synchronisation verticale.</span><span class="sxs-lookup"><span data-stu-id="d32f0-286">Vertical sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="d32f0-287">VideoStandardType</span><span class="sxs-lookup"><span data-stu-id="d32f0-287">VideoStandardType</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d32f0-288">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d32f0-288">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d32f0-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d32f0-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d32f0-290">Type de vidéo standard.</span><span class="sxs-lookup"><span data-stu-id="d32f0-290">Video standard type.</span></span>



| <span data-ttu-id="d32f0-291">Valeur</span><span class="sxs-lookup"><span data-stu-id="d32f0-291">Value</span></span>                                                                                | <span data-ttu-id="d32f0-292">Signification</span><span class="sxs-lookup"><span data-stu-id="d32f0-292">Meaning</span></span>                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d32f0-293"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-293"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-294">Autres</span><span class="sxs-lookup"><span data-stu-id="d32f0-294">Other</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="d32f0-295"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-295"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-296">VESA DMT.</span><span class="sxs-lookup"><span data-stu-id="d32f0-296">VESA DMT.</span></span> <span data-ttu-id="d32f0-297">À partir de Video Electronics standard Association (VESA), affichez la spécification des minutages de moniteur.</span><span class="sxs-lookup"><span data-stu-id="d32f0-297">From Video Electronics Standard Association (VESA) Display Monitor Timings specification.</span></span><br/> |
| <dl> <span data-ttu-id="d32f0-298"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-298"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-299">GTF VESA.</span><span class="sxs-lookup"><span data-stu-id="d32f0-299">VESA GTF.</span></span> <span data-ttu-id="d32f0-300">À partir de la norme de formule de minutage généralisée VESA.</span><span class="sxs-lookup"><span data-stu-id="d32f0-300">From VESA Generalized Timing Formula standard.</span></span><br/>                                            |
| <dl> <span data-ttu-id="d32f0-301"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-301"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-302">VESA CVT/à partir de la norme des minutages vidéo coordonné VESA.</span><span class="sxs-lookup"><span data-stu-id="d32f0-302">VESA CVT/ From VESA Coordinated Video Timings standard.</span></span><br/>                                             |
| <dl> <span data-ttu-id="d32f0-303"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-303"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-304">IBM</span><span class="sxs-lookup"><span data-stu-id="d32f0-304">IBM</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="d32f0-305"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-305"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-306">pomme</span><span class="sxs-lookup"><span data-stu-id="d32f0-306">APPLE</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="d32f0-307"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-307"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-308">NTSC M</span><span class="sxs-lookup"><span data-stu-id="d32f0-308">NTSC M</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d32f0-309"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-309"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-310">NTSC J</span><span class="sxs-lookup"><span data-stu-id="d32f0-310">NTSC J</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d32f0-311"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-311"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-312">NTSC 433</span><span class="sxs-lookup"><span data-stu-id="d32f0-312">NTSC 433</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="d32f0-313"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-313"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="d32f0-314">PAL B</span><span class="sxs-lookup"><span data-stu-id="d32f0-314">PAL B</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="d32f0-315"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-315"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="d32f0-316">PAL B1</span><span class="sxs-lookup"><span data-stu-id="d32f0-316">PAL B1</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d32f0-317"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-317"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="d32f0-318">PAL G</span><span class="sxs-lookup"><span data-stu-id="d32f0-318">PAL G</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="d32f0-319"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-319"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="d32f0-320">PAL H</span><span class="sxs-lookup"><span data-stu-id="d32f0-320">PAL H</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="d32f0-321"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-321"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="d32f0-322">PAL I</span><span class="sxs-lookup"><span data-stu-id="d32f0-322">PAL I</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="d32f0-323"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-323"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="d32f0-324">PAL D</span><span class="sxs-lookup"><span data-stu-id="d32f0-324">PAL D</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="d32f0-325"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-325"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="d32f0-326">PAL N</span><span class="sxs-lookup"><span data-stu-id="d32f0-326">PAL N</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="d32f0-327"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-327"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="d32f0-328">CONTEXTE DE NOMMAGE PAL</span><span class="sxs-lookup"><span data-stu-id="d32f0-328">PAL NC</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d32f0-329"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-329"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="d32f0-330">SECAM B</span><span class="sxs-lookup"><span data-stu-id="d32f0-330">SECAM B</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d32f0-331"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-331"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="d32f0-332">SECAM D</span><span class="sxs-lookup"><span data-stu-id="d32f0-332">SECAM D</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d32f0-333"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-333"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="d32f0-334">SECAM G</span><span class="sxs-lookup"><span data-stu-id="d32f0-334">SECAM G</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d32f0-335"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-335"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="d32f0-336">SECAM H</span><span class="sxs-lookup"><span data-stu-id="d32f0-336">SECAM H</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d32f0-337"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-337"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="d32f0-338">SECAM K</span><span class="sxs-lookup"><span data-stu-id="d32f0-338">SECAM K</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d32f0-339"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-339"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="d32f0-340">SECAM K1</span><span class="sxs-lookup"><span data-stu-id="d32f0-340">SECAM K1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="d32f0-341"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-341"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="d32f0-342">SECAM L</span><span class="sxs-lookup"><span data-stu-id="d32f0-342">SECAM L</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d32f0-343"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-343"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="d32f0-344">SECAM L1</span><span class="sxs-lookup"><span data-stu-id="d32f0-344">SECAM L1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="d32f0-345"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-345"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="d32f0-346">EIA861</span><span class="sxs-lookup"><span data-stu-id="d32f0-346">EIA861</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d32f0-347"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-347"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="d32f0-348">EIA861A</span><span class="sxs-lookup"><span data-stu-id="d32f0-348">EIA861A</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d32f0-349"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-349"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="d32f0-350">EIA861B</span><span class="sxs-lookup"><span data-stu-id="d32f0-350">EIA861B</span></span><br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d32f0-351">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d32f0-351">Requirements</span></span>



| <span data-ttu-id="d32f0-352">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d32f0-352">Requirement</span></span> | <span data-ttu-id="d32f0-353">Valeur</span><span class="sxs-lookup"><span data-stu-id="d32f0-353">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d32f0-354">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d32f0-354">Minimum supported client</span></span><br/> | <span data-ttu-id="d32f0-355">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d32f0-355">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d32f0-356">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d32f0-356">Minimum supported server</span></span><br/> | <span data-ttu-id="d32f0-357">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d32f0-357">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d32f0-358">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d32f0-358">Namespace</span></span><br/>                | <span data-ttu-id="d32f0-359">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="d32f0-359">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="d32f0-360">MOF</span><span class="sxs-lookup"><span data-stu-id="d32f0-360">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d32f0-361"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-361"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="d32f0-362">DLL</span><span class="sxs-lookup"><span data-stu-id="d32f0-362">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d32f0-363"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d32f0-363"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d32f0-364">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d32f0-364">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d32f0-365">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="d32f0-365">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




