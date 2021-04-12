---
title: Type complexe repetitionType
description: Définit les éléments enfants et les informations de séquence pour l’élément de répétition (triggerBaseType).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- Planificateur de tâches de type complexe repetitionType
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa9ee8c08a79f5db053b772c86929f98a72f011c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384996"
---
# <a name="repetitiontype-complex-type"></a><span data-ttu-id="a2a08-104">Type complexe repetitionType</span><span class="sxs-lookup"><span data-stu-id="a2a08-104">repetitionType Complex Type</span></span>

<span data-ttu-id="a2a08-105">Définit les éléments enfants et les informations de séquence pour l’élément de [**répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a2a08-105">Defines the child elements and sequence information for the [**Repetition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Duration"
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
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a2a08-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a2a08-106">Child elements</span></span>



| <span data-ttu-id="a2a08-107">Élément</span><span class="sxs-lookup"><span data-stu-id="a2a08-107">Element</span></span>                                                                                   | <span data-ttu-id="a2a08-108">Type</span><span class="sxs-lookup"><span data-stu-id="a2a08-108">Type</span></span>    | <span data-ttu-id="a2a08-109">Description</span><span class="sxs-lookup"><span data-stu-id="a2a08-109">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2a08-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="a2a08-110">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   |         | <span data-ttu-id="a2a08-111">Spécifie la durée de répétition du modèle.</span><span class="sxs-lookup"><span data-stu-id="a2a08-111">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="a2a08-112">Si aucune valeur n’est spécifiée, le modèle est répété indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="a2a08-112">If no value is specified, the pattern is repeated indefinitely.</span></span><br/> |
| [<span data-ttu-id="a2a08-113">**Défini**</span><span class="sxs-lookup"><span data-stu-id="a2a08-113">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   |         | <span data-ttu-id="a2a08-114">Spécifie la durée entre chaque redémarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a2a08-114">Specifies the amount of time between each restart of the task.</span></span><br/>                                              |
| [<span data-ttu-id="a2a08-115">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="a2a08-115">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="a2a08-116">boolean</span><span class="sxs-lookup"><span data-stu-id="a2a08-116">boolean</span></span> | <span data-ttu-id="a2a08-117">Spécifie qu’une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.</span><span class="sxs-lookup"><span data-stu-id="a2a08-117">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="a2a08-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2a08-118">Requirements</span></span>



| <span data-ttu-id="a2a08-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2a08-119">Requirement</span></span> | <span data-ttu-id="a2a08-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2a08-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a2a08-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2a08-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a08-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2a08-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a2a08-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2a08-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a08-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2a08-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2a08-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2a08-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a08-126">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a2a08-126">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a2a08-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a2a08-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





