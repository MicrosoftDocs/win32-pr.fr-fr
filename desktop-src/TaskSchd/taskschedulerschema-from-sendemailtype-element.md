---
title: Élément from (sendEmailType)
description: Contient l’adresse e-mail de l’expéditeur de l’e-mail.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- À partir de l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032646"
---
# <a name="from-sendemailtype-element"></a><span data-ttu-id="dc019-104">Élément from (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="dc019-104">From (sendEmailType) Element</span></span>

<span data-ttu-id="dc019-105">Contient l’adresse e-mail de l’expéditeur de l’e-mail.</span><span class="sxs-lookup"><span data-stu-id="dc019-105">Contains the email address of the email sender.</span></span>

``` syntax
<xs:element name="From"
    type="string"
 />
```

<span data-ttu-id="dc019-106">L’élément **from** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="dc019-106">The **From** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dc019-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dc019-107">Parent element</span></span>



| <span data-ttu-id="dc019-108">Élément</span><span class="sxs-lookup"><span data-stu-id="dc019-108">Element</span></span>                                                                              | <span data-ttu-id="dc019-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="dc019-109">Derived from</span></span>                                                           | <span data-ttu-id="dc019-110">Description</span><span class="sxs-lookup"><span data-stu-id="dc019-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="dc019-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="dc019-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="dc019-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="dc019-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="dc019-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="dc019-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dc019-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dc019-114">Remarks</span></span>

<span data-ttu-id="dc019-115">Pour le développement C++, consultez [**from property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span><span class="sxs-lookup"><span data-stu-id="dc019-115">For C++ development, see [**From Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span></span>

<span data-ttu-id="dc019-116">Pour le développement de scripts, consultez [**EmailAction. from**](emailaction-from.md).</span><span class="sxs-lookup"><span data-stu-id="dc019-116">For script development, see [**EmailAction.From**](emailaction-from.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc019-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc019-117">Requirements</span></span>



| <span data-ttu-id="dc019-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc019-118">Requirement</span></span> | <span data-ttu-id="dc019-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc019-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc019-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc019-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dc019-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc019-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dc019-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc019-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dc019-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc019-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





