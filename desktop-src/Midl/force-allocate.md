---
title: attribut force_allocate
description: L’attribut ACF \ force \_ allocate \ force l’allocation d’un paramètre de pointeur à l’aide \_ de l’allocation d’utilisateur MIDL \_ au lieu d’optimiser l’allocation.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate MIDL de l’attribut
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463007"
---
# <a name="force_allocate-attribute"></a><span data-ttu-id="3e2e2-104">forcer l’allocation de l' \_ attribut</span><span class="sxs-lookup"><span data-stu-id="3e2e2-104">force\_allocate attribute</span></span>

<span data-ttu-id="3e2e2-105">L’attribut ACF \[ **force \_ allocate** \] force un paramètre de pointeur à être alloué à l’aide de l’allocation d' [**\_ utilisateur \_ MIDL**](midl-user-allocate-1.md) au lieu d’optimiser l’allocation.</span><span class="sxs-lookup"><span data-stu-id="3e2e2-105">The ACF attribute \[**force\_allocate**\] forces a pointer parameter to be allocated using [**midl\_user\_allocate**](midl-user-allocate-1.md) instead of optimizing away the allocation.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a><span data-ttu-id="3e2e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e2e2-106">Parameters</span></span>

<span data-ttu-id="3e2e2-107">Cet attribut n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3e2e2-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e2e2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3e2e2-108">Remarks</span></span>

<span data-ttu-id="3e2e2-109">RPC tente de réduire les allocations de mémoire sur le serveur en fournissant des pointeurs aux mémoires tampons de mémoire internes.</span><span class="sxs-lookup"><span data-stu-id="3e2e2-109">RPC attempts to minimize memory allocations on the server by supplying pointers to internal memory buffers.</span></span> <span data-ttu-id="3e2e2-110">Cette approche peut provoquer des problèmes pour les applications qui tentent d’appeler directement l' [**\_ utilisateur MIDL \_**](midl-user-free-1.md) sur les pointeurs fournis par RPC, car un pointeur qui a été optimisé ne peut pas être libéré.</span><span class="sxs-lookup"><span data-stu-id="3e2e2-110">This approach can cause problems for applications that attempt to directly call [**midl\_user\_free**](midl-user-free-1.md) on RPC-supplied pointers, because a pointer that has been optimized cannot be freed.</span></span> <span data-ttu-id="3e2e2-111">Le marquage d’un paramètre avec l' **\[ \_ allocation \] forcée** empêche cette optimisation pour tous les pointeurs qui le dérivent.</span><span class="sxs-lookup"><span data-stu-id="3e2e2-111">Marking a parameter with **\[force\_allocate\]** will prevent this optimization for all pointers deriving it.</span></span>

<span data-ttu-id="3e2e2-112">Une autre utilisation courante de **\[ force \_ allocate \]** consiste à garantir l’alignement de la mémoire vers laquelle pointe la mémoire si une application requiert un alignement supérieur à celui de la mémoire vers laquelle pointe.</span><span class="sxs-lookup"><span data-stu-id="3e2e2-112">Another common use for **\[force\_allocate\]** is to guarantee the alignment of the memory being pointed to if an application requires an alignment greater than that of the memory pointed to.</span></span> <span data-ttu-id="3e2e2-113">Par exemple, les applications transmettent souvent des données dans un tableau générique d’octets plutôt que d’utiliser le type réel, mais l’alignement d’un octet est garanti uniquement à 1, ce qui peut entraîner des problèmes pour les applications qui supposent un plus grand alignement.</span><span class="sxs-lookup"><span data-stu-id="3e2e2-113">For example, applications often pass data in a generic array of bytes rather than using the actual type, but a byte is only guaranteed to be aligned at 1, which may cause problems for applications that assume a larger alignment.</span></span> <span data-ttu-id="3e2e2-114">En marquant le paramètre avec **\[ force \_ allocate \]**, l’application peut garantir que toute la mémoire pointée aura un alignement égal à celui garanti par l' [**\_ \_ allocation d’utilisateur MIDL**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="3e2e2-114">By marking the parameter with **\[force\_allocate\]**, the application can guarantee all memory pointed to will have an alignment equal to that guaranteed by [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3e2e2-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="3e2e2-115">Examples</span></span>

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a><span data-ttu-id="3e2e2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e2e2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2e2-117">Éviter le masquage des informations</span><span class="sxs-lookup"><span data-stu-id="3e2e2-117">Avoiding Information Hiding</span></span>](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[<span data-ttu-id="3e2e2-118">Conception d’interfaces compatibles 64 bits</span><span class="sxs-lookup"><span data-stu-id="3e2e2-118">Designing 64-bit-Compatible Interfaces</span></span>](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[<span data-ttu-id="3e2e2-119">**allouer un \_ utilisateur MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="3e2e2-119">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="3e2e2-120">**\_utilisateur \_ gratuit MIDL**</span><span class="sxs-lookup"><span data-stu-id="3e2e2-120">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="3e2e2-121">**lui**</span><span class="sxs-lookup"><span data-stu-id="3e2e2-121">**allocate**</span></span>](allocate.md)
</dt> </dl>

 

 