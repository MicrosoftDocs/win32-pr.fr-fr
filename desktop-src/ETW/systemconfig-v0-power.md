---
description: Classe SystemConfig_V0_Power-cette classe est la classe de type d’événement pour les événements de configuration de l’alimentation. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: Classe SystemConfig_V0_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab268e719374906e149dc9c1b733487f986e8308
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105937"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="60392-104">SystemConfig \_ v0 \_ Power Class</span><span class="sxs-lookup"><span data-stu-id="60392-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="60392-105">Cette classe est la classe de type d’événement pour les événements de configuration de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="60392-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="60392-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="60392-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="60392-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60392-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a><span data-ttu-id="60392-108">Membres</span><span class="sxs-lookup"><span data-stu-id="60392-108">Members</span></span>

<span data-ttu-id="60392-109">La **classe \_ \_ d’alimentation SystemConfig v0** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="60392-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="60392-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="60392-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60392-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="60392-111">Properties</span></span>

<span data-ttu-id="60392-112">La **classe \_ \_ d’alimentation SystemConfig v0** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="60392-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60392-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="60392-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60392-114">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="60392-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="60392-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60392-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60392-116">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="60392-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="60392-117">Réservé.</span><span class="sxs-lookup"><span data-stu-id="60392-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="60392-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="60392-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60392-119">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="60392-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="60392-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60392-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60392-121">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="60392-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="60392-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="60392-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="60392-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="60392-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60392-124">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="60392-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="60392-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60392-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60392-126">Qualificateurs : WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="60392-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="60392-127">Réservé.</span><span class="sxs-lookup"><span data-stu-id="60392-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="60392-128">s1</span><span class="sxs-lookup"><span data-stu-id="60392-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60392-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60392-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60392-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60392-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60392-131">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="60392-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="60392-132">True indique que le système prend en charge l’état de veille S1.</span><span class="sxs-lookup"><span data-stu-id="60392-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="60392-133">s2</span><span class="sxs-lookup"><span data-stu-id="60392-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60392-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60392-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60392-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60392-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60392-136">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="60392-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="60392-137">True indique que le système prend en charge l’état de veille S2.</span><span class="sxs-lookup"><span data-stu-id="60392-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="60392-138">s3</span><span class="sxs-lookup"><span data-stu-id="60392-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60392-139">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60392-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60392-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60392-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60392-141">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="60392-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="60392-142">True indique que le système prend en charge l’état de veille S3.</span><span class="sxs-lookup"><span data-stu-id="60392-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="60392-143">S4</span><span class="sxs-lookup"><span data-stu-id="60392-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60392-144">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60392-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60392-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60392-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60392-146">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="60392-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="60392-147">True indique que le système prend en charge l’état de veille S4.</span><span class="sxs-lookup"><span data-stu-id="60392-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="60392-148">S5</span><span class="sxs-lookup"><span data-stu-id="60392-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60392-149">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60392-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60392-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60392-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60392-151">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="60392-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="60392-152">La valeur true indique que le système prend en charge l’état de veille S5.</span><span class="sxs-lookup"><span data-stu-id="60392-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60392-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60392-153">Requirements</span></span>



| <span data-ttu-id="60392-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60392-154">Requirement</span></span> | <span data-ttu-id="60392-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="60392-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60392-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60392-156">Minimum supported client</span></span><br/> | <span data-ttu-id="60392-157">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="60392-157">None supported</span></span><br/>                            |
| <span data-ttu-id="60392-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60392-158">Minimum supported server</span></span><br/> | <span data-ttu-id="60392-159">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60392-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60392-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60392-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60392-161">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="60392-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




