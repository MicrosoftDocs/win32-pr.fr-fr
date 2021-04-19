---
title: Élément WorkingDirectory (execType)
description: Spécifie le répertoire dans lequel le fichier exécutable ou les fichiers utilisés par l’exécutable existent.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Élément WorkingDirectory Planificateur de tâches
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106514867"
---
# <a name="workingdirectory-exectype-element"></a><span data-ttu-id="ab782-104">Élément WorkingDirectory (execType)</span><span class="sxs-lookup"><span data-stu-id="ab782-104">WorkingDirectory (execType) Element</span></span>

<span data-ttu-id="ab782-105">Spécifie le répertoire dans lequel le fichier exécutable ou les fichiers utilisés par l’exécutable existent.</span><span class="sxs-lookup"><span data-stu-id="ab782-105">Specifies the directory where either the executable or those files used by the executable exists.</span></span>

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

<span data-ttu-id="ab782-106">L’élément **WorkingDirectory** est défini par le type complexe [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ab782-106">The **WorkingDirectory** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ab782-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ab782-107">Parent element</span></span>



| <span data-ttu-id="ab782-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ab782-108">Element</span></span>                                                      | <span data-ttu-id="ab782-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="ab782-109">Derived from</span></span>                                                 | <span data-ttu-id="ab782-110">Description</span><span class="sxs-lookup"><span data-stu-id="ab782-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="ab782-111">**Exécutable**</span><span class="sxs-lookup"><span data-stu-id="ab782-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="ab782-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="ab782-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="ab782-113">Spécifie une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ab782-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ab782-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ab782-114">Remarks</span></span>

<span data-ttu-id="ab782-115">Pour le développement de scripts, le répertoire de travail est spécifié par la propriété [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="ab782-115">For script development, the working directory is specified by the [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md) property.</span></span>

<span data-ttu-id="ab782-116">Pour le développement C++, le répertoire de travail est spécifié par la propriété [**IExecAction :: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .</span><span class="sxs-lookup"><span data-stu-id="ab782-116">For C++ development, the working directory is specified by the [**IExecAction::WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ab782-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="ab782-117">Examples</span></span>

<span data-ttu-id="ab782-118">Le code XML suivant définit une action d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ab782-118">The following XML defines a execution action.</span></span>


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a><span data-ttu-id="ab782-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab782-119">Requirements</span></span>



| <span data-ttu-id="ab782-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab782-120">Requirement</span></span> | <span data-ttu-id="ab782-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab782-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab782-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab782-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ab782-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab782-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ab782-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab782-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ab782-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab782-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab782-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab782-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab782-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ab782-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ab782-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ab782-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





