---
title: Élément RequiredPrivileges (requiredPrivilegesType)
description: Spécifie les privilèges requis par la tâche.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Élément RequiredPrivileges Planificateur de tâches
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106354"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a><span data-ttu-id="ab4f4-104">Élément RequiredPrivileges (requiredPrivilegesType)</span><span class="sxs-lookup"><span data-stu-id="ab4f4-104">RequiredPrivileges (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="ab4f4-105">Spécifie les privilèges requis par la tâche.</span><span class="sxs-lookup"><span data-stu-id="ab4f4-105">Specifies the privileges that are required by the task.</span></span>

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

<span data-ttu-id="ab4f4-106">L’élément **RequiredPrivileges** est défini par le type complexe [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ab4f4-106">The **RequiredPrivileges** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ab4f4-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ab4f4-107">Parent element</span></span>



| <span data-ttu-id="ab4f4-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ab4f4-108">Element</span></span>                                                                                  | <span data-ttu-id="ab4f4-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="ab4f4-109">Derived from</span></span>                                                           | <span data-ttu-id="ab4f4-110">Description</span><span class="sxs-lookup"><span data-stu-id="ab4f4-110">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ab4f4-111">**Principal (principalType)**</span><span class="sxs-lookup"><span data-stu-id="ab4f4-111">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="ab4f4-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="ab4f4-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="ab4f4-113">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="ab4f4-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ab4f4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ab4f4-114">Remarks</span></span>

<span data-ttu-id="ab4f4-115">Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**IPrincipal2 :: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="ab4f4-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ab4f4-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="ab4f4-116">Examples</span></span>

<span data-ttu-id="ab4f4-117">Le code XML suivant définit l’utilisation d’un identificateur de groupe et des privilèges requis.</span><span class="sxs-lookup"><span data-stu-id="ab4f4-117">The following XML defines using a group identifier and the required privileges.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="ab4f4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab4f4-118">Requirements</span></span>



| <span data-ttu-id="ab4f4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab4f4-119">Requirement</span></span> | <span data-ttu-id="ab4f4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab4f4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ab4f4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab4f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ab4f4-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab4f4-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ab4f4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab4f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ab4f4-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab4f4-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab4f4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab4f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab4f4-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ab4f4-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





