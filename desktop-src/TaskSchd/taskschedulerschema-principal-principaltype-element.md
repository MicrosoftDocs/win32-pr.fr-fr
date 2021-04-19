---
title: Élément principal (principalType)
description: Spécifie les informations d’identification de sécurité pour un principal.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Planificateur de tâches d’élément principal
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510306"
---
# <a name="principal-principaltype-element"></a><span data-ttu-id="78edb-104">Élément principal (principalType)</span><span class="sxs-lookup"><span data-stu-id="78edb-104">Principal (principalType) Element</span></span>

<span data-ttu-id="78edb-105">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="78edb-105">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="78edb-106">Ces informations d’identification définissent le contexte de sécurité sous lequel une tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="78edb-106">These credentials define the security context that a task runs under.</span></span>

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

<span data-ttu-id="78edb-107">L’élément **principal** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="78edb-107">The **Principal** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="78edb-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="78edb-108">Parent element</span></span>



| <span data-ttu-id="78edb-109">Élément</span><span class="sxs-lookup"><span data-stu-id="78edb-109">Element</span></span>                                                               | <span data-ttu-id="78edb-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="78edb-110">Derived from</span></span>                                                             | <span data-ttu-id="78edb-111">Description</span><span class="sxs-lookup"><span data-stu-id="78edb-111">Description</span></span>                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="78edb-112">**Principaux**</span><span class="sxs-lookup"><span data-stu-id="78edb-112">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md) | [<span data-ttu-id="78edb-113">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="78edb-113">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md) | <span data-ttu-id="78edb-114">Spécifie les principaux de sécurité associés à la tâche.</span><span class="sxs-lookup"><span data-stu-id="78edb-114">Specifies the security principals associated with the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="78edb-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="78edb-115">Child elements</span></span>



| <span data-ttu-id="78edb-116">Élément</span><span class="sxs-lookup"><span data-stu-id="78edb-116">Element</span></span>                                                                      | <span data-ttu-id="78edb-117">Type</span><span class="sxs-lookup"><span data-stu-id="78edb-117">Type</span></span>                                                          | <span data-ttu-id="78edb-118">Description</span><span class="sxs-lookup"><span data-stu-id="78edb-118">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78edb-119">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="78edb-119">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md) | <span data-ttu-id="78edb-120">**string**</span><span class="sxs-lookup"><span data-stu-id="78edb-120">**string**</span></span>                                                    | <span data-ttu-id="78edb-121">Spécifie le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="78edb-121">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                 |
| [<span data-ttu-id="78edb-122">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="78edb-122">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)         | <span data-ttu-id="78edb-123">**string**</span><span class="sxs-lookup"><span data-stu-id="78edb-123">**string**</span></span>                                                    | <span data-ttu-id="78edb-124">Spécifie l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="78edb-124">Specifies the identifier of the user group required to run tasks associated with the principal.</span></span><br/> |
| [<span data-ttu-id="78edb-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="78edb-125">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)     | [<span data-ttu-id="78edb-126">**logonType**</span><span class="sxs-lookup"><span data-stu-id="78edb-126">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md) | <span data-ttu-id="78edb-127">Spécifie la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="78edb-127">Specifies the security logon method required to run those tasks associated with the principal.</span></span><br/>  |
| [<span data-ttu-id="78edb-128">**IDutilisateur**</span><span class="sxs-lookup"><span data-stu-id="78edb-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)           | <span data-ttu-id="78edb-129">**string**</span><span class="sxs-lookup"><span data-stu-id="78edb-129">**string**</span></span>                                                    | <span data-ttu-id="78edb-130">Spécifie l’identificateur d’utilisateur requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="78edb-130">Specifies the user identifier required to run tasks associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="78edb-131">Attributs</span><span class="sxs-lookup"><span data-stu-id="78edb-131">Attributes</span></span>



| <span data-ttu-id="78edb-132">Nom</span><span class="sxs-lookup"><span data-stu-id="78edb-132">Name</span></span> | <span data-ttu-id="78edb-133">Type</span><span class="sxs-lookup"><span data-stu-id="78edb-133">Type</span></span> | <span data-ttu-id="78edb-134">Description</span><span class="sxs-lookup"><span data-stu-id="78edb-134">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="78edb-135">Id</span><span class="sxs-lookup"><span data-stu-id="78edb-135">Id</span></span>   | <span data-ttu-id="78edb-136">id</span><span class="sxs-lookup"><span data-stu-id="78edb-136">ID</span></span>   | <span data-ttu-id="78edb-137">Identificateur de la définition du principal.</span><span class="sxs-lookup"><span data-stu-id="78edb-137">Identifier of the principal definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="78edb-138">Notes</span><span class="sxs-lookup"><span data-stu-id="78edb-138">Remarks</span></span>

<span data-ttu-id="78edb-139">Pour le développement de scripts, les informations d’identification de sécurité pour un principal sont spécifiées à l’aide de l’objet [**principal**](principal.md) .</span><span class="sxs-lookup"><span data-stu-id="78edb-139">For scripting development, the security credentials for a principal are specified using the [**Principal**](principal.md) object.</span></span>

<span data-ttu-id="78edb-140">Pour le développement C++, les informations d’identification de sécurité d’un principal sont spécifiées à l’aide de l’interface [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .</span><span class="sxs-lookup"><span data-stu-id="78edb-140">For C++ development, the security credentials for a principal are specified using the [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) interface.</span></span>

<span data-ttu-id="78edb-141">Les éléments enfants répertoriés ci-dessus sont définis par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="78edb-141">The child elements listed above are defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span> <span data-ttu-id="78edb-142">Pour plus d’informations sur le séquencement de ces éléments enfants, consultez [**principalType**](taskschedulerschema-principaltype-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="78edb-142">For sequencing information for these child elements, see [**principalType**](taskschedulerschema-principaltype-complextype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="78edb-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="78edb-143">Examples</span></span>

<span data-ttu-id="78edb-144">Le code XML suivant définit un principal avec un identificateur d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78edb-144">The following XML defines a principal with a user identifier.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



<span data-ttu-id="78edb-145">Le code XML suivant définit un principal avec un identificateur de groupe.</span><span class="sxs-lookup"><span data-stu-id="78edb-145">The following XML defines a principal with a group identifier.</span></span>


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="78edb-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78edb-146">Requirements</span></span>



| <span data-ttu-id="78edb-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78edb-147">Requirement</span></span> | <span data-ttu-id="78edb-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="78edb-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78edb-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78edb-149">Minimum supported client</span></span><br/> | <span data-ttu-id="78edb-150">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78edb-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78edb-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78edb-151">Minimum supported server</span></span><br/> | <span data-ttu-id="78edb-152">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78edb-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78edb-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78edb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78edb-154">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="78edb-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





