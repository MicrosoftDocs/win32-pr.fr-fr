---
title: attribut byte_count
description: L’attribut \ \_ CCP Count \ ACF est un attribut de paramètre qui associe une taille, en octets, à la zone de mémoire indiquée par le pointeur.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count MIDL de l’attribut
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312850"
---
# <a name="byte_count-attribute"></a><span data-ttu-id="d308d-104">attribut de nombre d’octets \_</span><span class="sxs-lookup"><span data-stu-id="d308d-104">byte\_count attribute</span></span>

<span data-ttu-id="d308d-105">L’attribut ACF de **\[ \_ nombre \] d’octets** est un attribut de paramètre qui associe une taille, en octets, à la zone de mémoire indiquée par le pointeur.</span><span class="sxs-lookup"><span data-stu-id="d308d-105">The **\[byte\_count\]** ACF attribute is a parameter attribute that associates a size, in bytes, with the memory area indicated by the pointer.</span></span>

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a><span data-ttu-id="d308d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d308d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d308d-107">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d308d-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d308d-108">Spécifie zéro, un ou plusieurs attributs de fonction ACF.</span><span class="sxs-lookup"><span data-stu-id="d308d-108">Specifies zero or more ACF function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="d308d-109">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="d308d-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d308d-110">Spécifie le nom de la fonction définie dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d308d-110">Specifies the name of the function defined in the IDL file.</span></span> <span data-ttu-id="d308d-111">Le nom de la fonction est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d308d-111">The function name is required.</span></span>

</dd> <dt>

<span data-ttu-id="d308d-112">*Length-variable-name*</span><span class="sxs-lookup"><span data-stu-id="d308d-112">*length-variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d308d-113">Spécifie le nom du paramètre [**\[ en \]**](in.md)uniquement qui spécifie la taille, en octets, de la zone mémoire référencée par le *paramètre-Name*.</span><span class="sxs-lookup"><span data-stu-id="d308d-113">Specifies the name of the [**\[in\]**](in.md)-only parameter that specifies the size, in bytes, of the memory area referenced by *parameter-name*.</span></span>

</dd> <dt>

<span data-ttu-id="d308d-114">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="d308d-114">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d308d-115">Spécifie le nom du paramètre de pointeur en [**\[ sortie \]**](out-idl.md)seule défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d308d-115">Specifies the name of the [**\[out\]**](out-idl.md)-only pointer parameter defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d308d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d308d-116">Remarks</span></span>

<span data-ttu-id="d308d-117">Le **\[ \_ nombre \] d’octets** de l’attribut ACF représente une extension Microsoft de l’IDL DCE.</span><span class="sxs-lookup"><span data-stu-id="d308d-117">The ACF attribute **\[byte\_count\]** represents a Microsoft extension to DCE IDL.</span></span> <span data-ttu-id="d308d-118">Par conséquent, cet attribut n’est pas disponible lorsque vous utilisez le commutateur du compilateur MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="d308d-118">Therefore, this attribute is not available when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

> [!Note]  
> <span data-ttu-id="d308d-119">L’attribut **\[ nombre \] d’octets** n’est plus pris en charge dans la syntaxe NDR64 en raison de la difficulté à estimer la taille requise pour tous les paramètres de [**\[ sortie \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="d308d-119">The **\[byte count\]** attribute is no longer supported in NDR64 syntax due to the difficulty in estimating the size required for all [**\[out\]**](out-idl.md) parameters.</span></span>

 

<span data-ttu-id="d308d-120">La mémoire référencée par le paramètre de pointeur est contiguë et n’est pas allouée ou libérée par les stubs client.</span><span class="sxs-lookup"><span data-stu-id="d308d-120">Memory referenced by the pointer parameter is contiguous and is not allocated or freed by the client stubs.</span></span> <span data-ttu-id="d308d-121">Cette fonctionnalité de l’attribut **\[ \_ nombre \] d’octets** vous permet de créer une zone de mémoire tampon persistante dans la mémoire du client qui peut être réutilisée lors de plusieurs appels à la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="d308d-121">This feature of the **\[byte\_count\]** attribute lets you create a persistent buffer area in client memory that can be reused during more than one call to the remote procedure.</span></span>

<span data-ttu-id="d308d-122">La possibilité de désactiver l’allocation de mémoire stub du client vous permet de régler l’efficacité de l’application.</span><span class="sxs-lookup"><span data-stu-id="d308d-122">The ability to turn off the client stub memory allocation lets you tune the application for efficiency.</span></span> <span data-ttu-id="d308d-123">Par exemple, l’attribut **\[ \_ nombre \] d’octets** peut être utilisé par les fonctions de fournisseur de service qui utilisent Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="d308d-123">For example, the **\[byte\_count\]** attribute can be used by service-provider functions that use Microsoft RPC.</span></span> <span data-ttu-id="d308d-124">Lorsqu’une application utilisateur appelle l’API du fournisseur de services et envoie un pointeur vers une mémoire tampon, le fournisseur de services peut passer le pointeur de la mémoire tampon à la fonction distante.</span><span class="sxs-lookup"><span data-stu-id="d308d-124">When a user application calls the service-provider API and sends a pointer to a buffer, the service provider can pass the buffer pointer on to the remote function.</span></span> <span data-ttu-id="d308d-125">Le fournisseur de services peut réutiliser la mémoire tampon pendant plusieurs appels distants sans forcer l’utilisateur à réallouer la zone mémoire.</span><span class="sxs-lookup"><span data-stu-id="d308d-125">The service provider can reuse the buffer during multiple remote calls without forcing the user to reallocate the memory area.</span></span>

<span data-ttu-id="d308d-126">La zone mémoire peut contenir des structures de données complexes qui se composent de plusieurs pointeurs.</span><span class="sxs-lookup"><span data-stu-id="d308d-126">The memory area can contain complex data structures that consist of multiple pointers.</span></span> <span data-ttu-id="d308d-127">Étant donné que la zone mémoire est contiguë, l’application n’a pas besoin d’effectuer plusieurs appels pour libérer individuellement chaque pointeur et structure.</span><span class="sxs-lookup"><span data-stu-id="d308d-127">Because the memory area is contiguous, the application does not have to make several calls to individually free each pointer and structure.</span></span> <span data-ttu-id="d308d-128">Au lieu de cela, il peut allouer ou libérer la zone mémoire avec un appel à l’allocation de mémoire ou à la routine libre.</span><span class="sxs-lookup"><span data-stu-id="d308d-128">Instead, it can allocate or free the memory area with one call to the memory allocation or free routine.</span></span>

<span data-ttu-id="d308d-129">La mémoire tampon doit être un paramètre en [**\[ sortie \]**](out-idl.md)seule, tandis que la longueur de la mémoire tampon en octets doit être un paramètre [**\[ en \]**](in.md)uniquement.</span><span class="sxs-lookup"><span data-stu-id="d308d-129">The buffer must be an [**\[out\]**](out-idl.md)-only parameter, while the buffer length in bytes must be an [**\[in\]**](in.md)-only parameter.</span></span>

<span data-ttu-id="d308d-130">Spécifiez une mémoire tampon suffisamment grande pour contenir tous les paramètres de [**\[ sortie \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="d308d-130">Specify a buffer that is large enough to contain all the [**\[out\]**](out-idl.md) parameters.</span></span> <span data-ttu-id="d308d-131">En raison du remplissage masqué, utilisez des surestimations plutôt que des nombres exacts.</span><span class="sxs-lookup"><span data-stu-id="d308d-131">Because of hidden padding, use overestimates rather than exact counts.</span></span> <span data-ttu-id="d308d-132">Par exemple, les pointeurs de 4 octets sont démarshalés sur une limite alignée sur 4 octets sur les plateformes 32 bits et les pointeurs de 8 octets sur une limite de 8 octets sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d308d-132">For example, 4-byte pointers are unmarshaled on a 4-byte aligned boundary on 32-bit platforms and 8-byte pointers on an 8-byte boundary on 64-bit platforms.</span></span> <span data-ttu-id="d308d-133">Par conséquent, le remplissage de l’alignement effectué par les stubs doit être comptabilisé dans l’espace de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d308d-133">Therefore, the alignment padding the stubs will perform must be accounted for in the space for the buffer.</span></span> <span data-ttu-id="d308d-134">En outre, les niveaux de compression utilisés pendant la compilation en langage C peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="d308d-134">In addition, packing levels used during C-language compilation can vary.</span></span> <span data-ttu-id="d308d-135">Utilisez une valeur de nombre d’octets qui tient compte des octets de compression supplémentaires ajoutés au niveau de compactage utilisé lors de la compilation en langage C.</span><span class="sxs-lookup"><span data-stu-id="d308d-135">Use a byte count value that accounts for additional packing bytes added for the packing level used during C-language compilation.</span></span> <span data-ttu-id="d308d-136">Une pratique sûre qui couvre à la fois les plateformes 32 bits et les plateformes 64 bits consiste à supposer que chaque objet entrant dans le bloc Big Memory commence à une adresse qui est un multiple de 8.</span><span class="sxs-lookup"><span data-stu-id="d308d-136">A safe practice that covers both 32 bit platforms and 64 bit platforms is to assume that each object going into the big memory block starts at an address that is a multiple of 8.</span></span>

## <a name="examples"></a><span data-ttu-id="d308d-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="d308d-137">Examples</span></span>

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a><span data-ttu-id="d308d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d308d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d308d-139">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="d308d-139">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d308d-140">**in**</span><span class="sxs-lookup"><span data-stu-id="d308d-140">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="d308d-141">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="d308d-141">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="d308d-142">**/osf**</span><span class="sxs-lookup"><span data-stu-id="d308d-142">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="d308d-143">**à**</span><span class="sxs-lookup"><span data-stu-id="d308d-143">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="d308d-144">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="d308d-144">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 




