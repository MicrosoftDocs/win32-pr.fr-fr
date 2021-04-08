---
title: Groupe actionGroup
description: Définit le groupe d’actions qu’une tâche peut effectuer.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- Planificateur de tâches de groupe actionGroup
- actionGroup Planificateur de tâches
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740836"
---
# <a name="actiongroup-group"></a><span data-ttu-id="aef07-105">Groupe actionGroup</span><span class="sxs-lookup"><span data-stu-id="aef07-105">actionGroup Group</span></span>

<span data-ttu-id="aef07-106">Définit le groupe d’actions qu’une tâche peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="aef07-106">Defines the group of actions that a task can perform.</span></span>

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="aef07-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aef07-107">Child elements</span></span>



| <span data-ttu-id="aef07-108">Élément</span><span class="sxs-lookup"><span data-stu-id="aef07-108">Element</span></span>                                                                    | <span data-ttu-id="aef07-109">Type</span><span class="sxs-lookup"><span data-stu-id="aef07-109">Type</span></span>                                                                       | <span data-ttu-id="aef07-110">Description</span><span class="sxs-lookup"><span data-stu-id="aef07-110">Description</span></span>                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="aef07-111">**Comgérer**</span><span class="sxs-lookup"><span data-stu-id="aef07-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="aef07-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="aef07-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="aef07-113">Représente une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="aef07-113">Represents an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="aef07-114">**Exécutable**</span><span class="sxs-lookup"><span data-stu-id="aef07-114">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="aef07-115">**execType**</span><span class="sxs-lookup"><span data-stu-id="aef07-115">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="aef07-116">Représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="aef07-116">Represents an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="aef07-117">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="aef07-117">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="aef07-118">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="aef07-118">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="aef07-119">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="aef07-119">Represents an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="aef07-120">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="aef07-120">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="aef07-121">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="aef07-121">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="aef07-122">Représente une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="aef07-122">Represents an action that shows a message box.</span></span><br/>               |



## <a name="remarks"></a><span data-ttu-id="aef07-123">Notes</span><span class="sxs-lookup"><span data-stu-id="aef07-123">Remarks</span></span>

<span data-ttu-id="aef07-124">Lors de la lecture ou de l’écriture de code XML, les éléments définis par ce groupe sont les éléments enfants de l’élément [**actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aef07-124">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef07-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aef07-125">Requirements</span></span>



| <span data-ttu-id="aef07-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aef07-126">Requirement</span></span> | <span data-ttu-id="aef07-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="aef07-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aef07-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aef07-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aef07-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aef07-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aef07-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aef07-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aef07-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aef07-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aef07-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aef07-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef07-133">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="aef07-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





