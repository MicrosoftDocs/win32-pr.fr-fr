---
description: Cette classe est la classe de type d’événement pour les événements de requête d’interruption (IRQ). La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: Classe SystemConfig_IRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972167"
---
# <a name="systemconfig_irq-class"></a><span data-ttu-id="cc290-104">\_Classe IRQ SystemConfig</span><span class="sxs-lookup"><span data-stu-id="cc290-104">SystemConfig\_IRQ class</span></span>

<span data-ttu-id="cc290-105">Cette classe est la classe de type d’événement pour les événements de requête d’interruption (IRQ).</span><span class="sxs-lookup"><span data-stu-id="cc290-105">This class is the event type class for interrupt request (IRQ) events.</span></span>

<span data-ttu-id="cc290-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="cc290-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc290-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc290-107">Syntax</span></span>

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a><span data-ttu-id="cc290-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cc290-108">Members</span></span>

<span data-ttu-id="cc290-109">La classe **SystemConfig \_ IRQ** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cc290-109">The **SystemConfig\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="cc290-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc290-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc290-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc290-111">Properties</span></span>

<span data-ttu-id="cc290-112">La classe **SystemConfig \_ IRQ** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc290-112">The **SystemConfig\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc290-113">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="cc290-113">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc290-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cc290-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc290-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc290-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc290-116">Qualificateurs : WmiDataId (4), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="cc290-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="cc290-117">Description de l’appareil ou du logiciel à l’origine de la demande.</span><span class="sxs-lookup"><span data-stu-id="cc290-117">Description of the device or software making the request.</span></span>

</dd> <dt>

<span data-ttu-id="cc290-118">**DeviceDescriptionLen**</span><span class="sxs-lookup"><span data-stu-id="cc290-118">**DeviceDescriptionLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc290-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc290-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc290-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc290-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc290-121">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="cc290-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="cc290-122">Longueur, en caractères, de la chaîne dans **DeviceDescription**.</span><span class="sxs-lookup"><span data-stu-id="cc290-122">Length, in characters, of the string in **DeviceDescription**.</span></span>

</dd> <dt>

<span data-ttu-id="cc290-123">**IRQAffinity**</span><span class="sxs-lookup"><span data-stu-id="cc290-123">**IRQAffinity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc290-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc290-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc290-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc290-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc290-126">Qualificateurs : WmiDataId (1), format ("x")</span><span class="sxs-lookup"><span data-stu-id="cc290-126">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="cc290-127">Masque d’affinité d’IRQ.</span><span class="sxs-lookup"><span data-stu-id="cc290-127">IRQ affinity mask.</span></span> <span data-ttu-id="cc290-128">Le masque d’affinité identifie les processeurs (ou groupes de processeurs) spécifiques qui peuvent recevoir l’IRQ.</span><span class="sxs-lookup"><span data-stu-id="cc290-128">The affinity mask identifies the specific processors (or groups of processors) that can receive the IRQ.</span></span>

</dd> <dt>

<span data-ttu-id="cc290-129">**IRQNum**</span><span class="sxs-lookup"><span data-stu-id="cc290-129">**IRQNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc290-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc290-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc290-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc290-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc290-132">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="cc290-132">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="cc290-133">Numéro de ligne de la requête d’interruption.</span><span class="sxs-lookup"><span data-stu-id="cc290-133">Interrupt request line number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc290-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cc290-134">Requirements</span></span>



| <span data-ttu-id="cc290-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc290-135">Requirement</span></span> | <span data-ttu-id="cc290-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc290-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc290-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc290-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cc290-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc290-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc290-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc290-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cc290-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc290-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc290-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc290-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc290-142">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="cc290-142">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




