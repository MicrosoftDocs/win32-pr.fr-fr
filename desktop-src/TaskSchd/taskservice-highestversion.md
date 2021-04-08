---
title: TaskService. HighestVersion, propriété
description: Pour les scripts, indique la version la plus récente de Planificateur de tâches qu’un ordinateur prend en charge.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Planificateur de tâches de la propriété HighestVersion
- Planificateur de tâches de la propriété HighestVersion, objet TaskService
- Planificateur de tâches objet TaskService, propriété HighestVersion
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743733"
---
# <a name="taskservicehighestversion-property"></a><span data-ttu-id="d367a-106">TaskService. HighestVersion, propriété</span><span class="sxs-lookup"><span data-stu-id="d367a-106">TaskService.HighestVersion property</span></span>

<span data-ttu-id="d367a-107">Pour les scripts, indique la version la plus récente de Planificateur de tâches qu’un ordinateur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="d367a-107">For scripting, indicates the highest version of Task Scheduler that a computer supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="d367a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d367a-108">Syntax</span></span>


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a><span data-ttu-id="d367a-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d367a-109">Property value</span></span>

<span data-ttu-id="d367a-110">La version la plus récente de Planificateur de tâches qu’un ordinateur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="d367a-110">The highest version of Task Scheduler that a computer supports.</span></span> <span data-ttu-id="d367a-111">La version la plus élevée est une valeur qui est fractionnée en MajorVersion/MinorVersion sur la limite de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d367a-111">The highest version is a value that is split into MajorVersion/MinorVersion on the 16-bit boundary.</span></span> <span data-ttu-id="d367a-112">Le service Planificateur de tâches retourne 1 pour la version principale et 2 pour la version mineure.</span><span class="sxs-lookup"><span data-stu-id="d367a-112">The Task Scheduler service returns 1 for the major version and 2 for the minor version.</span></span> <span data-ttu-id="d367a-113">Utilisez la fonction [CLng](/previous-versions//ck4c5842(v=vs.85)) pour récupérer la valeur entière de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d367a-113">Use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the integer value of the property.</span></span>

## <a name="examples"></a><span data-ttu-id="d367a-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="d367a-114">Examples</span></span>

<span data-ttu-id="d367a-115">Le code suivant montre comment utiliser la fonction [CLng](/previous-versions//ck4c5842(v=vs.85)) pour récupérer la valeur de la propriété **HighestVersion** .</span><span class="sxs-lookup"><span data-stu-id="d367a-115">The following code shows how to use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the value of the **HighestVersion** property.</span></span>


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a><span data-ttu-id="d367a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d367a-116">Requirements</span></span>



| <span data-ttu-id="d367a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d367a-117">Requirement</span></span> | <span data-ttu-id="d367a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d367a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d367a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d367a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d367a-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d367a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d367a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d367a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d367a-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d367a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d367a-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d367a-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d367a-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d367a-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d367a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d367a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d367a-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d367a-126"><dt>Taskschd.dll</dt></span></span> </dl> |



 

