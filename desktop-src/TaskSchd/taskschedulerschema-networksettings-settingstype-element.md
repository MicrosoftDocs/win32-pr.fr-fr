---
title: Élément NetworkSettings (settingsType)
description: Contient les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau. Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément RunOnlyIfNetworkAvailable est défini sur true.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Élément NetworkSettings Planificateur de tâches
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465806"
---
# <a name="networksettings-settingstype-element"></a><span data-ttu-id="c653f-105">Élément NetworkSettings (settingsType)</span><span class="sxs-lookup"><span data-stu-id="c653f-105">NetworkSettings (settingsType) Element</span></span>

<span data-ttu-id="c653f-106">Contient les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="c653f-106">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="c653f-107">Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="c653f-107">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span>

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="c653f-108">L’élément **NetworkSettings** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c653f-108">The **NetworkSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c653f-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c653f-109">Parent element</span></span>



| <span data-ttu-id="c653f-110">Élément</span><span class="sxs-lookup"><span data-stu-id="c653f-110">Element</span></span>                                                                      | <span data-ttu-id="c653f-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="c653f-111">Derived from</span></span>                                                         | <span data-ttu-id="c653f-112">Description</span><span class="sxs-lookup"><span data-stu-id="c653f-112">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="c653f-113">**Paramètres (taskType)**</span><span class="sxs-lookup"><span data-stu-id="c653f-113">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c653f-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c653f-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c653f-115">Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="c653f-115">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c653f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c653f-116">Remarks</span></span>

<span data-ttu-id="c653f-117">Pour le développement C++, consultez la [**propriété NetworkSettings de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span><span class="sxs-lookup"><span data-stu-id="c653f-117">For C++ development, see [**NetworkSettings Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span></span>

<span data-ttu-id="c653f-118">Pour le développement de scripts, consultez [**TaskSettings. NetworkSettings**](tasksettings-networksettings.md).</span><span class="sxs-lookup"><span data-stu-id="c653f-118">For script development, see [**TaskSettings.NetworkSettings**](tasksettings-networksettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c653f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c653f-119">Requirements</span></span>



| <span data-ttu-id="c653f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c653f-120">Requirement</span></span> | <span data-ttu-id="c653f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c653f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c653f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c653f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c653f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c653f-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c653f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c653f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c653f-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c653f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





