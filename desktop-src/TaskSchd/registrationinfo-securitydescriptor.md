---
title: RegistrationInfo. SecurityDescriptor, propriété
description: Pour les scripts, obtient ou définit le descripteur de sécurité de la tâche.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Propriété SecurityDescriptor Planificateur de tâches
- Propriété SecurityDescriptor Planificateur de tâches, objet RegistrationInfo
- Objet RegistrationInfo Planificateur de tâches, propriété SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510928"
---
# <a name="registrationinfosecuritydescriptor-property"></a><span data-ttu-id="787e7-106">RegistrationInfo. SecurityDescriptor, propriété</span><span class="sxs-lookup"><span data-stu-id="787e7-106">RegistrationInfo.SecurityDescriptor property</span></span>

<span data-ttu-id="787e7-107">Pour les scripts, obtient ou définit le descripteur de sécurité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="787e7-107">For scripting, gets or sets the security descriptor of the task.</span></span> <span data-ttu-id="787e7-108">Si un descripteur de sécurité différent est fourni lors de l’inscription de la tâche, il remplacera le descripteur de sécurité défini par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="787e7-108">If a different security descriptor is supplied during task registration, it will supersede the security descriptor set with this property.</span></span>

## <a name="syntax"></a><span data-ttu-id="787e7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="787e7-109">Syntax</span></span>


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a><span data-ttu-id="787e7-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="787e7-110">Property value</span></span>

<span data-ttu-id="787e7-111">Descripteur de sécurité associé à la tâche.</span><span class="sxs-lookup"><span data-stu-id="787e7-111">The security descriptor that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="787e7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="787e7-112">Remarks</span></span>

<span data-ttu-id="787e7-113">Lors de la lecture ou de l’écriture de données XML pour une tâche, le descripteur de sécurité de la tâche est spécifié à l’aide de l’élément [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="787e7-113">When reading or writing XML for a task, the security descriptor of the task is specified using the [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="787e7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="787e7-114">Requirements</span></span>



| <span data-ttu-id="787e7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="787e7-115">Requirement</span></span> | <span data-ttu-id="787e7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="787e7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="787e7-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="787e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="787e7-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="787e7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="787e7-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="787e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="787e7-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="787e7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="787e7-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="787e7-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="787e7-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="787e7-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="787e7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="787e7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="787e7-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="787e7-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="787e7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="787e7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787e7-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="787e7-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





