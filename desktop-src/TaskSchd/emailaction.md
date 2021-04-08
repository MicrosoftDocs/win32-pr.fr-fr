---
title: EmailAction, objet
description: Objet de script qui représente une action qui envoie un message électronique.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Objet EmailAction Planificateur de tâches
- Planificateur de tâches d’objets EmailAction, Description
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844157"
---
# <a name="emailaction-object"></a><span data-ttu-id="76bb7-105">EmailAction, objet</span><span class="sxs-lookup"><span data-stu-id="76bb7-105">EmailAction object</span></span>

<span data-ttu-id="76bb7-106">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="76bb7-106">\[This object is no longer supported.</span></span> <span data-ttu-id="76bb7-107">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]</span><span class="sxs-lookup"><span data-stu-id="76bb7-107">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="76bb7-108">Objet de script qui représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="76bb7-108">Scripting object that represents an action that sends an email message.</span></span>

## <a name="members"></a><span data-ttu-id="76bb7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="76bb7-109">Members</span></span>

<span data-ttu-id="76bb7-110">L’objet **EmailAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="76bb7-110">The **EmailAction** object has these types of members:</span></span>

-   [<span data-ttu-id="76bb7-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76bb7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76bb7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76bb7-112">Properties</span></span>

<span data-ttu-id="76bb7-113">L’objet **EmailAction** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="76bb7-113">The **EmailAction** object has these properties.</span></span>



| <span data-ttu-id="76bb7-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="76bb7-114">Property</span></span>                                                    | <span data-ttu-id="76bb7-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="76bb7-115">Access type</span></span>           | <span data-ttu-id="76bb7-116">Description</span><span class="sxs-lookup"><span data-stu-id="76bb7-116">Description</span></span>                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76bb7-117">**Pièces jointes**</span><span class="sxs-lookup"><span data-stu-id="76bb7-117">**Attachments**</span></span>](emailaction-attachments.md)<br/>   | <span data-ttu-id="76bb7-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-118">Read/write</span></span><br/> | <span data-ttu-id="76bb7-119">Obtient ou définit un tableau des pièces jointes qui sont envoyées avec le message électronique.</span><span class="sxs-lookup"><span data-stu-id="76bb7-119">Gets or sets an array of attachments that is sent with the email message.</span></span><br/>                      |
| [<span data-ttu-id="76bb7-120">**Cci**</span><span class="sxs-lookup"><span data-stu-id="76bb7-120">**Bcc**</span></span>](emailaction-bcc.md)<br/>                   | <span data-ttu-id="76bb7-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-121">Read/write</span></span><br/> | <span data-ttu-id="76bb7-122">Obtient ou définit l’adresse ou les adresses de messagerie que vous souhaitez CCI dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="76bb7-122">Gets or sets the email address or addresses that you want to Bcc in the email message.</span></span><br/>         |
| [<span data-ttu-id="76bb7-123">**body**</span><span class="sxs-lookup"><span data-stu-id="76bb7-123">**Body**</span></span>](emailaction-body.md)<br/>                 | <span data-ttu-id="76bb7-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-124">Read/write</span></span><br/> | <span data-ttu-id="76bb7-125">Obtient ou définit le corps de l’e-mail qui contient le message électronique.</span><span class="sxs-lookup"><span data-stu-id="76bb7-125">Gets or sets the body of the email that contains the email message.</span></span><br/>                            |
| [<span data-ttu-id="76bb7-126">**CC**</span><span class="sxs-lookup"><span data-stu-id="76bb7-126">**Cc**</span></span>](emailaction-cc.md)<br/>                     | <span data-ttu-id="76bb7-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-127">Read/write</span></span><br/> | <span data-ttu-id="76bb7-128">Obtient ou définit l’adresse ou les adresses de messagerie que vous souhaitez envoyer en copie dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="76bb7-128">Gets or sets the email address or addresses that you want to Cc in the email message.</span></span><br/>          |
| [<span data-ttu-id="76bb7-129">**De**</span><span class="sxs-lookup"><span data-stu-id="76bb7-129">**From**</span></span>](emailaction-from.md)<br/>                 | <span data-ttu-id="76bb7-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-130">Read/write</span></span><br/> | <span data-ttu-id="76bb7-131">Obtient ou définit l’adresse de messagerie à partir de laquelle vous souhaitez envoyer le message électronique.</span><span class="sxs-lookup"><span data-stu-id="76bb7-131">Gets or sets the email address that you want to send the email from.</span></span><br/>                           |
| [<span data-ttu-id="76bb7-132">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="76bb7-132">**HeaderFields**</span></span>](emailaction-headerfields.md)<br/> | <span data-ttu-id="76bb7-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-133">Read/write</span></span><br/> | <span data-ttu-id="76bb7-134">Obtient ou définit les informations d’en-tête dans le message électronique que vous souhaitez envoyer.</span><span class="sxs-lookup"><span data-stu-id="76bb7-134">Gets or sets the header information in the email that you want to send.</span></span><br/>                        |
| [<span data-ttu-id="76bb7-135">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="76bb7-135">**Id**</span></span>](action-id.md)<br/>                          | <span data-ttu-id="76bb7-136">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-136">Read/write</span></span><br/> | <span data-ttu-id="76bb7-137">Hérité de l’objet d' [**action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="76bb7-137">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="76bb7-138">Obtient ou définit l’identificateur de l’action.</span><span class="sxs-lookup"><span data-stu-id="76bb7-138">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="76bb7-139">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="76bb7-139">**ReplyTo**</span></span>](emailaction-replyto.md)<br/>           | <span data-ttu-id="76bb7-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-140">Read/write</span></span><br/> | <span data-ttu-id="76bb7-141">Obtient ou définit l’adresse de messagerie à laquelle vous souhaitez répondre.</span><span class="sxs-lookup"><span data-stu-id="76bb7-141">Gets or sets the email address that you want to reply to.</span></span><br/>                                      |
| [<span data-ttu-id="76bb7-142">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="76bb7-142">**Server**</span></span>](emailaction-server.md)<br/>             | <span data-ttu-id="76bb7-143">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-143">Read/write</span></span><br/> | <span data-ttu-id="76bb7-144">Obtient ou définit le nom du serveur que vous utilisez pour envoyer des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="76bb7-144">Gets or sets the name of the server that you use to send email from.</span></span><br/>                           |
| [<span data-ttu-id="76bb7-145">**Objet**</span><span class="sxs-lookup"><span data-stu-id="76bb7-145">**Subject**</span></span>](emailaction-subject.md)<br/>           | <span data-ttu-id="76bb7-146">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-146">Read/write</span></span><br/> | <span data-ttu-id="76bb7-147">Obtient ou définit l’objet du message électronique.</span><span class="sxs-lookup"><span data-stu-id="76bb7-147">Gets or sets the subject of the email message.</span></span><br/>                                                 |
| [<span data-ttu-id="76bb7-148">**Pour**</span><span class="sxs-lookup"><span data-stu-id="76bb7-148">**To**</span></span>](emailaction-to.md)<br/>                     | <span data-ttu-id="76bb7-149">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76bb7-149">Read/write</span></span><br/> | <span data-ttu-id="76bb7-150">Obtient ou définit l’adresse e-mail à laquelle vous souhaitez envoyer le message électronique.</span><span class="sxs-lookup"><span data-stu-id="76bb7-150">Gets or sets the email address or addresses that you want to send the email to.</span></span><br/>                |
| [<span data-ttu-id="76bb7-151">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="76bb7-151">**Type**</span></span>](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | <span data-ttu-id="76bb7-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76bb7-152">Read-only</span></span><br/>  | <span data-ttu-id="76bb7-153">Hérité de l’objet d' [**action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="76bb7-153">Inherited from [**Action**](action.md) object.</span></span> <span data-ttu-id="76bb7-154">Obtient le type d'action.</span><span class="sxs-lookup"><span data-stu-id="76bb7-154">Gets the type of the action.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="76bb7-155">Notes</span><span class="sxs-lookup"><span data-stu-id="76bb7-155">Remarks</span></span>

<span data-ttu-id="76bb7-156">L’action de messagerie doit avoir une valeur valide pour les propriétés [**Server**](emailaction-server.md), [**from**](emailaction-from.md)et [**to**](emailaction-to.md) ou [**CC**](emailaction-cc.md) pour que la tâche s’inscrive et s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="76bb7-156">The email action must have a valid value for the [**Server**](emailaction-server.md), [**From**](emailaction-from.md), and [**To**](emailaction-to.md) or [**Cc**](emailaction-cc.md) properties for the task to register and run correctly.</span></span>

<span data-ttu-id="76bb7-157">Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, une action de messagerie est spécifiée à l’aide de l’élément [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="76bb7-157">When reading or writing your own XML for a task, an email action is specified using the [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="76bb7-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="76bb7-158">Examples</span></span>

<span data-ttu-id="76bb7-159">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur d’événements (script)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76bb7-159">For more information and example code for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="76bb7-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76bb7-160">Requirements</span></span>



| <span data-ttu-id="76bb7-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76bb7-161">Requirement</span></span> | <span data-ttu-id="76bb7-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="76bb7-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76bb7-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76bb7-163">Minimum supported client</span></span><br/> | <span data-ttu-id="76bb7-164">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76bb7-164">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="76bb7-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76bb7-165">Minimum supported server</span></span><br/> | <span data-ttu-id="76bb7-166">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76bb7-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76bb7-167">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="76bb7-167">End of client support</span></span><br/>    | <span data-ttu-id="76bb7-168">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76bb7-168">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="76bb7-169">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="76bb7-169">End of server support</span></span><br/>    | <span data-ttu-id="76bb7-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76bb7-170">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="76bb7-171">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="76bb7-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="76bb7-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76bb7-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76bb7-173">DLL</span><span class="sxs-lookup"><span data-stu-id="76bb7-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76bb7-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76bb7-174"><dt>Taskschd.dll</dt></span></span> </dl> |



 

