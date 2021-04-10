---
title: Poignées
description: Jusqu’à deux parties dans la description de la chaîne de format d’une adresse de procédure gère.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316067"
---
# <a name="handles"></a><span data-ttu-id="2a022-103">Poignées</span><span class="sxs-lookup"><span data-stu-id="2a022-103">Handles</span></span>

<span data-ttu-id="2a022-104">Jusqu’à deux parties dans la description de la chaîne de format d’une adresse de procédure gère.</span><span class="sxs-lookup"><span data-stu-id="2a022-104">As many as two parts in the format string description of a procedure address handles.</span></span> <span data-ttu-id="2a022-105">La première partie est le type de handle \_<1> champ de la description d’une procédure, utilisé pour indiquer des handles implicites.</span><span class="sxs-lookup"><span data-stu-id="2a022-105">The first part is the handle\_type<1> field of a procedure's description, used to indicate implicit handles.</span></span> <span data-ttu-id="2a022-106">Cette partie est toujours présente.</span><span class="sxs-lookup"><span data-stu-id="2a022-106">This part is always present.</span></span> <span data-ttu-id="2a022-107">La deuxième partie est une description de paramètre d’un handle explicite de la procédure.</span><span class="sxs-lookup"><span data-stu-id="2a022-107">The second part is a parameter description of any explicit handle in the procedure.</span></span> <span data-ttu-id="2a022-108">Les deux sont expliqués dans les sections suivantes, ainsi qu’une discussion de la prise en charge supplémentaire du compilateur MIDL de la structure du descripteur de stub pour les problèmes de handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="2a022-108">Both are explained in the following sections, along with a discussion of the additional MIDL compiler support of the Stub Descriptor structure for binding handle issues.</span></span>

## <a name="implicit-handles"></a><span data-ttu-id="2a022-109">Handles implicites</span><span class="sxs-lookup"><span data-stu-id="2a022-109">Implicit Handles</span></span>

<span data-ttu-id="2a022-110">Si une procédure utilise un handle implicite pour la liaison, le \_ type de handle<1> champ de la description de la procédure contient une des trois valeurs non nulles valides.</span><span class="sxs-lookup"><span data-stu-id="2a022-110">If a procedure uses an implicit handle for binding, the handle\_type<1> field of the procedure's description contains one of three valid nonzero values.</span></span> <span data-ttu-id="2a022-111">La prise en charge du compilateur MIDL pour les handles implicites se trouve dans le \_ \_ champ informations de handle implicite de la structure du descripteur stub :</span><span class="sxs-lookup"><span data-stu-id="2a022-111">MIDL compiler support for implicit handles is found in the IMPLICIT\_HANDLE\_INFO field of the Stub Descriptor structure:</span></span>

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

<span data-ttu-id="2a022-112">Si la procédure utilise un descripteur automatique, le membre **pAutoHandle** contient l’adresse de la variable de handle stub définie-auto.</span><span class="sxs-lookup"><span data-stu-id="2a022-112">If the procedure uses an auto handle, the **pAutoHandle** member contains the address of the stub defined–auto handle variable.</span></span>

<span data-ttu-id="2a022-113">Si la procédure utilise un handle primitif implicite, le membre **pPrimitiveHandle** contient l’adresse de la variable de handle stub définie-primitive.</span><span class="sxs-lookup"><span data-stu-id="2a022-113">If the procedure uses an implicit primitive handle, the **pPrimitiveHandle** member contains the address of the stub defined–primitive handle variable.</span></span>

<span data-ttu-id="2a022-114">Enfin, si la procédure utilise un handle générique implicite, le membre **pGenericBindingInfo** contient l’adresse du pointeur vers la structure **d' \_ \_ informations de liaison générique** correspondante.</span><span class="sxs-lookup"><span data-stu-id="2a022-114">Finally, if the procedure uses an implicit generic handle, the **pGenericBindingInfo** member holds the address of the pointer to the corresponding **GENERIC\_BINDING\_INFO** structure.</span></span> <span data-ttu-id="2a022-115">La **\_ \_ Description du stub MIDL** de la structure de données contient un pointeur vers une collection de structures de **\_ \_ paires de liaisons génériques** .</span><span class="sxs-lookup"><span data-stu-id="2a022-115">The data structure **MIDL\_STUB\_DESC** contains a pointer to a collection of **GENERIC\_BINDING\_PAIR** structures.</span></span> <span data-ttu-id="2a022-116">L’entrée dans la position zéro de cette collection est réservée aux routines de **liaison et de** **séparation** correspondant au handle de liaison générique référencé par **pGenericBindingInfo** dans les **\_ \_ informations de handle implicites**.</span><span class="sxs-lookup"><span data-stu-id="2a022-116">The entry in the zero position of this collection is reserved for the **bind** and **unbind** routines corresponding to the generic binding handle referenced by **pGenericBindingInfo** in **IMPLICIT\_HANDLE\_INFO**.</span></span> <span data-ttu-id="2a022-117">Le type de handle de liaison implicite est indiqué dans la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="2a022-117">The type of implicit binding handle is indicated in the format string.</span></span>

## <a name="explicit-handles"></a><span data-ttu-id="2a022-118">Handles explicites</span><span class="sxs-lookup"><span data-stu-id="2a022-118">Explicit Handles</span></span>

<span data-ttu-id="2a022-119">Il existe trois types de handle explicites possibles : Context, Generic et primitive.</span><span class="sxs-lookup"><span data-stu-id="2a022-119">There are three possible explicit handle types: context, generic, and primitive.</span></span> <span data-ttu-id="2a022-120">Dans le cas d’un handle explicite (ou d’un \[  \] handle de contexte out uniquement, qui est géré de la même façon), les informations de handle de liaison s’affichent sous la forme de l’un des paramètres de la procédure.</span><span class="sxs-lookup"><span data-stu-id="2a022-120">In the case of an explicit handle (or an \[**out**\] only context handle, which is handled in the same way), the binding handle information appears as one of the procedure's parameters.</span></span> <span data-ttu-id="2a022-121">Les trois descriptions possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="2a022-121">The three possible descriptions are as follows.</span></span>

<span data-ttu-id="2a022-122">Primitives</span><span class="sxs-lookup"><span data-stu-id="2a022-122">Primitive</span></span>

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

<span data-ttu-id="2a022-123">L’indicateur<1> indique si le handle est passé par un pointeur.</span><span class="sxs-lookup"><span data-stu-id="2a022-123">The flag<1> indicates whether the handle is passed by a pointer.</span></span>

<span data-ttu-id="2a022-124">Le décalage<2> fournit le décalage à partir du début de la pile jusqu’au handle primitif.</span><span class="sxs-lookup"><span data-stu-id="2a022-124">The offset<2> provides the offset from the beginning of the stack to the primitive handle.</span></span>

> [!Note]  
> <span data-ttu-id="2a022-125">Une description de handle primitif dans la chaîne de format de type est réduite à une seule valeur FC \_ ignorée.</span><span class="sxs-lookup"><span data-stu-id="2a022-125">A primitive handle description in the type format string is reduced to a single FC\_IGNORE.</span></span>

 

<span data-ttu-id="2a022-126">Générique</span><span class="sxs-lookup"><span data-stu-id="2a022-126">Generic</span></span>

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

<span data-ttu-id="2a022-127">L’indicateur \_ et la \_ taille<1> ont le grignot d’indicateur supérieur et le Quartet de la taille inférieure.</span><span class="sxs-lookup"><span data-stu-id="2a022-127">The flag\_and \_size<1> has the upper flag nibble and the lower size nibble.</span></span> <span data-ttu-id="2a022-128">L’indicateur indique si le handle est passé par un pointeur.</span><span class="sxs-lookup"><span data-stu-id="2a022-128">The flag indicates whether the handle is passed by a pointer.</span></span> <span data-ttu-id="2a022-129">Le champ Taille fournit la taille du type de handle générique défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2a022-129">The size field provides the size of the user defined–generic handle type.</span></span> <span data-ttu-id="2a022-130">Cette taille est limitée à 1, 2 ou 4 octets sur les systèmes 32 bits et 1, 2, 4 ou 8 octets sur les systèmes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2a022-130">This size is limited to be 1, 2 or 4 bytes on 32-bit systems and 1, 2, 4 or 8 bytes on 64-bit systems.</span></span>

<span data-ttu-id="2a022-131">Le champ décalage<2> fournit le décalage à partir du début de la pile du pointeur vers les données de la taille donnée.</span><span class="sxs-lookup"><span data-stu-id="2a022-131">The offset<2> field provides the offset from the beginning of the stack of the pointer to the data of the size given.</span></span>

<span data-ttu-id="2a022-132">L' \_ \_ index de paire de routines de liaison \_<1> champ donne l’index dans le champ AGenericBindingRoutinePairs du descripteur stub aux pointeurs de fonction de **liaison** et de **détachement** de la fonction de routine pour le handle générique.</span><span class="sxs-lookup"><span data-stu-id="2a022-132">The binding\_routine\_pair\_index<1> field gives the index into the aGenericBindingRoutinePairs field of the Stub Descriptor to the **bind** and **unbind** routine function pointers for the generic handle.</span></span>

> [!Note]  
> <span data-ttu-id="2a022-133">Une description de handle générique dans le format de type est la description du type de données associé uniquement.</span><span class="sxs-lookup"><span data-stu-id="2a022-133">A generic handle description in the type format is the description of the related data type only.</span></span>

 

<span data-ttu-id="2a022-134">Context</span><span class="sxs-lookup"><span data-stu-id="2a022-134">Context</span></span>

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

<span data-ttu-id="2a022-135">Les indicateurs<1> indiquent comment le descripteur est passé et le type.</span><span class="sxs-lookup"><span data-stu-id="2a022-135">The flags<1> indicate how the handle is passed and what type it is.</span></span> <span data-ttu-id="2a022-136">Les indicateurs valides sont indiqués dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2a022-136">Valid flags are shown in the following table.</span></span>



| <span data-ttu-id="2a022-137">Hex</span><span class="sxs-lookup"><span data-stu-id="2a022-137">Hex</span></span> | <span data-ttu-id="2a022-138">Indicateur</span><span class="sxs-lookup"><span data-stu-id="2a022-138">Flag</span></span>                                   |
|-----|----------------------------------------|
| <span data-ttu-id="2a022-139">80</span><span class="sxs-lookup"><span data-stu-id="2a022-139">80</span></span>  | <span data-ttu-id="2a022-140">le \_ paramètre handle \_ est \_ via \_ ptr</span><span class="sxs-lookup"><span data-stu-id="2a022-140">HANDLE\_PARAM\_IS\_VIA\_PTR</span></span>            |
| <span data-ttu-id="2a022-141">40</span><span class="sxs-lookup"><span data-stu-id="2a022-141">40</span></span>  | <span data-ttu-id="2a022-142">le \_ paramètre \_ du handle est \_ in</span><span class="sxs-lookup"><span data-stu-id="2a022-142">HANDLE\_PARAM\_IS\_IN</span></span>                  |
| <span data-ttu-id="2a022-143">20</span><span class="sxs-lookup"><span data-stu-id="2a022-143">20</span></span>  | <span data-ttu-id="2a022-144">le \_ paramètre de handle \_ est \_ out</span><span class="sxs-lookup"><span data-stu-id="2a022-144">HANDLE\_PARAM\_IS\_OUT</span></span>                 |
| <span data-ttu-id="2a022-145">21</span><span class="sxs-lookup"><span data-stu-id="2a022-145">21</span></span>  | <span data-ttu-id="2a022-146">le \_ paramètre handle \_ est \_ retourné</span><span class="sxs-lookup"><span data-stu-id="2a022-146">HANDLE\_PARAM\_IS\_RETURN</span></span>              |
| <span data-ttu-id="2a022-147">08</span><span class="sxs-lookup"><span data-stu-id="2a022-147">08</span></span>  | <span data-ttu-id="2a022-148">\_handle de \_ contexte \_ strict NDR</span><span class="sxs-lookup"><span data-stu-id="2a022-148">NDR\_STRICT\_CONTEXT\_HANDLE</span></span>           |
| <span data-ttu-id="2a022-149">04</span><span class="sxs-lookup"><span data-stu-id="2a022-149">04</span></span>  | <span data-ttu-id="2a022-150">descripteur de contexte de NDR \_ \_ \_ non \_ Serialize</span><span class="sxs-lookup"><span data-stu-id="2a022-150">NDR\_CONTEXT\_HANDLE\_NO\_SERIALIZE</span></span>    |
| <span data-ttu-id="2a022-151">02</span><span class="sxs-lookup"><span data-stu-id="2a022-151">02</span></span>  | <span data-ttu-id="2a022-152">désérialisation du \_ handle de contexte NDR \_ \_</span><span class="sxs-lookup"><span data-stu-id="2a022-152">NDR\_CONTEXT\_HANDLE\_SERIALIZE</span></span>        |
| <span data-ttu-id="2a022-153">01</span><span class="sxs-lookup"><span data-stu-id="2a022-153">01</span></span>  | <span data-ttu-id="2a022-154">le \_ \_ descripteur de contexte NDR \_ ne peut pas \_ être \_ null</span><span class="sxs-lookup"><span data-stu-id="2a022-154">NDR\_CONTEXT\_HANDLE\_CANNOT\_BE\_NULL</span></span> |



 

<span data-ttu-id="2a022-155">Les quatre premiers indicateurs ont toujours été présents, les quatre derniers ont été ajoutés dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2a022-155">The first four flags have always been present, the last four were added in Windows 2000.</span></span>

<span data-ttu-id="2a022-156">Le champ décalage<2> fournit le décalage à partir du début de la pile jusqu’au handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="2a022-156">The offset<2> field provides the offset from the start of the stack to the context handle.</span></span>

<span data-ttu-id="2a022-157">L' \_ \_ \_ index de routine d’arrêt de contexte<1> fournit un index dans le champ **apfnNdrRundownRoutines** du descripteur stub à la routine d’arrêt utilisée pour ce handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="2a022-157">The context\_rundown\_routine\_index<1> provides an index into the **apfnNdrRundownRoutines** field of the Stub Descriptor to the rundown routine used for this context handle.</span></span> <span data-ttu-id="2a022-158">Le compilateur génère toujours un index.</span><span class="sxs-lookup"><span data-stu-id="2a022-158">The compiler always generates an index.</span></span> <span data-ttu-id="2a022-159">Pour les routines qui n’ont pas de routine d’arrêt, il s’agit d’un index d’une position de table qui contient la valeur null.</span><span class="sxs-lookup"><span data-stu-id="2a022-159">For routines that do not have a rundown routine, this is an index to a table position that holds null.</span></span>

<span data-ttu-id="2a022-160">Pour les stubs intégrés à **– Oi2**, le paramètre param \_ num<1> fournit le nombre ordinal, en commençant à zéro, en spécifiant le handle de contexte dans la procédure donnée.</span><span class="sxs-lookup"><span data-stu-id="2a022-160">For stubs built in **–Oi2**, the param\_num<1> provides the ordinal count, starting at zero, specifying which context handle it is in the given procedure.</span></span>

<span data-ttu-id="2a022-161">Pour les versions précédentes de l’interpréteur, le \_ paramètre param num<1> fournit le numéro de paramètre du descripteur de contexte, à partir de zéro, dans sa procédure.</span><span class="sxs-lookup"><span data-stu-id="2a022-161">For previous versions of the interpreter, the param\_num<1> provides the context handle's parameter number, starting at zero, in its procedure.</span></span>

> [!Note]  
> <span data-ttu-id="2a022-162">Une description de handle de contexte dans la chaîne de format de type n’a pas le décalage<2> dans la description.</span><span class="sxs-lookup"><span data-stu-id="2a022-162">A context handle description in the type format string will not have the offset<2> in the description.</span></span>

 

## <a name="the-new-oif-header"></a><span data-ttu-id="2a022-163">Nouvel en-tête de l’interfaces de création</span><span class="sxs-lookup"><span data-stu-id="2a022-163">The New –Oif Header</span></span>

<span data-ttu-id="2a022-164">Comme mentionné précédemment, l’en-tête [**–**](/windows/desktop/Midl/-oi) de l’extension de la fonction se développe sur l’en-tête **– OI** .</span><span class="sxs-lookup"><span data-stu-id="2a022-164">As mentioned previously, the [**–Oif**](/windows/desktop/Midl/-oi) header expands on the **–Oi** header.</span></span> <span data-ttu-id="2a022-165">Pour plus de commodité, tous les champs sont affichés ici :</span><span class="sxs-lookup"><span data-stu-id="2a022-165">For convenience, all fields are shown here:</span></span>

<span data-ttu-id="2a022-166">(L’ancien en-tête)</span><span class="sxs-lookup"><span data-stu-id="2a022-166">(The old header)</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="2a022-167">(Les extensions de-l’extension de l' [**interfaces**](/windows/desktop/Midl/-oi) )</span><span class="sxs-lookup"><span data-stu-id="2a022-167">(The [**–Oif**](/windows/desktop/Midl/-oi) extensions)</span></span>

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

<span data-ttu-id="2a022-168">La \_ \_ taille de la mémoire tampon du client constante \_<2> fournit la taille de la mémoire tampon de marshaling qui aurait pu être précalculée par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="2a022-168">The constant\_client\_buffer\_size<2> provides the size of the marshaling buffer that could have been pre-computed by the compiler.</span></span> <span data-ttu-id="2a022-169">Il peut s’agir d’une taille partielle, car l’indicateur ClientMustSize déclenche le dimensionnement.</span><span class="sxs-lookup"><span data-stu-id="2a022-169">This may be only a partial size, as the ClientMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="2a022-170">La \_ \_ taille de la mémoire tampon du serveur constante \_<2> fournit la taille de la mémoire tampon de marshaling telle qu’elle est précalculée par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="2a022-170">The constant\_server\_buffer\_size<2> provides the size of the marshaling buffer as precomputed by the compiler.</span></span> <span data-ttu-id="2a022-171">Il peut s’agir d’une taille partielle, car l’indicateur ServerMustSize déclenche le dimensionnement.</span><span class="sxs-lookup"><span data-stu-id="2a022-171">This may be only a partial size, as the ServerMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="2a022-172">Les indicateurs de l’INTERPRÉTeur \_ OPT \_ sont définis dans Ndrtypes. h :</span><span class="sxs-lookup"><span data-stu-id="2a022-172">The INTERPRETER\_OPT\_FLAGS are defined in Ndrtypes.h:</span></span>

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   <span data-ttu-id="2a022-173">Le bit ServerMustSize est défini si le serveur doit effectuer une passe de dimensionnement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2a022-173">The ServerMustSize bit is set if the server needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="2a022-174">Le bit ClientMustSize est défini si le client doit effectuer une passe de dimensionnement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2a022-174">The ClientMustSize bit is set if the client needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="2a022-175">Le bit HasReturn est défini si la procédure a une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="2a022-175">The HasReturn bit is set if the procedure has a return value.</span></span>
-   <span data-ttu-id="2a022-176">Le bit HasPipes est défini si le package de canal doit être utilisé pour prendre en charge un argument de canal.</span><span class="sxs-lookup"><span data-stu-id="2a022-176">The HasPipes bit is set if the pipe package needs to be used to support a pipe argument.</span></span>
-   <span data-ttu-id="2a022-177">Le bit HasAsyncUuid est défini si la procédure est une procédure DCOM asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2a022-177">The HasAsyncUuid bit is set if the procedure is an asynchronous DCOM procedure.</span></span>
-   <span data-ttu-id="2a022-178">Le bit HasExtensions indique que les extensions Windows 2000 et versions ultérieures sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="2a022-178">The HasExtensions bit indicates that Windows 2000 and later extensions are used.</span></span>
-   <span data-ttu-id="2a022-179">Le bit HasAsyncHandle indique une procédure RPC asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2a022-179">The HasAsyncHandle bit indicates an asynchronous RPC procedure.</span></span>

<span data-ttu-id="2a022-180">Le bit HasAsyncHandle a été initialement utilisé pour une implémentation DCOM différente de la prise en charge de Async et n’a donc pas pu être utilisé pour la prise en charge actuelle du style asynchrone dans DCOM.</span><span class="sxs-lookup"><span data-stu-id="2a022-180">The HasAsyncHandle bit has been initially used for a different DCOM implementation of async support, and hence could not be used for the current style async support in DCOM.</span></span> <span data-ttu-id="2a022-181">Le bit HasAsyncUuid indique actuellement cela.</span><span class="sxs-lookup"><span data-stu-id="2a022-181">The HasAsyncUuid bit currently indicates this.</span></span>

 

 