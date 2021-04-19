---
title: RunningTask. EnginePID, propriété
description: Pour les scripts, obtient l’ID de processus du moteur (processus) qui exécute la tâche.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Planificateur de tâches de la propriété EnginePID
- Planificateur de tâches de la propriété EnginePID, objet RunningTask
- Planificateur de tâches objet RunningTask, propriété EnginePID
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509931"
---
# <a name="runningtaskenginepid-property"></a><span data-ttu-id="1e2b6-106">RunningTask. EnginePID, propriété</span><span class="sxs-lookup"><span data-stu-id="1e2b6-106">RunningTask.EnginePID property</span></span>

<span data-ttu-id="1e2b6-107">Pour les scripts, obtient l’ID de processus du moteur (processus) qui exécute la tâche.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-107">For scripting, gets the process ID for the engine (process) which is running the task.</span></span>

<span data-ttu-id="1e2b6-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2b6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e2b6-109">Syntax</span></span>


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a><span data-ttu-id="1e2b6-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1e2b6-110">Property value</span></span>

<span data-ttu-id="1e2b6-111">ID de processus du moteur qui exécute la tâche.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-111">The process ID for the engine which is running the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e2b6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1e2b6-112">Remarks</span></span>

<span data-ttu-id="1e2b6-113">L’ID de processus retourné par cette propriété ne peut pas être ajouté directement à une chaîne.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-113">The process ID returned by this property cannot be appended directly to a string.</span></span> <span data-ttu-id="1e2b6-114">La valeur retournée doit être convertie en une valeur entière en appelant la fonction [CInt](/previous-versions//fctcwhw9(v=vs.85)) sur la valeur retournée.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-114">The returned value needs to be converted to an integer value first by calling the [CInt](/previous-versions//fctcwhw9(v=vs.85)) function on the returned value.</span></span>


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a><span data-ttu-id="1e2b6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e2b6-115">Requirements</span></span>



| <span data-ttu-id="1e2b6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e2b6-116">Requirement</span></span> | <span data-ttu-id="1e2b6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e2b6-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2b6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e2b6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2b6-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e2b6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1e2b6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e2b6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2b6-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e2b6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e2b6-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1e2b6-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e2b6-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1e2b6-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1e2b6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1e2b6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e2b6-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e2b6-125"><dt>Taskschd.dll</dt></span></span> </dl> |



 

