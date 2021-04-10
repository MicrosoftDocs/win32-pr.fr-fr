---
title: EmailAction. Server, propriété
description: Pour les scripts, obtient ou définit le nom du serveur SMTP que vous utilisez pour envoyer des messages électroniques à partir de.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Planificateur de tâches de propriétés de serveur
- Planificateur de tâches de propriétés de serveur, objet EmailAction
- Planificateur de tâches objet EmailAction, propriété de serveur
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317285"
---
# <a name="emailactionserver-property"></a><span data-ttu-id="98267-106">EmailAction. Server, propriété</span><span class="sxs-lookup"><span data-stu-id="98267-106">EmailAction.Server property</span></span>

<span data-ttu-id="98267-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="98267-107">\[This object is no longer supported.</span></span> <span data-ttu-id="98267-108">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="98267-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="98267-109">Pour les scripts, obtient ou définit le nom du serveur SMTP que vous utilisez pour envoyer des messages électroniques à partir de.</span><span class="sxs-lookup"><span data-stu-id="98267-109">For scripting, gets or sets the name of the SMTP server that you use to send email from.</span></span>

<span data-ttu-id="98267-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="98267-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="98267-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98267-111">Syntax</span></span>


```VB
EmailAction.Server As String
```



## <a name="property-value"></a><span data-ttu-id="98267-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="98267-112">Property value</span></span>

<span data-ttu-id="98267-113">Nom du serveur que vous utilisez pour envoyer des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="98267-113">The name of the server that you use to send email from.</span></span>

## <a name="remarks"></a><span data-ttu-id="98267-114">Notes</span><span class="sxs-lookup"><span data-stu-id="98267-114">Remarks</span></span>

<span data-ttu-id="98267-115">Assurez-vous que le serveur SMTP qui envoie l’e-mail est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="98267-115">Make sure the SMTP server that sends the email is setup correctly.</span></span> <span data-ttu-id="98267-116">Le courrier électronique est envoyé à l’aide de l’authentification NTLM pour les serveurs SMTP Windows, ce qui signifie que les informations d’identification de sécurité utilisées pour l’exécution de la tâche doivent également disposer de privilèges sur le serveur SMTP pour envoyer un message électronique.</span><span class="sxs-lookup"><span data-stu-id="98267-116">E-mail is sent using NTLM authentication for Windows SMTP servers, which means that the security credentials used for running the task must also have privileges on the SMTP server to send email message.</span></span> <span data-ttu-id="98267-117">Si le serveur SMTP est un serveur non-Windows, le courrier électronique est envoyé si le serveur autorise l’accès anonyme.</span><span class="sxs-lookup"><span data-stu-id="98267-117">If the SMTP server is a non-Windows based server, then the email will be sent if the server allows anonymous access.</span></span> <span data-ttu-id="98267-118">Pour plus d’informations sur la configuration du serveur SMTP, consultez [installation du serveur SMTP](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)et pour plus d’informations sur la gestion des paramètres du serveur SMTP, consultez [administration SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="98267-118">For information about setting up the SMTP server, see [SMTP Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true), and for information about managing SMTP server settings, see [SMTP Administration](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="98267-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98267-119">Requirements</span></span>



| <span data-ttu-id="98267-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98267-120">Requirement</span></span> | <span data-ttu-id="98267-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="98267-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98267-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98267-122">Minimum supported client</span></span><br/> | <span data-ttu-id="98267-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98267-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="98267-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98267-124">Minimum supported server</span></span><br/> | <span data-ttu-id="98267-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98267-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98267-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="98267-126">End of client support</span></span><br/>    | <span data-ttu-id="98267-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="98267-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="98267-128">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="98267-128">End of server support</span></span><br/>    | <span data-ttu-id="98267-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="98267-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="98267-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="98267-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="98267-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="98267-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="98267-132">DLL</span><span class="sxs-lookup"><span data-stu-id="98267-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98267-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98267-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98267-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98267-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98267-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="98267-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="98267-136">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="98267-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

