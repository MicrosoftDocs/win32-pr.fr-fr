---
title: TaskFolder. GetFolder, propriété
description: Pour les scripts, obtient un dossier qui contient des tâches à un emplacement spécifié.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Planificateur de tâches de propriété GetFolder
- Propriété GetFolder Planificateur de tâches, objet TaskFolder
- Objet TaskFolder Planificateur de tâches, GetFolder, propriété
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308173660ffff7d2062febd087c89cb63bcd8d99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103185"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="44465-106">TaskFolder. GetFolder, propriété</span><span class="sxs-lookup"><span data-stu-id="44465-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="44465-107">Pour les scripts, obtient un dossier qui contient des tâches à un emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="44465-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="44465-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44465-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="44465-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="44465-109">Property value</span></span>

<span data-ttu-id="44465-110">Chemin d’accès (emplacement) au dossier.</span><span class="sxs-lookup"><span data-stu-id="44465-110">The path (location) to the folder.</span></span> <span data-ttu-id="44465-111">N’utilisez pas de barre oblique inverse à la suite du nom du dernier dossier dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="44465-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="44465-112">Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \) .</span><span class="sxs-lookup"><span data-stu-id="44465-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="44465-113">Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="44465-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="44465-114">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="44465-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="44465-115">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="44465-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44465-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="44465-116">Error codes</span></span>

<span data-ttu-id="44465-117">Dossier à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="44465-117">The folder at the specified location.</span></span> <span data-ttu-id="44465-118">Le dossier est un objet [**TaskFolder**](taskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="44465-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="44465-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44465-119">Requirements</span></span>



| <span data-ttu-id="44465-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44465-120">Requirement</span></span> | <span data-ttu-id="44465-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="44465-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44465-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44465-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44465-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44465-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="44465-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44465-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44465-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44465-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="44465-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="44465-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="44465-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="44465-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="44465-128">DLL</span><span class="sxs-lookup"><span data-stu-id="44465-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44465-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44465-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





