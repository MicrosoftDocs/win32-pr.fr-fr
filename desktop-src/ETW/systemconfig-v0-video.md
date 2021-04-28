---
description: 'Classe SystemConfig_V0_Video : cette classe est la classe de type d’événement pour les événements de configuration vidéo.'
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: Classe SystemConfig_V0_Video
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 94fb9e50344cfbdde4be67815b80e4074ab1a878
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105917"
---
# <a name="systemconfig_v0_video-class"></a><span data-ttu-id="15595-103">\_ \_ Classe vidéo SystemConfig v0</span><span class="sxs-lookup"><span data-stu-id="15595-103">SystemConfig\_V0\_Video class</span></span>

<span data-ttu-id="15595-104">Cette classe est la classe de type d’événement pour les événements de configuration vidéo.</span><span class="sxs-lookup"><span data-stu-id="15595-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="15595-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="15595-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="15595-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15595-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a><span data-ttu-id="15595-107">Membres</span><span class="sxs-lookup"><span data-stu-id="15595-107">Members</span></span>

<span data-ttu-id="15595-108">La **classe \_ \_ vidéo SystemConfig v0** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="15595-108">The **SystemConfig\_V0\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="15595-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15595-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15595-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15595-110">Properties</span></span>

<span data-ttu-id="15595-111">La **classe \_ \_ vidéo SystemConfig v0** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="15595-111">The **SystemConfig\_V0\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15595-112">**AdapterString**</span><span class="sxs-lookup"><span data-stu-id="15595-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-113">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="15595-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="15595-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-115">Qualificateurs : **WmiDataId** (8), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="15595-115">Qualifiers: **WmiDataId** (8), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="15595-116">Nom ou description de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="15595-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="15595-117">**BiosString**</span><span class="sxs-lookup"><span data-stu-id="15595-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-118">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="15595-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="15595-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-120">Qualificateurs : **WmiDataId** (9), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="15595-120">Qualifiers: **WmiDataId** (9), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="15595-121">Nom du BIOS de la carte.</span><span class="sxs-lookup"><span data-stu-id="15595-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="15595-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="15595-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-123">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15595-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15595-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-125">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="15595-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="15595-126">Nombre de bits utilisés pour afficher chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="15595-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="15595-127">**ChipType**</span><span class="sxs-lookup"><span data-stu-id="15595-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-128">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="15595-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="15595-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-130">Qualificateurs : **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="15595-130">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="15595-131">Nom de la carte.</span><span class="sxs-lookup"><span data-stu-id="15595-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="15595-132">**DACType**</span><span class="sxs-lookup"><span data-stu-id="15595-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-133">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="15595-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="15595-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-135">Qualificateurs : **WmiDataId** (7), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="15595-135">Qualifiers: **WmiDataId** (7), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="15595-136">Nom de la puce de conversion numérique-analogique (DAC) de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="15595-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="15595-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="15595-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-138">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="15595-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="15595-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-140">Qualificateurs : **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="15595-140">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="15595-141">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="15595-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="15595-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="15595-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15595-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15595-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-145">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="15595-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="15595-146">Quantité maximale de mémoire prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="15595-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="15595-147">**StateFlags**</span><span class="sxs-lookup"><span data-stu-id="15595-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15595-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15595-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-150">Qualificateurs : **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="15595-150">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="15595-151">Indicateurs d’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="15595-151">Device state flags.</span></span> <span data-ttu-id="15595-152">Il peut s’agir d’une combinaison raisonnable des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="15595-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="15595-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="15595-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="15595-154">Signification</span><span class="sxs-lookup"><span data-stu-id="15595-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="15595-155"><dt>**Afficher \_ APPAREIL \_ attaché \_ au \_ Bureau**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="15595-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="15595-156">L’appareil fait partie du bureau.</span><span class="sxs-lookup"><span data-stu-id="15595-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="15595-157"><dt>**Afficher \_ \_ \_ Pilote de mise en miroir des appareils**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="15595-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="15595-158">Représente un Pseudo-appareil utilisé pour mettre en miroir le dessin d’application pour se connecter à un ordinateur distant ou à d’autres fins.</span><span class="sxs-lookup"><span data-stu-id="15595-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="15595-159">Un Pseudo-analyse invisible est associé à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="15595-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="15595-160">Par exemple, NetMeeting l’utilise.</span><span class="sxs-lookup"><span data-stu-id="15595-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="15595-161"><dt>**Afficher \_ \_MODESPRUNED d’appareil**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="15595-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="15595-162">L’appareil a plus de modes d’affichage que la prise en charge de ses appareils de sortie.</span><span class="sxs-lookup"><span data-stu-id="15595-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="15595-163"><dt>**Afficher \_ \_ \_ Périphérique principal**</dt> de l’appareil <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="15595-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="15595-164">Le bureau principal se trouve sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="15595-164">The primary desktop is on the device.</span></span> <span data-ttu-id="15595-165">Pour un système avec une carte d’affichage unique, cette valeur est toujours définie.</span><span class="sxs-lookup"><span data-stu-id="15595-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="15595-166">Pour un système avec plusieurs cartes d’affichage, un seul appareil peut avoir cet ensemble.</span><span class="sxs-lookup"><span data-stu-id="15595-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="15595-167"><dt>**Afficher \_ APPAREIL \_ amovible**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="15595-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="15595-168">L’appareil est amovible ; il ne peut pas être l’affichage principal.</span><span class="sxs-lookup"><span data-stu-id="15595-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="15595-169"><dt>**Afficher \_ PÉRIPHÉRIQUE \_ \_ compatible VGA**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="15595-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="15595-170">L’appareil est compatible VGA.</span><span class="sxs-lookup"><span data-stu-id="15595-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="15595-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="15595-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-172">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15595-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15595-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-174">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="15595-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="15595-175">Fréquence d’actualisation actuelle, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="15595-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="15595-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="15595-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15595-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15595-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-179">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="15595-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="15595-180">Nombre actuel de pixels horizontaux.</span><span class="sxs-lookup"><span data-stu-id="15595-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="15595-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="15595-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15595-182">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15595-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15595-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15595-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15595-184">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="15595-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="15595-185">Nombre actuel de pixels verticaux.</span><span class="sxs-lookup"><span data-stu-id="15595-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15595-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15595-186">Requirements</span></span>



| <span data-ttu-id="15595-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15595-187">Requirement</span></span> | <span data-ttu-id="15595-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="15595-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15595-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15595-189">Minimum supported client</span></span><br/> | <span data-ttu-id="15595-190">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="15595-190">None supported</span></span><br/>                            |
| <span data-ttu-id="15595-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15595-191">Minimum supported server</span></span><br/> | <span data-ttu-id="15595-192">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15595-192">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15595-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15595-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15595-194">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="15595-194">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




