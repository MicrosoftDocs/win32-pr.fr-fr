---
description: Classe SystemConfig_Power-cette classe est la classe de type d’événement pour les événements de configuration de l’alimentation. La syntaxe suivante est simplifiée à partir du code MOF.
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
ms.openlocfilehash: d7338faad8c313847ad7db7aaac5d4000abba5be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106067"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="a26d0-104">\_Classe SystemConfig Power</span><span class="sxs-lookup"><span data-stu-id="a26d0-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="a26d0-105">Cette classe est la classe de type d’événement pour les événements de configuration de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="a26d0-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="a26d0-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="a26d0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a26d0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a26d0-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="a26d0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a26d0-108">Members</span></span>

<span data-ttu-id="a26d0-109">La classe **SystemConfig \_ Power** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a26d0-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="a26d0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a26d0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a26d0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a26d0-111">Properties</span></span>

<span data-ttu-id="a26d0-112">La **classe \_ d’alimentation SystemConfig** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a26d0-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a26d0-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="a26d0-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a26d0-114">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a26d0-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a26d0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-116">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="a26d0-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="a26d0-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a26d0-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a26d0-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="a26d0-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a26d0-119">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a26d0-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a26d0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-121">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="a26d0-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="a26d0-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a26d0-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a26d0-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="a26d0-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a26d0-124">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a26d0-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a26d0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-126">Qualificateurs : WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="a26d0-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="a26d0-127">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a26d0-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a26d0-128">s1</span><span class="sxs-lookup"><span data-stu-id="a26d0-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a26d0-129">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a26d0-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a26d0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-131">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="a26d0-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="a26d0-132">True indique que le système prend en charge l’état de veille S1.</span><span class="sxs-lookup"><span data-stu-id="a26d0-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="a26d0-133">s2</span><span class="sxs-lookup"><span data-stu-id="a26d0-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a26d0-134">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a26d0-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a26d0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-136">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="a26d0-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a26d0-137">True indique que le système prend en charge l’état de veille S2.</span><span class="sxs-lookup"><span data-stu-id="a26d0-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="a26d0-138">s3</span><span class="sxs-lookup"><span data-stu-id="a26d0-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a26d0-139">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a26d0-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a26d0-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-141">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="a26d0-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="a26d0-142">True indique que le système prend en charge l’état de veille S3.</span><span class="sxs-lookup"><span data-stu-id="a26d0-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="a26d0-143">S4</span><span class="sxs-lookup"><span data-stu-id="a26d0-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a26d0-144">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a26d0-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a26d0-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-146">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="a26d0-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a26d0-147">True indique que le système prend en charge l’état de veille S4.</span><span class="sxs-lookup"><span data-stu-id="a26d0-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="a26d0-148">S5</span><span class="sxs-lookup"><span data-stu-id="a26d0-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a26d0-149">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a26d0-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a26d0-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a26d0-151">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="a26d0-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="a26d0-152">La valeur true indique que le système prend en charge l’état de veille S5.</span><span class="sxs-lookup"><span data-stu-id="a26d0-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a26d0-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a26d0-153">Requirements</span></span>



| <span data-ttu-id="a26d0-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a26d0-154">Requirement</span></span> | <span data-ttu-id="a26d0-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="a26d0-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a26d0-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a26d0-156">Minimum supported client</span></span><br/> | <span data-ttu-id="a26d0-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a26d0-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a26d0-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a26d0-158">Minimum supported server</span></span><br/> | <span data-ttu-id="a26d0-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a26d0-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a26d0-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a26d0-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a26d0-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="a26d0-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




