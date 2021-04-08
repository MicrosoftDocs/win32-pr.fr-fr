---
title: TaskFolder. SetSecurityDescriptor, propriété
description: Pour les scripts, définit le descripteur de sécurité du dossier.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Planificateur de tâches de la propriété SetSecurityDescriptor
- Planificateur de tâches de la propriété SetSecurityDescriptor, objet TaskFolder
- Planificateur de tâches objet TaskFolder, propriété SetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941895"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a><span data-ttu-id="dca93-106">TaskFolder. SetSecurityDescriptor, propriété</span><span class="sxs-lookup"><span data-stu-id="dca93-106">TaskFolder.SetSecurityDescriptor property</span></span>

<span data-ttu-id="dca93-107">Pour les scripts, définit le descripteur de sécurité du dossier.</span><span class="sxs-lookup"><span data-stu-id="dca93-107">For scripting, sets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="dca93-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dca93-108">Syntax</span></span>


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a><span data-ttu-id="dca93-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="dca93-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="dca93-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dca93-110">Remarks</span></span>

<span data-ttu-id="dca93-111">Vous pouvez spécifier la liste de contrôle d’accès (ACL) dans le descripteur de sécurité d’un dossier de tâches afin d’autoriser ou de refuser à certains utilisateurs et groupes l’accès à un dossier de tâches.</span><span class="sxs-lookup"><span data-stu-id="dca93-111">You can specify the access control list (ACL) in the security descriptor for a task folder in order to allow or deny certain users and groups access to a task folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="dca93-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dca93-112">Requirements</span></span>



| <span data-ttu-id="dca93-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dca93-113">Requirement</span></span> | <span data-ttu-id="dca93-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="dca93-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dca93-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dca93-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dca93-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dca93-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dca93-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dca93-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dca93-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dca93-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dca93-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="dca93-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="dca93-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dca93-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dca93-121">DLL</span><span class="sxs-lookup"><span data-stu-id="dca93-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dca93-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dca93-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dca93-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dca93-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca93-124">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="dca93-124">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="dca93-125">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="dca93-125">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





