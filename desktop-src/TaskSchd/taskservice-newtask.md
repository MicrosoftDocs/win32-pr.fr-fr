---
title: TaskService. NewTask, méthode
description: Pour les scripts, retourne un objet de définition de tâche vide à remplir avec les paramètres et les propriétés, puis inscrit à l’aide de la méthode TaskFolder. RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Méthode NewTask Planificateur de tâches
- Méthode NewTask Planificateur de tâches, objet TaskService
- Objet TaskService Planificateur de tâches, méthode NewTask
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512613"
---
# <a name="taskservicenewtask-method"></a><span data-ttu-id="8a658-106">TaskService. NewTask, méthode</span><span class="sxs-lookup"><span data-stu-id="8a658-106">TaskService.NewTask method</span></span>

<span data-ttu-id="8a658-107">Pour les scripts, retourne un objet de définition de tâche vide à remplir avec les paramètres et les propriétés, puis inscrit à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="8a658-107">For scripting, returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a658-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a658-108">Syntax</span></span>


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="8a658-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a658-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a658-110">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a658-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a658-111">Ce paramètre est réservé pour une utilisation ultérieure et doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="8a658-111">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a658-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a658-112">Return value</span></span>

<span data-ttu-id="8a658-113">Définition de la tâche qui spécifie toutes les informations requises pour créer une nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="8a658-113">The task definition that specifies all the information required to create a new task.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a658-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a658-114">Requirements</span></span>



| <span data-ttu-id="8a658-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a658-115">Requirement</span></span> | <span data-ttu-id="8a658-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a658-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a658-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a658-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8a658-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a658-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8a658-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a658-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8a658-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a658-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8a658-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8a658-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a658-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a658-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a658-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8a658-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a658-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a658-124"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





