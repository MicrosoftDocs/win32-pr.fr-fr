---
description: Cette classe est la classe de type d’événement pour les événements de configuration de service.
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: Classe SystemConfig_V0_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6c061c6a0c4cbb3e807bcb3418155b1194fcfa28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320705"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="16c17-103">\_Classe SystemConfig v0 \_ services</span><span class="sxs-lookup"><span data-stu-id="16c17-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="16c17-104">Cette classe est la classe de type d’événement pour les événements de configuration de service.</span><span class="sxs-lookup"><span data-stu-id="16c17-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="16c17-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="16c17-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c17-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16c17-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="16c17-107">Membres</span><span class="sxs-lookup"><span data-stu-id="16c17-107">Members</span></span>

<span data-ttu-id="16c17-108">La classe **SystemConfig \_ v0 \_ services** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="16c17-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="16c17-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16c17-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16c17-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16c17-110">Properties</span></span>

<span data-ttu-id="16c17-111">La classe **SystemConfig \_ v0 \_ services** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="16c17-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16c17-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="16c17-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c17-113">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="16c17-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="16c17-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16c17-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c17-115">Qualificateurs : **WmiDataId** (2), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="16c17-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="16c17-116">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="16c17-116">Display name of the service.</span></span> <span data-ttu-id="16c17-117">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="16c17-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="16c17-118">Toutefois, les comparaisons de noms complets ne respectent jamais pas la casse.</span><span class="sxs-lookup"><span data-stu-id="16c17-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="16c17-119">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="16c17-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c17-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16c17-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16c17-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16c17-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c17-122">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="16c17-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="16c17-123">Identificateur du processus dans lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="16c17-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="16c17-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="16c17-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c17-125">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="16c17-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="16c17-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16c17-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c17-127">Qualificateurs : **WmiDataId** (3), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="16c17-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="16c17-128">Nom du processus dans lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="16c17-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="16c17-129">**FormName**</span><span class="sxs-lookup"><span data-stu-id="16c17-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c17-130">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="16c17-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="16c17-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16c17-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c17-132">Qualificateurs : **WmiDataId** (1), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="16c17-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="16c17-133">Identificateur unique du service.</span><span class="sxs-lookup"><span data-stu-id="16c17-133">Unique identifier of the service.</span></span> <span data-ttu-id="16c17-134">L’identificateur fournit une indication de la fonctionnalité fournie par le service.</span><span class="sxs-lookup"><span data-stu-id="16c17-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16c17-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="16c17-135">Requirements</span></span>



| <span data-ttu-id="16c17-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16c17-136">Requirement</span></span> | <span data-ttu-id="16c17-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="16c17-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16c17-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16c17-138">Minimum supported client</span></span><br/> | <span data-ttu-id="16c17-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="16c17-139">None supported</span></span><br/>                            |
| <span data-ttu-id="16c17-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16c17-140">Minimum supported server</span></span><br/> | <span data-ttu-id="16c17-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16c17-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16c17-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16c17-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c17-143">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="16c17-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




