---
description: Cette classe est la classe de type d’événement pour les événements de registre. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 8d0e9d97-3837-46da-a217-13e943580352
title: Classe Registry_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_TypeGroup1
- Registry_TypeGroup1.InitialTime
- Registry_TypeGroup1.Status
- Registry_TypeGroup1.Index
- Registry_TypeGroup1.KeyHandle
- Registry_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bfbf0157141473be4cc2460659912dc662ef7c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972279"
---
# <a name="registry_typegroup1-class"></a><span data-ttu-id="6b258-104">Classe de TypeGroup1 du Registre \_</span><span class="sxs-lookup"><span data-stu-id="6b258-104">Registry\_TypeGroup1 class</span></span>

<span data-ttu-id="6b258-105">Cette classe est la classe de type d’événement pour les événements de registre.</span><span class="sxs-lookup"><span data-stu-id="6b258-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="6b258-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="6b258-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b258-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b258-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "KCBCreate", "KCBDelete", "KCBRundownBegin", "KCBRundownEnd", "Virtualize", "Close"}]
class Registry_TypeGroup1 : Registry
{
  sint64 InitialTime;
  uint32 Status;
  uint32 Index;
  uint32 KeyHandle;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="6b258-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6b258-108">Members</span></span>

<span data-ttu-id="6b258-109">La **classe \_ TypeGroup1 du registre** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6b258-109">The **Registry\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="6b258-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6b258-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b258-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6b258-111">Properties</span></span>

<span data-ttu-id="6b258-112">La **classe \_ TypeGroup1 du registre** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6b258-112">The **Registry\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b258-113">Index</span><span class="sxs-lookup"><span data-stu-id="6b258-113">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b258-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b258-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b258-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b258-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b258-116">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="6b258-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="6b258-117">Index de la sous-clé pour l’opération de Registre (par exemple, EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="6b258-117">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="6b258-118">InitialTime</span><span class="sxs-lookup"><span data-stu-id="6b258-118">InitialTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b258-119">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="6b258-119">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b258-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b258-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b258-121">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="6b258-121">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="6b258-122">Heure initiale de l’opération de registre.</span><span class="sxs-lookup"><span data-stu-id="6b258-122">Initial time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="6b258-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="6b258-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b258-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b258-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b258-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b258-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b258-126">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="6b258-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6b258-127">Handle de la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="6b258-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="6b258-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="6b258-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b258-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b258-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b258-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b258-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b258-131">Qualificateurs : WmiDataId (5), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="6b258-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="6b258-132">nom de la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="6b258-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="6b258-133">Statut</span><span class="sxs-lookup"><span data-stu-id="6b258-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b258-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b258-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b258-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6b258-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b258-136">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="6b258-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6b258-137">Valeur NTSTATUS de l’opération de registre.</span><span class="sxs-lookup"><span data-stu-id="6b258-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b258-138">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6b258-138">Requirements</span></span>



| <span data-ttu-id="6b258-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b258-139">Requirement</span></span> | <span data-ttu-id="6b258-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b258-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6b258-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b258-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6b258-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b258-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6b258-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b258-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6b258-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b258-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b258-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b258-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b258-146">**Registre**</span><span class="sxs-lookup"><span data-stu-id="6b258-146">**Registry**</span></span>](registry.md)
</dt> </dl>

 

 




