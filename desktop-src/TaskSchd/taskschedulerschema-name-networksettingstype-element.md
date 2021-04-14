---
title: Élément Name (networkSettingsType)
description: Contient le nom d’un profil réseau. Le nom est utilisé à des fins d’affichage.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Élément Name Planificateur de tâches
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508770"
---
# <a name="name-networksettingstype-element"></a><span data-ttu-id="78c73-105">Élément Name (networkSettingsType)</span><span class="sxs-lookup"><span data-stu-id="78c73-105">Name (networkSettingsType) Element</span></span>

<span data-ttu-id="78c73-106">Contient le nom d’un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="78c73-106">Contains the name of a network profile.</span></span> <span data-ttu-id="78c73-107">Le nom est utilisé à des fins d’affichage.</span><span class="sxs-lookup"><span data-stu-id="78c73-107">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

<span data-ttu-id="78c73-108">L’élément **Name** est défini par le type complexe [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="78c73-108">The **Name** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="78c73-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="78c73-109">Parent element</span></span>



| <span data-ttu-id="78c73-110">Élément</span><span class="sxs-lookup"><span data-stu-id="78c73-110">Element</span></span>                                                                                            | <span data-ttu-id="78c73-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="78c73-111">Derived from</span></span>                                                                       | <span data-ttu-id="78c73-112">Description</span><span class="sxs-lookup"><span data-stu-id="78c73-112">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78c73-113">**NetworkSettings (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="78c73-113">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="78c73-114">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="78c73-114">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="78c73-115">Contient les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="78c73-115">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="78c73-116">Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="78c73-116">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="78c73-117">Notes</span><span class="sxs-lookup"><span data-stu-id="78c73-117">Remarks</span></span>

<span data-ttu-id="78c73-118">Pour le développement C++, consultez la [**propriété Name de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span><span class="sxs-lookup"><span data-stu-id="78c73-118">For C++ development, see [**Name Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span></span>

<span data-ttu-id="78c73-119">Pour le développement de scripts, consultez [**NetworkSettings.Name**](networksettings-name.md).</span><span class="sxs-lookup"><span data-stu-id="78c73-119">For script development, see [**NetworkSettings.Name**](networksettings-name.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78c73-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78c73-120">Requirements</span></span>



| <span data-ttu-id="78c73-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78c73-121">Requirement</span></span> | <span data-ttu-id="78c73-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="78c73-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78c73-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78c73-123">Minimum supported client</span></span><br/> | <span data-ttu-id="78c73-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78c73-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78c73-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78c73-125">Minimum supported server</span></span><br/> | <span data-ttu-id="78c73-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78c73-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





