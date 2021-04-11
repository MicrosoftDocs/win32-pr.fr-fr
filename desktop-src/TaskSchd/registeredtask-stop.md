---
title: RegisteredTask. Stop, méthode
description: Pour les scripts, arrête immédiatement la tâche inscrite.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Stop, méthode Planificateur de tâches
- Stop, méthode Planificateur de tâches, objet RegisteredTask
- Objet RegisteredTask Planificateur de tâches, méthode Stop
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385187"
---
# <a name="registeredtaskstop-method"></a><span data-ttu-id="c89da-106">RegisteredTask. Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="c89da-106">RegisteredTask.Stop method</span></span>

<span data-ttu-id="c89da-107">Pour les scripts, arrête immédiatement la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="c89da-107">For scripting, stops the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="c89da-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c89da-108">Syntax</span></span>


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="c89da-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c89da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c89da-110">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c89da-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c89da-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c89da-111">Reserved.</span></span> <span data-ttu-id="c89da-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c89da-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c89da-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c89da-113">Return value</span></span>

<span data-ttu-id="c89da-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c89da-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c89da-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c89da-115">Remarks</span></span>

<span data-ttu-id="c89da-116">La fonction **RegisteredTask. Stop** arrête toutes les instances de la tâche.</span><span class="sxs-lookup"><span data-stu-id="c89da-116">The **RegisteredTask.Stop** function stops all instances of the task.</span></span>

<span data-ttu-id="c89da-117">Les utilisateurs du compte système peuvent arrêter une tâche, les utilisateurs disposant de privilèges de groupe d’administrateurs peuvent arrêter une tâche et, si un utilisateur dispose de droits pour exécuter et lire une tâche, l’utilisateur peut arrêter la tâche.</span><span class="sxs-lookup"><span data-stu-id="c89da-117">System account users can stop a task, users with Administrator group privileges can stop a task, and if a user has rights to execute and read a task, then the user can stop the task.</span></span> <span data-ttu-id="c89da-118">Un utilisateur peut arrêter les instances de tâche qui s’exécutent sous les mêmes informations d’identification que le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c89da-118">A user can stop the task instances that are running under the same credentials as the user account.</span></span> <span data-ttu-id="c89da-119">Dans tous les autres cas, l’utilisateur se voit refuser l’accès pour arrêter la tâche.</span><span class="sxs-lookup"><span data-stu-id="c89da-119">In all other cases, the user is denied access to stop the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="c89da-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c89da-120">Requirements</span></span>



| <span data-ttu-id="c89da-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c89da-121">Requirement</span></span> | <span data-ttu-id="c89da-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c89da-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c89da-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c89da-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c89da-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c89da-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c89da-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c89da-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c89da-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c89da-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c89da-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c89da-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="c89da-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c89da-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c89da-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c89da-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c89da-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c89da-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c89da-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c89da-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c89da-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="c89da-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





