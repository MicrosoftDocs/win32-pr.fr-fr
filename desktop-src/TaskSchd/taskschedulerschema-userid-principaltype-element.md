---
title: Élément UserId (principalType)
description: Spécifie l’identificateur d’utilisateur requis pour exécuter les tâches associées au principal.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- UserId, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385275"
---
# <a name="userid-principaltype-element"></a><span data-ttu-id="57946-104">Élément UserId (principalType)</span><span class="sxs-lookup"><span data-stu-id="57946-104">UserId (principalType) Element</span></span>

<span data-ttu-id="57946-105">Spécifie l’identificateur d’utilisateur requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="57946-105">Specifies the user identifier required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="57946-106">L’élément **userid** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="57946-106">The **UserId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="57946-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="57946-107">Parent element</span></span>



| <span data-ttu-id="57946-108">Élément</span><span class="sxs-lookup"><span data-stu-id="57946-108">Element</span></span>                                                                  | <span data-ttu-id="57946-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="57946-109">Derived from</span></span>                                                           | <span data-ttu-id="57946-110">Description</span><span class="sxs-lookup"><span data-stu-id="57946-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="57946-111">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="57946-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="57946-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="57946-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="57946-113">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="57946-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="57946-114">Notes</span><span class="sxs-lookup"><span data-stu-id="57946-114">Remarks</span></span>

<span data-ttu-id="57946-115">L’élément **userid** et l’élément [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) sont utilisés ensemble pour définir l’utilisateur requis pour exécuter les tâches qui utilisent ce principal.</span><span class="sxs-lookup"><span data-stu-id="57946-115">The **UserId** element and the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="57946-116">Vous ne pouvez pas spécifier d’identificateur d’utilisateur et d’identificateur de groupe en même temps.</span><span class="sxs-lookup"><span data-stu-id="57946-116">You cannot specify a user identifier and a group identifier at the same time.</span></span> <span data-ttu-id="57946-117">Spécifiez l' **ID d’utilisateur** ou l’élément [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) , mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="57946-117">Specify either the **UserId** or the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element, but not both.</span></span>

<span data-ttu-id="57946-118">Pour le développement de script, l’identificateur d’utilisateur est spécifié à l’aide de la propriété [**principal. UserID**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="57946-118">For scripting development, the user identifier is specified using the [**Principal.UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="57946-119">Pour le développement C++, l’identificateur d’utilisateur est spécifié à l’aide de la propriété [**IPrincipal :: userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="57946-119">For C++ development, the user identifier is specified using the [**IPrincipal::UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="57946-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="57946-120">Examples</span></span>

<span data-ttu-id="57946-121">Le code XML suivant définit un principe à l’aide d’un identificateur d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57946-121">The following XML defines a principle using a user identifier.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="57946-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57946-122">Requirements</span></span>



| <span data-ttu-id="57946-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57946-123">Requirement</span></span> | <span data-ttu-id="57946-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="57946-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="57946-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57946-125">Minimum supported client</span></span><br/> | <span data-ttu-id="57946-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57946-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="57946-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57946-127">Minimum supported server</span></span><br/> | <span data-ttu-id="57946-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57946-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57946-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57946-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57946-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="57946-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





