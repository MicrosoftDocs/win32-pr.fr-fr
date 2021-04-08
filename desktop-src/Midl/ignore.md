---
title: ignorer l’attribut
description: L’attribut \ ignore \ désigne un pointeur contenu dans une structure ou une Union, et l’objet indiqué par le pointeur n’est pas transmis. L’attribut \ ignore \ est limité aux membres de pointeur de structures ou d’unions.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- MIDL d’attribut ignore
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842162"
---
# <a name="ignore-attribute"></a><span data-ttu-id="8f16e-105">ignorer l’attribut</span><span class="sxs-lookup"><span data-stu-id="8f16e-105">ignore attribute</span></span>

<span data-ttu-id="8f16e-106">L’attribut **\[ ignore \]** désigne qu’un pointeur contenu dans une structure ou une Union et l’objet indiqué par le pointeur ne sont pas transmis.</span><span class="sxs-lookup"><span data-stu-id="8f16e-106">The **\[ignore\]** attribute designates that a pointer contained in a structure or union and the object indicated by the pointer is not transmitted.</span></span> <span data-ttu-id="8f16e-107">L’attribut **\[ ignore \]** est limité aux membres de pointeur de structures ou d’unions.</span><span class="sxs-lookup"><span data-stu-id="8f16e-107">The **\[ignore\]** attribute is restricted to pointer members of structures or unions.</span></span>

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a><span data-ttu-id="8f16e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f16e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f16e-109">*type de membre de pointeur*</span><span class="sxs-lookup"><span data-stu-id="8f16e-109">*pointer-member-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8f16e-110">Spécifie le type du membre pointeur de la structure ou de l’Union.</span><span class="sxs-lookup"><span data-stu-id="8f16e-110">Specifies the type of the pointer member of the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="8f16e-111">*nom du pointeur*</span><span class="sxs-lookup"><span data-stu-id="8f16e-111">*pointer-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8f16e-112">Spécifie le nom du membre pointeur qui doit être ignoré pendant le marshaling.</span><span class="sxs-lookup"><span data-stu-id="8f16e-112">Specifies the name of the pointer member that is to be ignored during marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f16e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8f16e-113">Remarks</span></span>

<span data-ttu-id="8f16e-114">La valeur d’un membre de structure avec l’attribut **\[ ignore \]** est non définie au niveau de la destination.</span><span class="sxs-lookup"><span data-stu-id="8f16e-114">The value of a structure member with the **\[ignore\]** attribute is undefined at the destination.</span></span> <span data-ttu-id="8f16e-115">Un **\[** paramètre [**in**](in.md) **\]** n’est pas défini sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="8f16e-115">An **\[**[**in**](in.md)**\]** parameter is not defined at the remote computer.</span></span> <span data-ttu-id="8f16e-116">Un **\[** [](out-idl.md) **\]** paramètre de sortie n’est pas défini sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8f16e-116">An **\[**[**out**](out-idl.md)**\]** parameter is not defined at the local computer.</span></span>

<span data-ttu-id="8f16e-117">L’attribut **\[ ignore \]** vous permet d’empêcher la transmission de données.</span><span class="sxs-lookup"><span data-stu-id="8f16e-117">The **\[ignore\]** attribute allows you to prevent transmission of data.</span></span> <span data-ttu-id="8f16e-118">Cela est utile dans des situations telles qu’une liste à double liaison.</span><span class="sxs-lookup"><span data-stu-id="8f16e-118">This is useful in situations such as a double-linked list.</span></span> <span data-ttu-id="8f16e-119">L’exemple suivant inclut une liste à double liaison qui introduit l’alias de données :</span><span class="sxs-lookup"><span data-stu-id="8f16e-119">The following example includes a double-linked list that introduces data aliasing:</span></span>

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

<span data-ttu-id="8f16e-120">L’alias se produit dans l’exemple précédent, car la même zone mémoire est disponible à partir de deux pointeurs différents dans la fonction **p** et **p->suivant->précédent**.</span><span class="sxs-lookup"><span data-stu-id="8f16e-120">Aliasing occurs in the preceding example because the same memory area is available from two different pointers in the function **p** and **p->next->previous**.</span></span>

<span data-ttu-id="8f16e-121">Notez que l’option **\[ Ignorer \]** ne peut pas être utilisée en tant qu’attribut de type.</span><span class="sxs-lookup"><span data-stu-id="8f16e-121">Note that **\[ignore\]** cannot be used as a type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="8f16e-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="8f16e-122">Examples</span></span>

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="8f16e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f16e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f16e-124">Attributs de tableau et de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="8f16e-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="8f16e-125">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="8f16e-125">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="8f16e-126">Tableaux et pointeurs</span><span class="sxs-lookup"><span data-stu-id="8f16e-126">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="8f16e-127">**in**</span><span class="sxs-lookup"><span data-stu-id="8f16e-127">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="8f16e-128">**à**</span><span class="sxs-lookup"><span data-stu-id="8f16e-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="8f16e-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="8f16e-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="8f16e-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="8f16e-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="8f16e-131">**unique**</span><span class="sxs-lookup"><span data-stu-id="8f16e-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 