---
description: Les ACE spécifiques à l’objet sont prises en charge pour les objets de service d’annuaire (DS). Une entrée du contrôle d’accès spécifique à un objet contient une paire de GUID qui étendent la manière dont l’entrée du contrôle d’accès peut protéger un objet.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: ACE spécifiques à l’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40760e5cd06af97e93f74c6ff8daff89cd5962f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034859"
---
# <a name="object-specific-aces"></a><span data-ttu-id="b0ea5-104">ACE spécifiques à l’objet</span><span class="sxs-lookup"><span data-stu-id="b0ea5-104">Object-specific ACEs</span></span>

<span data-ttu-id="b0ea5-105">Les [*ACE*](/windows/desktop/SecGloss/a-gly) spécifiques à l’objet sont prises en charge pour les objets de service d’annuaire (DS).</span><span class="sxs-lookup"><span data-stu-id="b0ea5-105">Object-specific [*ACEs*](/windows/desktop/SecGloss/a-gly) are supported for directory service (DS) objects.</span></span> <span data-ttu-id="b0ea5-106">Une entrée du contrôle d’accès spécifique à un objet contient une paire de GUID qui étendent la manière dont l’entrée du contrôle d’accès peut protéger un objet.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-106">An object-specific ACE contains a pair of GUIDs that expand the ways in which the ACE can protect an object.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0ea5-107">GUID</span><span class="sxs-lookup"><span data-stu-id="b0ea5-107">GUID</span></span></th>
<th><span data-ttu-id="b0ea5-108">Description</span><span class="sxs-lookup"><span data-stu-id="b0ea5-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b0ea5-109"><strong>ObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="b0ea5-109"><strong>ObjectType</strong></span></span></td>
<td><span data-ttu-id="b0ea5-110">Identifie l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b0ea5-110">Identifies one of the following:</span></span>
<ul>
<li><span data-ttu-id="b0ea5-111">Type d’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-111">A type of child object.</span></span> <span data-ttu-id="b0ea5-112">L’ACE contrôle le droit de créer un type spécifié d’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-112">The ACE controls the right to create a specified type of child object.</span></span> <span data-ttu-id="b0ea5-113">Pour plus d’informations, consultez <a href="controlling-child-object-creation-in-c--.md">contrôle de la création d’objets enfants en C++</a>.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-113">For more information, see <a href="controlling-child-object-creation-in-c--.md">Controlling Child Object Creation in C++</a>.</span></span></li>
<li><span data-ttu-id="b0ea5-114">Jeu de propriétés ou propriété.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-114">A property set or property.</span></span> <span data-ttu-id="b0ea5-115">L’ACE contrôle le droit de lire ou d’écrire la propriété ou le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-115">The ACE controls the right to read or write the property or property set.</span></span> <span data-ttu-id="b0ea5-116">Pour plus d’informations, consultez <a href="aces-to-control-access-to-an-object-s-properties.md">ACE pour contrôler l’accès aux propriétés d’un objet</a>.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-116">For more information, see <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs to Control Access to an Object's Properties</a>.</span></span></li>
<li><span data-ttu-id="b0ea5-117">Un droit étendu.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-117">An extended right.</span></span> <span data-ttu-id="b0ea5-118">L’ACE contrôle le droit d’exécuter l’opération associée au droit étendu.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-118">The ACE controls the right to perform the operation associated with the extended right.</span></span></li>
<li><span data-ttu-id="b0ea5-119">Écriture validée.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-119">A validated write.</span></span> <span data-ttu-id="b0ea5-120">L’ACE contrôle le droit d’effectuer certaines opérations d’écriture.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-120">The ACE controls the right to perform certain write operations.</span></span> <span data-ttu-id="b0ea5-121">Ces autorisations d’écriture validées, définies et exposées dans l’éditeur ACL, fournissent des autorisations pour les écritures de propriétés validées plutôt que des écritures de bas niveau non contrôlées de toute valeur dans une propriété accordée avec une &quot; autorisation Write Property &quot; .</span><span class="sxs-lookup"><span data-stu-id="b0ea5-121">These validated write permissions, defined and exposed in the ACL Editor, provide permissions for validated writes of properties rather than unchecked low-level writes of any value to a property that is granted with a &quot;write property&quot; permission.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0ea5-122"><strong>InheritedObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="b0ea5-122"><strong>InheritedObjectType</strong></span></span></td>
<td><span data-ttu-id="b0ea5-123">Indique le type d’objet enfant qui peut hériter de l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-123">Indicates the type of child object that can inherit the ACE.</span></span> <span data-ttu-id="b0ea5-124">L’héritage est également contrôlé par les indicateurs d’héritage dans le <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, ainsi que par toute protection contre l’héritage placée sur les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-124">Inheritance is also controlled by the inheritance flags in the <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, as well as by any protection against inheritance placed on the child objects.</span></span> <span data-ttu-id="b0ea5-125">Pour plus d’informations, consultez <a href="ace-inheritance.md">héritage de l’entrée</a>du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-125">For more information, see <a href="ace-inheritance.md">ACE Inheritance</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b0ea5-126">Trois types d’ACE spécifiques aux objets sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-126">Three types of object-specific ACEs are supported.</span></span>

> [!Note]  
> <span data-ttu-id="b0ea5-127">Les ACE de l’objet System-Alarm ne sont pas prises en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-127">System-alarm object ACEs are not currently supported.</span></span>

 



| <span data-ttu-id="b0ea5-128">Type</span><span class="sxs-lookup"><span data-stu-id="b0ea5-128">Type</span></span>                      | <span data-ttu-id="b0ea5-129">Description</span><span class="sxs-lookup"><span data-stu-id="b0ea5-129">Description</span></span>                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ea5-130">ACE d’accès refusé à l’objet</span><span class="sxs-lookup"><span data-stu-id="b0ea5-130">Access-denied object ACE</span></span>  | <span data-ttu-id="b0ea5-131">Utilisé dans une liste DACL pour refuser à un tiers de confiance l’accès à une propriété ou à une propriété définie sur l’objet, ou pour limiter l’héritage de l’entrée du contrôle d’accès à un type spécifié d’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-131">Used in a DACL to deny a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="b0ea5-132">Utilise la structure d' [**\_ ACE d' \_ objet \_ accès refusé**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="b0ea5-132">Uses the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) structure.</span></span>         |
| <span data-ttu-id="b0ea5-133">ACE de l’objet Access-allowed</span><span class="sxs-lookup"><span data-stu-id="b0ea5-133">Access-allowed object ACE</span></span> | <span data-ttu-id="b0ea5-134">Utilisé dans une liste DACL pour permettre à un tiers de confiance d’accéder à une propriété ou à une propriété définie sur l’objet, ou pour limiter l’héritage de l’entrée du contrôle d’accès à un type spécifié d’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-134">Used in a DACL to allow a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="b0ea5-135">Utilise la [**structure \_ \_ \_ ACE access allowed Object**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="b0ea5-135">Uses the [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) structure.</span></span>      |
| <span data-ttu-id="b0ea5-136">ACE de l’objet audit système</span><span class="sxs-lookup"><span data-stu-id="b0ea5-136">System-audit object ACE</span></span>   | <span data-ttu-id="b0ea5-137">Utilisé dans une liste SACL pour enregistrer les tentatives d’un tiers de confiance pour accéder à une propriété ou à un jeu de propriétés sur l’objet, ou pour limiter l’héritage de l’entrée du contrôle d’accès à un type spécifié d’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-137">Used in a SACL to log a trustee's attempts to access a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="b0ea5-138">Utilise la structure ACE de l' [**\_ \_ objet \_ audit du système**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="b0ea5-138">Uses the [**SYSTEM\_AUDIT\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) structure.</span></span> |



 

<span data-ttu-id="b0ea5-139">Toute liste de contrôle d’accès qui contient une entrée du contrôle d’accès spécifique à un objet doit utiliser la révision d’ACL de révision \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b0ea5-139">Any ACL that contains an object-specific ACE must use the revision ACL\_REVISION\_DS.</span></span>

 

 
