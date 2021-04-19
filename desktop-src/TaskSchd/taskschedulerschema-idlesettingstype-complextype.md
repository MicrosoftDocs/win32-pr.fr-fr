---
title: Type complexe idleSettingsType
description: Définit les éléments enfants et les informations de séquencement pour l’élément IdleSettings (settingsType).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- Planificateur de tâches de type complexe idleSettingsType
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538606"
---
# <a name="idlesettingstype-complex-type"></a><span data-ttu-id="1e3df-104">Type complexe idleSettingsType</span><span class="sxs-lookup"><span data-stu-id="1e3df-104">idleSettingsType Complex Type</span></span>

<span data-ttu-id="1e3df-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1e3df-105">Defines the child elements and sequencing information for the [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="WaitTimeout"
            default="PT1H"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1e3df-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1e3df-106">Child elements</span></span>



| <span data-ttu-id="1e3df-107">Élément</span><span class="sxs-lookup"><span data-stu-id="1e3df-107">Element</span></span>                                                                                  | <span data-ttu-id="1e3df-108">Type</span><span class="sxs-lookup"><span data-stu-id="1e3df-108">Type</span></span>    | <span data-ttu-id="1e3df-109">Description</span><span class="sxs-lookup"><span data-stu-id="1e3df-109">Description</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e3df-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="1e3df-110">**Duration**</span></span>](taskschedulerschema-duration-idlesettingstype-element.md)                |         | <span data-ttu-id="1e3df-111">Spécifie la durée autorisée pour démarrer la tâche en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="1e3df-111">Specifies the amount of time allowed to start the task while in an idle condition.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="1e3df-112">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="1e3df-112">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="1e3df-113">boolean</span><span class="sxs-lookup"><span data-stu-id="1e3df-113">boolean</span></span> | <span data-ttu-id="1e3df-114">La tâche est redémarrée dès qu’une condition d’inactivité démarre.</span><span class="sxs-lookup"><span data-stu-id="1e3df-114">The task is restarted as soon as an idle condition starts.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="1e3df-115">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="1e3df-115">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="1e3df-116">boolean</span><span class="sxs-lookup"><span data-stu-id="1e3df-116">boolean</span></span> | <span data-ttu-id="1e3df-117">Spécifie que la tâche est terminée si la condition d’inactivité se termine avant que la durée d’inactivité soit dépassée.</span><span class="sxs-lookup"><span data-stu-id="1e3df-117">Specifies that the task is terminated if the idle condition ends before the idle duration is exceeded.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="1e3df-118">**WaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="1e3df-118">**WaitTimeout**</span></span>](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | <span data-ttu-id="1e3df-119">Spécifie la durée d’attente du démarrage d’une condition d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="1e3df-119">Specifies the amount of time to wait for an idle condition to start.</span></span> <span data-ttu-id="1e3df-120">Si aucune valeur n’est spécifiée pour cet élément, le service Planificateur de tâches attend indéfiniment qu’une condition d’inactivité se produise.</span><span class="sxs-lookup"><span data-stu-id="1e3df-120">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1e3df-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e3df-121">Requirements</span></span>



| <span data-ttu-id="1e3df-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e3df-122">Requirement</span></span> | <span data-ttu-id="1e3df-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e3df-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1e3df-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e3df-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1e3df-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e3df-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1e3df-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e3df-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1e3df-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e3df-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e3df-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e3df-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e3df-129">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1e3df-129">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="1e3df-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1e3df-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





