---
title: EmailAction. Attachments, propriété
description: Pour les scripts, obtient ou définit un tableau de pièces jointes envoyées avec le message électronique.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Planificateur de tâches de propriétés des pièces jointes
- Propriété Attachments Planificateur de tâches, objet EmailAction
- Objet EmailAction Planificateur de tâches, propriété Attachments
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741901"
---
# <a name="emailactionattachments-property"></a><span data-ttu-id="b4911-106">EmailAction. Attachments, propriété</span><span class="sxs-lookup"><span data-stu-id="b4911-106">EmailAction.Attachments property</span></span>

<span data-ttu-id="b4911-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4911-107">\[This object is no longer supported.</span></span> <span data-ttu-id="b4911-108">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="b4911-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="b4911-109">Pour les scripts, obtient ou définit un tableau de pièces jointes envoyées avec le message électronique.</span><span class="sxs-lookup"><span data-stu-id="b4911-109">For scripting, gets or sets an array of attachments that is sent with the email message.</span></span>

<span data-ttu-id="b4911-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b4911-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4911-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4911-111">Syntax</span></span>


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a><span data-ttu-id="b4911-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b4911-112">Property value</span></span>

<span data-ttu-id="b4911-113">Tableau de pièces jointes qui est envoyé avec le message électronique.</span><span class="sxs-lookup"><span data-stu-id="b4911-113">An array of attachments that is sent with the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4911-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b4911-114">Remarks</span></span>

<span data-ttu-id="b4911-115">Un maximum de huit pièces jointes peuvent se trouver dans le tableau des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="b4911-115">A maximum of eight attachments can be in the array of attachments.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4911-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4911-116">Requirements</span></span>



| <span data-ttu-id="b4911-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4911-117">Requirement</span></span> | <span data-ttu-id="b4911-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4911-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4911-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4911-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4911-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4911-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b4911-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4911-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4911-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4911-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4911-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b4911-123">End of client support</span></span><br/>    | <span data-ttu-id="b4911-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4911-124">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b4911-125">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b4911-125">End of server support</span></span><br/>    | <span data-ttu-id="b4911-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4911-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b4911-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b4911-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4911-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b4911-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b4911-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b4911-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4911-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4911-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4911-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4911-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4911-132">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="b4911-132">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="b4911-133">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b4911-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

