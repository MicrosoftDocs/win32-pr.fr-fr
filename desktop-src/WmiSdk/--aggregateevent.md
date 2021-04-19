---
description: Représente un événement d’agrégation de plusieurs événements intrinsèques ou extrinsèques individuels.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: Classe __AggregateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534734"
---
# <a name="__aggregateevent-class"></a><span data-ttu-id="7b190-103">\_\_AggregateEvent, classe</span><span class="sxs-lookup"><span data-stu-id="7b190-103">\_\_AggregateEvent class</span></span>

<span data-ttu-id="7b190-104">La classe système **\_ \_ AggregateEvent** représente un événement d’agrégation de plusieurs événements intrinsèques ou extrinsèques individuels.</span><span class="sxs-lookup"><span data-stu-id="7b190-104">The **\_\_AggregateEvent** system class represents an aggregate event of several individual intrinsic or extrinsic events.</span></span> <span data-ttu-id="7b190-105">WMI génère une instance de **\_ \_ AggregateEvent** au lieu d’un [**\_ \_ événement**](--event.md) lorsque les consommateurs s’inscrivent auprès de la clause [Group within](group-clause.md) dans leur requête d’événement.</span><span class="sxs-lookup"><span data-stu-id="7b190-105">WMI generates an instance of **\_\_AggregateEvent** rather than [**\_\_Event**](--event.md) when consumers register with the [GROUP WITHIN](group-clause.md) clause in their event query.</span></span>

<span data-ttu-id="7b190-106">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7b190-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7b190-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7b190-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b190-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b190-108">Syntax</span></span>

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a><span data-ttu-id="7b190-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7b190-109">Members</span></span>

<span data-ttu-id="7b190-110">La classe **\_ \_ AggregateEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b190-110">The **\_\_AggregateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="7b190-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b190-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b190-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b190-112">Properties</span></span>

<span data-ttu-id="7b190-113">La classe **\_ \_ AggregateEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b190-113">The **\_\_AggregateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b190-114">**NumberOfEvents**</span><span class="sxs-lookup"><span data-stu-id="7b190-114">**NumberOfEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b190-115">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b190-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b190-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b190-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b190-117">Nombre d’événements combinés pour produire cet événement de résumé unique.</span><span class="sxs-lookup"><span data-stu-id="7b190-117">Number of events combined to produce this single summary event.</span></span>

</dd> <dt>

<span data-ttu-id="7b190-118">**Representative**</span><span class="sxs-lookup"><span data-stu-id="7b190-118">**Representative**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b190-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="7b190-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7b190-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b190-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b190-121">Copie de l’un des événements remis dans l’intervalle d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="7b190-121">Copy of one of the events delivered within the aggregation interval.</span></span> <span data-ttu-id="7b190-122">Par exemple, si un consommateur s’est inscrit pour les événements de modification de clé de Registre à partir du fournisseur d’événements du Registre, le **représentant** contiendrait une instance de la classe **RegistryKeyChangeEvent** .</span><span class="sxs-lookup"><span data-stu-id="7b190-122">For example, if a consumer has registered for registry key change events from the Registry Event provider, **Representative** would hold an instance of the **RegistryKeyChangeEvent** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b190-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7b190-123">Remarks</span></span>

<span data-ttu-id="7b190-124">La classe **\_ \_ AggregateEvent** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7b190-124">The **\_\_AggregateEvent** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="7b190-125">Les fournisseurs d’événements ne génèrent jamais d’événements d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="7b190-125">Event providers never generate aggregate events.</span></span> <span data-ttu-id="7b190-126">Ils doivent ignorer la clause GROUP WITHIN dans le traitement des requêtes d’événements.</span><span class="sxs-lookup"><span data-stu-id="7b190-126">They must ignore the GROUP WITHIN clause in their processing of event queries.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b190-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b190-127">Requirements</span></span>



| <span data-ttu-id="7b190-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b190-128">Requirement</span></span> | <span data-ttu-id="7b190-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b190-129">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7b190-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b190-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7b190-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b190-131">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7b190-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b190-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7b190-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b190-133">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7b190-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7b190-134">Namespace</span></span><br/>                | <span data-ttu-id="7b190-135">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="7b190-135">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7b190-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b190-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b190-137">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="7b190-137">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="7b190-138">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="7b190-138">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="7b190-139">Interrogation avec WQL</span><span class="sxs-lookup"><span data-stu-id="7b190-139">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

