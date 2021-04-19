---
description: Utilisez la propriété Count de l’objet SWbemObjectSet pour déterminer le nombre d’éléments contenus dans une collection SWbemObjectSet. Cette propriété est en lecture seule.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Propriété SWbemObjectSet. Count (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524477"
---
# <a name="swbemobjectsetcount-property"></a><span data-ttu-id="03304-104">Propriété SWbemObjectSet. Count</span><span class="sxs-lookup"><span data-stu-id="03304-104">SWbemObjectSet.Count property</span></span>

<span data-ttu-id="03304-105">Utilisez la propriété **Count** de l’objet [**SWbemObjectSet**](swbemobjectset.md) pour déterminer le nombre d’éléments contenus dans une collection **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="03304-105">Use the **Count** property of the [**SWbemObjectSet**](swbemobjectset.md) object to determine how many items are in an **SWbemObjectSet** collection.</span></span> <span data-ttu-id="03304-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="03304-106">This property is read-only.</span></span>

<span data-ttu-id="03304-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="03304-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="03304-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="03304-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03304-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03304-109">Syntax</span></span>


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a><span data-ttu-id="03304-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="03304-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="03304-111">Notes</span><span class="sxs-lookup"><span data-stu-id="03304-111">Remarks</span></span>

<span data-ttu-id="03304-112">L’une des points à prendre en compte lors de l’utilisation de Count est que WMI ne continue pas à s’exécuter avec le nombre d’éléments d’une collection.</span><span class="sxs-lookup"><span data-stu-id="03304-112">One thing to be careful of when using Count is that WMI does not keep a running tally of the number of items in a collection.</span></span> <span data-ttu-id="03304-113">Si vous demandez un nombre pour une collection, WMI ne peut pas répondre instantanément avec un chiffre ; au lieu de cela, il doit littéralement compter les éléments, en énumérant l’ensemble de la collection.</span><span class="sxs-lookup"><span data-stu-id="03304-113">If you request Count for a collection, WMI cannot instantly respond with a number; instead, it must literally count the items, enumerating the entire collection.</span></span> <span data-ttu-id="03304-114">Pour une collection qui a relativement peu d’éléments, tels que des services, cette énumération prend probablement moins d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="03304-114">For a collection that has relatively few items, such as services, this enumeration likely takes less than a second.</span></span> <span data-ttu-id="03304-115">Toutefois, le nombre d’événements dans une collection de journaux des événements peut prendre beaucoup plus de temps.</span><span class="sxs-lookup"><span data-stu-id="03304-115">Counting the number of events in an event log collection, however, can take considerably longer.</span></span>

<span data-ttu-id="03304-116">Supposons que vous souhaitez afficher les valeurs de propriété pour chaque événement de la collection.</span><span class="sxs-lookup"><span data-stu-id="03304-116">And then suppose you want to display the property values for every event in the collection.</span></span> <span data-ttu-id="03304-117">Dans ce cas, WMI devra énumérer la totalité de la collection une deuxième fois.</span><span class="sxs-lookup"><span data-stu-id="03304-117">If so, WMI will have to enumerate the entire collection a second time.</span></span>

> [!Note]  
> <span data-ttu-id="03304-118">Si vous tentez d’obtenir cette propriété à partir d’un objet [**SWbemObjectSet**](swbemobjectset.md) qui est retourné à partir d’une méthode où les indicateurs spécifiés sont inclus dans l’indicateur wbemFlagForwardOnly, vous obtiendrez une erreur wbemErrFailed.</span><span class="sxs-lookup"><span data-stu-id="03304-118">If you attempt to get this property from an [**SWbemObjectSet**](swbemobjectset.md) object that is returned from a method where the specified flags are included the wbemFlagForwardOnly flag, you will get an wbemErrFailed error.</span></span>

 

## <a name="examples"></a><span data-ttu-id="03304-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="03304-119">Examples</span></span>

<span data-ttu-id="03304-120">Pour l’essentiel, la seule chose que vous feriez avec une SWbemObjectSet est d’énumérer tous les objets contenus dans la collection elle-même.</span><span class="sxs-lookup"><span data-stu-id="03304-120">For the most part, the only thing you will ever do with an SWbemObjectSet is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="03304-121">Toutefois, le nombre de nombres qui peut être utile dans les scripts d’administration de système.</span><span class="sxs-lookup"><span data-stu-id="03304-121">However, the Count Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="03304-122">Comme son nom l’indique, count indique le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="03304-122">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="03304-123">Par exemple, ce script récupère une collection de tous les services installés sur un ordinateur, puis renvoie le nombre total de services trouvés :</span><span class="sxs-lookup"><span data-stu-id="03304-123">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



<span data-ttu-id="03304-124">Ce qui rend le nombre utile, c’est qu’il peut vous indiquer si une instance spécifique est disponible sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="03304-124">What makes Count useful is that it can tell you whether a specific instance is available on a computer.</span></span> <span data-ttu-id="03304-125">Par exemple, ce script récupère une collection de tous les services sur un ordinateur portant le nom W3SVC.</span><span class="sxs-lookup"><span data-stu-id="03304-125">For example, this script retrieves a collection of all the services on a computer that have the Name W3SVC.</span></span> <span data-ttu-id="03304-126">Si le nombre est égal à 0 (et qu’il est valide pour les collections qui n’ont pas d’instances), cela signifie que le service W3SVC n’est pas installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="03304-126">If the Count is 0 (and it is valid for collections to have no instances), that means the W3SVC service is not installed on the computer.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a><span data-ttu-id="03304-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03304-127">Requirements</span></span>



| <span data-ttu-id="03304-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03304-128">Requirement</span></span> | <span data-ttu-id="03304-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="03304-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03304-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03304-130">Minimum supported client</span></span><br/> | <span data-ttu-id="03304-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03304-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03304-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03304-132">Minimum supported server</span></span><br/> | <span data-ttu-id="03304-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03304-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03304-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="03304-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="03304-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="03304-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="03304-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="03304-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="03304-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="03304-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="03304-138">DLL</span><span class="sxs-lookup"><span data-stu-id="03304-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03304-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03304-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="03304-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="03304-140">CLSID</span></span><br/>                    | <span data-ttu-id="03304-141">CLSID \_ SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="03304-141">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="03304-142">IID</span><span class="sxs-lookup"><span data-stu-id="03304-142">IID</span></span><br/>                      | <span data-ttu-id="03304-143">IID \_ ISWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="03304-143">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




