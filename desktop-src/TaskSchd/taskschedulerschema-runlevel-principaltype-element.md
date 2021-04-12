---
title: Élément RunLevel (runLevelType)
description: Contient une valeur qui spécifie le niveau de contexte de sécurité pour l’exécution de la tâche.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Élément RunLevel Planificateur de tâches
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317498"
---
# <a name="runlevel-runleveltype-element"></a><span data-ttu-id="5bf1a-104">Élément RunLevel (runLevelType)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-104">RunLevel (runLevelType) Element</span></span>

<span data-ttu-id="5bf1a-105">Contient une valeur qui spécifie le niveau de contexte de sécurité pour l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-105">Contains a value that specifies the security context level for running the task.</span></span> <span data-ttu-id="5bf1a-106">Vous pouvez spécifier l’exécution d’une tâche en utilisant des privilèges minimum ou des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-106">You can specify to run a task using least privileges or elevated privileges.</span></span> <span data-ttu-id="5bf1a-107">La valeur 0 spécifie d’exécuter la tâche avec les privilèges les plus faibles, et la valeur 1 spécifie d’exécuter la tâche avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-107">A value of 0 specifies to run the task with lowest privileges, and a value of 1 specifies to run the task with elevated privileges.</span></span>

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

<span data-ttu-id="5bf1a-108">L’élément **runlevel** est défini par le type simple [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="5bf1a-108">The **RunLevel** element is defined by the [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5bf1a-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="5bf1a-109">Parent element</span></span>



| <span data-ttu-id="5bf1a-110">Élément</span><span class="sxs-lookup"><span data-stu-id="5bf1a-110">Element</span></span>                                                                                  | <span data-ttu-id="5bf1a-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="5bf1a-111">Derived from</span></span>                                                           | <span data-ttu-id="5bf1a-112">Description</span><span class="sxs-lookup"><span data-stu-id="5bf1a-112">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5bf1a-113">**Principal (principalType)**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-113">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="5bf1a-114">**principalType**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-114">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="5bf1a-115">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-115">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="5bf1a-116">Ces informations d’identification définissent le contexte de sécurité sous lequel une tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-116">These credentials define the security context that a task runs under.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="5bf1a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5bf1a-117">Remarks</span></span>

<span data-ttu-id="5bf1a-118">Pour le développement C++, consultez la [**propriété runlevel de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span><span class="sxs-lookup"><span data-stu-id="5bf1a-118">For C++ development, see [**RunLevel Property of IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span></span>

<span data-ttu-id="5bf1a-119">Pour le développement de scripts, consultez [**principal. runlevel**](principal-runlevel.md).</span><span class="sxs-lookup"><span data-stu-id="5bf1a-119">For script development, see [**Principal.RunLevel**](principal-runlevel.md).</span></span>

<span data-ttu-id="5bf1a-120">Si une tâche est inscrite à l’aide du compte **\\ administrateur builtin** ou des comptes [LocalSystem](/windows/desktop/Services/localsystem-account) ou [LocalService](/windows/desktop/Services/localservice-account) , la propriété [**runlevel**](principal-runlevel.md) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-120">If a task is registered using the **Builtin\\Administrator** account or the [LocalSystem](/windows/desktop/Services/localsystem-account) or [LocalService](/windows/desktop/Services/localservice-account) accounts, the [**RunLevel**](principal-runlevel.md) property is ignored.</span></span> <span data-ttu-id="5bf1a-121">La valeur de l’attribut sera également ignorée si le [contrôle de compte d’utilisateur](/windows/desktop/SecAuthZ/user-account-control) (UAC) est désactivé.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-121">The attribute value will also be ignored if [User Account Control](/windows/desktop/SecAuthZ/user-account-control) (UAC) is turned off.</span></span>

<span data-ttu-id="5bf1a-122">Si une tâche est inscrite à l’aide du groupe **administrateurs** pour le contexte de sécurité de la tâche, vous devez également définir la propriété [**runlevel**](principal-runlevel.md) sur « highestAvailable » pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-122">If a task is registered using the **Administrators** group for the security context of the task, then you must also set the [**RunLevel**](principal-runlevel.md) property to "HighestAvailable" to run the task.</span></span> <span data-ttu-id="5bf1a-123">Pour plus d’informations, consultez [contextes de sécurité pour les tâches](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="5bf1a-123">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf1a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bf1a-124">Requirements</span></span>



| <span data-ttu-id="5bf1a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bf1a-125">Requirement</span></span> | <span data-ttu-id="5bf1a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bf1a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5bf1a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bf1a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5bf1a-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bf1a-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5bf1a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bf1a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5bf1a-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bf1a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

