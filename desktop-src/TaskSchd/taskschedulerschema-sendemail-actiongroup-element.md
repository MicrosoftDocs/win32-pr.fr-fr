---
title: SendEmail (actionGroup), élément
description: Représente une action qui envoie un message électronique.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- Élément SendEmail Planificateur de tâches
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942580"
---
# <a name="sendemail-actiongroup-element"></a><span data-ttu-id="35aea-104">SendEmail (actionGroup), élément</span><span class="sxs-lookup"><span data-stu-id="35aea-104">SendEmail (actionGroup) Element</span></span>

<span data-ttu-id="35aea-105">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="35aea-105">Represents an action that sends an email message.</span></span>

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

<span data-ttu-id="35aea-106">L’élément **SendEmail** est défini par [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="35aea-106">The **SendEmail** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="35aea-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="35aea-107">Parent element</span></span>



| <span data-ttu-id="35aea-108">Élément</span><span class="sxs-lookup"><span data-stu-id="35aea-108">Element</span></span>                                                         | <span data-ttu-id="35aea-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="35aea-109">Derived from</span></span>                                                       | <span data-ttu-id="35aea-110">Description</span><span class="sxs-lookup"><span data-stu-id="35aea-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="35aea-111">**Actions**</span><span class="sxs-lookup"><span data-stu-id="35aea-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="35aea-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="35aea-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="35aea-113">Contient les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="35aea-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="35aea-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="35aea-114">Child elements</span></span>



| <span data-ttu-id="35aea-115">Élément</span><span class="sxs-lookup"><span data-stu-id="35aea-115">Element</span></span>                                                                        | <span data-ttu-id="35aea-116">Type</span><span class="sxs-lookup"><span data-stu-id="35aea-116">Type</span></span>                                                                         | <span data-ttu-id="35aea-117">Description</span><span class="sxs-lookup"><span data-stu-id="35aea-117">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35aea-118">**Pièces jointes**</span><span class="sxs-lookup"><span data-stu-id="35aea-118">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="35aea-119">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="35aea-119">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="35aea-120">Spécifie une liste de pièces jointes dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="35aea-120">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="35aea-121">**Cci**</span><span class="sxs-lookup"><span data-stu-id="35aea-121">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="35aea-122">**string**</span><span class="sxs-lookup"><span data-stu-id="35aea-122">**string**</span></span>                                                                   | <span data-ttu-id="35aea-123">Spécifie les adresses de messagerie utilisées sur la ligne CCI d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="35aea-123">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="35aea-124">**body**</span><span class="sxs-lookup"><span data-stu-id="35aea-124">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="35aea-125">**string**</span><span class="sxs-lookup"><span data-stu-id="35aea-125">**string**</span></span>                                                                   | <span data-ttu-id="35aea-126">Spécifie le texte dans le corps du message électronique.</span><span class="sxs-lookup"><span data-stu-id="35aea-126">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="35aea-127">**CC**</span><span class="sxs-lookup"><span data-stu-id="35aea-127">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="35aea-128">**string**</span><span class="sxs-lookup"><span data-stu-id="35aea-128">**string**</span></span>                                                                   | <span data-ttu-id="35aea-129">Spécifie les adresses de messagerie utilisées sur la ligne CC d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="35aea-129">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="35aea-130">**De**</span><span class="sxs-lookup"><span data-stu-id="35aea-130">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="35aea-131">**string**</span><span class="sxs-lookup"><span data-stu-id="35aea-131">**string**</span></span>                                                                   | <span data-ttu-id="35aea-132">Spécifie l’adresse de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="35aea-132">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="35aea-133">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="35aea-133">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="35aea-134">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="35aea-134">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="35aea-135">Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.</span><span class="sxs-lookup"><span data-stu-id="35aea-135">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="35aea-136">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="35aea-136">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="35aea-137">**string**</span><span class="sxs-lookup"><span data-stu-id="35aea-137">**string**</span></span>                                                                   | <span data-ttu-id="35aea-138">Spécifie les adresses de messagerie auxquelles il est répondu dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="35aea-138">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="35aea-139">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="35aea-139">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="35aea-140">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="35aea-140">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="35aea-141">Spécifie le serveur de messagerie utilisé pour envoyer le message électronique.</span><span class="sxs-lookup"><span data-stu-id="35aea-141">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="35aea-142">**Objet**</span><span class="sxs-lookup"><span data-stu-id="35aea-142">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="35aea-143">**string**</span><span class="sxs-lookup"><span data-stu-id="35aea-143">**string**</span></span>                                                                   | <span data-ttu-id="35aea-144">Spécifie l’objet du message électronique.</span><span class="sxs-lookup"><span data-stu-id="35aea-144">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="35aea-145">**Pour**</span><span class="sxs-lookup"><span data-stu-id="35aea-145">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="35aea-146">**string**</span><span class="sxs-lookup"><span data-stu-id="35aea-146">**string**</span></span>                                                                   | <span data-ttu-id="35aea-147">Spécifie les adresses de messagerie auxquelles le courrier électronique sera envoyé.</span><span class="sxs-lookup"><span data-stu-id="35aea-147">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="35aea-148">Notes</span><span class="sxs-lookup"><span data-stu-id="35aea-148">Remarks</span></span>

<span data-ttu-id="35aea-149">Pour le développement C++, consultez l’interface [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .</span><span class="sxs-lookup"><span data-stu-id="35aea-149">For C++ development, see the [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) interface.</span></span>

<span data-ttu-id="35aea-150">Pour le développement de scripts, consultez l’objet [**EmailAction**](emailaction.md) .</span><span class="sxs-lookup"><span data-stu-id="35aea-150">For script development, see the [**EmailAction**](emailaction.md) object.</span></span>

<span data-ttu-id="35aea-151">**Windows 8 et Windows Server 2012 :** Cet élément a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="35aea-151">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="35aea-152">Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.</span><span class="sxs-lookup"><span data-stu-id="35aea-152">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.</span></span>

## <a name="examples"></a><span data-ttu-id="35aea-153">Exemples</span><span class="sxs-lookup"><span data-stu-id="35aea-153">Examples</span></span>

<span data-ttu-id="35aea-154">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie une action de messagerie, consultez [exemple de déclencheur d’événements (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35aea-154">For a complete example of the XML for a task that specifies an email action, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="35aea-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35aea-155">Requirements</span></span>



| <span data-ttu-id="35aea-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35aea-156">Requirement</span></span> | <span data-ttu-id="35aea-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="35aea-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35aea-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35aea-158">Minimum supported client</span></span><br/> | <span data-ttu-id="35aea-159">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35aea-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35aea-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35aea-160">Minimum supported server</span></span><br/> | <span data-ttu-id="35aea-161">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35aea-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="35aea-162">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="35aea-162">End of client support</span></span><br/>    | <span data-ttu-id="35aea-163">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35aea-163">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="35aea-164">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="35aea-164">End of server support</span></span><br/>    | <span data-ttu-id="35aea-165">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35aea-165">Windows Server 2008 R2</span></span><br/>                    |



 

