---
description: Génère des événements à intervalles réguliers, comme un \_ message du minuteur WM dans la programmation Windows.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: Classe __IntervalTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536611"
---
# <a name="__intervaltimerinstruction-class"></a><span data-ttu-id="452ea-103">\_\_IntervalTimerInstruction, classe</span><span class="sxs-lookup"><span data-stu-id="452ea-103">\_\_IntervalTimerInstruction class</span></span>

<span data-ttu-id="452ea-104">La classe système **\_ \_ IntervalTimerInstruction** génère des événements à intervalles réguliers, comme un \_ message de minuteur WM dans la programmation Windows.</span><span class="sxs-lookup"><span data-stu-id="452ea-104">The **\_\_IntervalTimerInstruction** system class generates events at intervals, similar to a WM\_TIMER message in Windows programming.</span></span> <span data-ttu-id="452ea-105">Un consommateur d’événements s’inscrit pour recevoir des événements de minuterie d’intervalle en créant une requête d’événement qui fait référence à cette classe.</span><span class="sxs-lookup"><span data-stu-id="452ea-105">An event consumer registers to receive interval timer events by creating an event query that references this class.</span></span> <span data-ttu-id="452ea-106">En raison du comportement du système d’exploitation, il n’existe aucune garantie que les événements seront remis à l’intervalle demandé précisément.</span><span class="sxs-lookup"><span data-stu-id="452ea-106">Due to operating system behavior, there are no guarantees that events will be delivered at precisely the requested interval.</span></span>

<span data-ttu-id="452ea-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="452ea-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="452ea-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="452ea-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="452ea-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="452ea-109">Syntax</span></span>

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="452ea-110">Membres</span><span class="sxs-lookup"><span data-stu-id="452ea-110">Members</span></span>

<span data-ttu-id="452ea-111">La classe **\_ \_ IntervalTimerInstruction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="452ea-111">The **\_\_IntervalTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="452ea-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="452ea-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="452ea-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="452ea-113">Properties</span></span>

<span data-ttu-id="452ea-114">La classe **\_ \_ IntervalTimerInstruction** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="452ea-114">The **\_\_IntervalTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="452ea-115">**IntervalBetweenEvents**</span><span class="sxs-lookup"><span data-stu-id="452ea-115">**IntervalBetweenEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452ea-116">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="452ea-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="452ea-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="452ea-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452ea-118">Qualificateurs : [**unités**](standard-qualifiers.md) (millisecondes)</span><span class="sxs-lookup"><span data-stu-id="452ea-118">Qualifiers: [**Units**](standard-qualifiers.md) (milliseconds)</span></span>
</dt> </dl>

<span data-ttu-id="452ea-119">Nombre de millisecondes entre les déclenchements d’événements.</span><span class="sxs-lookup"><span data-stu-id="452ea-119">Number of milliseconds between event firings.</span></span>

</dd> <dt>

<span data-ttu-id="452ea-120">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="452ea-120">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452ea-121">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="452ea-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="452ea-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="452ea-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="452ea-123">Si la **valeur est true**, cet événement doit être ignoré si l’intervalle est déjà passé.</span><span class="sxs-lookup"><span data-stu-id="452ea-123">If **TRUE**, this event is to be skipped if the interval is already passed.</span></span> <span data-ttu-id="452ea-124">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="452ea-124">The default is **FALSE**.</span></span> <span data-ttu-id="452ea-125">Cette propriété est héritée de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="452ea-125">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="452ea-126">FALSE</span><span class="sxs-lookup"><span data-stu-id="452ea-126">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="452ea-127">Lorsque WMI ou le consommateur redevient disponible, un événement de notification est généré et reçu.</span><span class="sxs-lookup"><span data-stu-id="452ea-127">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="452ea-128">TRUE</span><span class="sxs-lookup"><span data-stu-id="452ea-128">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="452ea-129">L’événement du minuteur ne se produit pas si WMI n’est pas disponible pour le générer à l’intervalle de temps approprié, ou si le consommateur qui demande à recevoir l’événement n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="452ea-129">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="452ea-130">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="452ea-130">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452ea-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="452ea-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452ea-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="452ea-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452ea-133">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="452ea-133">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="452ea-134">Identificateur unique de cet objet **\_ \_ IntervalTimerInstruction** .</span><span class="sxs-lookup"><span data-stu-id="452ea-134">Unique identifier for this **\_\_IntervalTimerInstruction** object.</span></span> <span data-ttu-id="452ea-135">Cette propriété est héritée de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="452ea-135">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="452ea-136">Notes</span><span class="sxs-lookup"><span data-stu-id="452ea-136">Remarks</span></span>

<span data-ttu-id="452ea-137">La classe **\_ \_ IntervalTimerInstruction** est dérivée de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="452ea-137">The **\_\_IntervalTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="452ea-138">La requête d’événement entrée pour s’inscrire à un événement de minuteur d’intervalle est généralement basée sur la propriété **timerId** .</span><span class="sxs-lookup"><span data-stu-id="452ea-138">The event query entered to register for an interval timer event is usually based on the **TimerId** property.</span></span> <span data-ttu-id="452ea-139">Les événements de notification générés à partir d’un événement intervalle de minuterie contiennent la propriété **NumFirings** qui contient des données reflétant le nombre d’événements déclenchés au moment où les événements n’ont pas pu être reçus.</span><span class="sxs-lookup"><span data-stu-id="452ea-139">Notification events generated from an interval timer event contain the property **NumFirings** which contains data reflecting how many events fired during the time the events were unable to be received.</span></span> <span data-ttu-id="452ea-140">Si **SkipIfPassed** a la valeur **true**, ces informations sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="452ea-140">If **SkipIfPassed** is set to **TRUE**, that information is discarded.</span></span>

<span data-ttu-id="452ea-141">La valeur de la propriété **IntervalBetweenEvents** doit être raisonnablement importante.</span><span class="sxs-lookup"><span data-stu-id="452ea-141">The value for the **IntervalBetweenEvents** property should be reasonably large.</span></span> <span data-ttu-id="452ea-142">S’il est trop petit, WMI peut l’ignorer et ne pas générer l’événement en raison de limitations dans certains systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="452ea-142">If it is too small, WMI may ignore it and not generate the event due to limitations in some operating systems.</span></span>

<span data-ttu-id="452ea-143">WMI génère l’événement du minuteur d’intervalle en créant une instance de la classe [**\_ \_ TimerEvent**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="452ea-143">WMI generates the interval timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

<span data-ttu-id="452ea-144">Pour recevoir ces événements de minuterie dans un consommateur d’événements temporaire, exécutez [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) avec la chaîne de requête d’événement suivante :</span><span class="sxs-lookup"><span data-stu-id="452ea-144">To receive these timer events in a temporary event consumer, execute [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) with the following event query string:</span></span>


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



<span data-ttu-id="452ea-145">Pour recevoir ces événements de minuterie dans un consommateur d’événements permanent, vous devez charger la requête précédente dans un filtre d’événements, définir un consommateur logique et créer une liaison de filtre à consommateur pour le filtre et le consommateur.</span><span class="sxs-lookup"><span data-stu-id="452ea-145">To receive these timer events in a permanent event consumer, you must load the previous query into an event filter, define a logical consumer, and create a filter-to-consumer binding for the filter and consumer.</span></span> <span data-ttu-id="452ea-146">Pour plus d’informations, consultez [réception d’événements à tout moment](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="452ea-146">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

## <a name="examples"></a><span data-ttu-id="452ea-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="452ea-147">Examples</span></span>

<span data-ttu-id="452ea-148">La déclaration MOF suivante montre comment générer un événement de minuteur Interval avec la propriété Key définie sur « MyEvent » toutes les 10 secondes :</span><span class="sxs-lookup"><span data-stu-id="452ea-148">The following MOF declaration shows how to generate an interval timer event with the key property set to "MyEvent" every 10 seconds:</span></span>


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a><span data-ttu-id="452ea-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="452ea-149">Requirements</span></span>



| <span data-ttu-id="452ea-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="452ea-150">Requirement</span></span> | <span data-ttu-id="452ea-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="452ea-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="452ea-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="452ea-152">Minimum supported client</span></span><br/> | <span data-ttu-id="452ea-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="452ea-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="452ea-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="452ea-154">Minimum supported server</span></span><br/> | <span data-ttu-id="452ea-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="452ea-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="452ea-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="452ea-156">Namespace</span></span><br/>                | <span data-ttu-id="452ea-157">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="452ea-157">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="452ea-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="452ea-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452ea-159">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="452ea-159">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="452ea-160">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="452ea-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="452ea-161">Réception d’événements chronométrés ou répétitifs</span><span class="sxs-lookup"><span data-stu-id="452ea-161">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

