---
title: Extensions de Binding-Handle Microsoft RPC
description: Les extensions Microsoft du langage IDL prennent en charge plusieurs paramètres de handle qui apparaissent dans des positions autres que le premier paramètre, le plus à gauche.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104032003"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a><span data-ttu-id="f157c-103">Extensions de Binding-Handle Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="f157c-103">Microsoft RPC Binding-Handle Extensions</span></span>

<span data-ttu-id="f157c-104">Les extensions Microsoft du langage IDL prennent en charge plusieurs paramètres de handle qui apparaissent dans des positions autres que le premier paramètre, le plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="f157c-104">The Microsoft extensions to the IDL language support multiple handle parameters that appear in positions other than the first, leftmost, parameter.</span></span> <span data-ttu-id="f157c-105">Les étapes suivantes décrivent la séquence que le compilateur MIDL passe pour résoudre le paramètre de handle de liaison en mode de compatibilité DCE (/**OSF**) et en mode par défaut (étendu Microsoft).</span><span class="sxs-lookup"><span data-stu-id="f157c-105">The following steps describe the sequence that the MIDL compiler goes through to resolve the binding-handle parameter in DCE-compatibility mode (/**osf**), and in default (Microsoft-extended) mode.</span></span>

## <a name="dce-compatibility-mode"></a><span data-ttu-id="f157c-106">DCE-mode de compatibilité</span><span class="sxs-lookup"><span data-stu-id="f157c-106">DCE-compatibility mode</span></span>

-   <span data-ttu-id="f157c-107">Handle de liaison qui apparaît à la première position.</span><span class="sxs-lookup"><span data-stu-id="f157c-107">Binding handle that appears in first position.</span></span>
-   <span data-ttu-id="f157c-108">\[ [**À l'**](/windows/desktop/Midl/in)extrême gauche, paramètre de [**\_ handle de contexte**](/windows/desktop/Midl/context-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="f157c-108">Leftmost \[[**in**](/windows/desktop/Midl/in), [**context\_handle**](/windows/desktop/Midl/context-handle)\] parameter.</span></span>
-   <span data-ttu-id="f157c-109">Handle de liaison implicite spécifié par un handle \[ [**implicite \_**](/windows/desktop/Midl/implicit-handle) \] ou un \[ [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="f157c-109">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="f157c-110">Si aucun CCP n’est présent, utilise par défaut le \[ **\_ descripteur automatique** \] .</span><span class="sxs-lookup"><span data-stu-id="f157c-110">If no ACF present, default to use of \[**auto\_handle**\].</span></span>

## <a name="default-mode"></a><span data-ttu-id="f157c-111">Mode par défaut</span><span class="sxs-lookup"><span data-stu-id="f157c-111">Default mode</span></span>

-   <span data-ttu-id="f157c-112">Handle de liaison explicite le plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="f157c-112">Leftmost explicit binding handle.</span></span>
-   <span data-ttu-id="f157c-113">Handle de liaison implicite spécifié par un handle \[ [**implicite \_**](/windows/desktop/Midl/implicit-handle) \] ou un \[ [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="f157c-113">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="f157c-114">Si aucun CCP n’est présent, utilise par défaut le \[ [**\_ descripteur automatique**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="f157c-114">If no ACF present, default to use of \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="f157c-115">Les compilateurs IDL DCE recherchent un handle de liaison explicite comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="f157c-115">DCE IDL compilers look for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="f157c-116">Lorsque le premier paramètre n’est pas un handle de liaison et qu’un ou plusieurs descripteurs de contexte sont spécifiés, le descripteur de contexte le plus à gauche est utilisé comme handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="f157c-116">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="f157c-117">Lorsque le premier paramètre n’est pas un handle et qu’il n’existe aucun descripteur de contexte, la procédure utilise une liaison implicite à l’aide du handle \[ [**implicite \_**](/windows/desktop/Midl/implicit-handle) de l’attribut ACF \] ou du \[ [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="f157c-117">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="f157c-118">Les extensions Microsoft de l’IDL permettent au handle de liaison d’être dans une position autre que le premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="f157c-118">The Microsoft extensions to the IDL allow the binding handle to be in a position other than the first parameter.</span></span> <span data-ttu-id="f157c-119">Le plus \[ [**à gauche dans**](/windows/desktop/Midl/in) le \] paramètre de handle explicite, qu’il s’agisse d’un handle primitif, défini par le programmeur ou d’un handle de contexte, est le handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="f157c-119">The leftmost \[[**in**](/windows/desktop/Midl/in)\] explicit-handle parameter–whether it is a primitive, programmer-defined, or context handle–is the binding handle.</span></span> <span data-ttu-id="f157c-120">Lorsqu’il n’y a aucun paramètre de handle, la procédure utilise une liaison implicite à l’aide du handle \[ [**implicite \_**](/windows/desktop/Midl/implicit-handle) de l’attribut ACF \] ou du \[ [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="f157c-120">When there are no handle parameters, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="f157c-121">Les règles suivantes s’appliquent à la fois au mode de compatibilité DCE (/OSF) et au mode par défaut :</span><span class="sxs-lookup"><span data-stu-id="f157c-121">The following rules apply to both DCE-compatibility (/osf) mode and default mode:</span></span>

-   <span data-ttu-id="f157c-122">La liaison de gestion automatique est utilisée quand aucun CCP n’est présent.</span><span class="sxs-lookup"><span data-stu-id="f157c-122">Auto-handle binding is used when no ACF is present.</span></span>
-   <span data-ttu-id="f157c-123">\[ [](/windows/desktop/Midl/in) \] Descripteurs in ou \[ **in**, [**out**](/windows/desktop/Midl/out-idl) explicites \] pour une fonction individuelle preempt toute liaison implicite spécifiée pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="f157c-123">Explicit \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, [**out**](/windows/desktop/Midl/out-idl)\] handles for an individual function preempt any implicit binding specified for the interface.</span></span>
-   <span data-ttu-id="f157c-124">Plusieurs \[ [](/windows/desktop/Midl/in) \] \[ Handles de primitives in ou **in**, out \] ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f157c-124">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] primitive handles are not supported.</span></span>
-   <span data-ttu-id="f157c-125">Plusieurs \[ [](/windows/desktop/Midl/in) \] \[ Handles de contexte explicites in ou **in**, out \] sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="f157c-125">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] explicit context handles are allowed.</span></span>
-   <span data-ttu-id="f157c-126">Tous les paramètres de handle définis par le programmeur, à l’exception du paramètre de handle de liaison, sont traités comme des données transmissibles.</span><span class="sxs-lookup"><span data-stu-id="f157c-126">All programmer-defined handle parameters except the binding-handle parameter are treated as transmissible data.</span></span>

<span data-ttu-id="f157c-127">Le tableau suivant contient des exemples et décrit comment les handles de liaison sont assignés dans chaque mode de compilateur.</span><span class="sxs-lookup"><span data-stu-id="f157c-127">The following table contains examples and describes how binding handles are assigned in each compiler mode.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f157c-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="f157c-128">Example</span></span></th>
<th><span data-ttu-id="f157c-129">Description</span><span class="sxs-lookup"><span data-stu-id="f157c-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td><span data-ttu-id="f157c-130">Aucun handle explicite n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="f157c-130">No explicit handle is specified.</span></span> <span data-ttu-id="f157c-131">Le handle de liaison implicite, spécifié par [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] ou [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f157c-131">The implicit binding handle, specified by [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] or [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], is used.</span></span> <span data-ttu-id="f157c-132">Quand aucun CCP n’est présent, un descripteur automatique est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f157c-132">When no ACF is present, an auto handle is used.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td><span data-ttu-id="f157c-133">Un handle explicite de type handle_t est spécifié.</span><span class="sxs-lookup"><span data-stu-id="f157c-133">An explicit handle of type handle_t is specified.</span></span> <span data-ttu-id="f157c-134">Le paramètre <em>H</em> est le handle de liaison de la procédure.</span><span class="sxs-lookup"><span data-stu-id="f157c-134">The parameter <em>H</em> is the binding handle for the procedure.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td><span data-ttu-id="f157c-135">Le premier paramètre n’est pas un descripteur.</span><span class="sxs-lookup"><span data-stu-id="f157c-135">The first parameter is not a handle.</span></span> <span data-ttu-id="f157c-136">En mode par défaut, le paramètre de handle le plus à gauche, <em>H</em>, est le handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="f157c-136">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="f157c-137">En mode/OSF, la liaison implicite est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f157c-137">In /osf mode, implicit binding is used.</span></span> <span data-ttu-id="f157c-138">Une erreur est signalée, car le deuxième paramètre est supposé être transmissible et handle_t ne peut pas être transmis.</span><span class="sxs-lookup"><span data-stu-id="f157c-138">An error is reported because the second parameter is expected to be transmissible, and handle_t cannot be transmitted.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td><span data-ttu-id="f157c-139">Le premier paramètre n’est pas un descripteur.</span><span class="sxs-lookup"><span data-stu-id="f157c-139">The first parameter is not a handle.</span></span> <span data-ttu-id="f157c-140">En mode par défaut, le paramètre de handle le plus à gauche, <em>H</em>, est le handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="f157c-140">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="f157c-141">Les stubs appellent les routines fournies par l’utilisateur MY_HDL_bind et MY_HDL_unbind.</span><span class="sxs-lookup"><span data-stu-id="f157c-141">The stubs call the user-supplied routines MY_HDL_bind and MY_HDL_unbind.</span></span> <span data-ttu-id="f157c-142">En mode OSF, la liaison implicite est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f157c-142">In/osf mode, implicit binding is used.</span></span> <span data-ttu-id="f157c-143">Le paramètre de descripteur défini par le programmeur <em>H</em> est traité comme des données transmissibles.</span><span class="sxs-lookup"><span data-stu-id="f157c-143">The programmer-defined handle parameter <em>H</em> is treated as transmissible data.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td><span data-ttu-id="f157c-144">Le premier paramètre est un handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="f157c-144">The first parameter is a binding handle.</span></span> <span data-ttu-id="f157c-145">Le paramètre <em>H</em> est le paramètre de handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="f157c-145">The parameter <em>H</em> is the binding-handle parameter.</span></span> <span data-ttu-id="f157c-146">Le deuxième paramètre de handle défini par le programmeur est traité comme des données transmissibles.</span><span class="sxs-lookup"><span data-stu-id="f157c-146">The second programmer-defined handle parameter is treated as transmissible data.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td><span data-ttu-id="f157c-147">Le handle de liaison est un handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="f157c-147">The binding handle is a context handle.</span></span> <span data-ttu-id="f157c-148">Le paramètre <em>H</em> est le handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="f157c-148">The parameter <em>H</em> is the binding handle.</span></span></td>
</tr>
</tbody>
</table>



 

 

 