---
title: DisplayName (principalType) (élément)
description: Spécifie le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- DisplayName, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519137"
---
# <a name="displayname-principaltype-element"></a><span data-ttu-id="848fa-104">DisplayName (principalType) (élément)</span><span class="sxs-lookup"><span data-stu-id="848fa-104">DisplayName (principalType) Element</span></span>

<span data-ttu-id="848fa-105">Spécifie le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="848fa-105">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span>

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

<span data-ttu-id="848fa-106">L’élément **DisplayName** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="848fa-106">The **DisplayName** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="848fa-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="848fa-107">Parent element</span></span>



| <span data-ttu-id="848fa-108">Élément</span><span class="sxs-lookup"><span data-stu-id="848fa-108">Element</span></span>                                                                  | <span data-ttu-id="848fa-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="848fa-109">Derived from</span></span>                                                           | <span data-ttu-id="848fa-110">Description</span><span class="sxs-lookup"><span data-stu-id="848fa-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="848fa-111">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="848fa-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="848fa-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="848fa-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="848fa-113">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="848fa-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="848fa-114">Notes</span><span class="sxs-lookup"><span data-stu-id="848fa-114">Remarks</span></span>

<span data-ttu-id="848fa-115">Pour le développement de scripts, le nom complet du principal est spécifié à l’aide de la propriété [**principal. DisplayName**](principal-displayname.md) .</span><span class="sxs-lookup"><span data-stu-id="848fa-115">For scripting development, the display name of the principal is specified using the [**Principal.DisplayName**](principal-displayname.md) property.</span></span>

<span data-ttu-id="848fa-116">Pour le développement C++, le nom complet du principal est spécifié à l’aide de la propriété [**IPrincipal ::D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) .</span><span class="sxs-lookup"><span data-stu-id="848fa-116">For C++ development, the display name of the principal is specified using the [**IPrincipal::DisplayName**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) property.</span></span>

## <a name="examples"></a><span data-ttu-id="848fa-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="848fa-117">Examples</span></span>

<span data-ttu-id="848fa-118">Le code XML suivant définit un à l’aide d’un identificateur de groupe et d’un nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="848fa-118">The following XML defines a using a group identifier and a display name.</span></span>


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



<span data-ttu-id="848fa-119">Le code XML suivant définit un principal à l’aide d’un identificateur d’utilisateur et d’un nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="848fa-119">The following XML defines a principal using a user identifier and a display name.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="848fa-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="848fa-120">Requirements</span></span>



| <span data-ttu-id="848fa-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="848fa-121">Requirement</span></span> | <span data-ttu-id="848fa-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="848fa-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="848fa-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="848fa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="848fa-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="848fa-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="848fa-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="848fa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="848fa-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="848fa-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="848fa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="848fa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="848fa-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="848fa-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





