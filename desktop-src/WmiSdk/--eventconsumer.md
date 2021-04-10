---
description: Est une classe de base abstraite utilisée pour l’inscription d’un consommateur d’événements permanent.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: Classe __EventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953144"
---
# <a name="__eventconsumer-class"></a><span data-ttu-id="b2bd4-103">\_\_EventConsumer, classe</span><span class="sxs-lookup"><span data-stu-id="b2bd4-103">\_\_EventConsumer class</span></span>

<span data-ttu-id="b2bd4-104">La classe système **\_ \_ EventConsumer** est une classe de base abstraite utilisée pour l’inscription d’un consommateur d’événements permanent.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-104">The **\_\_EventConsumer** system class is an abstract base class that is used in the registration of a permanent event consumer.</span></span> <span data-ttu-id="b2bd4-105">Vous pouvez dériver une nouvelle classe de consommateur d’événements à partir de **\_ \_ EventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-105">You can derive a new event consumer class from **\_\_EventConsumer**.</span></span>

<span data-ttu-id="b2bd4-106">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b2bd4-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2bd4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2bd4-108">Syntax</span></span>

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a><span data-ttu-id="b2bd4-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b2bd4-109">Members</span></span>

<span data-ttu-id="b2bd4-110">La classe **\_ \_ EventConsumer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b2bd4-110">The **\_\_EventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="b2bd4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2bd4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2bd4-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2bd4-112">Properties</span></span>

<span data-ttu-id="b2bd4-113">La classe **\_ \_ EventConsumer** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-113">The **\_\_EventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2bd4-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="b2bd4-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2bd4-115">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="b2bd4-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b2bd4-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2bd4-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2bd4-117">Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée un filtre.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="b2bd4-118">WMI stocke le SID de l’utilisateur qui crée une instance de **\_ \_ EventConsumer** ou le SID d’administrateur, selon le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-118">WMI stores the SID of the user who creates an instance of **\_\_EventConsumer** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="b2bd4-119">Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="b2bd4-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2bd4-120">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="b2bd4-120">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2bd4-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2bd4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2bd4-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2bd4-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2bd4-123">Nom de l’ordinateur sur lequel Windows Management Instrumentation (WMI) envoie des événements.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-123">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

</dd> <dt>

<span data-ttu-id="b2bd4-124">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="b2bd4-124">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2bd4-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2bd4-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2bd4-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2bd4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2bd4-127">File d’attente maximale pour un consommateur spécifique, en octets.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-127">Maximum queue for a specific consumer, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2bd4-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b2bd4-128">Remarks</span></span>

<span data-ttu-id="b2bd4-129">La classe **\_ \_ EventConsumer** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-129">The **\_\_EventConsumer** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which does not have properties.</span></span>

<span data-ttu-id="b2bd4-130">Les consommateurs permanents définissent de nouvelles classes de consommateurs pour décrire une action à entreprendre et les données à traiter lorsque les consommateurs reçoivent des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-130">Permanent consumers define new consumer classes to describe an action to take and data to be processed when consumers receive event notifications.</span></span> <span data-ttu-id="b2bd4-131">Les consommateurs permanents ont des problèmes de sécurité particuliers.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-131">Permanent consumers have special security concerns.</span></span> <span data-ttu-id="b2bd4-132">Pour plus d’informations, consultez [sécurisation des événements WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="b2bd4-132">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2bd4-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2bd4-133">Requirements</span></span>



| <span data-ttu-id="b2bd4-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2bd4-134">Requirement</span></span> | <span data-ttu-id="b2bd4-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2bd4-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b2bd4-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2bd4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b2bd4-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2bd4-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b2bd4-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2bd4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b2bd4-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2bd4-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b2bd4-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2bd4-140">Namespace</span></span><br/>                | <span data-ttu-id="b2bd4-141">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="b2bd4-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b2bd4-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2bd4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2bd4-143">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="b2bd4-143">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="b2bd4-144">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="b2bd4-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b2bd4-145">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="b2bd4-145">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="b2bd4-146">Création d’une classe de consommateur d’événements permanente</span><span class="sxs-lookup"><span data-stu-id="b2bd4-146">Creating a New Permanent Event Consumer Class</span></span>](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[<span data-ttu-id="b2bd4-147">Création d’un consommateur logique</span><span class="sxs-lookup"><span data-stu-id="b2bd4-147">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="b2bd4-148">Sécurisation des événements WMI</span><span class="sxs-lookup"><span data-stu-id="b2bd4-148">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

