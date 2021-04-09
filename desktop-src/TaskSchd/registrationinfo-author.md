---
title: RegistrationInfo. Author, propriété
description: Pour les scripts, obtient ou définit l’auteur de la tâche.
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- Planificateur de tâches de propriété auteur
- Propriété Author Planificateur de tâches, objet RegistrationInfo
- Objet RegistrationInfo Planificateur de tâches, propriété Author
topic_type:
- apiref
api_name:
- RegistrationInfo.Author
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7e940ff9da2cfccaa306ebf73080da2a28a091
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032310"
---
# <a name="registrationinfoauthor-property"></a><span data-ttu-id="c913e-106">RegistrationInfo. Author, propriété</span><span class="sxs-lookup"><span data-stu-id="c913e-106">RegistrationInfo.Author property</span></span>

<span data-ttu-id="c913e-107">Pour les scripts, obtient ou définit l’auteur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="c913e-107">For scripting, gets or sets the author of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="c913e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c913e-108">Syntax</span></span>


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a><span data-ttu-id="c913e-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c913e-109">Property value</span></span>

<span data-ttu-id="c913e-110">Auteur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="c913e-110">The author of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="c913e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c913e-111">Remarks</span></span>

<span data-ttu-id="c913e-112">Lors de la lecture ou de l’écriture de données XML pour une tâche, l’auteur de la tâche est spécifié à l’aide de l’élément [**Author**](taskschedulerschema-author-registrationinfotype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="c913e-112">When reading or writing XML for a task, the task author is specified using the [**Author**](taskschedulerschema-author-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="c913e-113">Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’un fichier Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="c913e-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="c913e-114">Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="c913e-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="c913e-115">Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier. dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource.</span><span class="sxs-lookup"><span data-stu-id="c913e-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="c913e-116">Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="c913e-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c913e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c913e-117">Requirements</span></span>



| <span data-ttu-id="c913e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c913e-118">Requirement</span></span> | <span data-ttu-id="c913e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c913e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c913e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c913e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c913e-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c913e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c913e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c913e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c913e-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c913e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c913e-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c913e-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="c913e-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c913e-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c913e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c913e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c913e-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c913e-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c913e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c913e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c913e-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c913e-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





