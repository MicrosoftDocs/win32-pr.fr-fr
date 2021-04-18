---
title: Élément version (registrationInfoType)
description: Spécifie le numéro de version de la tâche.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Version, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb1ae5094ad6f69a61e86da1716169a1b7929e3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509300"
---
# <a name="version-registrationinfotype-element"></a><span data-ttu-id="10b84-104">Élément version (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="10b84-104">Version (registrationInfoType) Element</span></span>

<span data-ttu-id="10b84-105">Spécifie le numéro de version de la tâche.</span><span class="sxs-lookup"><span data-stu-id="10b84-105">Specifies the version number of the task.</span></span>

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="10b84-106">L’élément **version** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="10b84-106">The **Version** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="10b84-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="10b84-107">Parent element</span></span>



| <span data-ttu-id="10b84-108">Élément</span><span class="sxs-lookup"><span data-stu-id="10b84-108">Element</span></span>                                                                           | <span data-ttu-id="10b84-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="10b84-109">Derived from</span></span>                                                                         | <span data-ttu-id="10b84-110">Description</span><span class="sxs-lookup"><span data-stu-id="10b84-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10b84-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="10b84-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="10b84-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="10b84-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="10b84-113">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="10b84-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="10b84-114">Notes</span><span class="sxs-lookup"><span data-stu-id="10b84-114">Remarks</span></span>

<span data-ttu-id="10b84-115">Pour le développement de script, la version d’une tâche est spécifiée à l’aide de la propriété [**RegistrationInfo. version**](registrationinfo-version.md) .</span><span class="sxs-lookup"><span data-stu-id="10b84-115">For scripting development, the version of a task is specified using [**RegistrationInfo.Version**](registrationinfo-version.md) property.</span></span>

<span data-ttu-id="10b84-116">Pour le développement C++, la version d’une tâche est spécifiée à l’aide de la propriété [**IRegistrationInfo :: version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) .</span><span class="sxs-lookup"><span data-stu-id="10b84-116">For C++ development, the version of a task is specified using [**IRegistrationInfo::Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) property.</span></span>

## <a name="examples"></a><span data-ttu-id="10b84-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="10b84-117">Examples</span></span>

<span data-ttu-id="10b84-118">Le code XML suivant définit la version d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="10b84-118">The following XML defines the version of a task.</span></span>


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="10b84-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10b84-119">Requirements</span></span>



| <span data-ttu-id="10b84-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10b84-120">Requirement</span></span> | <span data-ttu-id="10b84-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b84-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="10b84-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10b84-122">Minimum supported client</span></span><br/> | <span data-ttu-id="10b84-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10b84-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="10b84-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10b84-124">Minimum supported server</span></span><br/> | <span data-ttu-id="10b84-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10b84-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10b84-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10b84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b84-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="10b84-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="10b84-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="10b84-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





