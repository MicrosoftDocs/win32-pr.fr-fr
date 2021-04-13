---
title: Élément Body (showMessageType)
description: Contient le texte à afficher dans le corps de la boîte de message.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
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
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465810"
---
# <a name="body-showmessagetype-element"></a><span data-ttu-id="84a0d-104">Élément Body (showMessageType)</span><span class="sxs-lookup"><span data-stu-id="84a0d-104">Body (showMessageType) Element</span></span>

<span data-ttu-id="84a0d-105">Contient le texte à afficher dans le corps de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="84a0d-105">Contains the text to display in the body of the message box.</span></span>

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

<span data-ttu-id="84a0d-106">L’élément **Body** est défini par le type complexe [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="84a0d-106">The **Body** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="84a0d-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="84a0d-107">Parent element</span></span>



| <span data-ttu-id="84a0d-108">Élément</span><span class="sxs-lookup"><span data-stu-id="84a0d-108">Element</span></span>                                                                                  | <span data-ttu-id="84a0d-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="84a0d-109">Derived from</span></span>                                                               | <span data-ttu-id="84a0d-110">Description</span><span class="sxs-lookup"><span data-stu-id="84a0d-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="84a0d-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="84a0d-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="84a0d-112">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="84a0d-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="84a0d-113">Représente une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="84a0d-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="84a0d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="84a0d-114">Remarks</span></span>

<span data-ttu-id="84a0d-115">Pour le développement C++, consultez la [**propriété MessageBody de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span><span class="sxs-lookup"><span data-stu-id="84a0d-115">For C++ development, see [**MessageBody Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span></span>

<span data-ttu-id="84a0d-116">Pour le développement de scripts, consultez [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md).</span><span class="sxs-lookup"><span data-stu-id="84a0d-116">For script development, see [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84a0d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84a0d-117">Requirements</span></span>



| <span data-ttu-id="84a0d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84a0d-118">Requirement</span></span> | <span data-ttu-id="84a0d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="84a0d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84a0d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84a0d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="84a0d-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84a0d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="84a0d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84a0d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="84a0d-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84a0d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





