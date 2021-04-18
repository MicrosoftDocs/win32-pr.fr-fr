---
title: Élément LogonType (principalType)
description: Spécifie la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Élément LogonType Planificateur de tâches
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512556"
---
# <a name="logontype-principaltype-element"></a><span data-ttu-id="6163a-104">Élément LogonType (principalType)</span><span class="sxs-lookup"><span data-stu-id="6163a-104">LogonType (principalType) Element</span></span>

<span data-ttu-id="6163a-105">Spécifie la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="6163a-105">Specifies the security logon method required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

<span data-ttu-id="6163a-106">L’élément **LogonType** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6163a-106">The **LogonType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6163a-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="6163a-107">Parent element</span></span>



| <span data-ttu-id="6163a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="6163a-108">Element</span></span>                                                                  | <span data-ttu-id="6163a-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="6163a-109">Derived from</span></span>                                                           | <span data-ttu-id="6163a-110">Description</span><span class="sxs-lookup"><span data-stu-id="6163a-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6163a-111">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="6163a-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="6163a-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="6163a-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="6163a-113">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="6163a-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6163a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6163a-114">Remarks</span></span>

<span data-ttu-id="6163a-115">L’élément **LogonType** et l’élément [**userid**](taskschedulerschema-userid-principaltype-element.md) sont utilisés ensemble pour définir l’utilisateur requis pour exécuter les tâches qui utilisent ce principal.</span><span class="sxs-lookup"><span data-stu-id="6163a-115">The **LogonType** element and the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="6163a-116">Pour le développement de scripts, le type d’ouverture de session du principal est spécifié par la propriété [**principal. LogonType**](principal-logontype.md) .</span><span class="sxs-lookup"><span data-stu-id="6163a-116">For scripting development, the logon type for the principal is specified by the [**Principal.LogonType**](principal-logontype.md) property.</span></span>

<span data-ttu-id="6163a-117">Pour le développement C++, le type d’ouverture de session du principal est spécifié par la propriété [**IPrincipal :: LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) .</span><span class="sxs-lookup"><span data-stu-id="6163a-117">For C++ development, the logon type for the principal is specified by the [**IPrincipal::LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) property.</span></span>

<span data-ttu-id="6163a-118">Cet élément (défini par le type simple [**LogonType**](taskschedulerschema-logontype-simpletype.md) ) doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6163a-118">This element (defined by the [**logonType**](taskschedulerschema-logontype-simpletype.md) simple type) must have one of the following values.</span></span>

-   <span data-ttu-id="6163a-119">S4U : l’utilisateur doit se connecter à l’aide d’une connexion S4U (service for user).</span><span class="sxs-lookup"><span data-stu-id="6163a-119">S4U: User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="6163a-120">Lorsqu’une ouverture de session S4U est utilisée, aucun mot de passe n’est stocké par le système et il n’y a pas d’accès au réseau ou aux fichiers chiffrés.</span><span class="sxs-lookup"><span data-stu-id="6163a-120">When an S4U logon is used, no password is stored by the system and there is no access to the network or encrypted files.</span></span>
-   <span data-ttu-id="6163a-121">Mot de passe : l’utilisateur doit se connecter à l’aide d’un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="6163a-121">Password: User must log on using a password.</span></span>
-   <span data-ttu-id="6163a-122">InteractiveToken : l’utilisateur doit déjà avoir ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="6163a-122">InteractiveToken: User must already be logged on.</span></span> <span data-ttu-id="6163a-123">La tâche est exécutée uniquement dans une session interactive existante.</span><span class="sxs-lookup"><span data-stu-id="6163a-123">The task will be run only in an existing interactive session.</span></span>

<span data-ttu-id="6163a-124">Pour une tâche, qui contient une action de MessageBox, la boîte de message s’affiche si la tâche est activée et que la tâche a un type de connexion interactive.</span><span class="sxs-lookup"><span data-stu-id="6163a-124">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="6163a-125">Pour définir le type d’ouverture de session de la tâche sur Interactive, spécifiez **InteractiveToken** dans l' **<LogonType>** élément du principal de tâche.</span><span class="sxs-lookup"><span data-stu-id="6163a-125">To set the task logon type to be interactive, specify **InteractiveToken** in the **<LogonType>** element of the task principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="6163a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6163a-126">Requirements</span></span>



| <span data-ttu-id="6163a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6163a-127">Requirement</span></span> | <span data-ttu-id="6163a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6163a-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6163a-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6163a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6163a-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6163a-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6163a-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6163a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6163a-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6163a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6163a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6163a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6163a-134">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="6163a-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





