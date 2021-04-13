---
title: Objet TaskVariables
description: Objet de script qui définit les variables de tâche qui peuvent être passées en tant que paramètres aux gestionnaires de tâches et aux exécutables externes qui sont lancés par les tâches.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- Objet TaskVariables Planificateur de tâches
- Planificateur de tâches d’objets TaskVariables, Description
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466398"
---
# <a name="taskvariables-object"></a><span data-ttu-id="98ba9-105">Objet TaskVariables</span><span class="sxs-lookup"><span data-stu-id="98ba9-105">TaskVariables object</span></span>

<span data-ttu-id="98ba9-106">Objet de script qui définit les variables de tâche qui peuvent être passées en tant que paramètres aux gestionnaires de tâches et aux exécutables externes qui sont lancés par les tâches.</span><span class="sxs-lookup"><span data-stu-id="98ba9-106">Scripting object that defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.</span></span>

## <a name="members"></a><span data-ttu-id="98ba9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="98ba9-107">Members</span></span>

<span data-ttu-id="98ba9-108">L’objet **TaskVariables** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="98ba9-108">The **TaskVariables** object has these types of members:</span></span>

-   [<span data-ttu-id="98ba9-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="98ba9-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="98ba9-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="98ba9-110">Methods</span></span>

<span data-ttu-id="98ba9-111">L’objet **TaskVariables** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="98ba9-111">The **TaskVariables** object has these methods.</span></span>



| <span data-ttu-id="98ba9-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="98ba9-112">Method</span></span>                                         | <span data-ttu-id="98ba9-113">Description</span><span class="sxs-lookup"><span data-stu-id="98ba9-113">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98ba9-114">**GetContext**</span><span class="sxs-lookup"><span data-stu-id="98ba9-114">**GetContext**</span></span>](taskvariables-getcontext.md) | <span data-ttu-id="98ba9-115">Utilisé pour partager le contexte entre différentes étapes et tâches qui se trouvent dans la même instance de tâche.</span><span class="sxs-lookup"><span data-stu-id="98ba9-115">Used to share the context between different steps and tasks that are in the same job instance.</span></span><br/> |
| [<span data-ttu-id="98ba9-116">**GetInput**</span><span class="sxs-lookup"><span data-stu-id="98ba9-116">**GetInput**</span></span>](taskvariables-getinput.md)     | <span data-ttu-id="98ba9-117">Obtient les variables d’entrée pour une tâche.</span><span class="sxs-lookup"><span data-stu-id="98ba9-117">Gets the input variables for a task.</span></span><br/>                                                           |
| [<span data-ttu-id="98ba9-118">**SetOutput**</span><span class="sxs-lookup"><span data-stu-id="98ba9-118">**SetOutput**</span></span>](taskvariables-setoutput.md)   | <span data-ttu-id="98ba9-119">Définit les variables de sortie pour une tâche.</span><span class="sxs-lookup"><span data-stu-id="98ba9-119">Sets the output variables for a task.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="98ba9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98ba9-120">Requirements</span></span>



| <span data-ttu-id="98ba9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98ba9-121">Requirement</span></span> | <span data-ttu-id="98ba9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="98ba9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98ba9-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98ba9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="98ba9-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98ba9-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="98ba9-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98ba9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="98ba9-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98ba9-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98ba9-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="98ba9-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="98ba9-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="98ba9-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="98ba9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="98ba9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98ba9-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98ba9-130"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





