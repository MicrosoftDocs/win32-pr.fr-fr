---
title: EmailAction. Body, propriété
description: Pour les scripts, obtient ou définit le corps de l’e-mail qui contient le message électronique.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Planificateur de tâches de propriété du corps
- Propriété de corps Planificateur de tâches, objet EmailAction
- Objet EmailAction Planificateur de tâches, propriété Body
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84be176fcf63c7a5191588dc0a68ccaf06c69f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540777"
---
# <a name="emailactionbody-property"></a><span data-ttu-id="4adc2-106">EmailAction. Body, propriété</span><span class="sxs-lookup"><span data-stu-id="4adc2-106">EmailAction.Body property</span></span>

<span data-ttu-id="4adc2-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4adc2-107">\[This object is no longer supported.</span></span> <span data-ttu-id="4adc2-108">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="4adc2-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="4adc2-109">Pour les scripts, obtient ou définit le corps de l’e-mail qui contient le message électronique.</span><span class="sxs-lookup"><span data-stu-id="4adc2-109">For scripting, gets or sets the body of the email that contains the email message.</span></span>

<span data-ttu-id="4adc2-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4adc2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4adc2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4adc2-111">Syntax</span></span>


```VB
EmailAction.Body As String
```



## <a name="property-value"></a><span data-ttu-id="4adc2-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4adc2-112">Property value</span></span>

<span data-ttu-id="4adc2-113">Corps de l’e-mail qui contient le message électronique.</span><span class="sxs-lookup"><span data-stu-id="4adc2-113">The body of the email that contains the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="4adc2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4adc2-114">Remarks</span></span>

<span data-ttu-id="4adc2-115">Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’un fichier Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="4adc2-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="4adc2-116">Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="4adc2-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="4adc2-117">Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier. dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource.</span><span class="sxs-lookup"><span data-stu-id="4adc2-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="4adc2-118">Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="4adc2-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="4adc2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4adc2-119">Requirements</span></span>



| <span data-ttu-id="4adc2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4adc2-120">Requirement</span></span> | <span data-ttu-id="4adc2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4adc2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4adc2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4adc2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4adc2-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4adc2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4adc2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4adc2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4adc2-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4adc2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4adc2-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4adc2-126">End of client support</span></span><br/>    | <span data-ttu-id="4adc2-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4adc2-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="4adc2-128">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4adc2-128">End of server support</span></span><br/>    | <span data-ttu-id="4adc2-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4adc2-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="4adc2-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4adc2-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="4adc2-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4adc2-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4adc2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4adc2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4adc2-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4adc2-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4adc2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4adc2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4adc2-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="4adc2-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="4adc2-136">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4adc2-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

