---
title: Élément ReplyTo (sendEmailType)
description: Contient les adresses de messagerie auxquelles il est répondu dans le message électronique.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- ReplyTo, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106357"
---
# <a name="replyto-sendemailtype-element"></a><span data-ttu-id="f0e48-104">Élément ReplyTo (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="f0e48-104">ReplyTo (sendEmailType) Element</span></span>

<span data-ttu-id="f0e48-105">Contient les adresses de messagerie auxquelles il est répondu dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="f0e48-105">Contains the email addresses that are replied to in the email message.</span></span>

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

<span data-ttu-id="f0e48-106">L’élément **ReplyTo** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e48-106">The **ReplyTo** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f0e48-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f0e48-107">Parent element</span></span>



| <span data-ttu-id="f0e48-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f0e48-108">Element</span></span>                                                                              | <span data-ttu-id="f0e48-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="f0e48-109">Derived from</span></span>                                                           | <span data-ttu-id="f0e48-110">Description</span><span class="sxs-lookup"><span data-stu-id="f0e48-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="f0e48-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="f0e48-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="f0e48-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="f0e48-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="f0e48-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="f0e48-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f0e48-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f0e48-114">Remarks</span></span>

<span data-ttu-id="f0e48-115">Pour le développement C++, consultez la [**propriété ReplyTo de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span><span class="sxs-lookup"><span data-stu-id="f0e48-115">For C++ development, see [**ReplyTo Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span></span>

<span data-ttu-id="f0e48-116">Pour le développement de scripts, consultez [**EmailAction. ReplyTo**](emailaction-replyto.md).</span><span class="sxs-lookup"><span data-stu-id="f0e48-116">For script development, see [**EmailAction.ReplyTo**](emailaction-replyto.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e48-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0e48-117">Requirements</span></span>



| <span data-ttu-id="f0e48-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0e48-118">Requirement</span></span> | <span data-ttu-id="f0e48-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0e48-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0e48-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0e48-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e48-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0e48-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f0e48-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0e48-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e48-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0e48-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





