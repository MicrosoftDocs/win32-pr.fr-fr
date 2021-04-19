---
description: Provoque la génération d’un événement à une date spécifique à un moment donné.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: Classe __AbsoluteTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524739"
---
# <a name="__absolutetimerinstruction-class"></a><span data-ttu-id="5d36a-103">\_\_AbsoluteTimerInstruction, classe</span><span class="sxs-lookup"><span data-stu-id="5d36a-103">\_\_AbsoluteTimerInstruction class</span></span>

<span data-ttu-id="5d36a-104">La classe système **\_ \_ AbsoluteTimerInstruction** provoque la génération d’un événement à une date spécifique à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="5d36a-104">The **\_\_AbsoluteTimerInstruction** system class causes an event to be generated on a specific date at a specific time.</span></span> <span data-ttu-id="5d36a-105">Un consommateur d’événements s’inscrit pour recevoir un événement de minuteur absolu en créant une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="5d36a-105">An event consumer registers to receive an absolute timer event by creating an instance of this class.</span></span> <span data-ttu-id="5d36a-106">L’événement est généré une fois.</span><span class="sxs-lookup"><span data-stu-id="5d36a-106">The event is generated one time.</span></span>

<span data-ttu-id="5d36a-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5d36a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5d36a-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5d36a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d36a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d36a-109">Syntax</span></span>

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a><span data-ttu-id="5d36a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="5d36a-110">Members</span></span>

<span data-ttu-id="5d36a-111">La classe **\_ \_ AbsoluteTimerInstruction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5d36a-111">The **\_\_AbsoluteTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="5d36a-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5d36a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d36a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5d36a-113">Properties</span></span>

<span data-ttu-id="5d36a-114">La classe **\_ \_ AbsoluteTimerInstruction** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5d36a-114">The **\_\_AbsoluteTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d36a-115">**EventDateTime**</span><span class="sxs-lookup"><span data-stu-id="5d36a-115">**EventDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d36a-116">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5d36a-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5d36a-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5d36a-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5d36a-118">Chaîne de longueur fixe au [format DMTF](date-and-time-format.md) qui spécifie le moment où le minuteur se déclenche.</span><span class="sxs-lookup"><span data-stu-id="5d36a-118">Fixed-length string in [DMTF format](date-and-time-format.md) that specifies when the timer fires.</span></span>

</dd> <dt>

<span data-ttu-id="5d36a-119">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="5d36a-119">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d36a-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5d36a-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d36a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d36a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d36a-122">Si la **valeur est true**, l’événement du minuteur se produit si WMI ne peut pas le générer à l’intervalle de temps approprié, ou si le consommateur qui demande à recevoir l’événement n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="5d36a-122">If **TRUE**, the timer event occurs if WMI cannot generate it at the correct time interval, or the consumer requesting to receive the event is unavailable.</span></span> <span data-ttu-id="5d36a-123">Si la **valeur est true**, l’événement ne se produit pas.</span><span class="sxs-lookup"><span data-stu-id="5d36a-123">If **TRUE**, the event will not occur.</span></span> <span data-ttu-id="5d36a-124">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-124">The default is **FALSE**.</span></span> <span data-ttu-id="5d36a-125">Lorsque WMI ou le consommateur devient disponible, un événement de notification est généré et reçu.</span><span class="sxs-lookup"><span data-stu-id="5d36a-125">When WMI or the consumer becomes available, a notification event is generated and received.</span></span> <span data-ttu-id="5d36a-126">Cette propriété est héritée de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="5d36a-126">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="5d36a-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="5d36a-127">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="5d36a-128">Lorsque WMI ou le consommateur redevient disponible, un événement de notification est généré et reçu.</span><span class="sxs-lookup"><span data-stu-id="5d36a-128">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="5d36a-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="5d36a-129">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="5d36a-130">L’événement du minuteur ne se produit pas si WMI n’est pas disponible pour le générer à l’intervalle de temps approprié, ou si le consommateur qui demande à recevoir l’événement n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="5d36a-130">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d36a-131">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="5d36a-131">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d36a-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5d36a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d36a-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d36a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d36a-134">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5d36a-134">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5d36a-135">Chaîne unique assignée par l’utilisateur qui identifie un événement de minuteur spécifique.</span><span class="sxs-lookup"><span data-stu-id="5d36a-135">Unique user-assigned string that identifies a specific timer event.</span></span> <span data-ttu-id="5d36a-136">Pour éviter les conflits de noms avec d’autres identificateurs de minuterie, la forme de chaîne d’un GUID de style d’environnement d’ordinateur distribué peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="5d36a-136">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment style GUID can be used.</span></span> <span data-ttu-id="5d36a-137">Cette propriété est héritée de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="5d36a-137">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d36a-138">Notes</span><span class="sxs-lookup"><span data-stu-id="5d36a-138">Remarks</span></span>

<span data-ttu-id="5d36a-139">La classe **\_ \_ AbsoluteTimerInstruction** est dérivée de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="5d36a-139">The **\_\_AbsoluteTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="5d36a-140">WMI génère l’événement de minuteur absolu en créant une instance de la classe [**\_ \_ TimerEvent**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="5d36a-140">WMI generates the absolute timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d36a-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d36a-141">Requirements</span></span>



| <span data-ttu-id="5d36a-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d36a-142">Requirement</span></span> | <span data-ttu-id="5d36a-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d36a-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5d36a-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d36a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5d36a-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d36a-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5d36a-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d36a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5d36a-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d36a-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5d36a-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5d36a-148">Namespace</span></span><br/>                | <span data-ttu-id="5d36a-149">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="5d36a-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5d36a-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d36a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d36a-151">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="5d36a-151">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="5d36a-152">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="5d36a-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5d36a-153">Réception d’événements chronométrés ou répétitifs</span><span class="sxs-lookup"><span data-stu-id="5d36a-153">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[<span data-ttu-id="5d36a-154">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="5d36a-154">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="5d36a-155">Réception d’événements pendant la durée de votre application</span><span class="sxs-lookup"><span data-stu-id="5d36a-155">Receiving Events for the Duration of Your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

