---
title: StateChange (sessionStateChangeTriggerType) (élément)
description: Contient le type de Terminal Server modification de session qui déclencherait un lancement de tâche.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- StateChange, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106348"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a><span data-ttu-id="e00fb-104">StateChange (sessionStateChangeTriggerType) (élément)</span><span class="sxs-lookup"><span data-stu-id="e00fb-104">StateChange (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="e00fb-105">Contient le type de Terminal Server modification de session qui déclencherait un lancement de tâche.</span><span class="sxs-lookup"><span data-stu-id="e00fb-105">Contains the kind of Terminal Server session change that would trigger a task launch.</span></span>

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

<span data-ttu-id="e00fb-106">L’élément **StateChange** est défini par le type complexe [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e00fb-106">The **StateChange** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e00fb-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e00fb-107">Parent element</span></span>



| <span data-ttu-id="e00fb-108">Élément</span><span class="sxs-lookup"><span data-stu-id="e00fb-108">Element</span></span>                       | <span data-ttu-id="e00fb-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="e00fb-109">Derived from</span></span>                                                                                           | <span data-ttu-id="e00fb-110">Description</span><span class="sxs-lookup"><span data-stu-id="e00fb-110">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e00fb-111">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00fb-111">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="e00fb-112">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e00fb-112">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="e00fb-113">Spécifie un déclencheur qui démarre une tâche quand une session de Terminal Server change d’État.</span><span class="sxs-lookup"><span data-stu-id="e00fb-113">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e00fb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e00fb-114">Remarks</span></span>

<span data-ttu-id="e00fb-115">Pour le développement C++, consultez la [**propriété StateChange de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span><span class="sxs-lookup"><span data-stu-id="e00fb-115">For C++ development, see [**StateChange Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span></span>

<span data-ttu-id="e00fb-116">Pour le développement de scripts, consultez [**SessionStateChangeTrigger. StateChange**](sessionstatechangetrigger-statechange.md).</span><span class="sxs-lookup"><span data-stu-id="e00fb-116">For script development, see [**SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e00fb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e00fb-117">Requirements</span></span>



| <span data-ttu-id="e00fb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e00fb-118">Requirement</span></span> | <span data-ttu-id="e00fb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e00fb-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e00fb-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e00fb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e00fb-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e00fb-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e00fb-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e00fb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e00fb-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e00fb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





