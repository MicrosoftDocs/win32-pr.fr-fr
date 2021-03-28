---
description: Cette classe est la classe de type d’événement pour les événements de configuration vidéo.
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: Classe SystemConfig_Video
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 370c67501b75f0fd4ac88488744280f1e0065bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973843"
---
# <a name="systemconfig_video-class"></a><span data-ttu-id="f0ddc-103">\_Classe vidéo SystemConfig</span><span class="sxs-lookup"><span data-stu-id="f0ddc-103">SystemConfig\_Video class</span></span>

<span data-ttu-id="f0ddc-104">Cette classe est la classe de type d’événement pour les événements de configuration vidéo.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="f0ddc-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ddc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0ddc-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
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

## <a name="members"></a><span data-ttu-id="f0ddc-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f0ddc-107">Members</span></span>

<span data-ttu-id="f0ddc-108">La **classe \_ Video SystemConfig** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f0ddc-108">The **SystemConfig\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="f0ddc-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f0ddc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0ddc-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f0ddc-110">Properties</span></span>

<span data-ttu-id="f0ddc-111">La **classe \_ Video SystemConfig** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-111">The **SystemConfig\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0ddc-112">**AdapterString**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-113">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-115">Qualificateurs : **WmiDataId** (8), **Max** (256), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-115">Qualifiers: **WmiDataId** (8), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-116">Nom ou description de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f0ddc-117">**BiosString**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-118">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-120">Qualificateurs : **WmiDataId** (9), **Max** (256), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-120">Qualifiers: **WmiDataId** (9), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-121">Nom du BIOS de la carte.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f0ddc-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-123">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-125">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="f0ddc-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-126">Nombre de bits utilisés pour afficher chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="f0ddc-127">**ChipType**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-128">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-130">Qualificateurs : **WmiDataId** (6), **Max** (256), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-130">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-131">Nom de la carte.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f0ddc-132">**DACType**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-133">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-135">Qualificateurs : **WmiDataId** (7), **Max** (256), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-135">Qualifiers: **WmiDataId** (7), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-136">Nom de la puce de conversion numérique-analogique (DAC) de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f0ddc-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-138">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-140">Qualificateurs : **WmiDataId** (10), **Max** (256), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-140">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-141">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="f0ddc-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-145">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="f0ddc-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-146">Quantité maximale de mémoire prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f0ddc-147">**StateFlags**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-150">Qualificateurs : **WmiDataId** (11), **format ("x")**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-150">Qualifiers: **WmiDataId** (11), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-151">Indicateurs d’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-151">Device state flags.</span></span> <span data-ttu-id="f0ddc-152">Il peut s’agir d’une combinaison raisonnable des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="f0ddc-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0ddc-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="f0ddc-154">Signification</span><span class="sxs-lookup"><span data-stu-id="f0ddc-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="f0ddc-155"><dt>**Afficher \_ APPAREIL \_ attaché \_ au \_ Bureau**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ddc-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="f0ddc-156">L’appareil fait partie du bureau.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="f0ddc-157"><dt>**Afficher \_ \_ \_ Pilote de mise en miroir des appareils**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ddc-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="f0ddc-158">Représente un Pseudo-appareil utilisé pour mettre en miroir le dessin d’application pour se connecter à un ordinateur distant ou à d’autres fins.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="f0ddc-159">Un Pseudo-analyse invisible est associé à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="f0ddc-160">Par exemple, NetMeeting l’utilise.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="f0ddc-161"><dt>**Afficher \_ \_MODESPRUNED d’appareil**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ddc-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="f0ddc-162">L’appareil a plus de modes d’affichage que la prise en charge de ses appareils de sortie.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="f0ddc-163"><dt>**Afficher \_ \_ \_ Périphérique principal**</dt> de l’appareil <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ddc-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="f0ddc-164">Le bureau principal se trouve sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-164">The primary desktop is on the device.</span></span> <span data-ttu-id="f0ddc-165">Pour un système avec une carte d’affichage unique, cette valeur est toujours définie.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="f0ddc-166">Pour un système avec plusieurs cartes d’affichage, un seul appareil peut avoir cet ensemble.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="f0ddc-167"><dt>**Afficher \_ APPAREIL \_ amovible**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ddc-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="f0ddc-168">L’appareil est amovible ; il ne peut pas être l’affichage principal.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="f0ddc-169"><dt>**Afficher \_ PÉRIPHÉRIQUE \_ \_ compatible VGA**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ddc-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="f0ddc-170">L’appareil est compatible VGA.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="f0ddc-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-172">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-174">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="f0ddc-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-175">Fréquence d’actualisation actuelle, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="f0ddc-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-179">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="f0ddc-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-180">Nombre actuel de pixels horizontaux.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f0ddc-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0ddc-182">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f0ddc-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0ddc-184">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="f0ddc-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="f0ddc-185">Nombre actuel de pixels verticaux.</span><span class="sxs-lookup"><span data-stu-id="f0ddc-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0ddc-186">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f0ddc-186">Requirements</span></span>



| <span data-ttu-id="f0ddc-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0ddc-187">Requirement</span></span> | <span data-ttu-id="f0ddc-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0ddc-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0ddc-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0ddc-189">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ddc-190">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0ddc-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f0ddc-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0ddc-191">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ddc-192">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0ddc-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f0ddc-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0ddc-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ddc-194">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="f0ddc-194">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




