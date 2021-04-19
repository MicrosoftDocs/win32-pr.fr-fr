---
title: TaskFolder. GetSecurityDescriptor, propriété
description: Pour les scripts, obtient le descripteur de sécurité pour le dossier.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Planificateur de tâches de la propriété GetSecurityDescriptor
- Planificateur de tâches de la propriété GetSecurityDescriptor, objet TaskFolder
- Planificateur de tâches objet TaskFolder, propriété GetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106531620"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a><span data-ttu-id="7c83d-106">TaskFolder. GetSecurityDescriptor, propriété</span><span class="sxs-lookup"><span data-stu-id="7c83d-106">TaskFolder.GetSecurityDescriptor property</span></span>

<span data-ttu-id="7c83d-107">Pour les scripts, obtient le descripteur de sécurité pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="7c83d-107">For scripting, gets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c83d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c83d-108">Syntax</span></span>


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a><span data-ttu-id="7c83d-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7c83d-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="7c83d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c83d-110">Requirements</span></span>



| <span data-ttu-id="7c83d-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c83d-111">Requirement</span></span> | <span data-ttu-id="7c83d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c83d-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c83d-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c83d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7c83d-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c83d-114">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7c83d-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c83d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7c83d-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c83d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c83d-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7c83d-117">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c83d-118"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c83d-118"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c83d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7c83d-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c83d-120"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c83d-120"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c83d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c83d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c83d-122">**TaskFolder.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7c83d-122">**TaskFolder.SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="7c83d-123">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7c83d-123">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





