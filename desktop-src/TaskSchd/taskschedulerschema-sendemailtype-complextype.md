---
title: Type complexe sendEmailType
description: Définit le type d’action utilisé pour spécifier qu’un courrier électronique sera envoyé lors de l’exécution d’une tâche. Ce type définit tous les éléments utilisés pour modéliser le message électronique.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- Planificateur de tâches de type complexe sendEmailType
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513833"
---
# <a name="sendemailtype-complex-type"></a><span data-ttu-id="bde8a-105">Type complexe sendEmailType</span><span class="sxs-lookup"><span data-stu-id="bde8a-105">sendEmailType Complex Type</span></span>

<span data-ttu-id="bde8a-106">Définit le type d’action utilisé pour spécifier qu’un courrier électronique sera envoyé lors de l’exécution d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="bde8a-106">Defines the action type used to specify that an email will be sent when a task executes.</span></span> <span data-ttu-id="bde8a-107">Ce type définit tous les éléments utilisés pour modéliser le message électronique.</span><span class="sxs-lookup"><span data-stu-id="bde8a-107">This type defines all the elements used to model the email message.</span></span>

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="bde8a-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bde8a-108">Child elements</span></span>



| <span data-ttu-id="bde8a-109">Élément</span><span class="sxs-lookup"><span data-stu-id="bde8a-109">Element</span></span>                                                                        | <span data-ttu-id="bde8a-110">Type</span><span class="sxs-lookup"><span data-stu-id="bde8a-110">Type</span></span>                                                                         | <span data-ttu-id="bde8a-111">Description</span><span class="sxs-lookup"><span data-stu-id="bde8a-111">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bde8a-112">**Pièces jointes**</span><span class="sxs-lookup"><span data-stu-id="bde8a-112">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="bde8a-113">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="bde8a-113">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="bde8a-114">Spécifie une liste de pièces jointes dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="bde8a-114">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="bde8a-115">**Cci**</span><span class="sxs-lookup"><span data-stu-id="bde8a-115">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="bde8a-116">**string**</span><span class="sxs-lookup"><span data-stu-id="bde8a-116">**string**</span></span>                                                                   | <span data-ttu-id="bde8a-117">Spécifie les adresses de messagerie utilisées sur la ligne CCI d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="bde8a-117">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="bde8a-118">**body**</span><span class="sxs-lookup"><span data-stu-id="bde8a-118">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="bde8a-119">**string**</span><span class="sxs-lookup"><span data-stu-id="bde8a-119">**string**</span></span>                                                                   | <span data-ttu-id="bde8a-120">Spécifie le texte dans le corps du message électronique.</span><span class="sxs-lookup"><span data-stu-id="bde8a-120">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="bde8a-121">**CC**</span><span class="sxs-lookup"><span data-stu-id="bde8a-121">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="bde8a-122">**string**</span><span class="sxs-lookup"><span data-stu-id="bde8a-122">**string**</span></span>                                                                   | <span data-ttu-id="bde8a-123">Spécifie les adresses de messagerie utilisées sur la ligne CC d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="bde8a-123">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="bde8a-124">**De**</span><span class="sxs-lookup"><span data-stu-id="bde8a-124">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="bde8a-125">**string**</span><span class="sxs-lookup"><span data-stu-id="bde8a-125">**string**</span></span>                                                                   | <span data-ttu-id="bde8a-126">Spécifie l’adresse de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="bde8a-126">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="bde8a-127">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="bde8a-127">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="bde8a-128">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="bde8a-128">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="bde8a-129">Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.</span><span class="sxs-lookup"><span data-stu-id="bde8a-129">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="bde8a-130">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="bde8a-130">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="bde8a-131">**string**</span><span class="sxs-lookup"><span data-stu-id="bde8a-131">**string**</span></span>                                                                   | <span data-ttu-id="bde8a-132">Spécifie les adresses de messagerie auxquelles il est répondu dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="bde8a-132">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="bde8a-133">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="bde8a-133">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="bde8a-134">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="bde8a-134">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="bde8a-135">Spécifie le serveur de messagerie utilisé pour envoyer le message électronique.</span><span class="sxs-lookup"><span data-stu-id="bde8a-135">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="bde8a-136">**Objet**</span><span class="sxs-lookup"><span data-stu-id="bde8a-136">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="bde8a-137">**string**</span><span class="sxs-lookup"><span data-stu-id="bde8a-137">**string**</span></span>                                                                   | <span data-ttu-id="bde8a-138">Spécifie l’objet du message électronique.</span><span class="sxs-lookup"><span data-stu-id="bde8a-138">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="bde8a-139">**Pour**</span><span class="sxs-lookup"><span data-stu-id="bde8a-139">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="bde8a-140">**string**</span><span class="sxs-lookup"><span data-stu-id="bde8a-140">**string**</span></span>                                                                   | <span data-ttu-id="bde8a-141">Spécifie les adresses de messagerie auxquelles le courrier électronique sera envoyé.</span><span class="sxs-lookup"><span data-stu-id="bde8a-141">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="bde8a-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bde8a-142">Requirements</span></span>



| <span data-ttu-id="bde8a-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bde8a-143">Requirement</span></span> | <span data-ttu-id="bde8a-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="bde8a-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bde8a-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bde8a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bde8a-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bde8a-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bde8a-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bde8a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bde8a-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bde8a-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





