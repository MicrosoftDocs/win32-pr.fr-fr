---
title: Privilege (élément requiredPrivilegesType)
description: Spécifie le droit d’une tâche à effectuer diverses opérations liées au système, telles que l’arrêt du système, le chargement des pilotes de périphérique ou la modification de l’heure système.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Privilège, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466422"
---
# <a name="privilege-requiredprivilegestype-element"></a><span data-ttu-id="44c15-104">Privilege (élément requiredPrivilegesType)</span><span class="sxs-lookup"><span data-stu-id="44c15-104">Privilege (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="44c15-105">Spécifie le droit d’une tâche à effectuer diverses opérations liées au système, telles que l’arrêt du système, le chargement des pilotes de périphérique ou la modification de l’heure système.</span><span class="sxs-lookup"><span data-stu-id="44c15-105">Specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

<span data-ttu-id="44c15-106">L’élément **Privilege** est défini par le type complexe [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="44c15-106">The **Privilege** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="44c15-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="44c15-107">Parent element</span></span>



| <span data-ttu-id="44c15-108">Élément</span><span class="sxs-lookup"><span data-stu-id="44c15-108">Element</span></span>                                                                                             | <span data-ttu-id="44c15-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="44c15-109">Derived from</span></span>                                                                             | <span data-ttu-id="44c15-110">Description</span><span class="sxs-lookup"><span data-stu-id="44c15-110">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="44c15-111">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="44c15-111">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="44c15-112">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="44c15-112">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="44c15-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="44c15-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="44c15-114">Notes</span><span class="sxs-lookup"><span data-stu-id="44c15-114">Remarks</span></span>

<span data-ttu-id="44c15-115">Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**IPrincipal2 :: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="44c15-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="44c15-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="44c15-116">Examples</span></span>

<span data-ttu-id="44c15-117">Le code XML suivant définit un élément Settings qui spécifie le droit d’une tâche à effectuer diverses opérations liées au système, telles que l’arrêt du système, le chargement des pilotes de périphérique ou la modification de l’heure système.</span><span class="sxs-lookup"><span data-stu-id="44c15-117">The following XML defines a settings element that specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
        
```



## <a name="requirements"></a><span data-ttu-id="44c15-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44c15-118">Requirements</span></span>



| <span data-ttu-id="44c15-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44c15-119">Requirement</span></span> | <span data-ttu-id="44c15-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="44c15-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="44c15-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44c15-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44c15-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44c15-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="44c15-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44c15-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44c15-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44c15-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44c15-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44c15-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c15-126">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="44c15-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





