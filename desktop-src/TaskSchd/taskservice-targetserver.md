---
title: TaskService. TargetServer, propriété
description: Pour les scripts, obtient le nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- Propriété TargetServer Planificateur de tâches
- Propriété TargetServer Planificateur de tâches, objet TaskService
- Objet TaskService Planificateur de tâches, propriété TargetServer
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519097"
---
# <a name="taskservicetargetserver-property"></a><span data-ttu-id="84a7f-106">TaskService. TargetServer, propriété</span><span class="sxs-lookup"><span data-stu-id="84a7f-106">TaskService.TargetServer property</span></span>

<span data-ttu-id="84a7f-107">Pour les scripts, obtient le nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="84a7f-107">For scripting, gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a7f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84a7f-108">Syntax</span></span>


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a><span data-ttu-id="84a7f-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="84a7f-109">Property value</span></span>

<span data-ttu-id="84a7f-110">Nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="84a7f-110">The name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="remarks"></a><span data-ttu-id="84a7f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="84a7f-111">Remarks</span></span>

<span data-ttu-id="84a7f-112">Cette propriété retourne une chaîne vide lorsque l’utilisateur passe une adresse IP, localhost ou'. 'en tant que paramètre, et retourne le nom de l’ordinateur qui exécute le service Planificateur de tâches lorsque l’utilisateur ne passe aucune valeur de paramètre.</span><span class="sxs-lookup"><span data-stu-id="84a7f-112">This property returns an empty string when the user passes an IP address, Localhost, or '.' as a parameter, and it returns the name of the computer that is running the Task Scheduler service when the user does not pass any parameter value.</span></span>

## <a name="requirements"></a><span data-ttu-id="84a7f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84a7f-113">Requirements</span></span>



| <span data-ttu-id="84a7f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84a7f-114">Requirement</span></span> | <span data-ttu-id="84a7f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="84a7f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84a7f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84a7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84a7f-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84a7f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="84a7f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84a7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84a7f-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84a7f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="84a7f-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="84a7f-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="84a7f-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="84a7f-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="84a7f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="84a7f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84a7f-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84a7f-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





