---
title: EmailAction. ReplyTo, propriété
description: Pour les scripts, obtient ou définit l’adresse de messagerie à laquelle vous souhaitez répondre.
ms.assetid: 2b267e6e-c0c9-42ca-bc4a-cc18af5bcb9c
keywords:
- Propriété ReplyTo Planificateur de tâches
- Propriété ReplyTo Planificateur de tâches, objet EmailAction
- Planificateur de tâches de l’objet EmailAction, propriété ReplyTo
topic_type:
- apiref
api_name:
- EmailAction.ReplyTo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7ed1fd84245e4d938d329f0e9773271efec45b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843729"
---
# <a name="emailactionreplyto-property"></a><span data-ttu-id="e7230-106">EmailAction. ReplyTo, propriété</span><span class="sxs-lookup"><span data-stu-id="e7230-106">EmailAction.ReplyTo property</span></span>

<span data-ttu-id="e7230-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e7230-107">\[This object is no longer supported.</span></span> <span data-ttu-id="e7230-108">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="e7230-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="e7230-109">Pour les scripts, obtient ou définit l’adresse de messagerie à laquelle vous souhaitez répondre.</span><span class="sxs-lookup"><span data-stu-id="e7230-109">For scripting, gets or sets the email address that you want to reply to.</span></span>

<span data-ttu-id="e7230-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e7230-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7230-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7230-111">Syntax</span></span>


```VB
EmailAction.ReplyTo As String
```



## <a name="property-value"></a><span data-ttu-id="e7230-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e7230-112">Property value</span></span>

<span data-ttu-id="e7230-113">Adresse de messagerie à laquelle vous souhaitez répondre.</span><span class="sxs-lookup"><span data-stu-id="e7230-113">The email address that you want to reply to.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7230-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7230-114">Requirements</span></span>



| <span data-ttu-id="e7230-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7230-115">Requirement</span></span> | <span data-ttu-id="e7230-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7230-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7230-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7230-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7230-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7230-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e7230-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7230-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7230-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7230-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7230-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e7230-121">End of client support</span></span><br/>    | <span data-ttu-id="e7230-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7230-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="e7230-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e7230-123">End of server support</span></span><br/>    | <span data-ttu-id="e7230-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7230-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e7230-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e7230-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7230-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7230-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7230-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e7230-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7230-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7230-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7230-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7230-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7230-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="e7230-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="e7230-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e7230-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

