---
description: Classe SystemConfig_Services-cette classe est la classe de type d’événement pour les événements de configuration de service.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: Classe SystemConfig_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106057"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="94028-103">\_Classe de services SystemConfig</span><span class="sxs-lookup"><span data-stu-id="94028-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="94028-104">Cette classe est la classe de type d’événement pour les événements de configuration de service.</span><span class="sxs-lookup"><span data-stu-id="94028-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="94028-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="94028-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="94028-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94028-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a><span data-ttu-id="94028-107">Membres</span><span class="sxs-lookup"><span data-stu-id="94028-107">Members</span></span>

<span data-ttu-id="94028-108">La classe **SystemConfig \_ services** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="94028-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="94028-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="94028-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94028-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="94028-110">Properties</span></span>

<span data-ttu-id="94028-111">La classe **SystemConfig \_ services** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="94028-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94028-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="94028-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94028-113">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="94028-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="94028-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94028-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94028-115">Qualificateurs : **WmiDataId** (5), **StringTermination ("NullTerminated")**, **format ("w")**</span><span class="sxs-lookup"><span data-stu-id="94028-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="94028-116">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="94028-116">Display name of the service.</span></span> <span data-ttu-id="94028-117">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="94028-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="94028-118">Toutefois, les comparaisons de noms complets ne respectent jamais pas la casse.</span><span class="sxs-lookup"><span data-stu-id="94028-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="94028-119">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="94028-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94028-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94028-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94028-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94028-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94028-122">Qualificateurs : **WmiDataId** (1), **format ("x")**</span><span class="sxs-lookup"><span data-stu-id="94028-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="94028-123">Identificateur du processus dans lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="94028-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="94028-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="94028-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94028-125">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="94028-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="94028-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94028-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94028-127">Qualificateurs : **WmiDataId** (6), **StringTermination ("NullTerminated")**, **format ("w")**</span><span class="sxs-lookup"><span data-stu-id="94028-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="94028-128">Nom du processus dans lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="94028-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="94028-129">**FormName**</span><span class="sxs-lookup"><span data-stu-id="94028-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94028-130">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="94028-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="94028-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94028-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94028-132">Qualificateurs : **WmiDataId** (4), **StringTermination ("NullTerminated")**, **format ("w")**</span><span class="sxs-lookup"><span data-stu-id="94028-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="94028-133">Identificateur unique du service.</span><span class="sxs-lookup"><span data-stu-id="94028-133">Unique identifier of the service.</span></span> <span data-ttu-id="94028-134">L’identificateur fournit une indication de la fonctionnalité fournie par le service.</span><span class="sxs-lookup"><span data-stu-id="94028-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="94028-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="94028-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94028-136">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94028-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94028-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94028-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94028-138">Qualificateurs : **WmiDataId** (2), **format ("x")**</span><span class="sxs-lookup"><span data-stu-id="94028-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="94028-139">État actuel du service.</span><span class="sxs-lookup"><span data-stu-id="94028-139">Current state of the service.</span></span> <span data-ttu-id="94028-140">Pour connaître les valeurs possibles, consultez le membre **dwCurrentState** du **processus d' \_ état \_ du service**.</span><span class="sxs-lookup"><span data-stu-id="94028-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="94028-141">**SubProcessTag**</span><span class="sxs-lookup"><span data-stu-id="94028-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94028-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94028-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94028-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="94028-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94028-144">Qualificateurs : **WmiDataId** (3), **format ("x")**</span><span class="sxs-lookup"><span data-stu-id="94028-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="94028-145">Identifie le service.</span><span class="sxs-lookup"><span data-stu-id="94028-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94028-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94028-146">Requirements</span></span>



| <span data-ttu-id="94028-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94028-147">Requirement</span></span> | <span data-ttu-id="94028-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="94028-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94028-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94028-149">Minimum supported client</span></span><br/> | <span data-ttu-id="94028-150">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94028-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94028-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94028-151">Minimum supported server</span></span><br/> | <span data-ttu-id="94028-152">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94028-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94028-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94028-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94028-154">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="94028-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




