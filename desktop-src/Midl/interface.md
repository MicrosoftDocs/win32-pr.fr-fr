---
title: interface (attribut)
description: Le mot clé interface spécifie le nom de l’interface. Le nom de l’interface doit être fourni à la fois dans le fichier IDL et dans le CCP.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- MIDL, attribut d’interface
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842157"
---
# <a name="interface-attribute"></a><span data-ttu-id="070c8-105">interface (attribut)</span><span class="sxs-lookup"><span data-stu-id="070c8-105">interface attribute</span></span>

<span data-ttu-id="070c8-106">Le mot clé **interface** spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="070c8-106">The **interface** keyword specifies the name of the interface.</span></span> <span data-ttu-id="070c8-107">Le nom de l’interface doit être fourni à la fois dans le fichier IDL et dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="070c8-107">The interface name must be provided in both the IDL file and the ACF.</span></span>

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a><span data-ttu-id="070c8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="070c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="070c8-109">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="070c8-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="070c8-110">Spécifie des attributs qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="070c8-110">Specifies attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="070c8-111">Les attributs d’interface valides pour un fichier IDL incluent le **\[** [**point de terminaison**](endpoint.md) **\]** , l' **\[** objet [**local**](local.md) **\]** , l' **\[** [**objet**](object.md) **\]** , le **\[** [**pointeur \_ par défaut**](pointer-default.md) **\]** , l' **\[** [**UUID**](uuid.md) **\]** et la **\[** [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="070c8-111">Valid interface attributes for an IDL file include **\[**[**endpoint**](endpoint.md)**\]**, **\[**[**local**](local.md)**\]**, **\[**[**object**](object.md)**\]**, **\[**[**pointer\_default**](pointer-default.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span> <span data-ttu-id="070c8-112">Les attributs d’interface valides pour un CCP incluent l' **\[** [**encodage**](encode.md) **\]** , le **\[** [**décodage**](decode.md) **\]** , le **\[** [**\_ handle automatique**](auto-handle.md) **\]** ou le **\[** [**\_ handle implicite**](implicit-handle.md) **\]** , ainsi que le **\[** [**code**](code.md) **\]** ou le **\[** [**nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="070c8-112">Valid interface attributes for an ACF include **\[**[**encode**](encode.md)**\]**, **\[**[**decode**](decode.md)**\]**, either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]**, and either **\[**[**code**](code.md)**\]** or **\[**[**nocode**](nocode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="070c8-113">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="070c8-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="070c8-114">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="070c8-114">Specifies the name of the interface.</span></span> <span data-ttu-id="070c8-115">Le nom de l’interface doit être un nom unique et doit commencer par un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="070c8-115">The interface name must be a unique name and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="070c8-116">*interface de base*</span><span class="sxs-lookup"><span data-stu-id="070c8-116">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="070c8-117">Spécifie le nom d’une interface à partir de laquelle cette interface dérivée hérite des fonctions membres, des codes d’État et des attributs d’interface.</span><span class="sxs-lookup"><span data-stu-id="070c8-117">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="070c8-118">L’interface dérivée n’hérite pas des définitions de type.</span><span class="sxs-lookup"><span data-stu-id="070c8-118">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="070c8-119">Pour ce faire, utilisez le mot clé [**Import**](import.md) pour importer le fichier IDL de l’interface de base.</span><span class="sxs-lookup"><span data-stu-id="070c8-119">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> <dt>

<span data-ttu-id="070c8-120">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="070c8-120">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="070c8-121">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="070c8-121">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="070c8-122">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md)et [pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="070c8-122">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="070c8-123">La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="070c8-123">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="070c8-124">Notes</span><span class="sxs-lookup"><span data-stu-id="070c8-124">Remarks</span></span>

<span data-ttu-id="070c8-125">Les noms d’interface dans le fichier IDL et ACF doivent être identiques, sauf lorsque vous utilisez le commutateur du compilateur MIDL [**/ACF**](-acf.md).</span><span class="sxs-lookup"><span data-stu-id="070c8-125">The interface names in the IDL file and ACF must be the same, except when you use the MIDL compiler switch [**/acf**](-acf.md).</span></span>

<span data-ttu-id="070c8-126">Le nom d’interface constitue la première partie du nom des structures de données de handle d’interface qui sont des paramètres pour les fonctions runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="070c8-126">The interface name forms the first part of the name of interface-handle data structures that are parameters to the RPC run-time functions.</span></span> <span data-ttu-id="070c8-127">Pour plus d’informations, consultez [**RPC \_ if \_ descripteur**](/windows/desktop/Rpc/rpc-if-handle).</span><span class="sxs-lookup"><span data-stu-id="070c8-127">For more information, see [**RPC\_IF\_HANDLE**](/windows/desktop/Rpc/rpc-if-handle).</span></span>

<span data-ttu-id="070c8-128">Si l’en-tête d’interface inclut l' **\[** [](object.md) **\]** attribut d’objet pour indiquer une interface com, il doit également inclure l' **\[** attribut [**UUID**](uuid.md) **\]** et doit spécifier l’interface com de base à partir de laquelle elle est dérivée.</span><span class="sxs-lookup"><span data-stu-id="070c8-128">If the interface header includes the **\[**[**object**](object.md)**\]** attribute to indicate a COM interface, it must also include the **\[**[**uuid**](uuid.md)**\]** attribute and must specify the base COM interface from which it is derived.</span></span> <span data-ttu-id="070c8-129">Pour plus d’informations sur les interfaces COM, consultez **\[** [**objet**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="070c8-129">For more information about COM interfaces, see **\[**[**object**](object.md)**\]**.</span></span>

<span data-ttu-id="070c8-130">Vous pouvez également utiliser le mot clé **interface** avec le mot clé [**typedef**](typedef.md) pour définir un type de données d’interface.</span><span class="sxs-lookup"><span data-stu-id="070c8-130">You can also use the **interface** keyword with the [**typedef**](typedef.md) keyword to define an interface data type.</span></span>

## <a name="examples"></a><span data-ttu-id="070c8-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="070c8-131">Examples</span></span>

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a><span data-ttu-id="070c8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="070c8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="070c8-133">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="070c8-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="070c8-134">**poste**</span><span class="sxs-lookup"><span data-stu-id="070c8-134">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="070c8-135">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="070c8-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="070c8-136">**localisé**</span><span class="sxs-lookup"><span data-stu-id="070c8-136">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="070c8-137">**object**</span><span class="sxs-lookup"><span data-stu-id="070c8-137">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="070c8-138">**pointeur \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="070c8-138">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="070c8-139">**\_handle RPC if \_**</span><span class="sxs-lookup"><span data-stu-id="070c8-139">**RPC\_IF\_HANDLE**</span></span>](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[<span data-ttu-id="070c8-140">**typedef**</span><span class="sxs-lookup"><span data-stu-id="070c8-140">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="070c8-141">**universel**</span><span class="sxs-lookup"><span data-stu-id="070c8-141">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="070c8-142">**Version**</span><span class="sxs-lookup"><span data-stu-id="070c8-142">**version**</span></span>](version.md)
</dt> </dl>

 

 