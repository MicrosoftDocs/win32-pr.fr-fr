---
title: RegistrationInfo. source, propriété
description: Pour les scripts, obtient ou définit l’origine de la tâche. Par exemple, une tâche peut provenir d’un composant, d’un service, d’une application ou d’un utilisateur.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Planificateur de tâches de la propriété source
- Planificateur de tâches de propriété source, objet RegistrationInfo
- Planificateur de tâches de l’objet RegistrationInfo, propriété source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742444"
---
# <a name="registrationinfosource-property"></a><span data-ttu-id="4104d-107">RegistrationInfo. source, propriété</span><span class="sxs-lookup"><span data-stu-id="4104d-107">RegistrationInfo.Source property</span></span>

<span data-ttu-id="4104d-108">Pour les scripts, obtient ou définit l’origine de la tâche.</span><span class="sxs-lookup"><span data-stu-id="4104d-108">For scripting, gets or sets where the task originated from.</span></span> <span data-ttu-id="4104d-109">Par exemple, une tâche peut provenir d’un composant, d’un service, d’une application ou d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4104d-109">For example, a task may originate from a component, service, application, or user.</span></span>

## <a name="syntax"></a><span data-ttu-id="4104d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4104d-110">Syntax</span></span>


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a><span data-ttu-id="4104d-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4104d-111">Property value</span></span>

<span data-ttu-id="4104d-112">Origine de la tâche.</span><span class="sxs-lookup"><span data-stu-id="4104d-112">Where the task originated from.</span></span> <span data-ttu-id="4104d-113">Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4104d-113">For example, from a component, service, application, or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="4104d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4104d-114">Remarks</span></span>

<span data-ttu-id="4104d-115">Lors de la lecture ou de l’écriture de données XML pour une tâche, les informations sur la source de la tâche sont spécifiées à l’aide de l’élément [**source**](taskschedulerschema-source-registrationinfotype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="4104d-115">When reading or writing XML for a task, the task source information is specified using the [**Source**](taskschedulerschema-source-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="4104d-116">Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’un fichier Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="4104d-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="4104d-117">Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="4104d-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="4104d-118">Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier. dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource.</span><span class="sxs-lookup"><span data-stu-id="4104d-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="4104d-119">Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="4104d-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="4104d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4104d-120">Requirements</span></span>



| <span data-ttu-id="4104d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4104d-121">Requirement</span></span> | <span data-ttu-id="4104d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4104d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4104d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4104d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4104d-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4104d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4104d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4104d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4104d-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4104d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4104d-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4104d-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="4104d-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4104d-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4104d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4104d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4104d-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4104d-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4104d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4104d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4104d-132">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4104d-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





