---
title: Élément NetworkProfileName (settingsType)
description: Contient le nom d’un profil réseau. Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément RunOnlyIfNetworkAvailable est défini sur true. Le nom est utilisé à des fins d’affichage.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Élément NetworkProfileName Planificateur de tâches
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742157"
---
# <a name="networkprofilename-settingstype-element"></a><span data-ttu-id="cbe22-106">Élément NetworkProfileName (settingsType)</span><span class="sxs-lookup"><span data-stu-id="cbe22-106">NetworkProfileName (settingsType) Element</span></span>

<span data-ttu-id="cbe22-107">Contient le nom d’un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="cbe22-107">Contains the name of a network profile.</span></span> <span data-ttu-id="cbe22-108">Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="cbe22-108">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="cbe22-109">Le nom est utilisé à des fins d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cbe22-109">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="cbe22-110">L’élément **NetworkProfileName** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cbe22-110">The **NetworkProfileName** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cbe22-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="cbe22-111">Parent element</span></span>



| <span data-ttu-id="cbe22-112">Élément</span><span class="sxs-lookup"><span data-stu-id="cbe22-112">Element</span></span>                                                                      | <span data-ttu-id="cbe22-113">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="cbe22-113">Derived from</span></span>                                                         | <span data-ttu-id="cbe22-114">Description</span><span class="sxs-lookup"><span data-stu-id="cbe22-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbe22-115">**Paramètres (taskType)**</span><span class="sxs-lookup"><span data-stu-id="cbe22-115">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="cbe22-116">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="cbe22-116">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="cbe22-117">Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="cbe22-117">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cbe22-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbe22-118">Requirements</span></span>



| <span data-ttu-id="cbe22-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbe22-119">Requirement</span></span> | <span data-ttu-id="cbe22-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbe22-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cbe22-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbe22-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe22-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbe22-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cbe22-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbe22-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe22-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbe22-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





