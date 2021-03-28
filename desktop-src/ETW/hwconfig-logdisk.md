---
description: La \_ classe HWConfig LogDisk est la classe de type d’événement pour les événements de configuration de disque logique. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: Classe HWConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529884"
---
# <a name="hwconfig_logdisk-class"></a><span data-ttu-id="ad9a5-104">HWConfig \_ LogDisk, classe</span><span class="sxs-lookup"><span data-stu-id="ad9a5-104">HWConfig\_LogDisk class</span></span>

<span data-ttu-id="ad9a5-105">La classe **HWConfig \_ LogDisk** est la classe de type d’événement pour les événements de configuration de disque logique.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-105">The **HWConfig\_LogDisk** class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="ad9a5-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9a5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad9a5-107">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a><span data-ttu-id="ad9a5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ad9a5-108">Members</span></span>

<span data-ttu-id="ad9a5-109">La classe **HWConfig \_ LogDisk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ad9a5-109">The **HWConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="ad9a5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ad9a5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad9a5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ad9a5-111">Properties</span></span>

<span data-ttu-id="ad9a5-112">La classe **HWConfig \_ LogDisk** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-112">The **HWConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad9a5-113">DiskNumber</span><span class="sxs-lookup"><span data-stu-id="ad9a5-113">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad9a5-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad9a5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad9a5-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad9a5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad9a5-116">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="ad9a5-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="ad9a5-117">Numéro d’index du disque contenant cette partition.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-117">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="ad9a5-118">Remplir</span><span class="sxs-lookup"><span data-stu-id="ad9a5-118">Pad</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad9a5-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad9a5-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad9a5-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad9a5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad9a5-121">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="ad9a5-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="ad9a5-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ad9a5-123">PartitionSize</span><span class="sxs-lookup"><span data-stu-id="ad9a5-123">PartitionSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad9a5-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ad9a5-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ad9a5-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad9a5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad9a5-126">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="ad9a5-126">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="ad9a5-127">Taille totale de la partition, en octets.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-127">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ad9a5-128">StartOffset</span><span class="sxs-lookup"><span data-stu-id="ad9a5-128">StartOffset</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad9a5-129">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ad9a5-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ad9a5-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad9a5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad9a5-131">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="ad9a5-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="ad9a5-132">Décalage de départ (en octets) de la partition à partir du début du disque.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-132">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad9a5-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ad9a5-133">Requirements</span></span>



| <span data-ttu-id="ad9a5-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad9a5-134">Requirement</span></span> | <span data-ttu-id="ad9a5-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad9a5-135">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="ad9a5-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad9a5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ad9a5-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad9a5-137">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ad9a5-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad9a5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ad9a5-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad9a5-139">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="ad9a5-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad9a5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9a5-141">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="ad9a5-141">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




