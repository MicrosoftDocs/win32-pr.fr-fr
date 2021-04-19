---
description: Est une classe de base abstraite qui sert de classe parente pour tous les événements intrinsèques et extrinsèques.
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: Classe __Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 39a032b3f082ed64ba7999d20366b89e8b3890c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538723"
---
# <a name="__event-class"></a><span data-ttu-id="d6e0e-103">\_\_Event, classe</span><span class="sxs-lookup"><span data-stu-id="d6e0e-103">\_\_Event class</span></span>

<span data-ttu-id="d6e0e-104">La classe de système d' **\_ \_ événements** est une classe de base abstraite qui sert de classe parente pour tous les événements intrinsèques et extrinsèques.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-104">The **\_\_Event** system class is an abstract base class that serves as the parent class for all intrinsic and extrinsic events.</span></span> <span data-ttu-id="d6e0e-105">Tous les nouveaux types d’événements doivent finalement dériver d' **\_ \_ Event**.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-105">All new event types must ultimately derive from **\_\_Event**.</span></span> <span data-ttu-id="d6e0e-106">Les événements intrinsèques dérivent directement de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-106">Intrinsic events derive directly from this class.</span></span> <span data-ttu-id="d6e0e-107">Les événements extrinsèques définis par l’utilisateur dérivent d’une sous-classe de cette classe appelée [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="d6e0e-107">User-defined extrinsic events derive from a subclass of this class called [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span>

<span data-ttu-id="d6e0e-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d6e0e-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e0e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6e0e-110">Syntax</span></span>

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="d6e0e-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d6e0e-111">Members</span></span>

<span data-ttu-id="d6e0e-112">La classe d' **\_ \_ événements** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6e0e-112">The **\_\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="d6e0e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6e0e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6e0e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6e0e-114">Properties</span></span>

<span data-ttu-id="d6e0e-115">La classe d' **\_ \_ événements** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-115">The **\_\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6e0e-116">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="d6e0e-116">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6e0e-117">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d6e0e-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d6e0e-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6e0e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6e0e-119">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-119">Descriptor that the event provider uses to determine which users can receive the event.</span></span> <span data-ttu-id="d6e0e-120">Pour plus d’informations, consultez [constantes de sécurité WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d6e0e-120">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6e0e-121">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="d6e0e-121">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6e0e-122">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d6e0e-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d6e0e-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6e0e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6e0e-124">Valeur unique qui indique l’heure à laquelle l’événement est généré.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-124">Unique value that indicates the time the event is generated.</span></span> <span data-ttu-id="d6e0e-125">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-125">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="d6e0e-126">Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="d6e0e-126">The information is in the Coordinated Universal Time (UTC) format.</span></span>

<span data-ttu-id="d6e0e-127">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d6e0e-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6e0e-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d6e0e-128">Remarks</span></span>

<span data-ttu-id="d6e0e-129">La classe d' **\_ \_ événements** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-129">The **\_\_Event** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e0e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6e0e-130">Requirements</span></span>



| <span data-ttu-id="d6e0e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6e0e-131">Requirement</span></span> | <span data-ttu-id="d6e0e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6e0e-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d6e0e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6e0e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e0e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6e0e-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d6e0e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6e0e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e0e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6e0e-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d6e0e-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d6e0e-137">Namespace</span></span><br/>                | <span data-ttu-id="d6e0e-138">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="d6e0e-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d6e0e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6e0e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e0e-140">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="d6e0e-140">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="d6e0e-141">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="d6e0e-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d6e0e-142">Détermination du type d’événement à recevoir</span><span class="sxs-lookup"><span data-stu-id="d6e0e-142">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="d6e0e-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d6e0e-143">**\_\_ClassOperationEvent**</span></span>](--classoperationevent.md)
</dt> <dt>

[<span data-ttu-id="d6e0e-144">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d6e0e-144">**\_\_InstanceOperationEvent**</span></span>](--instanceoperationevent.md)
</dt> <dt>

[<span data-ttu-id="d6e0e-145">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d6e0e-145">**\_\_NamespaceOperationEvent**</span></span>](--namespaceoperationevent.md)
</dt> </dl>

 

