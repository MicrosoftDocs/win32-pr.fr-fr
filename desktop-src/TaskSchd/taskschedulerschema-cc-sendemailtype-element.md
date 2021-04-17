---
title: Élément CC (sendEmailType)
description: Contient les adresses de messagerie utilisées sur la ligne CC d’un message électronique.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Élément CC Planificateur de tâches
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466026"
---
# <a name="cc-sendemailtype-element"></a><span data-ttu-id="589ff-104">Élément CC (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="589ff-104">Cc (sendEmailType) Element</span></span>

<span data-ttu-id="589ff-105">Contient les adresses de messagerie utilisées sur la ligne CC d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="589ff-105">Contains the email addresses used on the Cc line of an email message.</span></span>

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

<span data-ttu-id="589ff-106">L’élément **CC** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="589ff-106">The **Cc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="589ff-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="589ff-107">Parent element</span></span>



| <span data-ttu-id="589ff-108">Élément</span><span class="sxs-lookup"><span data-stu-id="589ff-108">Element</span></span>                                                                              | <span data-ttu-id="589ff-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="589ff-109">Derived from</span></span>                                                           | <span data-ttu-id="589ff-110">Description</span><span class="sxs-lookup"><span data-stu-id="589ff-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="589ff-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="589ff-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="589ff-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="589ff-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="589ff-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="589ff-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="589ff-114">Notes</span><span class="sxs-lookup"><span data-stu-id="589ff-114">Remarks</span></span>

<span data-ttu-id="589ff-115">Pour le développement C++, consultez la [**propriété CC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span><span class="sxs-lookup"><span data-stu-id="589ff-115">For C++ development, see [**Cc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span></span>

<span data-ttu-id="589ff-116">Pour le développement de scripts, consultez [**EmailAction.cc**](emailaction-cc.md).</span><span class="sxs-lookup"><span data-stu-id="589ff-116">For script development, see [**EmailAction.Cc**](emailaction-cc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="589ff-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="589ff-117">Requirements</span></span>



| <span data-ttu-id="589ff-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="589ff-118">Requirement</span></span> | <span data-ttu-id="589ff-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="589ff-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="589ff-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="589ff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="589ff-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="589ff-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="589ff-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="589ff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="589ff-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="589ff-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





