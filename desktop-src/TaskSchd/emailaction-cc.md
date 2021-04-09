---
title: Propriété EmailAction.Cc
description: Pour les scripts, obtient ou définit l’adresse ou les adresses de messagerie que vous souhaitez envoyer dans le message électronique.
ms.assetid: 4ad67064-3e6b-4666-a3ce-66e4dcc3f873
keywords:
- Planificateur de tâches de propriété CC
- Planificateur de tâches de propriété CC, objet EmailAction
- Objet EmailAction Planificateur de tâches, propriété CC
topic_type:
- apiref
api_name:
- EmailAction.Cc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f05d7fbd1883aa38ba972eba1eb14767349357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741900"
---
# <a name="emailactioncc-property"></a><span data-ttu-id="b7ab2-106">Propriété EmailAction.Cc</span><span class="sxs-lookup"><span data-stu-id="b7ab2-106">EmailAction.Cc property</span></span>

<span data-ttu-id="b7ab2-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b7ab2-107">\[This object is no longer supported.</span></span> <span data-ttu-id="b7ab2-108">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="b7ab2-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="b7ab2-109">Pour les scripts, obtient ou définit l’adresse ou les adresses de messagerie que vous souhaitez envoyer dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="b7ab2-109">For scripting, gets or sets the email address or addresses that you want to Cc in the email message.</span></span>

<span data-ttu-id="b7ab2-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b7ab2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ab2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7ab2-111">Syntax</span></span>


```VB
EmailAction.Cc As String
```



## <a name="property-value"></a><span data-ttu-id="b7ab2-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b7ab2-112">Property value</span></span>

<span data-ttu-id="b7ab2-113">L’adresse e-mail ou les adresses que vous souhaitez envoyer dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="b7ab2-113">The email address or addresses that you want to Cc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ab2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7ab2-114">Requirements</span></span>



| <span data-ttu-id="b7ab2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7ab2-115">Requirement</span></span> | <span data-ttu-id="b7ab2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7ab2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ab2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7ab2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7ab2-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7ab2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b7ab2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7ab2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7ab2-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7ab2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7ab2-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b7ab2-121">End of client support</span></span><br/>    | <span data-ttu-id="b7ab2-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7ab2-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b7ab2-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b7ab2-123">End of server support</span></span><br/>    | <span data-ttu-id="b7ab2-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7ab2-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b7ab2-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b7ab2-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7ab2-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b7ab2-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b7ab2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b7ab2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7ab2-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7ab2-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ab2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7ab2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ab2-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="b7ab2-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="b7ab2-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b7ab2-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

