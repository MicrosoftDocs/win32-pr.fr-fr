---
title: Type complexe execType
description: Définit les éléments enfants et les informations de séquencement de l’élément exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- Planificateur de tâches de type complexe execType
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464598"
---
# <a name="exectype-complex-type"></a><span data-ttu-id="7da73-104">Type complexe execType</span><span class="sxs-lookup"><span data-stu-id="7da73-104">execType Complex Type</span></span>

<span data-ttu-id="7da73-105">Définit les éléments enfants et les informations de séquencement de l’élément [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7da73-105">Defines the child elements and sequencing information of the [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7da73-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7da73-106">Child elements</span></span>



| <span data-ttu-id="7da73-107">Élément</span><span class="sxs-lookup"><span data-stu-id="7da73-107">Element</span></span>                                                                           | <span data-ttu-id="7da73-108">Type</span><span class="sxs-lookup"><span data-stu-id="7da73-108">Type</span></span>                                                        | <span data-ttu-id="7da73-109">Description</span><span class="sxs-lookup"><span data-stu-id="7da73-109">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7da73-110">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="7da73-110">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="7da73-111">**string**</span><span class="sxs-lookup"><span data-stu-id="7da73-111">**string**</span></span>                                                  | <span data-ttu-id="7da73-112">Spécifie les arguments associés à l’opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7da73-112">Specifies the arguments associated with the command-line operation.</span></span> <br/>                              |
| [<span data-ttu-id="7da73-113">**Commande**</span><span class="sxs-lookup"><span data-stu-id="7da73-113">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | [<span data-ttu-id="7da73-114">**pathType**</span><span class="sxs-lookup"><span data-stu-id="7da73-114">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="7da73-115">Spécifie le fichier exécutable ou le document à exécuter.</span><span class="sxs-lookup"><span data-stu-id="7da73-115">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="7da73-116">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="7da73-116">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | [<span data-ttu-id="7da73-117">**pathType**</span><span class="sxs-lookup"><span data-stu-id="7da73-117">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="7da73-118">Spécifie le répertoire dans lequel le fichier exécutable ou les fichiers utilisés par l’exécutable existent.</span><span class="sxs-lookup"><span data-stu-id="7da73-118">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7da73-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7da73-119">Requirements</span></span>



| <span data-ttu-id="7da73-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7da73-120">Requirement</span></span> | <span data-ttu-id="7da73-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7da73-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7da73-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7da73-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7da73-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7da73-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7da73-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7da73-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7da73-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7da73-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7da73-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7da73-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da73-127">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7da73-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="7da73-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7da73-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





