---
description: Cette classe est la classe de type d’événement pour les événements de registre. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Classe Registry_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1_TypeGroup1
- Registry_V1_TypeGroup1.Status
- Registry_V1_TypeGroup1.KeyHandle
- Registry_V1_TypeGroup1.ElapsedTime
- Registry_V1_TypeGroup1.Index
- Registry_V1_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2cd77ad0c12769c657b4e7c23c1fe1993a248481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862870"
---
# <a name="registry_v1_typegroup1-class"></a><span data-ttu-id="bc2c5-104">Classe de TypeGroup1 du Registre \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="bc2c5-104">Registry\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="bc2c5-105">Cette classe est la classe de type d’événement pour les événements de registre.</span><span class="sxs-lookup"><span data-stu-id="bc2c5-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="bc2c5-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="bc2c5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2c5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc2c5-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "RunDown"}]
class Registry_V1_TypeGroup1 : Registry
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  uint32 Index;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="bc2c5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bc2c5-108">Members</span></span>

<span data-ttu-id="bc2c5-109">La **classe \_ \_ TypeGroup1 du Registre v1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bc2c5-109">The **Registry\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="bc2c5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc2c5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc2c5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc2c5-111">Properties</span></span>

<span data-ttu-id="bc2c5-112">La **classe \_ \_ TypeGroup1 du Registre v1** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bc2c5-112">The **Registry\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc2c5-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="bc2c5-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc2c5-114">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="bc2c5-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc2c5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-116">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="bc2c5-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="bc2c5-117">Temps écoulé de l’opération de registre.</span><span class="sxs-lookup"><span data-stu-id="bc2c5-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="bc2c5-118">Index</span><span class="sxs-lookup"><span data-stu-id="bc2c5-118">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc2c5-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc2c5-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc2c5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-121">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="bc2c5-121">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="bc2c5-122">Index de la sous-clé pour l’opération de Registre (par exemple, EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="bc2c5-122">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="bc2c5-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="bc2c5-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc2c5-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc2c5-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc2c5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-126">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="bc2c5-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="bc2c5-127">Handle de la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="bc2c5-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="bc2c5-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="bc2c5-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc2c5-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bc2c5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc2c5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-131">Qualificateurs : WmiDataId (5), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="bc2c5-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="bc2c5-132">nom de la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="bc2c5-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="bc2c5-133">Statut</span><span class="sxs-lookup"><span data-stu-id="bc2c5-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc2c5-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc2c5-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc2c5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc2c5-136">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="bc2c5-136">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="bc2c5-137">Valeur NTSTATUS de l’opération de registre.</span><span class="sxs-lookup"><span data-stu-id="bc2c5-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc2c5-138">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bc2c5-138">Requirements</span></span>



| <span data-ttu-id="bc2c5-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc2c5-139">Requirement</span></span> | <span data-ttu-id="bc2c5-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc2c5-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bc2c5-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc2c5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bc2c5-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc2c5-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bc2c5-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc2c5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bc2c5-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc2c5-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bc2c5-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc2c5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc2c5-146">**Registre**</span><span class="sxs-lookup"><span data-stu-id="bc2c5-146">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="bc2c5-147">**Registre \_ v1**</span><span class="sxs-lookup"><span data-stu-id="bc2c5-147">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 




