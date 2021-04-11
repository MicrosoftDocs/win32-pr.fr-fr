---
title: attribut handle_t
description: Le \_ mot clé handle t déclare un objet comme étant du handle de type de handle primitif \_ t. Un handle de liaison primitif est un objet de données qui peut être utilisé par l’application pour représenter la liaison.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t MIDL de l’attribut
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314820"
---
# <a name="handle_t-attribute"></a><span data-ttu-id="7f040-105">handle \_ t (attribut)</span><span class="sxs-lookup"><span data-stu-id="7f040-105">handle\_t attribute</span></span>

<span data-ttu-id="7f040-106">Le mot clé **handle \_ t** déclare un objet comme étant du handle de type de handle primitif **\_ t**.</span><span class="sxs-lookup"><span data-stu-id="7f040-106">The **handle\_t** keyword declares an object to be of the primitive handle type **handle\_t**.</span></span> <span data-ttu-id="7f040-107">Un handle de liaison primitif est un objet de données qui peut être utilisé par l’application pour représenter la liaison.</span><span class="sxs-lookup"><span data-stu-id="7f040-107">A primitive binding handle is a data object that can be used by the application to represent the binding.</span></span>

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a><span data-ttu-id="7f040-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f040-108">Parameters</span></span>

<span data-ttu-id="7f040-109">Cet attribut n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7f040-109">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f040-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7f040-110">Remarks</span></span>

<span data-ttu-id="7f040-111">Le type de **handle \_ t** est l’un des types prédéfinis du langage IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="7f040-111">The **handle\_t** type is one of the predefined types of the interface definition language (IDL).</span></span> <span data-ttu-id="7f040-112">Il peut apparaître comme un spécificateur de type dans les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et spécificateur de type de paramètre).</span><span class="sxs-lookup"><span data-stu-id="7f040-112">It can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="7f040-113">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="7f040-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="7f040-114">Dans Microsoft RPC, les paramètres de type **handle \_ t** peuvent se produire uniquement comme **\[** paramètres [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7f040-114">In Microsoft RPC, parameters of type **handle\_t** can occur only as **\[**[**in**](in.md)**\]** parameters.</span></span> <span data-ttu-id="7f040-115">Les handles primitifs ne peuvent pas avoir l' **\[** attribut [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7f040-115">Primitive handles cannot have the **\[**[**unique**](unique.md)**\]** or **\[**[**ptr**](ptr.md)**\]** attribute.</span></span>

<span data-ttu-id="7f040-116">Les paramètres de type **handle \_ t** (paramètres de handle primitifs) ne sont pas transmis sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="7f040-116">Parameters of type **handle\_t** (primitive handle parameters) are not transmitted on the network.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f040-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f040-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f040-118">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="7f040-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="7f040-119">Liaison et Handles</span><span class="sxs-lookup"><span data-stu-id="7f040-119">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="7f040-120">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="7f040-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7f040-121">**in**</span><span class="sxs-lookup"><span data-stu-id="7f040-121">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="7f040-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="7f040-122">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="7f040-123">**ptr**</span><span class="sxs-lookup"><span data-stu-id="7f040-123">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="7f040-124">**unique**</span><span class="sxs-lookup"><span data-stu-id="7f040-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 