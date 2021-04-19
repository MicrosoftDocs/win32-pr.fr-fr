---
title: EmailAction. BCC, propriété
description: Pour les scripts, obtient ou définit l’adresse e-mail ou les adresses que vous souhaitez voir dans le message électronique.
ms.assetid: ab340cd7-d6ce-4dce-8474-fdbbc02bd65b
keywords:
- Planificateur de tâches de propriété BCC
- Planificateur de tâches de propriété BCC, objet EmailAction
- Objet EmailAction Planificateur de tâches, BCC, propriété
topic_type:
- apiref
api_name:
- EmailAction.Bcc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bded5e88c236123832956ce42413352348ea535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510544"
---
# <a name="emailactionbcc-property"></a><span data-ttu-id="dfa6a-106">EmailAction. BCC, propriété</span><span class="sxs-lookup"><span data-stu-id="dfa6a-106">EmailAction.Bcc property</span></span>

<span data-ttu-id="dfa6a-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-107">\[This object is no longer supported.</span></span> <span data-ttu-id="dfa6a-108">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="dfa6a-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="dfa6a-109">Pour les scripts, obtient ou définit l’adresse e-mail ou les adresses que vous souhaitez voir dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-109">For scripting, gets or sets the email address or addresses that you want to Bcc in the email message.</span></span>

<span data-ttu-id="dfa6a-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa6a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfa6a-111">Syntax</span></span>


```VB
EmailAction.Bcc As String
```



## <a name="property-value"></a><span data-ttu-id="dfa6a-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="dfa6a-112">Property value</span></span>

<span data-ttu-id="dfa6a-113">L’adresse ou les adresses de messagerie que vous souhaitez voir CCI dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-113">The email address or addresses that you want to Bcc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa6a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfa6a-114">Requirements</span></span>



| <span data-ttu-id="dfa6a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfa6a-115">Requirement</span></span> | <span data-ttu-id="dfa6a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfa6a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa6a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfa6a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa6a-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfa6a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dfa6a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfa6a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa6a-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfa6a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dfa6a-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="dfa6a-121">End of client support</span></span><br/>    | <span data-ttu-id="dfa6a-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa6a-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="dfa6a-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="dfa6a-123">End of server support</span></span><br/>    | <span data-ttu-id="dfa6a-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dfa6a-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="dfa6a-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="dfa6a-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="dfa6a-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dfa6a-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dfa6a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dfa6a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfa6a-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfa6a-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfa6a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfa6a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa6a-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="dfa6a-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="dfa6a-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="dfa6a-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

