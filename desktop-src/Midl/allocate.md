---
title: Allocate (attribut)
description: L’attribut \ Allocate \ ACF vous permet de personnaliser l’allocation et la désallocation de mémoire pour un type défini dans le fichier IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- MIDL de l’attribut Allocate
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841154"
---
# <a name="allocate-attribute"></a><span data-ttu-id="d842a-104">Allocate (attribut)</span><span class="sxs-lookup"><span data-stu-id="d842a-104">allocate attribute</span></span>

<span data-ttu-id="d842a-105">L’attribut **\[ allocate \]** ACF vous permet de personnaliser l’allocation et la désallocation de mémoire pour un type défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d842a-105">The **\[allocate\]** ACF attribute lets you customize memory allocation and deallocation for a type defined in the IDL file.</span></span>

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="d842a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d842a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d842a-107">*allocate-option-list*</span><span class="sxs-lookup"><span data-stu-id="d842a-107">*allocate-option-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d842a-108">Spécifie une ou plusieurs options d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d842a-108">Specifies one or more memory-allocation options.</span></span> <span data-ttu-id="d842a-109">Sélectionnez l’un des nœuds **uniques \_** ou **tous les \_ nœuds**, ou l’un des deux, **gratuit** ou non, ou un de chaque paire. **\_**</span><span class="sxs-lookup"><span data-stu-id="d842a-109">Select one of either **single\_node** or **all\_nodes**, or one of either **free** or **dont\_free**, or one from each pair.</span></span> <span data-ttu-id="d842a-110">Lorsque vous spécifiez plusieurs options, séparez-les par des virgules.</span><span class="sxs-lookup"><span data-stu-id="d842a-110">When you specify more than one option, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d842a-111">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="d842a-111">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d842a-112">Spécifie d’autres attributs CCP-type facultatifs.</span><span class="sxs-lookup"><span data-stu-id="d842a-112">Specifies other optional ACF-type attributes.</span></span> <span data-ttu-id="d842a-113">Lorsque vous spécifiez plusieurs attributs de type, séparez les options par des virgules.</span><span class="sxs-lookup"><span data-stu-id="d842a-113">When you specify more than one type attribute, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d842a-114">*nom du type*</span><span class="sxs-lookup"><span data-stu-id="d842a-114">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d842a-115">Spécifie un type défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d842a-115">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d842a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d842a-116">Remarks</span></span>

<span data-ttu-id="d842a-117">L’attribut **\[ allocate \]** a les options valides suivantes.</span><span class="sxs-lookup"><span data-stu-id="d842a-117">The **\[allocate\]** attribute has the following valid options.</span></span>



| <span data-ttu-id="d842a-118">Option</span><span class="sxs-lookup"><span data-stu-id="d842a-118">Option</span></span>           | <span data-ttu-id="d842a-119">Description</span><span class="sxs-lookup"><span data-stu-id="d842a-119">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d842a-120">**tous les \_ nœuds**</span><span class="sxs-lookup"><span data-stu-id="d842a-120">**all\_nodes**</span></span>   | <span data-ttu-id="d842a-121">Effectue un appel pour allouer et libérer de la mémoire pour tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="d842a-121">Makes one call to allocate and free memory for all nodes.</span></span>             |
| <span data-ttu-id="d842a-122">**\_nœud unique**</span><span class="sxs-lookup"><span data-stu-id="d842a-122">**single\_node**</span></span> | <span data-ttu-id="d842a-123">Effectue de nombreux appels individuels pour allouer et libérer chaque nœud de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d842a-123">Makes many individual calls to allocate and free each node of memory.</span></span> |
| <span data-ttu-id="d842a-124">**free**</span><span class="sxs-lookup"><span data-stu-id="d842a-124">**free**</span></span>         | <span data-ttu-id="d842a-125">Libère de la mémoire au retour du stub serveur.</span><span class="sxs-lookup"><span data-stu-id="d842a-125">Frees memory on return from the server stub.</span></span>                          |
| <span data-ttu-id="d842a-126">**ne pas \_ libérer**</span><span class="sxs-lookup"><span data-stu-id="d842a-126">**dont\_free**</span></span>   | <span data-ttu-id="d842a-127">Ne libère pas de mémoire au retour du stub serveur.</span><span class="sxs-lookup"><span data-stu-id="d842a-127">Does not free memory on return from the server stub.</span></span>                  |



 

<span data-ttu-id="d842a-128">Par défaut, les stubs peuvent allouer du stockage pour les données référencées par un pointeur unique ou complet en appelant [**MIDL \_ User \_ allocate**](midl-user-allocate-1.md) et [**MIDL \_ User \_ Free**](midl-user-free-1.md) individuellement pour chaque pointeur.</span><span class="sxs-lookup"><span data-stu-id="d842a-128">By default, the stubs may allocate storage for data referenced by a unique or full pointer by calling [**midl\_user\_allocate**](midl-user-allocate-1.md) and [**midl\_user\_free**](midl-user-free-1.md) individually for each pointer.</span></span>

<span data-ttu-id="d842a-129">Vous pouvez optimiser la vitesse de votre application en spécifiant l’option **tous les \_ nœuds**.</span><span class="sxs-lookup"><span data-stu-id="d842a-129">You can optimize the speed of your application by specifying the option **all\_nodes**.</span></span> <span data-ttu-id="d842a-130">Cette option indique au stub de calculer la taille de la mémoire référencée par le pointeur du type spécifié et d’effectuer un appel unique à l' [**\_ \_ allocation d’utilisateur MIDL**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="d842a-130">This option directs the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span> <span data-ttu-id="d842a-131">Le stub libère la mémoire en effectuant un appel à l' [**\_ utilisateur MIDL \_ gratuit**](midl-user-free-1.md).</span><span class="sxs-lookup"><span data-stu-id="d842a-131">The stub releases the memory by making one call to [**midl\_user\_free**](midl-user-free-1.md).</span></span>

<span data-ttu-id="d842a-132">L’option **ne pas \_ libérer** indique au compilateur MIDL de générer un stub de serveur qui n’appelle pas l' [**\_ utilisateur MIDL \_ gratuit**](midl-user-free-1.md) pour le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="d842a-132">The **dont\_free** option directs the MIDL compiler to generate a server stub that does not call [**midl\_user\_free**](midl-user-free-1.md) for the specified type.</span></span> <span data-ttu-id="d842a-133">L’option **ne pas \_ libérer** permet aux structures de pointeur de rester accessibles à l’application serveur une fois que l’appel de procédure distante est terminé et retourné au client.</span><span class="sxs-lookup"><span data-stu-id="d842a-133">The **dont\_free** option allows the pointer structures to remain accessible to the server application after the remote procedure call has completed and returned to the client.</span></span>

<span data-ttu-id="d842a-134">L’attribut **\[ allocate \]** entraîne un paramètre **\[ in \] , out** qui est un pointeur vers un type qualifié avec l’option **All \_ Nodes** pour réallouer de la mémoire lorsque les données sont démarshalées.</span><span class="sxs-lookup"><span data-stu-id="d842a-134">The **\[allocate\]** attribute will cause any **\[in, out\]** parameter that is a pointer to a type qualified with the **all\_nodes** option to reallocate memory when the data is unmarshaled.</span></span> <span data-ttu-id="d842a-135">Il est de la responsabilité de l’application de libérer la mémoire allouée précédemment pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="d842a-135">It is the responsibility of the application to free the memory allocated previously for this parameter.</span></span> <span data-ttu-id="d842a-136">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d842a-136">For example:</span></span>

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

<span data-ttu-id="d842a-137">Le type de données PTHISTYPE sera réalloué dans le sens de [**\[ sortie \]**](out-idl.md) par le stub avant d’être démarshalé.</span><span class="sxs-lookup"><span data-stu-id="d842a-137">The data type PTHISTYPE will be reallocated in the [**\[out\]**](out-idl.md) direction by the stub before unmarshaling.</span></span> <span data-ttu-id="d842a-138">Par conséquent, l’application doit libérer la mémoire qu’elle avait allouée précédemment pour les données de ce paramètre, ou une fuite de mémoire se produira.</span><span class="sxs-lookup"><span data-stu-id="d842a-138">Therefore, the application must free the memory it previously allocated for this parameter's data, or a memory leak will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="d842a-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="d842a-139">Examples</span></span>

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a><span data-ttu-id="d842a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d842a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d842a-141">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="d842a-141">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d842a-142">**in**</span><span class="sxs-lookup"><span data-stu-id="d842a-142">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="d842a-143">**allouer un \_ utilisateur MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="d842a-143">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="d842a-144">**\_utilisateur \_ gratuit MIDL**</span><span class="sxs-lookup"><span data-stu-id="d842a-144">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="d842a-145">**à**</span><span class="sxs-lookup"><span data-stu-id="d842a-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="d842a-146">**typedef**</span><span class="sxs-lookup"><span data-stu-id="d842a-146">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




