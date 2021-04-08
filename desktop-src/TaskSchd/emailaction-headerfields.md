---
title: EmailAction. HeaderFields, propriété
description: Pour les scripts, obtient ou définit les informations d’en-tête dans le message électronique que vous souhaitez envoyer.
ms.assetid: 492c1e7c-805a-4c58-82d3-45c82420c694
keywords:
- Planificateur de tâches de la propriété HeaderFields
- Planificateur de tâches de la propriété HeaderFields, objet EmailAction
- Planificateur de tâches objet EmailAction, propriété HeaderFields
topic_type:
- apiref
api_name:
- EmailAction.HeaderFields
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cfb963879e47e51e1096d2559fe4e72c6b2543
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843730"
---
# <a name="emailactionheaderfields-property"></a><span data-ttu-id="ec880-106">EmailAction. HeaderFields, propriété</span><span class="sxs-lookup"><span data-stu-id="ec880-106">EmailAction.HeaderFields property</span></span>

<span data-ttu-id="ec880-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ec880-107">\[This object is no longer supported.</span></span> <span data-ttu-id="ec880-108">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="ec880-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="ec880-109">Pour les scripts, obtient ou définit les informations d’en-tête dans le message électronique que vous souhaitez envoyer.</span><span class="sxs-lookup"><span data-stu-id="ec880-109">For scripting, gets or sets the header information in the email you want to send.</span></span>

<span data-ttu-id="ec880-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ec880-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec880-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec880-111">Syntax</span></span>


```VB
EmailAction.HeaderFields As TaskNamedValueCollection
```



## <a name="property-value"></a><span data-ttu-id="ec880-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ec880-112">Property value</span></span>

<span data-ttu-id="ec880-113">Informations d’en-tête dans le message électronique que vous souhaitez envoyer.</span><span class="sxs-lookup"><span data-stu-id="ec880-113">The header information in the email you want to send.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec880-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec880-114">Requirements</span></span>



| <span data-ttu-id="ec880-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec880-115">Requirement</span></span> | <span data-ttu-id="ec880-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec880-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec880-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec880-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ec880-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec880-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ec880-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec880-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ec880-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec880-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec880-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ec880-121">End of client support</span></span><br/>    | <span data-ttu-id="ec880-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ec880-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="ec880-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ec880-123">End of server support</span></span><br/>    | <span data-ttu-id="ec880-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec880-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ec880-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ec880-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec880-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec880-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec880-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ec880-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec880-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec880-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec880-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec880-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec880-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="ec880-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="ec880-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ec880-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

