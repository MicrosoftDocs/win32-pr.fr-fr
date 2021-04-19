---
title: Type complexe logonTriggerType
description: Définit les éléments enfants et les informations de séquencement pour l’élément LogonTrigger.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- Planificateur de tâches de type complexe logonTriggerType
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516101"
---
# <a name="logontriggertype-complex-type"></a><span data-ttu-id="cdfd7-104">Type complexe logonTriggerType</span><span class="sxs-lookup"><span data-stu-id="cdfd7-104">logonTriggerType Complex Type</span></span>

<span data-ttu-id="cdfd7-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cdfd7-105">Defines the child elements and sequencing information for the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cdfd7-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cdfd7-106">Child elements</span></span>



| <span data-ttu-id="cdfd7-107">Élément</span><span class="sxs-lookup"><span data-stu-id="cdfd7-107">Element</span></span>                                                               | <span data-ttu-id="cdfd7-108">Type</span><span class="sxs-lookup"><span data-stu-id="cdfd7-108">Type</span></span>                                                                    | <span data-ttu-id="cdfd7-109">Description</span><span class="sxs-lookup"><span data-stu-id="cdfd7-109">Description</span></span>                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdfd7-110">**Retard**</span><span class="sxs-lookup"><span data-stu-id="cdfd7-110">**Delay**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)   | <span data-ttu-id="cdfd7-111">duration</span><span class="sxs-lookup"><span data-stu-id="cdfd7-111">duration</span></span>                                                                | <span data-ttu-id="cdfd7-112">Intervalle de temps entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="cdfd7-112">Amount of time between when the user logs on and when the task is started.</span></span><br/>         |
| [<span data-ttu-id="cdfd7-113">**IDutilisateur**</span><span class="sxs-lookup"><span data-stu-id="cdfd7-113">**UserId**</span></span>](taskschedulerschema-userid-logontriggertype-element.md) | [<span data-ttu-id="cdfd7-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="cdfd7-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="cdfd7-115">Identificateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cdfd7-115">Identifier of the user.</span></span> <span data-ttu-id="cdfd7-116">La tâche est démarrée lorsque cet utilisateur ouvre une session sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cdfd7-116">The task is started when this user logs onto the computer.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cdfd7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cdfd7-117">Remarks</span></span>

<span data-ttu-id="cdfd7-118">Outre les éléments enfants définis ici, l’élément [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) utilise également les éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cdfd7-118">In addition to the child elements defined here, the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdfd7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdfd7-119">Requirements</span></span>



| <span data-ttu-id="cdfd7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdfd7-120">Requirement</span></span> | <span data-ttu-id="cdfd7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdfd7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cdfd7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdfd7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cdfd7-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdfd7-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cdfd7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdfd7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cdfd7-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdfd7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cdfd7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdfd7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdfd7-127">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="cdfd7-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="cdfd7-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="cdfd7-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





