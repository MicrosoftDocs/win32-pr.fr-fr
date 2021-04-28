---
description: Classe Registry_V0_TypeGroup1-cette classe est la classe de type d’événement pour les événements de registre. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Classe Registry_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V0_TypeGroup1
- Registry_V0_TypeGroup1.Status
- Registry_V0_TypeGroup1.KeyHandle
- Registry_V0_TypeGroup1.ElapsedTime
- Registry_V0_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 86f6d695afa2e05c87a076cf88ed8023e9416beb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106187"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="e3e44-104">Registre \_ v0 \_ TypeGroup1, classe</span><span class="sxs-lookup"><span data-stu-id="e3e44-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="e3e44-105">Cette classe est la classe de type d’événement pour les événements de registre.</span><span class="sxs-lookup"><span data-stu-id="e3e44-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="e3e44-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="e3e44-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e44-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3e44-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush"}]
class Registry_V0_TypeGroup1 : Registry_V0
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="e3e44-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e3e44-108">Members</span></span>

<span data-ttu-id="e3e44-109">La classe de **Registre \_ v0 \_ TypeGroup1** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e3e44-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="e3e44-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3e44-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3e44-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3e44-111">Properties</span></span>

<span data-ttu-id="e3e44-112">La classe de **Registre \_ v0 \_ TypeGroup1** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e3e44-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3e44-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="e3e44-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3e44-114">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="e3e44-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="e3e44-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3e44-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3e44-116">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="e3e44-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e3e44-117">Temps écoulé de l’opération de registre.</span><span class="sxs-lookup"><span data-stu-id="e3e44-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="e3e44-118">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="e3e44-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3e44-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3e44-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e3e44-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3e44-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3e44-121">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="e3e44-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e3e44-122">Handle de la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="e3e44-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="e3e44-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="e3e44-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3e44-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e3e44-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3e44-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3e44-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3e44-126">Qualificateurs : WmiDataId (4), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="e3e44-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="e3e44-127">nom de la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="e3e44-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="e3e44-128">Statut</span><span class="sxs-lookup"><span data-stu-id="e3e44-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3e44-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3e44-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e3e44-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3e44-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3e44-131">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="e3e44-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e3e44-132">Valeur NTSTATUS de l’opération de registre.</span><span class="sxs-lookup"><span data-stu-id="e3e44-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3e44-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3e44-133">Requirements</span></span>



| <span data-ttu-id="e3e44-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3e44-134">Requirement</span></span> | <span data-ttu-id="e3e44-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3e44-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e3e44-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3e44-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e3e44-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3e44-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e3e44-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3e44-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e3e44-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3e44-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3e44-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3e44-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e44-141">**Registre \_ v0**</span><span class="sxs-lookup"><span data-stu-id="e3e44-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 




