---
title: call_as (attribut)
description: L’attribut \ Call \_ As \ vous permet de mapper une fonction qui ne peut pas être appelée à distance à une fonction distante.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as MIDL de l’attribut
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106512077"
---
# <a name="call_as-attribute"></a><span data-ttu-id="e92bd-104">appeler \_ en tant qu’attribut</span><span class="sxs-lookup"><span data-stu-id="e92bd-104">call\_as attribute</span></span>

<span data-ttu-id="e92bd-105">L' **\[ appel \_ en \] tant qu'** attribut vous permet de mapper une fonction qui ne peut pas être appelée à distance à une fonction distante.</span><span class="sxs-lookup"><span data-stu-id="e92bd-105">The **\[call\_as\]** attribute enables you to map a function that cannot be called remotely to a remote function.</span></span>

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a><span data-ttu-id="e92bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e92bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e92bd-107">*local-proc*</span><span class="sxs-lookup"><span data-stu-id="e92bd-107">*local-proc*</span></span> 
</dt> <dd>

<span data-ttu-id="e92bd-108">Spécifie une routine définie par l’opération.</span><span class="sxs-lookup"><span data-stu-id="e92bd-108">Specifies an operation-defined routine.</span></span>

</dd> <dt>

<span data-ttu-id="e92bd-109">*Operation-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e92bd-109">*operation-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e92bd-110">Spécifie un ou plusieurs attributs qui s’appliquent à l’opération.</span><span class="sxs-lookup"><span data-stu-id="e92bd-110">Specifies one or more attributes that apply to the operation.</span></span> <span data-ttu-id="e92bd-111">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="e92bd-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e92bd-112">*Operation-name*</span><span class="sxs-lookup"><span data-stu-id="e92bd-112">*operation-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e92bd-113">Spécifie l’opération nommée présentée à l’application.</span><span class="sxs-lookup"><span data-stu-id="e92bd-113">Specifies the named operation presented to the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e92bd-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e92bd-114">Remarks</span></span>

<span data-ttu-id="e92bd-115">La possibilité de mapper une fonction qui ne peut pas être appelée à distance à une fonction distante est particulièrement utile dans les interfaces qui ont de nombreux types de paramètres qui ne peuvent pas être transmis sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="e92bd-115">The ability to map a function that cannot be called remotely to a remote function is particularly helpful in interfaces that have numerous parameter types that cannot be transmitted across the network.</span></span> <span data-ttu-id="e92bd-116">Au lieu d’utiliser plusieurs types de **\[** [**représentation \_**](represent-as.md) comme **\]** et de **\[** [**transmission \_ en tant que**](transmit-as.md) **\]** types, vous pouvez combiner toutes les conversions à l’aide de routines **\[ Call \_ As \]** .</span><span class="sxs-lookup"><span data-stu-id="e92bd-116">Rather than using many **\[**[**represent\_as**](represent-as.md)**\]** and **\[**[**transmit\_as**](transmit-as.md)**\]** types, you can combine all the conversions using **\[call\_as\]** routines.</span></span> <span data-ttu-id="e92bd-117">Vous fournissez les deux **\[ appels \_ en tant que \]** routines (côté client et côté serveur) pour lier la routine entre les appels d’application et les appels distants.</span><span class="sxs-lookup"><span data-stu-id="e92bd-117">You supply the two **\[call\_as\]** routines (client side and server side) to bind the routine between the application calls and the remote calls.</span></span>

<span data-ttu-id="e92bd-118">L' **\[ appel \_ en \] tant qu'** attribut peut être utilisé pour les interfaces d’objet.</span><span class="sxs-lookup"><span data-stu-id="e92bd-118">The **\[call\_as\]** attribute can be used for object interfaces.</span></span> <span data-ttu-id="e92bd-119">Dans ce cas, la définition d’interface peut être utilisée pour les appels locaux et les appels distants, car l' **\[ appel \_ de la fonction \]** autorise une interface qui n’est pas accessible à distance pour être mappée en toute transparence à une interface distante.</span><span class="sxs-lookup"><span data-stu-id="e92bd-119">In this case, the interface definition can be used for local calls as well as remote calls because **\[call\_as\]** allows an interface that can't be accessed remotely to be transparently mapped to a remote interface.</span></span> <span data-ttu-id="e92bd-120">L' **\[ appel \_ en \] tant qu'** attribut ne peut pas être utilisé avec le mode [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="e92bd-120">The **\[call\_as\]** attribute cannot be used with [**/osf**](-osf.md) mode.</span></span>

<span data-ttu-id="e92bd-121">Par exemple, supposons que la routine **F1** dans l’interface d’objet **IFace** nécessite de nombreuses conversions entre les appels utilisateur et ce qui est réellement transmis.</span><span class="sxs-lookup"><span data-stu-id="e92bd-121">For example, assume that the routine **f1** in object interface **IFace** requires numerous conversions between the user calls and what is actually transmitted.</span></span> <span data-ttu-id="e92bd-122">Les exemples suivants décrivent les fichiers IDL et ACF pour l’interface **IFace**:</span><span class="sxs-lookup"><span data-stu-id="e92bd-122">The following examples describe the IDL and ACF files for interface **IFace**:</span></span>

<span data-ttu-id="e92bd-123">Dans le fichier IDL de l’interface **IFace**:</span><span class="sxs-lookup"><span data-stu-id="e92bd-123">In the IDL file for interface **IFace**:</span></span>

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

<span data-ttu-id="e92bd-124">Dans le ACF pour l’interface **IFace**:</span><span class="sxs-lookup"><span data-stu-id="e92bd-124">In the ACF for interface **IFace**:</span></span>

``` syntax
[call_as( f1 )] Remf1();
```

<span data-ttu-id="e92bd-125">Le fichier d’en-tête généré définit alors l’interface à l’aide de la définition de la **touche F1**, mais il fournit également des stubs pour **Remf1**.</span><span class="sxs-lookup"><span data-stu-id="e92bd-125">This causes the generated header file to define the interface using the definition of **f1**, yet it also provides stubs for **Remf1**.</span></span>

<span data-ttu-id="e92bd-126">Le compilateur MIDL génère le vtable suivant dans le fichier d’en-tête pour l’interface **IFace**:</span><span class="sxs-lookup"><span data-stu-id="e92bd-126">The MIDL compiler will generate the following Vtable in the header file for interface **IFace**:</span></span>

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

<span data-ttu-id="e92bd-127">Le proxy côté client a ensuite un proxy généré par MIDL standard pour **Remf1**, tandis que le stub côté serveur pour **Remf1** est le même que le stub généré par MIDL standard :</span><span class="sxs-lookup"><span data-stu-id="e92bd-127">The client-side proxy would then have a typical MIDL-generated proxy for **Remf1**, while the server side stub for **Remf1** would be the same as the typical MIDL-generated stub:</span></span>

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

<span data-ttu-id="e92bd-128">Ensuite, les deux **\[ appels \_ en \] tant que** routines de liaison (côté client et côté serveur) doivent être codés manuellement :</span><span class="sxs-lookup"><span data-stu-id="e92bd-128">Then, the two **\[call\_as\]** bond routines (client side and server side) must be manually coded:</span></span>

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

<span data-ttu-id="e92bd-129">Pour les interfaces d’objet, il s’agit des prototypes pour les routines de liaison.</span><span class="sxs-lookup"><span data-stu-id="e92bd-129">For object interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="e92bd-130">Côté client :</span><span class="sxs-lookup"><span data-stu-id="e92bd-130">For client side:</span></span>

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

<span data-ttu-id="e92bd-131">Côté serveur :</span><span class="sxs-lookup"><span data-stu-id="e92bd-131">For server side:</span></span>

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

<span data-ttu-id="e92bd-132">Pour les interfaces qui ne sont pas des objets, il s’agit des prototypes pour les routines de liaison.</span><span class="sxs-lookup"><span data-stu-id="e92bd-132">For nonobject interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="e92bd-133">Côté client :</span><span class="sxs-lookup"><span data-stu-id="e92bd-133">For client side:</span></span>

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

<span data-ttu-id="e92bd-134">Côté serveur :</span><span class="sxs-lookup"><span data-stu-id="e92bd-134">For server side:</span></span>

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a><span data-ttu-id="e92bd-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e92bd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e92bd-136">**/osf**</span><span class="sxs-lookup"><span data-stu-id="e92bd-136">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="e92bd-137">**représenter \_ comme**</span><span class="sxs-lookup"><span data-stu-id="e92bd-137">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="e92bd-138">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="e92bd-138">**transmit\_as**</span></span>](transmit-as.md)
</dt> </dl>

 

 




