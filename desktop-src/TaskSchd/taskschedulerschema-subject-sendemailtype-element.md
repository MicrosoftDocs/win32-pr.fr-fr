---
title: Élément Subject (sendEmailType)
description: Contient l’objet du message électronique.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Élément subject Planificateur de tâches
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519121"
---
# <a name="subject-sendemailtype-element"></a><span data-ttu-id="58610-104">Élément Subject (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="58610-104">Subject (sendEmailType) Element</span></span>

<span data-ttu-id="58610-105">Contient l’objet du message électronique.</span><span class="sxs-lookup"><span data-stu-id="58610-105">Contains the subject of the email message.</span></span>

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

<span data-ttu-id="58610-106">L’élément **Subject** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="58610-106">The **Subject** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="58610-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="58610-107">Parent element</span></span>



| <span data-ttu-id="58610-108">Élément</span><span class="sxs-lookup"><span data-stu-id="58610-108">Element</span></span>                                                                              | <span data-ttu-id="58610-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="58610-109">Derived from</span></span>                                                           | <span data-ttu-id="58610-110">Description</span><span class="sxs-lookup"><span data-stu-id="58610-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="58610-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="58610-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="58610-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="58610-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="58610-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="58610-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="58610-114">Notes</span><span class="sxs-lookup"><span data-stu-id="58610-114">Remarks</span></span>

<span data-ttu-id="58610-115">Pour le développement C++, consultez la [**propriété Subject de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span><span class="sxs-lookup"><span data-stu-id="58610-115">For C++ development, see [**Subject Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span></span>

<span data-ttu-id="58610-116">Pour le développement de scripts, consultez [**EmailAction. Subject**](emailaction-subject.md).</span><span class="sxs-lookup"><span data-stu-id="58610-116">For script development, see [**EmailAction.Subject**](emailaction-subject.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58610-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58610-117">Requirements</span></span>



| <span data-ttu-id="58610-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58610-118">Requirement</span></span> | <span data-ttu-id="58610-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="58610-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58610-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58610-120">Minimum supported client</span></span><br/> | <span data-ttu-id="58610-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58610-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="58610-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58610-122">Minimum supported server</span></span><br/> | <span data-ttu-id="58610-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58610-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





