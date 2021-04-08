---
title: Objet principal
description: Objet de script qui fournit les informations d’identification de sécurité pour un principal.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Planificateur de tâches de l’objet principal
- Planificateur de tâches de l’objet principal, Description
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843325"
---
# <a name="principal-object"></a><span data-ttu-id="2b030-105">Objet principal</span><span class="sxs-lookup"><span data-stu-id="2b030-105">Principal object</span></span>

<span data-ttu-id="2b030-106">Objet de script qui fournit les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="2b030-106">Scripting object that provides the security credentials for a principal.</span></span> <span data-ttu-id="2b030-107">Ces informations d’identification de sécurité définissent le contexte de sécurité pour les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="2b030-107">These security credentials define the security context for the tasks that are associated with the principal.</span></span>

## <a name="members"></a><span data-ttu-id="2b030-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2b030-108">Members</span></span>

<span data-ttu-id="2b030-109">L’objet **principal** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2b030-109">The **Principal** object has these types of members:</span></span>

-   [<span data-ttu-id="2b030-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b030-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b030-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b030-111">Properties</span></span>

<span data-ttu-id="2b030-112">L’objet **principal** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b030-112">The **Principal** object has these properties.</span></span>



| <span data-ttu-id="2b030-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="2b030-113">Property</span></span>                                                | <span data-ttu-id="2b030-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="2b030-114">Access type</span></span>           | <span data-ttu-id="2b030-115">Description</span><span class="sxs-lookup"><span data-stu-id="2b030-115">Description</span></span>                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b030-116">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="2b030-116">**DisplayName**</span></span>](principal-displayname.md)<br/> | <span data-ttu-id="2b030-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2b030-117">Read/write</span></span><br/> | <span data-ttu-id="2b030-118">Obtient ou définit le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="2b030-118">Gets or sets the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                                                                |
| [<span data-ttu-id="2b030-119">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="2b030-119">**GroupId**</span></span>](principal-groupid.md)<br/>         | <span data-ttu-id="2b030-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2b030-120">Read/write</span></span><br/> | <span data-ttu-id="2b030-121">Obtient ou définit l’identificateur du groupe d’utilisateurs qui est requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="2b030-121">Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span><br/>                           |
| [<span data-ttu-id="2b030-122">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="2b030-122">**Id**</span></span>](principal-id.md)<br/>                   | <span data-ttu-id="2b030-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2b030-123">Read/write</span></span><br/> | <span data-ttu-id="2b030-124">Obtient ou définit l'identificateur unique du principal.</span><span class="sxs-lookup"><span data-stu-id="2b030-124">Gets or sets the identifier of the principal.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="2b030-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="2b030-125">**LogonType**</span></span>](principal-logontype.md)<br/>     | <span data-ttu-id="2b030-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2b030-126">Read/write</span></span><br/> | <span data-ttu-id="2b030-127">Obtient ou définit la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="2b030-127">Gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span><br/>                                  |
| [<span data-ttu-id="2b030-128">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="2b030-128">**RunLevel**</span></span>](principal-runlevel.md)<br/>       | <span data-ttu-id="2b030-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2b030-129">Read/write</span></span><br/> | <span data-ttu-id="2b030-130">Obtient ou définit l’identificateur qui est utilisé pour spécifier le niveau de privilège requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="2b030-130">Gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="2b030-131">**IDutilisateur**</span><span class="sxs-lookup"><span data-stu-id="2b030-131">**UserId**</span></span>](principal-userid.md)<br/>           | <span data-ttu-id="2b030-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2b030-132">Read/write</span></span><br/> | <span data-ttu-id="2b030-133">Obtient ou définit l’identificateur de l’utilisateur qui est requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="2b030-133">Gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="2b030-134">Notes</span><span class="sxs-lookup"><span data-stu-id="2b030-134">Remarks</span></span>

<span data-ttu-id="2b030-135">Lorsque vous spécifiez un compte, n’oubliez pas d’utiliser correctement la double barre oblique inverse dans le code pour spécifier le domaine et le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b030-135">When specifying an account, remember to properly use the double backslash in code to specify the domain and user name.</span></span> <span data-ttu-id="2b030-136">Par exemple, utilisez domaine \\ \\ nom d’utilisateur pour spécifier une valeur pour la propriété [**userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="2b030-136">For example, use DOMAIN\\\\UserName to specify a value for the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

<span data-ttu-id="2b030-137">Lors de la lecture ou de l’écriture de données XML pour une tâche, les informations d’identification de sécurité d’un principal sont spécifiées dans l’élément [**principal**](taskschedulerschema-principal-principaltype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="2b030-137">When reading or writing XML for a task, the security credentials for a principal are specified in the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="2b030-138">Si une tâche est inscrite à l’aide de l’outil de ligne de commande at.exe, et que cet objet est utilisé pour extraire des informations sur la tâche, la propriété [**LogonType**](principal-logontype.md) retourne 0, la propriété [**runlevel**](principal-runlevel.md) retourne 0 et la propriété [**userid**](principal-userid.md) retourne la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="2b030-138">If a task is registered using the at.exe command line tool, and this object is used to retrieve information about the task, then the [**LogonType**](principal-logontype.md) property will return 0, the [**RunLevel**](principal-runlevel.md) property will return 0, and the [**UserId**](principal-userid.md) property will return Nothing.</span></span>

## <a name="examples"></a><span data-ttu-id="2b030-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="2b030-139">Examples</span></span>

<span data-ttu-id="2b030-140">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="2b030-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b030-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b030-141">Requirements</span></span>



| <span data-ttu-id="2b030-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b030-142">Requirement</span></span> | <span data-ttu-id="2b030-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b030-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b030-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b030-144">Minimum supported client</span></span><br/> | <span data-ttu-id="2b030-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b030-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2b030-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b030-146">Minimum supported server</span></span><br/> | <span data-ttu-id="2b030-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b030-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b030-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2b030-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b030-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2b030-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2b030-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2b030-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b030-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b030-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





