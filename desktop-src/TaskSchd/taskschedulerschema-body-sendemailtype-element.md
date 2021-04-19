---
title: Élément Body (sendEmailType)
description: Contient le texte du corps du message électronique.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Élément Body Planificateur de tâches
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106542860"
---
# <a name="body-sendemailtype-element"></a><span data-ttu-id="1718b-104">Élément Body (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="1718b-104">Body (sendEmailType) Element</span></span>

<span data-ttu-id="1718b-105">Contient le texte du corps du message électronique.</span><span class="sxs-lookup"><span data-stu-id="1718b-105">Contains the text in the body of the email message.</span></span>

``` syntax
<xs:element name="Body"
    type="string"
 />
```

<span data-ttu-id="1718b-106">L’élément **Body** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1718b-106">The **Body** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1718b-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="1718b-107">Parent element</span></span>



| <span data-ttu-id="1718b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="1718b-108">Element</span></span>                                                                              | <span data-ttu-id="1718b-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="1718b-109">Derived from</span></span>                                                           | <span data-ttu-id="1718b-110">Description</span><span class="sxs-lookup"><span data-stu-id="1718b-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1718b-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="1718b-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="1718b-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="1718b-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="1718b-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="1718b-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1718b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1718b-114">Remarks</span></span>

<span data-ttu-id="1718b-115">Pour le développement C++, consultez la [**propriété Body de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span><span class="sxs-lookup"><span data-stu-id="1718b-115">For C++ development, see [**Body Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span></span>

<span data-ttu-id="1718b-116">Pour le développement de scripts, consultez [**EmailAction. Body**](emailaction-body.md).</span><span class="sxs-lookup"><span data-stu-id="1718b-116">For script development, see [**EmailAction.Body**](emailaction-body.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1718b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1718b-117">Requirements</span></span>



| <span data-ttu-id="1718b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1718b-118">Requirement</span></span> | <span data-ttu-id="1718b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1718b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1718b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1718b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1718b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1718b-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1718b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1718b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1718b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1718b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





