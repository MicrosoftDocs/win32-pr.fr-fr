---
title: EmailAction. from, propriété
description: Pour les scripts, obtient ou définit l’adresse de messagerie à partir de laquelle vous souhaitez envoyer le message électronique.
ms.assetid: befe6900-6fbe-4ba2-aeda-271b770e971a
keywords:
- À partir de la propriété Planificateur de tâches
- À partir de la propriété Planificateur de tâches, objet EmailAction
- Objet EmailAction Planificateur de tâches, from, propriété
topic_type:
- apiref
api_name:
- EmailAction.From
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d91b132e8d56caba1a21768e4aacfdda855fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104116"
---
# <a name="emailactionfrom-property"></a><span data-ttu-id="2370f-106">EmailAction. from, propriété</span><span class="sxs-lookup"><span data-stu-id="2370f-106">EmailAction.From property</span></span>

<span data-ttu-id="2370f-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2370f-107">\[This object is no longer supported.</span></span> <span data-ttu-id="2370f-108">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="2370f-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="2370f-109">Pour les scripts, obtient ou définit l’adresse de messagerie à partir de laquelle vous souhaitez envoyer le message électronique.</span><span class="sxs-lookup"><span data-stu-id="2370f-109">For scripting, gets or sets the email address that you want to send the email from.</span></span>

<span data-ttu-id="2370f-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2370f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2370f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2370f-111">Syntax</span></span>


```VB
EmailAction.From As String
```



## <a name="property-value"></a><span data-ttu-id="2370f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2370f-112">Property value</span></span>

<span data-ttu-id="2370f-113">Adresse de messagerie à partir de laquelle vous souhaitez envoyer le message électronique.</span><span class="sxs-lookup"><span data-stu-id="2370f-113">The email address that you want to send the email from.</span></span>

## <a name="requirements"></a><span data-ttu-id="2370f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2370f-114">Requirements</span></span>



| <span data-ttu-id="2370f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2370f-115">Requirement</span></span> | <span data-ttu-id="2370f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2370f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2370f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2370f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2370f-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2370f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2370f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2370f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2370f-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2370f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2370f-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2370f-121">End of client support</span></span><br/>    | <span data-ttu-id="2370f-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2370f-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="2370f-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="2370f-123">End of server support</span></span><br/>    | <span data-ttu-id="2370f-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2370f-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="2370f-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2370f-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="2370f-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2370f-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2370f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2370f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2370f-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2370f-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2370f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2370f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2370f-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="2370f-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="2370f-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2370f-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

