---
title: TaskSettings. NetworkSettings, propriété
description: Pour les scripts, obtient ou définit l’objet paramètres réseau qui contient un identificateur et un nom de profil réseau.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Planificateur de tâches de la propriété NetworkSettings
- Planificateur de tâches de la propriété NetworkSettings, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété NetworkSettings
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740428"
---
# <a name="tasksettingsnetworksettings-property"></a><span data-ttu-id="0efd4-106">TaskSettings. NetworkSettings, propriété</span><span class="sxs-lookup"><span data-stu-id="0efd4-106">TaskSettings.NetworkSettings property</span></span>

<span data-ttu-id="0efd4-107">Pour les scripts, obtient ou définit l’objet paramètres réseau qui contient un identificateur et un nom de profil réseau.</span><span class="sxs-lookup"><span data-stu-id="0efd4-107">For scripting, gets or sets the network settings object that contains a network profile identifier and name.</span></span> <span data-ttu-id="0efd4-108">Si la propriété [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de [**TaskSettings**](tasksettings.md) a la **valeur true** et qu’un propfile réseau est spécifié dans la propriété **NetworkSettings** , la tâche s’exécute uniquement si le profil réseau spécifié est disponible.</span><span class="sxs-lookup"><span data-stu-id="0efd4-108">If the [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) property of [**TaskSettings**](tasksettings.md) is **True** and a network propfile is specified in the **NetworkSettings** property, then the task will run only if the specified network profile is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="0efd4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0efd4-109">Syntax</span></span>


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a><span data-ttu-id="0efd4-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0efd4-110">Property value</span></span>

<span data-ttu-id="0efd4-111">Objet [**NetworkSettings**](networksettings.md) qui contient un identificateur et un nom de profil réseau.</span><span class="sxs-lookup"><span data-stu-id="0efd4-111">A [**NetworkSettings**](networksettings.md) object that contains a network profile identifier and name.</span></span>

## <a name="requirements"></a><span data-ttu-id="0efd4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0efd4-112">Requirements</span></span>



| <span data-ttu-id="0efd4-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0efd4-113">Requirement</span></span> | <span data-ttu-id="0efd4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0efd4-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0efd4-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0efd4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0efd4-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0efd4-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0efd4-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0efd4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0efd4-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0efd4-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0efd4-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0efd4-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="0efd4-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0efd4-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0efd4-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0efd4-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0efd4-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0efd4-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0efd4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0efd4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0efd4-124">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="0efd4-124">**TaskSettings**</span></span>](tasksettings.md)
</dt> <dt>

[<span data-ttu-id="0efd4-125">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="0efd4-125">**NetworkSettings**</span></span>](networksettings.md)
</dt> </dl>

 

 





