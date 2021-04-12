---
description: Représente un événement système.
ms.assetid: 84099483-03e4-4c21-b680-f0975b18c1f6
ms.tgt_platform: multiple
title: Classe __SystemEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7cc443c9e130106c2f5e8a05a1a2983927f1963e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209655"
---
# <a name="__systemevent-class"></a><span data-ttu-id="54c71-103">\_\_SystemEvent, classe</span><span class="sxs-lookup"><span data-stu-id="54c71-103">\_\_SystemEvent class</span></span>

<span data-ttu-id="54c71-104">La classe système **\_ \_ SystemEvent** représente un événement système.</span><span class="sxs-lookup"><span data-stu-id="54c71-104">The **\_\_SystemEvent** system class represents a system event.</span></span>

<span data-ttu-id="54c71-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="54c71-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="54c71-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="54c71-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="54c71-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54c71-107">Syntax</span></span>

``` syntax
class __SystemEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="54c71-108">Membres</span><span class="sxs-lookup"><span data-stu-id="54c71-108">Members</span></span>

<span data-ttu-id="54c71-109">La classe **\_ \_ SystemEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="54c71-109">The **\_\_SystemEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="54c71-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="54c71-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54c71-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="54c71-111">Properties</span></span>

<span data-ttu-id="54c71-112">La classe **\_ \_ SystemEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="54c71-112">The **\_\_SystemEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54c71-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="54c71-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c71-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="54c71-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="54c71-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54c71-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54c71-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="54c71-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="54c71-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="54c71-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="54c71-118">Une liste de Access Control **null** (ACL) dans [**le \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité à tout le monde en permanence.</span><span class="sxs-lookup"><span data-stu-id="54c71-118">A **NULL** Access Control List (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="54c71-119">Pour plus d’informations, consultez [création d’un descripteur de sécurité pour un nouvel objet](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="54c71-119">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="54c71-120">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="54c71-120">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c71-121">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="54c71-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="54c71-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54c71-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54c71-123">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="54c71-123">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="54c71-124">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="54c71-124">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="54c71-125">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="54c71-125">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="54c71-126">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="54c71-126">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="54c71-127">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="54c71-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54c71-128">Notes</span><span class="sxs-lookup"><span data-stu-id="54c71-128">Remarks</span></span>

<span data-ttu-id="54c71-129">La classe **\_ \_ SystemEvent** est dérivée de la classe [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="54c71-129">The **\_\_SystemEvent** class is derived from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="54c71-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54c71-130">Requirements</span></span>



| <span data-ttu-id="54c71-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54c71-131">Requirement</span></span> | <span data-ttu-id="54c71-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="54c71-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="54c71-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54c71-133">Minimum supported client</span></span><br/> | <span data-ttu-id="54c71-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54c71-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="54c71-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54c71-135">Minimum supported server</span></span><br/> | <span data-ttu-id="54c71-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54c71-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="54c71-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="54c71-137">Namespace</span></span><br/>                | <span data-ttu-id="54c71-138">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="54c71-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="54c71-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54c71-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54c71-140">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="54c71-140">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[<span data-ttu-id="54c71-141">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="54c71-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

