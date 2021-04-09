---
title: iid_is (attribut)
description: L’attribut \ IID \_ est \ pointeur spécifie l’IID de l’interface com vers laquelle pointe un pointeur d’interface.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030068"
---
# <a name="iid_is-attribute"></a><span data-ttu-id="79fd5-104">IID \_ est l’attribut</span><span class="sxs-lookup"><span data-stu-id="79fd5-104">iid\_is attribute</span></span>

<span data-ttu-id="79fd5-105">L' **\[ IID \_ est \]** l’attribut de pointeur spécifie l’IID de l’interface com vers laquelle pointe un pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="79fd5-105">The **\[iid\_is\]** pointer attribute specifies the IID of the COM interface pointed to by an interface pointer.</span></span>

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a><span data-ttu-id="79fd5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79fd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79fd5-107">*Limited-expression*</span><span class="sxs-lookup"><span data-stu-id="79fd5-107">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="79fd5-108">Spécifie une expression de langage C.</span><span class="sxs-lookup"><span data-stu-id="79fd5-108">Specifies a C-language expression.</span></span> <span data-ttu-id="79fd5-109">Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="79fd5-109">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="79fd5-110">MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation.</span><span class="sxs-lookup"><span data-stu-id="79fd5-110">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79fd5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="79fd5-111">Remarks</span></span>

<span data-ttu-id="79fd5-112">Vous pouvez utiliser **\[ IID \_ \]** dans les listes d’attributs pour les paramètres de fonction et pour les membres de structure ou d’Union.</span><span class="sxs-lookup"><span data-stu-id="79fd5-112">You can use **\[iid\_is\]** in attribute lists for function parameters and for structure or union members.</span></span> <span data-ttu-id="79fd5-113">Les stubs utilisent l’IID pour déterminer comment marshaler le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="79fd5-113">The stubs use the IID to determine how to marshal the interface pointer.</span></span> <span data-ttu-id="79fd5-114">Cela est utile pour un pointeur d’interface qui est typé comme paramètre de classe de base.</span><span class="sxs-lookup"><span data-stu-id="79fd5-114">This is useful for an interface pointer that is typed as a base class parameter.</span></span>

<span data-ttu-id="79fd5-115">Les fichiers qui utilisent l' **\[ IID \_ sont \]** des attributs doivent être compilés avec le compilateur MIDL en mode par défaut, qui n’utilise pas le commutateur [**/OSF**](-osf.md)</span><span class="sxs-lookup"><span data-stu-id="79fd5-115">Files that use the **\[iid\_is\]** attribute must be compiled with the MIDL compiler in default mode, that is not using the [**/osf**](-osf.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="79fd5-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="79fd5-116">Examples</span></span>

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a><span data-ttu-id="79fd5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79fd5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fd5-118">**object**</span><span class="sxs-lookup"><span data-stu-id="79fd5-118">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="79fd5-119">**universel**</span><span class="sxs-lookup"><span data-stu-id="79fd5-119">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




