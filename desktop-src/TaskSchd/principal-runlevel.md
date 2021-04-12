---
title: Propriété principal. RunLevel
description: Pour les scripts, obtient ou définit l’identificateur qui est utilisé pour spécifier le niveau de privilège requis pour exécuter les tâches associées au principal.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Planificateur de tâches de la propriété RunLevel
- Planificateur de tâches de la propriété RunLevel, objet principal
- Planificateur de tâches de l’objet principal, propriété RunLevel
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508661"
---
# <a name="principalrunlevel-property"></a><span data-ttu-id="52e97-106">Propriété principal. RunLevel</span><span class="sxs-lookup"><span data-stu-id="52e97-106">Principal.RunLevel property</span></span>

<span data-ttu-id="52e97-107">Pour les scripts, obtient ou définit l’identificateur qui est utilisé pour spécifier le niveau de privilège requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="52e97-107">For scripting, gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>

<span data-ttu-id="52e97-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="52e97-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="52e97-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52e97-109">Syntax</span></span>


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="52e97-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="52e97-110">Property value</span></span>

<span data-ttu-id="52e97-111">Identificateur utilisé pour spécifier le niveau de privilège requis pour exécuter les tâches qui sont associées au principal.</span><span class="sxs-lookup"><span data-stu-id="52e97-111">The identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>



| <span data-ttu-id="52e97-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="52e97-112">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="52e97-113">Signification</span><span class="sxs-lookup"><span data-stu-id="52e97-113">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <span data-ttu-id="52e97-114"><dt>**Tâche \_ RUNLEVEL \_ LUA**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52e97-114"><dt>**TASK\_RUNLEVEL\_LUA**</dt> <dt>0</dt></span></span> </dl>             | <span data-ttu-id="52e97-115">Les tâches sont exécutées avec les privilèges minimum (LUA).</span><span class="sxs-lookup"><span data-stu-id="52e97-115">Tasks will be run with the least privileges (LUA).</span></span><br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <span data-ttu-id="52e97-116"><dt>**Tâche \_ RUNLEVEL \_ le plus élevé**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="52e97-116"><dt>**TASK\_RUNLEVEL\_HIGHEST**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="52e97-117">Les tâches sont exécutées avec les privilèges les plus élevés.</span><span class="sxs-lookup"><span data-stu-id="52e97-117">Tasks will be run with the highest privileges.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="52e97-118">Notes</span><span class="sxs-lookup"><span data-stu-id="52e97-118">Remarks</span></span>

<span data-ttu-id="52e97-119">Si une tâche est inscrite à l’aide du \\ compte administrateur intégré ou des comptes système local ou service local, la propriété **runlevel** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="52e97-119">If a task is registered using the Builtin\\Administrator account or the Local System or Local Service accounts, then the **RunLevel** property will be ignored.</span></span> <span data-ttu-id="52e97-120">La valeur de propriété sera également ignorée si le contrôle de compte d’utilisateur (UAC) est désactivé.</span><span class="sxs-lookup"><span data-stu-id="52e97-120">The property value will also be ignored if User Account Control (UAC) is turned off.</span></span>

<span data-ttu-id="52e97-121">Si une tâche est inscrite à l’aide du groupe administrateurs pour le contexte de sécurité de la tâche, vous devez également définir la propriété [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) sur la **tâche \_ runlevel la \_ plus élevée** si vous souhaitez exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="52e97-121">If a task is registered using the Administrators group for the security context of the task, then you must also set the [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) property to **TASK\_RUNLEVEL\_HIGHEST** if you want to run the task.</span></span> <span data-ttu-id="52e97-122">Pour plus d’informations, consultez [contextes de sécurité pour les tâches](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="52e97-122">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52e97-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52e97-123">Requirements</span></span>



| <span data-ttu-id="52e97-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52e97-124">Requirement</span></span> | <span data-ttu-id="52e97-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="52e97-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52e97-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52e97-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52e97-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52e97-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="52e97-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52e97-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52e97-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52e97-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52e97-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="52e97-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="52e97-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="52e97-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="52e97-132">DLL</span><span class="sxs-lookup"><span data-stu-id="52e97-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52e97-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52e97-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52e97-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52e97-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e97-135">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="52e97-135">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





