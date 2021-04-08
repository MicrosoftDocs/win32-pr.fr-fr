---
title: Type complexe maintenanceSettingsType
description: Définit les éléments enfants et les informations de séquencement pour l’élément MaintenanceSettings.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- Planificateur de tâches de type complexe maintenanceSettingsType
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742764"
---
# <a name="maintenancesettingstype-complex-type"></a><span data-ttu-id="ded1f-104">Type complexe maintenanceSettingsType</span><span class="sxs-lookup"><span data-stu-id="ded1f-104">maintenanceSettingsType Complex Type</span></span>

<span data-ttu-id="ded1f-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ded1f-105">Defines the child elements and sequencing information for the [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ded1f-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ded1f-106">Child elements</span></span>



| <span data-ttu-id="ded1f-107">Élément</span><span class="sxs-lookup"><span data-stu-id="ded1f-107">Element</span></span>                                                                        | <span data-ttu-id="ded1f-108">Type</span><span class="sxs-lookup"><span data-stu-id="ded1f-108">Type</span></span>    | <span data-ttu-id="ded1f-109">Description</span><span class="sxs-lookup"><span data-stu-id="ded1f-109">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ded1f-110">**Échéance**</span><span class="sxs-lookup"><span data-stu-id="ded1f-110">**Deadline**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | <span data-ttu-id="ded1f-111">Spécifie la durée après laquelle le planificateur de tâches tente de démarrer la tâche pendant la maintenance automatique d’urgence, si elle n’a pas pu se terminer pendant une maintenance régulière.</span><span class="sxs-lookup"><span data-stu-id="ded1f-111">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span><br/> |
| <span data-ttu-id="ded1f-112">**Exclusif**</span><span class="sxs-lookup"><span data-stu-id="ded1f-112">**Exclusive**</span></span>                                                                  | <span data-ttu-id="ded1f-113">boolean</span><span class="sxs-lookup"><span data-stu-id="ded1f-113">boolean</span></span> | <span data-ttu-id="ded1f-114">Si la valeur est true, la tâche est démarrée en mode exclusif parmi les autres tâches de maintenance.</span><span class="sxs-lookup"><span data-stu-id="ded1f-114">If set to true, the task will be started exclusively among other maintenance tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="ded1f-115">**Heures**</span><span class="sxs-lookup"><span data-stu-id="ded1f-115">**Period**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | <span data-ttu-id="ded1f-116">Spécifie la fréquence à laquelle la tâche doit être démarrée pendant la maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="ded1f-116">Specifies how often the task needs to be started during Automatic maintenance.</span></span><br/>                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="ded1f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ded1f-117">Requirements</span></span>



| <span data-ttu-id="ded1f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ded1f-118">Requirement</span></span> | <span data-ttu-id="ded1f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ded1f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ded1f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ded1f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ded1f-121">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ded1f-121">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="ded1f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ded1f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ded1f-123">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ded1f-123">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ded1f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ded1f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded1f-125">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ded1f-125">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="ded1f-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ded1f-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





