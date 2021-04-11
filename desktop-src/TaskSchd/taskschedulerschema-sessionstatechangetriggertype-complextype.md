---
title: Type complexe sessionStateChangeTriggerType
description: Définit les éléments utilisés pour créer un déclencheur de tâche pour la connexion à la console ou la déconnexion, la connexion à distance ou la déconnexion ou les notifications de verrouillage ou de déverrouillage de station de travail
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- Planificateur de tâches de type complexe sessionStateChangeTriggerType
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317497"
---
# <a name="sessionstatechangetriggertype-complex-type"></a><span data-ttu-id="1f79b-104">Type complexe sessionStateChangeTriggerType</span><span class="sxs-lookup"><span data-stu-id="1f79b-104">sessionStateChangeTriggerType Complex Type</span></span>

<span data-ttu-id="1f79b-105">Définit les éléments utilisés pour créer un déclencheur de tâche pour la connexion à la console ou la déconnexion, la connexion à distance ou la déconnexion ou les notifications de verrouillage ou de déverrouillage de station de travail</span><span class="sxs-lookup"><span data-stu-id="1f79b-105">Defines the elements used to create a task trigger for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
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
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1f79b-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1f79b-106">Child elements</span></span>



| <span data-ttu-id="1f79b-107">Élément</span><span class="sxs-lookup"><span data-stu-id="1f79b-107">Element</span></span>                                                                                      | <span data-ttu-id="1f79b-108">Type</span><span class="sxs-lookup"><span data-stu-id="1f79b-108">Type</span></span>                                                                                    | <span data-ttu-id="1f79b-109">Description</span><span class="sxs-lookup"><span data-stu-id="1f79b-109">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f79b-110">**Retard**</span><span class="sxs-lookup"><span data-stu-id="1f79b-110">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="1f79b-111">duration</span><span class="sxs-lookup"><span data-stu-id="1f79b-111">duration</span></span>                                                                                | <span data-ttu-id="1f79b-112">Spécifie une valeur qui indique la durée du délai avant le démarrage d’une tâche lorsqu’une modification d’état de session Terminal Server est détectée.</span><span class="sxs-lookup"><span data-stu-id="1f79b-112">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="1f79b-113">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="1f79b-113">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="1f79b-114">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="1f79b-114">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="1f79b-115">Spécifie le type de Terminal Server modification de session qui déclencherait un lancement de tâche.</span><span class="sxs-lookup"><span data-stu-id="1f79b-115">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="1f79b-116">**IDutilisateur**</span><span class="sxs-lookup"><span data-stu-id="1f79b-116">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="1f79b-117">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="1f79b-117">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="1f79b-118">Spécifie l’utilisateur pour la session de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="1f79b-118">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="1f79b-119">Lorsqu’une modification d’état de session est détectée pour cet utilisateur, une tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="1f79b-119">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="1f79b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f79b-120">Requirements</span></span>



| <span data-ttu-id="1f79b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f79b-121">Requirement</span></span> | <span data-ttu-id="1f79b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f79b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f79b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f79b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1f79b-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f79b-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1f79b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f79b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1f79b-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f79b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





