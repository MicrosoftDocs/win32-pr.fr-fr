---
description: Spécifie des instructions sur la façon dont les événements de minuterie doivent être générés pour les consommateurs.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: Classe __TimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321014"
---
# <a name="__timerinstruction-class"></a><span data-ttu-id="f8406-103">\_\_TimerInstruction, classe</span><span class="sxs-lookup"><span data-stu-id="f8406-103">\_\_TimerInstruction class</span></span>

<span data-ttu-id="f8406-104">La classe système abstraite **\_ \_ TimerInstruction** spécifie des instructions sur la façon dont les [événements de minuterie](receiving-a-timed-or-repeating-event.md) doivent être générés pour les consommateurs.</span><span class="sxs-lookup"><span data-stu-id="f8406-104">The **\_\_TimerInstruction** abstract system class specifies instructions on how [timer events](receiving-a-timed-or-repeating-event.md) should be generated for consumers.</span></span>

<span data-ttu-id="f8406-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f8406-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f8406-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f8406-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8406-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8406-107">Syntax</span></span>

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="f8406-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f8406-108">Members</span></span>

<span data-ttu-id="f8406-109">La classe **\_ \_ TimerInstruction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8406-109">The **\_\_TimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="f8406-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8406-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8406-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8406-111">Properties</span></span>

<span data-ttu-id="f8406-112">La classe **\_ \_ TimerInstruction** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8406-112">The **\_\_TimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8406-113">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="f8406-113">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8406-114">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f8406-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8406-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8406-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8406-116">Indique si un événement de notification sera généré et reçu quand un consommateur sera disponible.</span><span class="sxs-lookup"><span data-stu-id="f8406-116">Describes whether a notification event will be generated and receive when a consumer becomes available.</span></span>

<dt>

<span data-ttu-id="f8406-117">FALSE</span><span class="sxs-lookup"><span data-stu-id="f8406-117">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="f8406-118">Lorsque WMI ou le consommateur redevient disponible, un événement de notification est généré et reçu.</span><span class="sxs-lookup"><span data-stu-id="f8406-118">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="f8406-119">TRUE</span><span class="sxs-lookup"><span data-stu-id="f8406-119">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="f8406-120">L’événement du minuteur ne se produit pas si WMI n’est pas disponible pour le générer à l’intervalle de temps approprié, ou si le consommateur qui demande à recevoir l’événement n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="f8406-120">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f8406-121">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="f8406-121">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8406-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8406-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8406-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8406-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8406-124">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f8406-124">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f8406-125">Chaîne unique assignée par l’utilisateur qui identifie cet événement de minuteur spécifique.</span><span class="sxs-lookup"><span data-stu-id="f8406-125">Unique user-assigned string that identifies this particular timer event.</span></span> <span data-ttu-id="f8406-126">Pour éviter les conflits de noms avec d’autres identificateurs de minuterie, la forme de chaîne d’un GUID de style DCE (Distributed Computer Environment) peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8406-126">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment (DCE)-style GUID can be used.</span></span> <span data-ttu-id="f8406-127">Cette propriété fait partie de l’instance [**\_ \_ TimerEvent**](--timerevent.md) qui représente l’événement.</span><span class="sxs-lookup"><span data-stu-id="f8406-127">This property is part of the [**\_\_TimerEvent**](--timerevent.md) instance that represents the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8406-128">Notes</span><span class="sxs-lookup"><span data-stu-id="f8406-128">Remarks</span></span>

<span data-ttu-id="f8406-129">La classe **\_ \_ TimerInstruction** est dérivée de [**\_ \_ EventGenerator**](--eventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="f8406-129">The **\_\_TimerInstruction** class is derived from [**\_\_EventGenerator**](--eventgenerator.md).</span></span>

<span data-ttu-id="f8406-130">Les sous-classes **\_ \_ TimerInstruction** sont [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), utilisées par les consommateurs pour s’inscrire à un événement de minuteur absolu, et [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), utilisées pour s’inscrire à un événement de minuteur d’intervalle.</span><span class="sxs-lookup"><span data-stu-id="f8406-130">The **\_\_TimerInstruction** subclasses are [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md), used by consumers to register for an absolute timer event, and [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md), used to register for an interval timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8406-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8406-131">Requirements</span></span>



| <span data-ttu-id="f8406-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8406-132">Requirement</span></span> | <span data-ttu-id="f8406-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8406-133">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f8406-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8406-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f8406-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8406-135">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f8406-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8406-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f8406-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8406-137">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f8406-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f8406-138">Namespace</span></span><br/>                | <span data-ttu-id="f8406-139">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="f8406-139">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f8406-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8406-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8406-141">**\_\_EventGenerator**</span><span class="sxs-lookup"><span data-stu-id="f8406-141">**\_\_EventGenerator**</span></span>](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[<span data-ttu-id="f8406-142">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="f8406-142">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

