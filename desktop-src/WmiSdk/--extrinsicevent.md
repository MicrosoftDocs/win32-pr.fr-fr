---
description: Sert de classe parente pour tous les types d’événements définis par l’utilisateur, également appelés événements extrinsèques.
ms.assetid: 8fddbcd1-7393-4a3b-8a10-a8b620efc19f
ms.tgt_platform: multiple
title: Classe __ExtrinsicEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtrinsicEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 76af7a9f32c24b8d44f81c60b0f2fca693c26f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210224"
---
# <a name="__extrinsicevent-class"></a><span data-ttu-id="4995f-103">\_\_ExtrinsicEvent, classe</span><span class="sxs-lookup"><span data-stu-id="4995f-103">\_\_ExtrinsicEvent class</span></span>

<span data-ttu-id="4995f-104">La classe système **\_ \_ ExtrinsicEvent** est une classe de base abstraite qui sert de classe parente pour tous les types d’événements définis par l’utilisateur, également appelés [événements extrinsèques](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="4995f-104">The **\_\_ExtrinsicEvent** system class is an abstract base class that serves as a parent class for all user-defined event types, also known as [extrinsic events](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="4995f-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4995f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4995f-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4995f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4995f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4995f-107">Syntax</span></span>

``` syntax
class __ExtrinsicEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="4995f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4995f-108">Members</span></span>

<span data-ttu-id="4995f-109">La classe **\_ \_ ExtrinsicEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4995f-109">The **\_\_ExtrinsicEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="4995f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4995f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4995f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4995f-111">Properties</span></span>

<span data-ttu-id="4995f-112">La classe **\_ \_ ExtrinsicEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4995f-112">The **\_\_ExtrinsicEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4995f-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="4995f-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4995f-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="4995f-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4995f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4995f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4995f-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="4995f-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="4995f-117">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="4995f-117">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="4995f-118">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4995f-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4995f-119">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="4995f-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4995f-120">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4995f-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4995f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4995f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4995f-122">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="4995f-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="4995f-123">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="4995f-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="4995f-124">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="4995f-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="4995f-125">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="4995f-125">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="4995f-126">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4995f-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4995f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="4995f-127">Remarks</span></span>

<span data-ttu-id="4995f-128">La classe **\_ \_ ExtrinsicEvent** est dérivée de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="4995f-128">The **\_\_ExtrinsicEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4995f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4995f-129">Requirements</span></span>



| <span data-ttu-id="4995f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4995f-130">Requirement</span></span> | <span data-ttu-id="4995f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4995f-131">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4995f-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4995f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4995f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4995f-133">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4995f-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4995f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4995f-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4995f-135">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4995f-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4995f-136">Namespace</span></span><br/>                | <span data-ttu-id="4995f-137">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="4995f-137">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4995f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4995f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4995f-139">**\_\_Événement**</span><span class="sxs-lookup"><span data-stu-id="4995f-139">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="4995f-140">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="4995f-140">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

