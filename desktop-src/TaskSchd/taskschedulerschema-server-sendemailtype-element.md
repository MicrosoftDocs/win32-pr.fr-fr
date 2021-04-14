---
title: Élément Server (sendEmailType)
description: Contient le serveur de messagerie utilisé pour envoyer le message électronique.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Planificateur de tâches de l’élément serveur
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384096"
---
# <a name="server-sendemailtype-element"></a><span data-ttu-id="7cd66-104">Élément Server (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="7cd66-104">Server (sendEmailType) Element</span></span>

<span data-ttu-id="7cd66-105">Contient le serveur de messagerie utilisé pour envoyer le message électronique.</span><span class="sxs-lookup"><span data-stu-id="7cd66-105">Contains the email server used to send the email message.</span></span>

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

<span data-ttu-id="7cd66-106">L’élément **Server** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7cd66-106">The **Server** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7cd66-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7cd66-107">Parent element</span></span>



| <span data-ttu-id="7cd66-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7cd66-108">Element</span></span>                                                                              | <span data-ttu-id="7cd66-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7cd66-109">Derived from</span></span>                                                           | <span data-ttu-id="7cd66-110">Description</span><span class="sxs-lookup"><span data-stu-id="7cd66-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="7cd66-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="7cd66-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="7cd66-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="7cd66-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="7cd66-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="7cd66-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7cd66-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7cd66-114">Remarks</span></span>

<span data-ttu-id="7cd66-115">Pour le développement C++, consultez [**propriété de serveur de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span><span class="sxs-lookup"><span data-stu-id="7cd66-115">For C++ development, see [**Server Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span></span>

<span data-ttu-id="7cd66-116">Pour le développement de scripts, consultez [**EmailAction. Server**](emailaction-server.md).</span><span class="sxs-lookup"><span data-stu-id="7cd66-116">For script development, see [**EmailAction.Server**](emailaction-server.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd66-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cd66-117">Requirements</span></span>



| <span data-ttu-id="7cd66-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cd66-118">Requirement</span></span> | <span data-ttu-id="7cd66-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cd66-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7cd66-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd66-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd66-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cd66-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7cd66-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd66-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd66-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cd66-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





