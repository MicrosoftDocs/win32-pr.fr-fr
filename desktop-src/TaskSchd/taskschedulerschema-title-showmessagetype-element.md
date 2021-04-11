---
title: Title (élément showMessageType)
description: Contient le titre de la boîte de message.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Élément title Planificateur de tâches
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103109"
---
# <a name="title-showmessagetype-element"></a><span data-ttu-id="8156f-104">Title (élément showMessageType)</span><span class="sxs-lookup"><span data-stu-id="8156f-104">Title (showMessageType) Element</span></span>

<span data-ttu-id="8156f-105">Contient le titre de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="8156f-105">Contains the title of the message box.</span></span>

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

<span data-ttu-id="8156f-106">L’élément **title** est défini par le type complexe [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8156f-106">The **Title** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8156f-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="8156f-107">Parent element</span></span>



| <span data-ttu-id="8156f-108">Élément</span><span class="sxs-lookup"><span data-stu-id="8156f-108">Element</span></span>                                                                                  | <span data-ttu-id="8156f-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="8156f-109">Derived from</span></span>                                                               | <span data-ttu-id="8156f-110">Description</span><span class="sxs-lookup"><span data-stu-id="8156f-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="8156f-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="8156f-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="8156f-112">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="8156f-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="8156f-113">Représente une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="8156f-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8156f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8156f-114">Remarks</span></span>

<span data-ttu-id="8156f-115">Pour le développement C++, consultez [**propriété Title de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span><span class="sxs-lookup"><span data-stu-id="8156f-115">For C++ development, see [**Title Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span></span>

<span data-ttu-id="8156f-116">Pour le développement de scripts, consultez [**ShowMessageAction. title**](showmessageaction-title.md).</span><span class="sxs-lookup"><span data-stu-id="8156f-116">For script development, see [**ShowMessageAction.Title**](showmessageaction-title.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8156f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8156f-117">Requirements</span></span>



| <span data-ttu-id="8156f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8156f-118">Requirement</span></span> | <span data-ttu-id="8156f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8156f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8156f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8156f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8156f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8156f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8156f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8156f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8156f-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8156f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





