---
title: Type complexe TaskListType
description: Définit une liste de tâches utilisées pour identifier les composants d’une application.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- TaskListType type complexe EventLog
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383807"
---
# <a name="tasklisttype-complex-type"></a><span data-ttu-id="d1c21-104">Type complexe TaskListType</span><span class="sxs-lookup"><span data-stu-id="d1c21-104">TaskListType Complex Type</span></span>

<span data-ttu-id="d1c21-105">Définit une liste de tâches utilisées pour identifier les composants d’une application.</span><span class="sxs-lookup"><span data-stu-id="d1c21-105">Defines a list of tasks that are used to identify the components of an application.</span></span>

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d1c21-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d1c21-106">Child elements</span></span>



| <span data-ttu-id="d1c21-107">Élément</span><span class="sxs-lookup"><span data-stu-id="d1c21-107">Element</span></span>                                                       | <span data-ttu-id="d1c21-108">Type</span><span class="sxs-lookup"><span data-stu-id="d1c21-108">Type</span></span>                                                         | <span data-ttu-id="d1c21-109">Description</span><span class="sxs-lookup"><span data-stu-id="d1c21-109">Description</span></span>                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="d1c21-110">**tâche**</span><span class="sxs-lookup"><span data-stu-id="d1c21-110">**task**</span></span>](eventmanifestschema-task-tasklisttype-element.md) | [<span data-ttu-id="d1c21-111">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="d1c21-111">**TaskType**</span></span>](eventmanifestschema-tasktype-complextype.md) | <span data-ttu-id="d1c21-112">Définit un composant ou un sous-composant d’une application.</span><span class="sxs-lookup"><span data-stu-id="d1c21-112">Defines a component or subcomponent of an application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d1c21-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1c21-113">Requirements</span></span>



| <span data-ttu-id="d1c21-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1c21-114">Requirement</span></span> | <span data-ttu-id="d1c21-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1c21-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d1c21-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1c21-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c21-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1c21-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d1c21-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1c21-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c21-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1c21-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





