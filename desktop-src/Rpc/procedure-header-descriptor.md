---
title: Descripteur d’en-tête de procédure
description: L’en-tête a été étendu plusieurs fois pendant la durée de vie du moteur de NDR. Le compilateur actuel génère toujours des en-têtes différents en fonction du mode du compilateur. Toutefois, les en-têtes plus récents sont un sur-ensemble des plus anciens.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463538"
---
# <a name="procedure-header-descriptor"></a><span data-ttu-id="d94b1-105">Descripteur d’en-tête de procédure</span><span class="sxs-lookup"><span data-stu-id="d94b1-105">Procedure Header Descriptor</span></span>

<span data-ttu-id="d94b1-106">L’en-tête a été étendu plusieurs fois pendant la durée de vie du moteur de NDR.</span><span class="sxs-lookup"><span data-stu-id="d94b1-106">The header has been extended several times over the life of the NDR engine.</span></span> <span data-ttu-id="d94b1-107">Le compilateur actuel génère toujours des en-têtes différents en fonction du mode du compilateur.</span><span class="sxs-lookup"><span data-stu-id="d94b1-107">The current compiler still generates different headers depending on the mode of the compiler.</span></span> <span data-ttu-id="d94b1-108">Toutefois, les en-têtes plus récents sont un sur-ensemble des plus anciens.</span><span class="sxs-lookup"><span data-stu-id="d94b1-108">However, more recent headers are a superset of the older ones.</span></span>

## <a name="the-old-oi-header"></a><span data-ttu-id="d94b1-109">L’ancien en-tête-OI</span><span class="sxs-lookup"><span data-stu-id="d94b1-109">The Old –Oi Header</span></span>

<span data-ttu-id="d94b1-110">L’en-tête a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="d94b1-110">The header has the following format:</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="d94b1-111">Où le \_ type de handle<1> peut être l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d94b1-111">Where handle\_type<1> can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="d94b1-112">Hex</span><span class="sxs-lookup"><span data-stu-id="d94b1-112">Hex</span></span> | <span data-ttu-id="d94b1-113">Handle</span><span class="sxs-lookup"><span data-stu-id="d94b1-113">Handle</span></span>               |
|-----|----------------------|
| <span data-ttu-id="d94b1-114">31</span><span class="sxs-lookup"><span data-stu-id="d94b1-114">31</span></span>  | <span data-ttu-id="d94b1-115">\_générique de liaison FC \_</span><span class="sxs-lookup"><span data-stu-id="d94b1-115">FC\_BIND\_GENERIC</span></span>    |
| <span data-ttu-id="d94b1-116">32</span><span class="sxs-lookup"><span data-stu-id="d94b1-116">32</span></span>  | <span data-ttu-id="d94b1-117">\_primitive de liaison FC \_</span><span class="sxs-lookup"><span data-stu-id="d94b1-117">FC\_BIND\_PRIMITIVE</span></span>  |
| <span data-ttu-id="d94b1-118">33</span><span class="sxs-lookup"><span data-stu-id="d94b1-118">33</span></span>  | <span data-ttu-id="d94b1-119">\_descripteur automatique FC \_</span><span class="sxs-lookup"><span data-stu-id="d94b1-119">FC\_AUTO\_HANDLE</span></span>     |
| <span data-ttu-id="d94b1-120">34</span><span class="sxs-lookup"><span data-stu-id="d94b1-120">34</span></span>  | <span data-ttu-id="d94b1-121">\_handle de rappel FC \_</span><span class="sxs-lookup"><span data-stu-id="d94b1-121">FC\_CALLBACK\_HANDLE</span></span> |
| <span data-ttu-id="d94b1-122">0</span><span class="sxs-lookup"><span data-stu-id="d94b1-122">0</span></span>   | <span data-ttu-id="d94b1-123">(handle explicite)</span><span class="sxs-lookup"><span data-stu-id="d94b1-123">(explicit handle)</span></span>    |



 

<span data-ttu-id="d94b1-124">Si le type de handle \_<1> champ est différent de zéro, la procédure utilise alors un handle implicite du type indiqué.</span><span class="sxs-lookup"><span data-stu-id="d94b1-124">If the handle\_type<1> field is nonzero, then the procedure uses an implicit handle of the indicated kind.</span></span> <span data-ttu-id="d94b1-125">Pour plus d’informations, consultez la rubrique [Handles](handles.md) .</span><span class="sxs-lookup"><span data-stu-id="d94b1-125">See the [Handles](handles.md) topic for a more information.</span></span> <span data-ttu-id="d94b1-126">Si le type de handle \_<1> champ est égal à zéro, le handle utilisé pour la liaison est l’un des paramètres de la procédure.</span><span class="sxs-lookup"><span data-stu-id="d94b1-126">If the handle\_type<1> field is zero, the handle used for binding is one of the procedure's parameters.</span></span>

<span data-ttu-id="d94b1-127">Les handles explicites peuvent être de la primitive, du générique et du contexte. la dernière a le jeton FC suivant.</span><span class="sxs-lookup"><span data-stu-id="d94b1-127">Explicit handles can be primitive, generic, and context; the last one has the following FC token.</span></span>



| <span data-ttu-id="d94b1-128">Hex</span><span class="sxs-lookup"><span data-stu-id="d94b1-128">Hex</span></span> | <span data-ttu-id="d94b1-129">Handle</span><span class="sxs-lookup"><span data-stu-id="d94b1-129">Handle</span></span>            |
|-----|-------------------|
| <span data-ttu-id="d94b1-130">30</span><span class="sxs-lookup"><span data-stu-id="d94b1-130">30</span></span>  | <span data-ttu-id="d94b1-131">\_contexte de liaison FC \_</span><span class="sxs-lookup"><span data-stu-id="d94b1-131">FC\_BIND\_CONTEXT</span></span> |



 

<span data-ttu-id="d94b1-132">Par Convention, le type de handle pour les interfaces DCOM est le \_ \_ descripteur auto FC.</span><span class="sxs-lookup"><span data-stu-id="d94b1-132">By convention, the handle type for DCOM interfaces is FC\_AUTO\_HANDLE.</span></span>

<span data-ttu-id="d94b1-133">Les \_ indicateurs Oi<1> champ est un masque de 8 bits des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="d94b1-133">The Oi\_flags<1> field is an 8-bit mask of the following flags.</span></span>



| <span data-ttu-id="d94b1-134">Hex</span><span class="sxs-lookup"><span data-stu-id="d94b1-134">Hex</span></span> | <span data-ttu-id="d94b1-135">Indicateur</span><span class="sxs-lookup"><span data-stu-id="d94b1-135">Flag</span></span>                         | <span data-ttu-id="d94b1-136">Signification</span><span class="sxs-lookup"><span data-stu-id="d94b1-136">Meaning</span></span>                                  |
|-----|------------------------------|------------------------------------------|
| <span data-ttu-id="d94b1-137">01</span><span class="sxs-lookup"><span data-stu-id="d94b1-137">01</span></span>  | <span data-ttu-id="d94b1-138">Point de \_ pointeur complet de OI \_ \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="d94b1-138">Oi\_FULL\_PTR\_USED</span></span>          | <span data-ttu-id="d94b1-139">Utilise le package de pointeurs complet.</span><span class="sxs-lookup"><span data-stu-id="d94b1-139">Uses the full pointer package.</span></span>           |
| <span data-ttu-id="d94b1-140">02</span><span class="sxs-lookup"><span data-stu-id="d94b1-140">02</span></span>  | <span data-ttu-id="d94b1-141">OI \_ RPCSS \_ RPCSS \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="d94b1-141">Oi\_RPCSS\_ALLOC\_USED</span></span>       | <span data-ttu-id="d94b1-142">Utilise le package de mémoire RpcSs.</span><span class="sxs-lookup"><span data-stu-id="d94b1-142">Uses the RpcSs memory package.</span></span>           |
| <span data-ttu-id="d94b1-143">04</span><span class="sxs-lookup"><span data-stu-id="d94b1-143">04</span></span>  | <span data-ttu-id="d94b1-144">Procédure de l' \_ objet OI \_</span><span class="sxs-lookup"><span data-stu-id="d94b1-144">Oi\_OBJECT\_PROC</span></span>             | <span data-ttu-id="d94b1-145">Procédure dans une interface d’objet.</span><span class="sxs-lookup"><span data-stu-id="d94b1-145">A procedure in an object interface.</span></span>      |
| <span data-ttu-id="d94b1-146">08</span><span class="sxs-lookup"><span data-stu-id="d94b1-146">08</span></span>  | <span data-ttu-id="d94b1-147">OI \_ a \_ RPCFLAGS</span><span class="sxs-lookup"><span data-stu-id="d94b1-147">Oi\_HAS\_RPCFLAGS</span></span>            | <span data-ttu-id="d94b1-148">La procédure a des indicateurs RPC non nuls.</span><span class="sxs-lookup"><span data-stu-id="d94b1-148">The procedure has nonzero Rpc flags.</span></span>     |
| <span data-ttu-id="d94b1-149">10</span><span class="sxs-lookup"><span data-stu-id="d94b1-149">10</span></span>  | <span data-ttu-id="d94b1-150">OI\_\*</span><span class="sxs-lookup"><span data-stu-id="d94b1-150">Oi\_\*</span></span>                       | <span data-ttu-id="d94b1-151">Surchargé.</span><span class="sxs-lookup"><span data-stu-id="d94b1-151">Overloaded.</span></span>                              |
| <span data-ttu-id="d94b1-152">20</span><span class="sxs-lookup"><span data-stu-id="d94b1-152">20</span></span>  | <span data-ttu-id="d94b1-153">OI\_\*</span><span class="sxs-lookup"><span data-stu-id="d94b1-153">Oi\_\*</span></span>                       | <span data-ttu-id="d94b1-154">Surchargé.</span><span class="sxs-lookup"><span data-stu-id="d94b1-154">Overloaded.</span></span>                              |
| <span data-ttu-id="d94b1-155">40</span><span class="sxs-lookup"><span data-stu-id="d94b1-155">40</span></span>  | <span data-ttu-id="d94b1-156">OI \_ utiliser \_ de \_ nouvelles \_ routines init</span><span class="sxs-lookup"><span data-stu-id="d94b1-156">Oi\_USE\_NEW\_INIT\_ROUTINES</span></span> | <span data-ttu-id="d94b1-157">Utilise les routines init et Windows NT 3.5 bêta 2.</span><span class="sxs-lookup"><span data-stu-id="d94b1-157">Uses Windows NT3.5 Beta2+ init routines.</span></span> |
| <span data-ttu-id="d94b1-158">80</span><span class="sxs-lookup"><span data-stu-id="d94b1-158">80</span></span>  |                              | <span data-ttu-id="d94b1-159">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d94b1-159">Unused.</span></span>                                  |



 

<span data-ttu-id="d94b1-160">Les indicateurs suivants sont surchargés.</span><span class="sxs-lookup"><span data-stu-id="d94b1-160">The following flags are overloaded.</span></span>



| <span data-ttu-id="d94b1-161">Hex</span><span class="sxs-lookup"><span data-stu-id="d94b1-161">Hex</span></span> | <span data-ttu-id="d94b1-162">Indicateur</span><span class="sxs-lookup"><span data-stu-id="d94b1-162">Flag</span></span>                                    | <span data-ttu-id="d94b1-163">Signification</span><span class="sxs-lookup"><span data-stu-id="d94b1-163">Meaning</span></span>                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="d94b1-164">10</span><span class="sxs-lookup"><span data-stu-id="d94b1-164">10</span></span>  | <span data-ttu-id="d94b1-165">ENCODE \_ est \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="d94b1-165">ENCODE\_IS\_USED</span></span>                        | <span data-ttu-id="d94b1-166">Utilisé uniquement dans le choix.</span><span class="sxs-lookup"><span data-stu-id="d94b1-166">Used only in pickling.</span></span>                              |
| <span data-ttu-id="d94b1-167">20</span><span class="sxs-lookup"><span data-stu-id="d94b1-167">20</span></span>  | <span data-ttu-id="d94b1-168">le décodage \_ est \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="d94b1-168">DECODE\_IS\_USED</span></span>                        | <span data-ttu-id="d94b1-169">Utilisé uniquement dans le choix.</span><span class="sxs-lookup"><span data-stu-id="d94b1-169">Used only in pickling.</span></span>                              |
| <span data-ttu-id="d94b1-170">10</span><span class="sxs-lookup"><span data-stu-id="d94b1-170">10</span></span>  | <span data-ttu-id="d94b1-171">OI \_ Ignorer \_ la \_ gestion des exceptions d’objets \_</span><span class="sxs-lookup"><span data-stu-id="d94b1-171">Oi\_IGNORE\_OBJECT\_EXCEPTION\_HANDLING</span></span> | <span data-ttu-id="d94b1-172">N’est plus utilisé (anciennement OLE).</span><span class="sxs-lookup"><span data-stu-id="d94b1-172">Not used anymore (old OLE).</span></span>                         |
| <span data-ttu-id="d94b1-173">20</span><span class="sxs-lookup"><span data-stu-id="d94b1-173">20</span></span>  | <span data-ttu-id="d94b1-174">OI \_ a \_ comm \_ ou \_ Fault</span><span class="sxs-lookup"><span data-stu-id="d94b1-174">Oi\_HAS\_COMM\_OR\_FAULT</span></span>                | <span data-ttu-id="d94b1-175">Dans le protocole RPC brut uniquement, \[ comm \_ , état d’erreur \_ \] .</span><span class="sxs-lookup"><span data-stu-id="d94b1-175">In raw RPC only, \[comm \_, fault\_status\].</span></span>        |
| <span data-ttu-id="d94b1-176">20</span><span class="sxs-lookup"><span data-stu-id="d94b1-176">20</span></span>  | <span data-ttu-id="d94b1-177">OI \_ obj \_ use \_ v2 \_ interpréteur</span><span class="sxs-lookup"><span data-stu-id="d94b1-177">Oi\_OBJ\_USE\_V2\_INTERPRETER</span></span>           | <span data-ttu-id="d94b1-178">Dans DCOM uniquement, utilisez l’interpréteur d' [**interfaces**](/windows/desktop/Midl/-oi) de protocole.</span><span class="sxs-lookup"><span data-stu-id="d94b1-178">In DCOM only, use [**–Oif**](/windows/desktop/Midl/-oi) interpreter.</span></span> |



 

<span data-ttu-id="d94b1-179">Le \_ champ indicateurs rpc<4> décrit comment définir le champ **RpcFlags** de la structure [**de \_ message RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) .</span><span class="sxs-lookup"><span data-stu-id="d94b1-179">The rpc\_flags<4> field describes how to set the **RpcFlags** field of the [**RPC\_MESSAGE**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) structure.</span></span> <span data-ttu-id="d94b1-180">Ce champ est présent uniquement si les \_ indicateurs oi<1> champ contient la \_ valeur de \_ RPCFLAGS définie.</span><span class="sxs-lookup"><span data-stu-id="d94b1-180">This field is only present if the Oi\_flags<1> field has Oi\_HAD\_RPCFLAGS set.</span></span> <span data-ttu-id="d94b1-181">Si ce champ n’est pas présent, les indicateurs RPC de la procédure distante sont nuls.</span><span class="sxs-lookup"><span data-stu-id="d94b1-181">If this field is not present, then the RPC flags for the remote procedure are zero.</span></span>

> [!Note]  
> <span data-ttu-id="d94b1-182">Pour des performances, les interpréteurs Async ont toujours le \_ champ indicateurs rpc<4> présent.</span><span class="sxs-lookup"><span data-stu-id="d94b1-182">For performance, the async interpreters always have the rpc\_flags<4> field present.</span></span>

 

<span data-ttu-id="d94b1-183">Le \_ champ proc num<2> indique le numéro de procédure de la procédure.</span><span class="sxs-lookup"><span data-stu-id="d94b1-183">The proc\_num<2> field provides the procedure's procedure number.</span></span>

<span data-ttu-id="d94b1-184">La \_ taille de la pile<2> fournit la taille totale de tous les paramètres sur la pile, y compris ce pointeur et/ou la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="d94b1-184">The stack\_size<2> provides the total size of all parameters on the stack, including any this pointer and/or return value.</span></span>

<span data-ttu-id="d94b1-185">Le \_ champ Description du handle explicite \_<> est décrit plus loin dans ce document.</span><span class="sxs-lookup"><span data-stu-id="d94b1-185">The explicit\_handle\_description<> field is described later in this document.</span></span> <span data-ttu-id="d94b1-186">Ce champ n’est pas présent si la procédure utilise un handle implicite.</span><span class="sxs-lookup"><span data-stu-id="d94b1-186">This field is not present if the procedure uses an implicit handle.</span></span>

 

 