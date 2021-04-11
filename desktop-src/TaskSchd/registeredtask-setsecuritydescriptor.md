---
title: Méthode RegisteredTask. SetSecurityDescriptor
description: Pour les scripts, définit le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Planificateur de tâches de la méthode SetSecurityDescriptor
- Méthode SetSecurityDescriptor Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, méthode SetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105685"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a><span data-ttu-id="20ad7-106">Méthode RegisteredTask. SetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="20ad7-106">RegisteredTask.SetSecurityDescriptor method</span></span>

<span data-ttu-id="20ad7-107">Pour les scripts, définit le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="20ad7-107">For scripting, sets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ad7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20ad7-108">Syntax</span></span>


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="20ad7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20ad7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ad7-110">*langage SDDL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20ad7-110">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ad7-111">Descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="20ad7-111">The security descriptor that is used as credentials for the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="20ad7-112">Si l’accès à une tâche est refusé au compte système local, le service Planificateur de tâches peut produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="20ad7-112">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="20ad7-113">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20ad7-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ad7-114">Indicateurs qui spécifient comment définir le descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="20ad7-114">Flags that specify how to set the security descriptor.</span></span> <span data-ttu-id="20ad7-115">La tâche \_ \_ d’ajout \_ \_ de l’indicateur d’entrée de contrôle d’accès principal (0x10) à partir de l’énumération de [**\_ création de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="20ad7-115">The TASK\_DONT\_ADD\_PRINCIPAL\_ACE flag (0x10) from the [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) enumeration can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20ad7-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20ad7-116">Return value</span></span>

<span data-ttu-id="20ad7-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="20ad7-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20ad7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="20ad7-118">Remarks</span></span>

<span data-ttu-id="20ad7-119">Vous pouvez spécifier la liste de contrôle d’accès (ACL) dans le descripteur de sécurité d’une tâche afin d’autoriser ou de refuser l’accès à une tâche à certains utilisateurs et groupes.</span><span class="sxs-lookup"><span data-stu-id="20ad7-119">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ad7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20ad7-120">Requirements</span></span>



| <span data-ttu-id="20ad7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20ad7-121">Requirement</span></span> | <span data-ttu-id="20ad7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="20ad7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20ad7-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20ad7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="20ad7-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20ad7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="20ad7-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20ad7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="20ad7-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20ad7-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20ad7-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="20ad7-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="20ad7-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="20ad7-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="20ad7-129">DLL</span><span class="sxs-lookup"><span data-stu-id="20ad7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20ad7-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20ad7-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ad7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20ad7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ad7-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="20ad7-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="20ad7-133">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="20ad7-133">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="20ad7-134">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="20ad7-134">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





