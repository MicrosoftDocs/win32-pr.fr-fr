---
title: Élément GroupId (principalType)
description: Spécifie l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Élément GroupId Planificateur de tâches
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033123"
---
# <a name="groupid-principaltype-element"></a><span data-ttu-id="af508-104">Élément GroupId (principalType)</span><span class="sxs-lookup"><span data-stu-id="af508-104">GroupId (principalType) Element</span></span>

<span data-ttu-id="af508-105">Spécifie l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="af508-105">Specifies the identifier of the user group required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="af508-106">L’élément **GroupID** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="af508-106">The **GroupId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="af508-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="af508-107">Parent element</span></span>



| <span data-ttu-id="af508-108">Élément</span><span class="sxs-lookup"><span data-stu-id="af508-108">Element</span></span>                                                                  | <span data-ttu-id="af508-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="af508-109">Derived from</span></span>                                                           | <span data-ttu-id="af508-110">Description</span><span class="sxs-lookup"><span data-stu-id="af508-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="af508-111">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="af508-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="af508-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="af508-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="af508-113">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="af508-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="af508-114">Notes</span><span class="sxs-lookup"><span data-stu-id="af508-114">Remarks</span></span>

<span data-ttu-id="af508-115">Vous ne pouvez pas spécifier un identificateur de groupe et un identificateur d’utilisateur en même temps.</span><span class="sxs-lookup"><span data-stu-id="af508-115">You cannot specify a group identifier and a user identifier at the same time.</span></span> <span data-ttu-id="af508-116">Spécifiez les éléments [**userid**](taskschedulerschema-userid-principaltype-element.md) ou **GroupID** , mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="af508-116">Specify either the [**UserId**](taskschedulerschema-userid-principaltype-element.md) or **GroupId** elements, but not both.</span></span>

<span data-ttu-id="af508-117">Pour le développement de script, l’identificateur de groupe du principal est spécifié à l’aide de la propriété [**principal. GroupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="af508-117">For script development, the group identifier of the principal is specified using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="af508-118">Pour le développement C++, l’identificateur de groupe du principal est spécifié à l’aide de la propriété [**IPrincipal :: GroupID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .</span><span class="sxs-lookup"><span data-stu-id="af508-118">For C++ development, the group identifier of the principal is specified using the [**IPrincipal::GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="af508-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="af508-119">Examples</span></span>

<span data-ttu-id="af508-120">Pour obtenir un exemple complet du code XML d’une tâche qui utilise cet élément, consultez [exemple de déclencheur de connexion (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="af508-120">For a complete example of the XML for a task that uses this element, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af508-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af508-121">Requirements</span></span>



| <span data-ttu-id="af508-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af508-122">Requirement</span></span> | <span data-ttu-id="af508-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="af508-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af508-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af508-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af508-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af508-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af508-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af508-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af508-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af508-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af508-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af508-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af508-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="af508-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





