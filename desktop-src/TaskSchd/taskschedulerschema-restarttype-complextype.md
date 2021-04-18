---
title: Type complexe restartType
description: Définit les éléments enfants et les informations de séquence pour l’élément RestartOnFailure.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- Planificateur de tâches de type complexe restartType
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519129"
---
# <a name="restarttype-complex-type"></a><span data-ttu-id="3a818-104">Type complexe restartType</span><span class="sxs-lookup"><span data-stu-id="3a818-104">restartType Complex Type</span></span>

<span data-ttu-id="3a818-105">Définit les éléments enfants et les informations de séquence pour l’élément [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3a818-105">Defines the child elements and sequence information for the [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="restartType">
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
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3a818-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3a818-106">Child elements</span></span>



| <span data-ttu-id="3a818-107">Élément</span><span class="sxs-lookup"><span data-stu-id="3a818-107">Element</span></span>                                                              | <span data-ttu-id="3a818-108">Type</span><span class="sxs-lookup"><span data-stu-id="3a818-108">Type</span></span> | <span data-ttu-id="3a818-109">Description</span><span class="sxs-lookup"><span data-stu-id="3a818-109">Description</span></span>                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [<span data-ttu-id="3a818-110">**Saut**</span><span class="sxs-lookup"><span data-stu-id="3a818-110">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       |      | <span data-ttu-id="3a818-111">Nombre de tentatives de redémarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="3a818-111">Number of attempts to restart the task.</span></span><br/> |
| [<span data-ttu-id="3a818-112">**Défini**</span><span class="sxs-lookup"><span data-stu-id="3a818-112">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) |      | <span data-ttu-id="3a818-113">Durée d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="3a818-113">How long to try to start the task.</span></span><br/>      |



## <a name="requirements"></a><span data-ttu-id="3a818-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a818-114">Requirements</span></span>



| <span data-ttu-id="3a818-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a818-115">Requirement</span></span> | <span data-ttu-id="3a818-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a818-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a818-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a818-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3a818-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a818-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a818-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a818-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3a818-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a818-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a818-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a818-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a818-122">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="3a818-122">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3a818-123">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="3a818-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





