---
title: Méthode RegisteredTask. GetSecurityDescriptor
description: Pour les scripts, obtient le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Planificateur de tâches de la méthode GetSecurityDescriptor
- Méthode GetSecurityDescriptor Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, méthode GetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942588"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a><span data-ttu-id="22be8-106">Méthode RegisteredTask. GetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="22be8-106">RegisteredTask.GetSecurityDescriptor method</span></span>

<span data-ttu-id="22be8-107">Pour les scripts, obtient le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="22be8-107">For scripting, gets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="22be8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22be8-108">Syntax</span></span>


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a><span data-ttu-id="22be8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22be8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22be8-110">*securityInformation*</span><span class="sxs-lookup"><span data-stu-id="22be8-110">*securityInformation*</span></span> 
</dt> <dd>

<span data-ttu-id="22be8-111">Informations de sécurité à partir des [**\_ informations de sécurité**](/windows/desktop/SecAuthZ/security-information).</span><span class="sxs-lookup"><span data-stu-id="22be8-111">The security information from [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22be8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22be8-112">Return value</span></span>

<span data-ttu-id="22be8-113">Descripteur de sécurité pour la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="22be8-113">The security descriptor for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="22be8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22be8-114">Requirements</span></span>



| <span data-ttu-id="22be8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22be8-115">Requirement</span></span> | <span data-ttu-id="22be8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="22be8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22be8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22be8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="22be8-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22be8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="22be8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22be8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="22be8-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22be8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22be8-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="22be8-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="22be8-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="22be8-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="22be8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="22be8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22be8-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22be8-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22be8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22be8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22be8-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="22be8-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="22be8-127">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="22be8-127">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="22be8-128">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="22be8-128">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

