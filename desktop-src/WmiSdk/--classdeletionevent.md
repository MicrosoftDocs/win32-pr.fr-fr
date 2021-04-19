---
description: Représente un événement de suppression de classe, qui est un type d’événement intrinsèque généré lorsqu’une classe est supprimée de l’espace de noms.
ms.assetid: dd44c03e-4d0d-4750-942d-495893d21650
ms.tgt_platform: multiple
title: Classe __ClassDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29242335edeffbdc44deebb3acacd5631fcc7b68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536164"
---
# <a name="__classdeletionevent-class"></a><span data-ttu-id="53b5c-103">\_\_ClassDeletionEvent, classe</span><span class="sxs-lookup"><span data-stu-id="53b5c-103">\_\_ClassDeletionEvent class</span></span>

<span data-ttu-id="53b5c-104">La classe système **\_ \_ ClassDeletionEvent** représente un événement de suppression de classe, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) généré lorsqu’une classe est supprimée de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="53b5c-104">The **\_\_ClassDeletionEvent** system class represents a class deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is removed from the namespace.</span></span>

<span data-ttu-id="53b5c-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="53b5c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="53b5c-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="53b5c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b5c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53b5c-107">Syntax</span></span>

``` syntax
class __ClassDeletionEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="53b5c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="53b5c-108">Members</span></span>

<span data-ttu-id="53b5c-109">La classe **\_ \_ ClassDeletionEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="53b5c-109">The **\_\_ClassDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="53b5c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53b5c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53b5c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53b5c-111">Properties</span></span>

<span data-ttu-id="53b5c-112">La classe **\_ \_ ClassDeletionEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="53b5c-112">The **\_\_ClassDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53b5c-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="53b5c-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53b5c-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="53b5c-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="53b5c-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53b5c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53b5c-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="53b5c-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="53b5c-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="53b5c-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="53b5c-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="53b5c-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53b5c-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="53b5c-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="53b5c-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53b5c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53b5c-121">Copie de la classe récemment supprimée signalée par l’événement de suppression de classe.</span><span class="sxs-lookup"><span data-stu-id="53b5c-121">Copy of the newly deleted class reported by the class deletion event.</span></span> <span data-ttu-id="53b5c-122">Cette propriété est héritée de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="53b5c-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="53b5c-123">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="53b5c-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53b5c-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="53b5c-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="53b5c-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53b5c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53b5c-126">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="53b5c-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="53b5c-127">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="53b5c-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="53b5c-128">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="53b5c-128">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="53b5c-129">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="53b5c-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="53b5c-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="53b5c-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53b5c-131">Notes</span><span class="sxs-lookup"><span data-stu-id="53b5c-131">Remarks</span></span>

<span data-ttu-id="53b5c-132">La classe **\_ \_ ClassDeletionEvent** est dérivée de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="53b5c-132">The **\_\_ClassDeletionEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53b5c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53b5c-133">Requirements</span></span>



| <span data-ttu-id="53b5c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53b5c-134">Requirement</span></span> | <span data-ttu-id="53b5c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="53b5c-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="53b5c-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53b5c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="53b5c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53b5c-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="53b5c-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53b5c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="53b5c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53b5c-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="53b5c-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="53b5c-140">Namespace</span></span><br/>                | <span data-ttu-id="53b5c-141">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="53b5c-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="53b5c-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53b5c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b5c-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="53b5c-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="53b5c-144">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="53b5c-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

