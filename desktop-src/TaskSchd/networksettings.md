---
title: Objet NetworkSettings
description: Pour les scripts, fournit les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Objet NetworkSettings Planificateur de tâches
- Planificateur de tâches d’objets NetworkSettings, Description
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465631"
---
# <a name="networksettings-object"></a><span data-ttu-id="b2e69-105">Objet NetworkSettings</span><span class="sxs-lookup"><span data-stu-id="b2e69-105">NetworkSettings object</span></span>

<span data-ttu-id="b2e69-106">Pour les scripts, fournit les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="b2e69-106">For scripting, provides the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

## <a name="members"></a><span data-ttu-id="b2e69-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b2e69-107">Members</span></span>

<span data-ttu-id="b2e69-108">L’objet **NetworkSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b2e69-108">The **NetworkSettings** object has these types of members:</span></span>

-   [<span data-ttu-id="b2e69-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2e69-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2e69-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2e69-110">Properties</span></span>

<span data-ttu-id="b2e69-111">L’objet **NetworkSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b2e69-111">The **NetworkSettings** object has these properties.</span></span>



| <span data-ttu-id="b2e69-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="b2e69-112">Property</span></span>                                        | <span data-ttu-id="b2e69-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b2e69-113">Access type</span></span>           | <span data-ttu-id="b2e69-114">Description</span><span class="sxs-lookup"><span data-stu-id="b2e69-114">Description</span></span>                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2e69-115">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="b2e69-115">**Id**</span></span>](networksettings-id.md)<br/>     | <span data-ttu-id="b2e69-116">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b2e69-116">Read/write</span></span><br/> | <span data-ttu-id="b2e69-117">Obtient ou définit une valeur GUID qui identifie un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="b2e69-117">Gets or sets a GUID value that identifies a network profile.</span></span><br/>                        |
| [<span data-ttu-id="b2e69-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b2e69-118">**Name**</span></span>](networksettings-name.md)<br/> | <span data-ttu-id="b2e69-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b2e69-119">Read/write</span></span><br/> | <span data-ttu-id="b2e69-120">Obtient ou définit le nom d’un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="b2e69-120">Gets or sets the name of a network profile.</span></span> <span data-ttu-id="b2e69-121">Le nom est utilisé à des fins d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2e69-121">The name is used for display purposes.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2e69-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b2e69-122">Remarks</span></span>

<span data-ttu-id="b2e69-123">Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, les paramètres réseau sont spécifiés à l’aide de l’élément [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="b2e69-123">When reading or writing your own XML for a task, network settings are specified using the [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e69-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2e69-124">Requirements</span></span>



| <span data-ttu-id="b2e69-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2e69-125">Requirement</span></span> | <span data-ttu-id="b2e69-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2e69-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e69-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2e69-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e69-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2e69-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b2e69-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2e69-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e69-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2e69-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2e69-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b2e69-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2e69-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2e69-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2e69-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b2e69-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2e69-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2e69-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e69-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2e69-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e69-136">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b2e69-136">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="b2e69-137">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b2e69-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





