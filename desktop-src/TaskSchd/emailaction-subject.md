---
title: EmailAction. Subject, propriété
description: Pour les scripts, obtient ou définit l’objet du message électronique.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Planificateur de tâches de la propriété Subject
- Propriété Subject Planificateur de tâches, objet EmailAction
- Objet EmailAction Planificateur de tâches, propriété Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6236ded39993c4cb2499e64ba2e31959df91449e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515776"
---
# <a name="emailactionsubject-property"></a><span data-ttu-id="3d8ee-106">EmailAction. Subject, propriété</span><span class="sxs-lookup"><span data-stu-id="3d8ee-106">EmailAction.Subject property</span></span>

<span data-ttu-id="3d8ee-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3d8ee-107">\[This object is no longer supported.</span></span> <span data-ttu-id="3d8ee-108">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="3d8ee-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="3d8ee-109">Pour les scripts, obtient ou définit l’objet du message électronique.</span><span class="sxs-lookup"><span data-stu-id="3d8ee-109">For scripting, gets or sets the subject of the email message.</span></span>

<span data-ttu-id="3d8ee-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d8ee-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8ee-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d8ee-111">Syntax</span></span>


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a><span data-ttu-id="3d8ee-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3d8ee-112">Property value</span></span>

<span data-ttu-id="3d8ee-113">Objet du message électronique.</span><span class="sxs-lookup"><span data-stu-id="3d8ee-113">The subject of the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8ee-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3d8ee-114">Remarks</span></span>

<span data-ttu-id="3d8ee-115">Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’un fichier Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="3d8ee-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="3d8ee-116">Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="3d8ee-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="3d8ee-117">Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier. dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource.</span><span class="sxs-lookup"><span data-stu-id="3d8ee-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="3d8ee-118">Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="3d8ee-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d8ee-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d8ee-119">Requirements</span></span>



| <span data-ttu-id="3d8ee-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d8ee-120">Requirement</span></span> | <span data-ttu-id="3d8ee-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d8ee-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8ee-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d8ee-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3d8ee-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d8ee-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3d8ee-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d8ee-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3d8ee-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d8ee-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d8ee-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3d8ee-126">End of client support</span></span><br/>    | <span data-ttu-id="3d8ee-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d8ee-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="3d8ee-128">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3d8ee-128">End of server support</span></span><br/>    | <span data-ttu-id="3d8ee-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d8ee-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="3d8ee-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3d8ee-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d8ee-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3d8ee-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3d8ee-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3d8ee-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d8ee-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d8ee-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d8ee-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d8ee-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8ee-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="3d8ee-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="3d8ee-136">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="3d8ee-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

