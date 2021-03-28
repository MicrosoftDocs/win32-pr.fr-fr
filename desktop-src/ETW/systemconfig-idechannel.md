---
description: Cette classe est la classe de type d’événement pour les événements de canal IDE. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: Classe SystemConfig_IDEChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526380"
---
# <a name="systemconfig_idechannel-class"></a><span data-ttu-id="b17cd-104">SystemConfig \_ IDEChannel, classe</span><span class="sxs-lookup"><span data-stu-id="b17cd-104">SystemConfig\_IDEChannel class</span></span>

<span data-ttu-id="b17cd-105">Cette classe est la classe de type d’événement pour les événements de canal IDE.</span><span class="sxs-lookup"><span data-stu-id="b17cd-105">This class is the event type class for IDE channel events.</span></span>

<span data-ttu-id="b17cd-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="b17cd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17cd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b17cd-107">Syntax</span></span>

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a><span data-ttu-id="b17cd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b17cd-108">Members</span></span>

<span data-ttu-id="b17cd-109">La classe **SystemConfig \_ IDEChannel** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b17cd-109">The **SystemConfig\_IDEChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="b17cd-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b17cd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b17cd-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b17cd-111">Properties</span></span>

<span data-ttu-id="b17cd-112">La classe **SystemConfig \_ IDEChannel** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b17cd-112">The **SystemConfig\_IDEChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b17cd-113">**DeviceTimingMode**</span><span class="sxs-lookup"><span data-stu-id="b17cd-113">**DeviceTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17cd-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b17cd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17cd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-116">Qualificateurs : WmiDataId (3), format ("x")</span><span class="sxs-lookup"><span data-stu-id="b17cd-116">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b17cd-117">Mode dans lequel l’IDE peut fonctionner.</span><span class="sxs-lookup"><span data-stu-id="b17cd-117">The mode in which the IDE could function.</span></span> <span data-ttu-id="b17cd-118">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b17cd-118">The following are the possible values:</span></span>

-   <span data-ttu-id="b17cd-119">PIO \_ MODE0 (0x1)</span><span class="sxs-lookup"><span data-stu-id="b17cd-119">PIO\_MODE0 (0x1)</span></span>
-   <span data-ttu-id="b17cd-120">PIO \_ MODE1 (0X2)</span><span class="sxs-lookup"><span data-stu-id="b17cd-120">PIO\_MODE1 (0x2)</span></span>
-   <span data-ttu-id="b17cd-121">PIO \_ Mode2 (0x4)</span><span class="sxs-lookup"><span data-stu-id="b17cd-121">PIO\_MODE2 (0x4)</span></span>
-   <span data-ttu-id="b17cd-122">PIO \_ MODE3 (0x8)</span><span class="sxs-lookup"><span data-stu-id="b17cd-122">PIO\_MODE3 (0x8)</span></span>
-   <span data-ttu-id="b17cd-123">PIO \_ MODE4 (0x10)</span><span class="sxs-lookup"><span data-stu-id="b17cd-123">PIO\_MODE4 (0x10)</span></span>
-   <span data-ttu-id="b17cd-124">SWDMA \_ MODE0 (0x20)</span><span class="sxs-lookup"><span data-stu-id="b17cd-124">SWDMA\_MODE0 (0x20)</span></span>
-   <span data-ttu-id="b17cd-125">SWDMA \_ MODE1 (0x40)</span><span class="sxs-lookup"><span data-stu-id="b17cd-125">SWDMA\_MODE1 (0x40)</span></span>
-   <span data-ttu-id="b17cd-126">SWDMA \_ Mode2 (0x80)</span><span class="sxs-lookup"><span data-stu-id="b17cd-126">SWDMA\_MODE2 (0x80)</span></span>
-   <span data-ttu-id="b17cd-127">MWDMA \_ MODE0 (0x100)</span><span class="sxs-lookup"><span data-stu-id="b17cd-127">MWDMA\_MODE0 (0x100)</span></span>
-   <span data-ttu-id="b17cd-128">MWDMA \_ Mode2 (0x200)</span><span class="sxs-lookup"><span data-stu-id="b17cd-128">MWDMA\_MODE2 (0x200)</span></span>
-   <span data-ttu-id="b17cd-129">MWDMA \_ MODE3 (0x400)</span><span class="sxs-lookup"><span data-stu-id="b17cd-129">MWDMA\_MODE3 (0x400)</span></span>
-   <span data-ttu-id="b17cd-130">UDMA \_ MODE0 (0x800)</span><span class="sxs-lookup"><span data-stu-id="b17cd-130">UDMA\_MODE0 (0x800)</span></span>
-   <span data-ttu-id="b17cd-131">UDMA \_ MODE1 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="b17cd-131">UDMA\_MODE1 (0x1000)</span></span>
-   <span data-ttu-id="b17cd-132">\_Mode2 UDMA (0x2000)</span><span class="sxs-lookup"><span data-stu-id="b17cd-132">UDMA\_MODE2 (0x2000)</span></span>
-   <span data-ttu-id="b17cd-133">UDMA \_ MODE3 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="b17cd-133">UDMA\_MODE3 (0x4000)</span></span>
-   <span data-ttu-id="b17cd-134">UDMA \_ MODE4 (0x8000)</span><span class="sxs-lookup"><span data-stu-id="b17cd-134">UDMA\_MODE4 (0x8000)</span></span>
-   <span data-ttu-id="b17cd-135">UDMA \_ MODE5 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="b17cd-135">UDMA\_MODE5 (0x10000)</span></span>

</dd> <dt>

<span data-ttu-id="b17cd-136">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="b17cd-136">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17cd-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b17cd-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17cd-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-139">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="b17cd-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="b17cd-140">Type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b17cd-140">The device type.</span></span> <span data-ttu-id="b17cd-141">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b17cd-141">The following are the possible values:</span></span>

-   <span data-ttu-id="b17cd-142">ATA (1)</span><span class="sxs-lookup"><span data-stu-id="b17cd-142">ATA (1)</span></span>
-   <span data-ttu-id="b17cd-143">ATAPI (2)</span><span class="sxs-lookup"><span data-stu-id="b17cd-143">ATAPI (2)</span></span>

</dd> <dt>

<span data-ttu-id="b17cd-144">**LocationInformation**</span><span class="sxs-lookup"><span data-stu-id="b17cd-144">**LocationInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17cd-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17cd-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17cd-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-147">Qualificateurs : WmiDataId (5), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="b17cd-147">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="b17cd-148">Canal IDE (par exemple, canal principal, canal secondaire, etc.).</span><span class="sxs-lookup"><span data-stu-id="b17cd-148">The IDE channel (for example, Primary Channel, Secondary Channel, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="b17cd-149">**LocationInformationLen**</span><span class="sxs-lookup"><span data-stu-id="b17cd-149">**LocationInformationLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17cd-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b17cd-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17cd-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-152">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="b17cd-152">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="b17cd-153">Longueur de la chaîne **LocationInformation** .</span><span class="sxs-lookup"><span data-stu-id="b17cd-153">Length of the **LocationInformation** string.</span></span>

</dd> <dt>

<span data-ttu-id="b17cd-154">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="b17cd-154">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17cd-155">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b17cd-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17cd-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17cd-157">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="b17cd-157">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="b17cd-158">Identificateur du disque.</span><span class="sxs-lookup"><span data-stu-id="b17cd-158">The identifier of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b17cd-159">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b17cd-159">Requirements</span></span>



| <span data-ttu-id="b17cd-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b17cd-160">Requirement</span></span> | <span data-ttu-id="b17cd-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="b17cd-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b17cd-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b17cd-162">Minimum supported client</span></span><br/> | <span data-ttu-id="b17cd-163">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b17cd-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b17cd-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b17cd-164">Minimum supported server</span></span><br/> | <span data-ttu-id="b17cd-165">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b17cd-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b17cd-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b17cd-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17cd-167">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="b17cd-167">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




