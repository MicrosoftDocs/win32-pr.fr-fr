---
description: Cette classe est la classe de type d’événement pour les événements de configuration de l’alimentation. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7065b0b0-9a1d-4fce-a494-5762d5efb239
title: Classe SystemConfig_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Power
- SystemConfig_Power.s1
- SystemConfig_Power.s2
- SystemConfig_Power.s3
- SystemConfig_Power.s4
- SystemConfig_Power.s5
- SystemConfig_Power.Pad1
- SystemConfig_Power.Pad2
- SystemConfig_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d27586451f944ac9c94e9ec2d204035c21f37679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972110"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="bc381-104">\_Classe SystemConfig Power</span><span class="sxs-lookup"><span data-stu-id="bc381-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="bc381-105">Cette classe est la classe de type d’événement pour les événements de configuration de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="bc381-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="bc381-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="bc381-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc381-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc381-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_Power : SystemConfig
{
  uint8 s1;
  uint8 s2;
  uint8 s3;
  uint8 s4;
  uint8 s5;
  uint8 Pad1;
  uint8 Pad2;
  uint8 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="bc381-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bc381-108">Members</span></span>

<span data-ttu-id="bc381-109">La classe **SystemConfig \_ Power** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bc381-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="bc381-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc381-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc381-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc381-111">Properties</span></span>

<span data-ttu-id="bc381-112">La **classe \_ d’alimentation SystemConfig** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bc381-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc381-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="bc381-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc381-114">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="bc381-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bc381-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc381-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc381-116">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="bc381-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="bc381-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bc381-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc381-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="bc381-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc381-119">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="bc381-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bc381-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc381-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc381-121">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="bc381-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="bc381-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bc381-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc381-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="bc381-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc381-124">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="bc381-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bc381-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc381-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc381-126">Qualificateurs : WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="bc381-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="bc381-127">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bc381-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc381-128">s1</span><span class="sxs-lookup"><span data-stu-id="bc381-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc381-129">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="bc381-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bc381-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc381-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc381-131">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="bc381-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="bc381-132">True indique que le système prend en charge l’état de veille S1.</span><span class="sxs-lookup"><span data-stu-id="bc381-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="bc381-133">s2</span><span class="sxs-lookup"><span data-stu-id="bc381-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc381-134">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="bc381-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bc381-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc381-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc381-136">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="bc381-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="bc381-137">True indique que le système prend en charge l’état de veille S2.</span><span class="sxs-lookup"><span data-stu-id="bc381-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="bc381-138">s3</span><span class="sxs-lookup"><span data-stu-id="bc381-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc381-139">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="bc381-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bc381-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc381-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc381-141">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="bc381-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="bc381-142">True indique que le système prend en charge l’état de veille S3.</span><span class="sxs-lookup"><span data-stu-id="bc381-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="bc381-143">S4</span><span class="sxs-lookup"><span data-stu-id="bc381-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc381-144">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="bc381-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bc381-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc381-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc381-146">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="bc381-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="bc381-147">True indique que le système prend en charge l’état de veille S4.</span><span class="sxs-lookup"><span data-stu-id="bc381-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="bc381-148">S5</span><span class="sxs-lookup"><span data-stu-id="bc381-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc381-149">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="bc381-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bc381-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc381-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc381-151">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="bc381-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="bc381-152">La valeur true indique que le système prend en charge l’état de veille S5.</span><span class="sxs-lookup"><span data-stu-id="bc381-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc381-153">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bc381-153">Requirements</span></span>



| <span data-ttu-id="bc381-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc381-154">Requirement</span></span> | <span data-ttu-id="bc381-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc381-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc381-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc381-156">Minimum supported client</span></span><br/> | <span data-ttu-id="bc381-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc381-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bc381-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc381-158">Minimum supported server</span></span><br/> | <span data-ttu-id="bc381-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc381-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc381-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc381-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc381-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="bc381-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




