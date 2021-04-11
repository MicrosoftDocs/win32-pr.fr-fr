---
title: Élément ProcessTokenSidType (principalType)
description: Spécifie le type d’identification de sécurité du processus (SID) de la tâche.
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- Élément ProcessTokenSidType Planificateur de tâches
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875da055f2719afca454d225c3bebd13b404b3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104632"
---
# <a name="processtokensidtype-principaltype-element"></a><span data-ttu-id="a595d-104">Élément ProcessTokenSidType (principalType)</span><span class="sxs-lookup"><span data-stu-id="a595d-104">ProcessTokenSidType (principalType) Element</span></span>

<span data-ttu-id="a595d-105">Spécifie le type d’identification de sécurité du processus (SID) de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a595d-105">Specifies the process security identify (SID) type of the task.</span></span>

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="a595d-106">L’élément **ProcessTokenSidType** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a595d-106">The **ProcessTokenSidType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a595d-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="a595d-107">Parent element</span></span>



| <span data-ttu-id="a595d-108">Élément</span><span class="sxs-lookup"><span data-stu-id="a595d-108">Element</span></span>                                                                  | <span data-ttu-id="a595d-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="a595d-109">Derived from</span></span>                                                           | <span data-ttu-id="a595d-110">Description</span><span class="sxs-lookup"><span data-stu-id="a595d-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="a595d-111">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="a595d-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="a595d-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="a595d-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="a595d-113">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="a595d-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a595d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a595d-114">Remarks</span></span>

<span data-ttu-id="a595d-115">Pour le développement C++, le type de SID de processus est spécifié à l’aide de la propriété [**IPrincipal2 ::P rocesstokensidtype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) .</span><span class="sxs-lookup"><span data-stu-id="a595d-115">For C++ development, the process SID type is specified by using the [**IPrincipal2::ProcessTokenSidType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a595d-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="a595d-116">Examples</span></span>

<span data-ttu-id="a595d-117">Le code XML suivant définit le type de SID de processus de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a595d-117">The following XML defines the process SID type of the task.</span></span>


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="a595d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a595d-118">Requirements</span></span>



| <span data-ttu-id="a595d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a595d-119">Requirement</span></span> | <span data-ttu-id="a595d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a595d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a595d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a595d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a595d-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a595d-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a595d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a595d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a595d-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a595d-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a595d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a595d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a595d-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a595d-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





