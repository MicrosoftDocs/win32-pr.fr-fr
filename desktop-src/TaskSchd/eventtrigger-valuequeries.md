---
title: Propriété EventTrigger. ValueQueries
description: Pour les scripts, obtient ou définit une collection de requêtes XPath nommées. Chaque requête de la collection est appliquée au dernier fichier XML d’événement correspondant retourné par la requête d’abonnement spécifiée dans la propriété Subscription.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Planificateur de tâches de la propriété ValueQueries
- Planificateur de tâches de propriété ValueQueries, objet EventTrigger
- Objet EventTrigger Planificateur de tâches, propriété ValueQueries
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509062"
---
# <a name="eventtriggervaluequeries-property"></a><span data-ttu-id="67ec0-107">Propriété EventTrigger. ValueQueries</span><span class="sxs-lookup"><span data-stu-id="67ec0-107">EventTrigger.ValueQueries property</span></span>

<span data-ttu-id="67ec0-108">Pour les scripts, obtient ou définit une collection de requêtes XPath nommées.</span><span class="sxs-lookup"><span data-stu-id="67ec0-108">For scripting, gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="67ec0-109">Chaque requête de la collection est appliquée au dernier fichier XML d’événement correspondant retourné par la requête d’abonnement spécifiée dans la propriété [**subscription**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="67ec0-109">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ec0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67ec0-110">Syntax</span></span>


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a><span data-ttu-id="67ec0-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="67ec0-111">Property value</span></span>

<span data-ttu-id="67ec0-112">Collection de paires nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="67ec0-112">A collection of of name-value pairs.</span></span> <span data-ttu-id="67ec0-113">Chaque paire nom-valeur de la collection définit un nom unique pour une valeur de propriété de l’événement qui déclenche le déclencheur d’événement.</span><span class="sxs-lookup"><span data-stu-id="67ec0-113">Each name-value pair in the collection defines a unique name for a property value of the event that triggers the event trigger.</span></span> <span data-ttu-id="67ec0-114">La valeur de la propriété de l’événement est définie en tant que requête d’événement XPath.</span><span class="sxs-lookup"><span data-stu-id="67ec0-114">The property value of the event is defined as an XPath event query.</span></span> <span data-ttu-id="67ec0-115">Pour plus d’informations sur les requêtes d’événements XPath, consultez [sélection des événements](/previous-versions//aa385231(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ec0-115">For more information about XPath event queries, see [Event Selection](/previous-versions//aa385231(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="67ec0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="67ec0-116">Remarks</span></span>

<span data-ttu-id="67ec0-117">Le nom de la requête peut être utilisé en tant que variable dans les propriétés d’action suivantes :</span><span class="sxs-lookup"><span data-stu-id="67ec0-117">The name of the query can be used as a variable in the following action properties:</span></span>

-   [<span data-ttu-id="67ec0-118">**ShowMessageAction. MessageBody**</span><span class="sxs-lookup"><span data-stu-id="67ec0-118">**ShowMessageAction.MessageBody**</span></span>](showmessageaction-messagebody.md)
-   [<span data-ttu-id="67ec0-119">**ShowMessageAction. title**</span><span class="sxs-lookup"><span data-stu-id="67ec0-119">**ShowMessageAction.Title**</span></span>](showmessageaction-title.md)
-   [<span data-ttu-id="67ec0-120">**ExecAction. arguments**</span><span class="sxs-lookup"><span data-stu-id="67ec0-120">**ExecAction.Arguments**</span></span>](execaction-arguments.md)
-   [<span data-ttu-id="67ec0-121">**ExecAction. WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="67ec0-121">**ExecAction.WorkingDirectory**</span></span>](execaction-workingdirectory.md)
-   [<span data-ttu-id="67ec0-122">**EmailAction. Server**</span><span class="sxs-lookup"><span data-stu-id="67ec0-122">**EmailAction.Server**</span></span>](emailaction-server.md)
-   [<span data-ttu-id="67ec0-123">**EmailAction. Subject**</span><span class="sxs-lookup"><span data-stu-id="67ec0-123">**EmailAction.Subject**</span></span>](emailaction-subject.md)
-   [<span data-ttu-id="67ec0-124">**EmailAction.To**</span><span class="sxs-lookup"><span data-stu-id="67ec0-124">**EmailAction.To**</span></span>](emailaction-to.md)
-   [<span data-ttu-id="67ec0-125">**EmailAction.Cc**</span><span class="sxs-lookup"><span data-stu-id="67ec0-125">**EmailAction.Cc**</span></span>](emailaction-cc.md)
-   [<span data-ttu-id="67ec0-126">**EmailAction. CCI**</span><span class="sxs-lookup"><span data-stu-id="67ec0-126">**EmailAction.Bcc**</span></span>](emailaction-bcc.md)
-   [<span data-ttu-id="67ec0-127">**EmailAction. ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="67ec0-127">**EmailAction.ReplyTo**</span></span>](emailaction-replyto.md)
-   [<span data-ttu-id="67ec0-128">**EmailAction. from**</span><span class="sxs-lookup"><span data-stu-id="67ec0-128">**EmailAction.From**</span></span>](emailaction-from.md)
-   [<span data-ttu-id="67ec0-129">**EmailAction. Body**</span><span class="sxs-lookup"><span data-stu-id="67ec0-129">**EmailAction.Body**</span></span>](emailaction-body.md)
-   [<span data-ttu-id="67ec0-130">**ComHandlerAction. Data**</span><span class="sxs-lookup"><span data-stu-id="67ec0-130">**ComHandlerAction.Data**</span></span>](comhandleraction-data.md)

<span data-ttu-id="67ec0-131">Les chaînes d’exemple de code suivantes affichent deux paires nom/valeur qui peuvent être utilisées dans une collection nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="67ec0-131">The following code example strings show two name value pairs that can be used in a name-value collection.</span></span> <span data-ttu-id="67ec0-132">Les valeurs retournées par les requêtes XPath peuvent remplacer des variables dans la propriété d’une action.</span><span class="sxs-lookup"><span data-stu-id="67ec0-132">The values returned by the XPath queries can replace variables in an action's property.</span></span> <span data-ttu-id="67ec0-133">Les valeurs sont référencées par nom, avec `$(user)` et `$(machine)` , dans la propriété action.</span><span class="sxs-lookup"><span data-stu-id="67ec0-133">The values are referenced by name, with `$(user)` and `$(machine)`, in the action property.</span></span> <span data-ttu-id="67ec0-134">Par exemple, si les `$(user)` `$(machine)` variables et sont utilisées dans la chaîne [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md) , la valeur des requêtes XPath remplace les variables de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="67ec0-134">For example, if the `$(user)` and `$(machine)` variables are used in the [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md) string, then the value of the XPath queries will replace the variables in the string.</span></span>

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

<span data-ttu-id="67ec0-135">Pour plus d’informations sur l’écriture d’une chaîne de requête pour certains événements, consultez [sélection d’événements](/previous-versions//aa385231(v=vs.85)) et [abonnement à des événements](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="67ec0-135">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67ec0-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67ec0-136">Requirements</span></span>



| <span data-ttu-id="67ec0-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67ec0-137">Requirement</span></span> | <span data-ttu-id="67ec0-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="67ec0-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67ec0-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67ec0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="67ec0-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67ec0-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="67ec0-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67ec0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="67ec0-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67ec0-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67ec0-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="67ec0-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="67ec0-144"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="67ec0-144"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="67ec0-145">DLL</span><span class="sxs-lookup"><span data-stu-id="67ec0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67ec0-146"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67ec0-146"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ec0-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67ec0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ec0-148">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="67ec0-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="67ec0-149">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="67ec0-149">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

