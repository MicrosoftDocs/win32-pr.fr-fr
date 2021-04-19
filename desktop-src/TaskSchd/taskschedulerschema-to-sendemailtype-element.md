---
title: À (sendEmailType) (élément)
description: Contient les adresses de messagerie auxquelles le courrier électronique sera envoyé.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- À l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510522"
---
# <a name="to-sendemailtype-element"></a><span data-ttu-id="d4805-104">À (sendEmailType) (élément)</span><span class="sxs-lookup"><span data-stu-id="d4805-104">To (sendEmailType) Element</span></span>

<span data-ttu-id="d4805-105">Contient les adresses de messagerie auxquelles le courrier électronique sera envoyé.</span><span class="sxs-lookup"><span data-stu-id="d4805-105">Contains the email addresses to which the email will be sent.</span></span>

``` syntax
<xs:element name="To"
    type="string"
 />
```

<span data-ttu-id="d4805-106">L’élément **to** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d4805-106">The **To** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d4805-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="d4805-107">Parent element</span></span>



| <span data-ttu-id="d4805-108">Élément</span><span class="sxs-lookup"><span data-stu-id="d4805-108">Element</span></span>                                                                              | <span data-ttu-id="d4805-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="d4805-109">Derived from</span></span>                                                           | <span data-ttu-id="d4805-110">Description</span><span class="sxs-lookup"><span data-stu-id="d4805-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="d4805-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="d4805-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="d4805-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="d4805-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="d4805-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="d4805-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d4805-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d4805-114">Remarks</span></span>

<span data-ttu-id="d4805-115">Pour le développement C++, consultez la [**propriété to de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span><span class="sxs-lookup"><span data-stu-id="d4805-115">For C++ development, see [**To Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span></span>

<span data-ttu-id="d4805-116">Pour le développement de scripts, consultez [**EmailAction.to**](emailaction-to.md).</span><span class="sxs-lookup"><span data-stu-id="d4805-116">For script development, see [**EmailAction.To**](emailaction-to.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4805-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4805-117">Requirements</span></span>



| <span data-ttu-id="d4805-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4805-118">Requirement</span></span> | <span data-ttu-id="d4805-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4805-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d4805-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4805-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d4805-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4805-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d4805-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4805-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d4805-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4805-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





