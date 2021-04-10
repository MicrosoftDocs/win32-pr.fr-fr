---
title: Élément BCC (sendEmailType)
description: Contient les adresses de messagerie utilisées sur la ligne CCI d’un message électronique.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Élément BCC Planificateur de tâches
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104350"
---
# <a name="bcc-sendemailtype-element"></a><span data-ttu-id="7be82-104">Élément BCC (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="7be82-104">Bcc (sendEmailType) Element</span></span>

<span data-ttu-id="7be82-105">Contient les adresses de messagerie utilisées sur la ligne CCI d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="7be82-105">Contains the email addresses used on the Bcc line of an email message.</span></span>

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

<span data-ttu-id="7be82-106">L’élément **BCC** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7be82-106">The **Bcc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7be82-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7be82-107">Parent element</span></span>



| <span data-ttu-id="7be82-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7be82-108">Element</span></span>                                                                              | <span data-ttu-id="7be82-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7be82-109">Derived from</span></span>                                                           | <span data-ttu-id="7be82-110">Description</span><span class="sxs-lookup"><span data-stu-id="7be82-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="7be82-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="7be82-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="7be82-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="7be82-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="7be82-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="7be82-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7be82-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7be82-114">Remarks</span></span>

<span data-ttu-id="7be82-115">Pour le développement C++, consultez la [**propriété BCC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span><span class="sxs-lookup"><span data-stu-id="7be82-115">For C++ development, see [**Bcc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span></span>

<span data-ttu-id="7be82-116">Pour le développement de scripts, consultez [**EmailAction. CCI**](emailaction-bcc.md).</span><span class="sxs-lookup"><span data-stu-id="7be82-116">For script development, see [**EmailAction.Bcc**](emailaction-bcc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7be82-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7be82-117">Requirements</span></span>



| <span data-ttu-id="7be82-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7be82-118">Requirement</span></span> | <span data-ttu-id="7be82-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7be82-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7be82-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7be82-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7be82-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7be82-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7be82-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7be82-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7be82-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7be82-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





