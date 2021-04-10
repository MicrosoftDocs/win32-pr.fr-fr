---
title: Élément ID (networkSettingsType)
description: Contient une valeur GUID qui identifie un profil réseau.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- ID, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106369"
---
# <a name="id-networksettingstype-element"></a><span data-ttu-id="0efc0-104">Élément ID (networkSettingsType)</span><span class="sxs-lookup"><span data-stu-id="0efc0-104">Id (networkSettingsType) Element</span></span>

<span data-ttu-id="0efc0-105">Contient une valeur GUID qui identifie un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="0efc0-105">Contains a GUID value that identifies a network profile.</span></span>

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

<span data-ttu-id="0efc0-106">L’élément **ID** est défini par le type complexe [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0efc0-106">The **Id** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0efc0-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="0efc0-107">Parent element</span></span>



| <span data-ttu-id="0efc0-108">Élément</span><span class="sxs-lookup"><span data-stu-id="0efc0-108">Element</span></span>                                                                                            | <span data-ttu-id="0efc0-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="0efc0-109">Derived from</span></span>                                                                       | <span data-ttu-id="0efc0-110">Description</span><span class="sxs-lookup"><span data-stu-id="0efc0-110">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0efc0-111">**NetworkSettings (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="0efc0-111">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="0efc0-112">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="0efc0-112">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="0efc0-113">Contient les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="0efc0-113">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="0efc0-114">Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="0efc0-114">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0efc0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0efc0-115">Remarks</span></span>

<span data-ttu-id="0efc0-116">Pour le développement C++, consultez [**propriété ID de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span><span class="sxs-lookup"><span data-stu-id="0efc0-116">For C++ development, see [**Id Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span></span>

<span data-ttu-id="0efc0-117">Pour le développement de scripts, consultez [**NetworkSettings.ID**](networksettings-id.md).</span><span class="sxs-lookup"><span data-stu-id="0efc0-117">For script development, see [**NetworkSettings.Id**](networksettings-id.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0efc0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0efc0-118">Requirements</span></span>



| <span data-ttu-id="0efc0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0efc0-119">Requirement</span></span> | <span data-ttu-id="0efc0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0efc0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0efc0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0efc0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0efc0-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0efc0-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0efc0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0efc0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0efc0-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0efc0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





