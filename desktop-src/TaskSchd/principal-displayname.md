---
title: Propriété principal. DisplayName
description: Pour les scripts, obtient ou définit le nom du principal..
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- DisplayName, propriété Planificateur de tâches
- DisplayName Property Planificateur de tâches, objet principal
- Objet principal Planificateur de tâches, propriété DisplayName
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741876"
---
# <a name="principaldisplayname-property"></a><span data-ttu-id="8d850-106">Propriété principal. DisplayName</span><span class="sxs-lookup"><span data-stu-id="8d850-106">Principal.DisplayName property</span></span>

<span data-ttu-id="8d850-107">Pour les scripts, obtient ou définit le nom du principal..</span><span class="sxs-lookup"><span data-stu-id="8d850-107">For scripting, gets or sets the name of the principal..</span></span>

## <a name="syntax"></a><span data-ttu-id="8d850-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d850-108">Syntax</span></span>


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a><span data-ttu-id="8d850-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8d850-109">Property value</span></span>

<span data-ttu-id="8d850-110">Nom du principal.</span><span class="sxs-lookup"><span data-stu-id="8d850-110">The name of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d850-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8d850-111">Remarks</span></span>

<span data-ttu-id="8d850-112">Lors de la lecture ou de l’écriture de données XML pour une tâche, le nom complet d’un principal est spécifié dans l’élément [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="8d850-112">When reading or writing XML for a task, the display name for a principal is specified in the [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="8d850-113">Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’un fichier Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="8d850-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="8d850-114">Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="8d850-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="8d850-115">Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier. dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource.</span><span class="sxs-lookup"><span data-stu-id="8d850-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="8d850-116">Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="8d850-116">For example, setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d850-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d850-117">Requirements</span></span>



| <span data-ttu-id="8d850-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d850-118">Requirement</span></span> | <span data-ttu-id="8d850-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d850-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d850-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d850-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d850-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d850-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8d850-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d850-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d850-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d850-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8d850-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8d850-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d850-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d850-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8d850-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8d850-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d850-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d850-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d850-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d850-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d850-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8d850-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="8d850-130">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="8d850-130">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





