---
title: Élément UserId (sessionStateChangeTriggerType)
description: Contient l’utilisateur de la session de Terminal Server. Lorsqu’une modification d’état de session est détectée pour cet utilisateur, une tâche est démarrée.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
keywords:
- UserId, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509114"
---
# <a name="userid-sessionstatechangetriggertype-element"></a><span data-ttu-id="bca58-105">Élément UserId (sessionStateChangeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="bca58-105">UserId (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="bca58-106">Contient l’utilisateur de la session de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="bca58-106">Contains the user for the Terminal Server session.</span></span> <span data-ttu-id="bca58-107">Lorsqu’une modification d’état de session est détectée pour cet utilisateur, une tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="bca58-107">When a session state change is detected for this user, a task is started.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="bca58-108">L’élément **userid** est défini par le type complexe [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bca58-108">The **UserId** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bca58-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="bca58-109">Parent element</span></span>



| <span data-ttu-id="bca58-110">Élément</span><span class="sxs-lookup"><span data-stu-id="bca58-110">Element</span></span>                       | <span data-ttu-id="bca58-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="bca58-111">Derived from</span></span>                                                                                           | <span data-ttu-id="bca58-112">Description</span><span class="sxs-lookup"><span data-stu-id="bca58-112">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bca58-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="bca58-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="bca58-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="bca58-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="bca58-115">Spécifie un déclencheur qui démarre une tâche quand une session de Terminal Server change d’État.</span><span class="sxs-lookup"><span data-stu-id="bca58-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bca58-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bca58-116">Remarks</span></span>

<span data-ttu-id="bca58-117">Pour le développement C++, consultez [**userid Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span><span class="sxs-lookup"><span data-stu-id="bca58-117">For C++ development, see [**UserId Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span></span>

<span data-ttu-id="bca58-118">Pour le développement de scripts, consultez [**SessionStateChangeTrigger. UserID**](sessionstatechangetrigger-userid.md).</span><span class="sxs-lookup"><span data-stu-id="bca58-118">For script development, see [**SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bca58-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bca58-119">Requirements</span></span>



| <span data-ttu-id="bca58-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bca58-120">Requirement</span></span> | <span data-ttu-id="bca58-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bca58-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bca58-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bca58-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bca58-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bca58-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bca58-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bca58-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bca58-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bca58-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





