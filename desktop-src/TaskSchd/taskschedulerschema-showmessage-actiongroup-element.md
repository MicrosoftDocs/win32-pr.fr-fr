---
title: Élément ShowMessage (actionGroup)
description: Représente une action qui affiche une boîte de message.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- Élément ShowMessage Planificateur de tâches
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317174"
---
# <a name="showmessage-actiongroup-element"></a><span data-ttu-id="31523-104">Élément ShowMessage (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="31523-104">ShowMessage (actionGroup) Element</span></span>

<span data-ttu-id="31523-105">Représente une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="31523-105">Represents an action that shows a message box.</span></span>

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

<span data-ttu-id="31523-106">L’élément **ShowMessage** est défini par [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="31523-106">The **ShowMessage** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="31523-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="31523-107">Parent element</span></span>



| <span data-ttu-id="31523-108">Élément</span><span class="sxs-lookup"><span data-stu-id="31523-108">Element</span></span>                                                                    | <span data-ttu-id="31523-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="31523-109">Derived from</span></span>                                                       | <span data-ttu-id="31523-110">Description</span><span class="sxs-lookup"><span data-stu-id="31523-110">Description</span></span>                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="31523-111">**Actions (taskType)**</span><span class="sxs-lookup"><span data-stu-id="31523-111">**Actions (taskType)**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="31523-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="31523-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="31523-113">Contient les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="31523-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="31523-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="31523-114">Child elements</span></span>



| <span data-ttu-id="31523-115">Élément</span><span class="sxs-lookup"><span data-stu-id="31523-115">Element</span></span>                                                            | <span data-ttu-id="31523-116">Type</span><span class="sxs-lookup"><span data-stu-id="31523-116">Type</span></span>           | <span data-ttu-id="31523-117">Description</span><span class="sxs-lookup"><span data-stu-id="31523-117">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="31523-118">**Corps**</span><span class="sxs-lookup"><span data-stu-id="31523-118">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="31523-119">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="31523-119">nonEmptyString</span></span> | <span data-ttu-id="31523-120">Spécifie le texte à afficher dans le corps de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="31523-120">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="31523-121">**Intitulé**</span><span class="sxs-lookup"><span data-stu-id="31523-121">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="31523-122">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="31523-122">nonEmptyString</span></span> | <span data-ttu-id="31523-123">Spécifie le titre de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="31523-123">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="remarks"></a><span data-ttu-id="31523-124">Notes</span><span class="sxs-lookup"><span data-stu-id="31523-124">Remarks</span></span>

<span data-ttu-id="31523-125">Pour le développement de script, une action de MessageBox est spécifiée à l’aide de l’objet [**ShowMessageAction**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="31523-125">For scripting development, a message box action is specified using the [**ShowMessageAction**](showmessageaction.md) object.</span></span>

<span data-ttu-id="31523-126">Pour le développement C++, une action de MessageBox est spécifiée à l’aide de l’interface [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .</span><span class="sxs-lookup"><span data-stu-id="31523-126">For C++ development, a message box action is specified using the [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) interface.</span></span>

<span data-ttu-id="31523-127">**Windows 8 et Windows Server 2012 :** Cet élément a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="31523-127">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="31523-128">Vous pouvez utiliser IExecAction avec la fonction Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) pour afficher un message dans la session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31523-128">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.</span></span>

## <a name="examples"></a><span data-ttu-id="31523-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="31523-129">Examples</span></span>

<span data-ttu-id="31523-130">Pour obtenir un exemple complet du code XML d’une tâche qui utilise une action de MessageBox, consultez exemple de MessageBox [(XML)](/previous-versions//aa381917(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="31523-130">For a complete example of the XML for a task that uses a message box action, see [Message Box Example (XML)](/previous-versions//aa381917(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="31523-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31523-131">Requirements</span></span>



| <span data-ttu-id="31523-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31523-132">Requirement</span></span> | <span data-ttu-id="31523-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="31523-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31523-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31523-134">Minimum supported client</span></span><br/> | <span data-ttu-id="31523-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31523-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="31523-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31523-136">Minimum supported server</span></span><br/> | <span data-ttu-id="31523-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31523-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="31523-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="31523-138">End of client support</span></span><br/>    | <span data-ttu-id="31523-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31523-139">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="31523-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="31523-140">End of server support</span></span><br/>    | <span data-ttu-id="31523-141">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31523-141">Windows Server 2008 R2</span></span><br/>                    |



 

