---
title: Types de pointeurs par défaut
description: Il n’est pas nécessaire que les pointeurs aient une description explicite de l’attribut. Lorsqu’un attribut explicite n’est pas fourni, le compilateur MIDL utilise un attribut de pointeur par défaut.
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c565fe8019567fd1fe319d7b34287d9729bbe1d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031555"
---
# <a name="default-pointer-types"></a><span data-ttu-id="fcaa9-104">Types de pointeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="fcaa9-104">Default Pointer Types</span></span>

<span data-ttu-id="fcaa9-105">Il n’est pas nécessaire que les pointeurs aient une description explicite de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="fcaa9-105">Pointers are not required to have an explicit attribute description.</span></span> <span data-ttu-id="fcaa9-106">Lorsqu’un attribut explicite n’est pas fourni, le compilateur MIDL utilise un attribut de pointeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="fcaa9-106">When an explicit attribute is not provided, the MIDL Compiler uses a default pointer attribute.</span></span>

<span data-ttu-id="fcaa9-107">Les cas par défaut des pointeurs sans attributs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fcaa9-107">The default cases for unattributed pointers are the following:</span></span>

-   <span data-ttu-id="fcaa9-108">Les pointeurs de niveau supérieur qui apparaissent dans les listes de paramètres sont par défaut des \[ [](/windows/desktop/Midl/ref) \] pointeurs Ref.</span><span class="sxs-lookup"><span data-stu-id="fcaa9-108">Top-level pointers that appear in parameter lists default to \[[**ref**](/windows/desktop/Midl/ref)\] pointers.</span></span>
-   <span data-ttu-id="fcaa9-109">Tous les autres pointeurs ont comme valeur par défaut le type spécifié par l' \[ attribut [**\_ par défaut du pointeur**](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="fcaa9-109">All other pointers default to the type specified by the \[[**pointer\_default**](/windows/desktop/Midl/pointer-default)\] attribute.</span></span> <span data-ttu-id="fcaa9-110">Quand aucun \[ **attribut \_ par défaut** \] de pointeur n’est fourni, ces pointeurs sont définis par défaut sur l' \[ [](/windows/desktop/Midl/unique) \] attribut unique lorsque le compilateur MIDL est en mode [extensions Microsoft](microsoft-rpc-binding-handle-extensions.md) ou en tant \[ [](/windows/desktop/Midl/ptr) \] qu’attribut PTR lorsque le compilateur MIDL est en mode compatible DCE.</span><span class="sxs-lookup"><span data-stu-id="fcaa9-110">When no \[**pointer\_default**\] attribute is supplied, these pointers default to the \[ [**unique**](/windows/desktop/Midl/unique) \] attribute when the MIDL compiler is in [Microsoft Extensions](microsoft-rpc-binding-handle-extensions.md) mode or the \[[**ptr**](/windows/desktop/Midl/ptr)\] attribute when the MIDL compiler is in DCE-compatible mode.</span></span>

<span data-ttu-id="fcaa9-111">Lorsqu’une procédure distante retourne un pointeur, la valeur de retour doit être un \[ pointeur [**unique**](/windows/desktop/Midl/unique) \] ou complet ( \[ [**ptr**](/windows/desktop/Midl/ptr) \] ).</span><span class="sxs-lookup"><span data-stu-id="fcaa9-111">When a remote procedure returns a pointer, the return value must be a \[ [**unique**](/windows/desktop/Midl/unique) \] or full (\[ [**ptr**](/windows/desktop/Midl/ptr) \]) pointer.</span></span>

``` syntax
/* IDL file compiled without /osf */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0),
  pointer_default(ptr)
]
interface MyInterface
{
    typedef long *PLONG;
  
    struct MyCircularList {
        struct MyCircularList *pRight;
        struct MyCircularList *pLeft;
        long Data;
    };

    void Foo1( [in] PLONG p );                   // p is ref
 
    void Foo2( [in] struct MyCircularList *p );  // p is ref, p->pRight and p->pLeft is ptr

    struct MyCircularList *Foo3( void );         // returned pointer is ptr.    
}

[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea46),
  version(1.0)
]
interface MyInterface2
{
    struct MySingleList
       {
       struct MySingleList *pNext;
       long Data;
       };
    void Foo4( [in] struct MySingleList *p );  // p is ref, p->pNext is unique

    struct MySingleList *Foo5( void );         // returned pointer is unique.    
}
```

### <a name="remarks"></a><span data-ttu-id="fcaa9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fcaa9-112">Remarks</span></span>

<span data-ttu-id="fcaa9-113">Pour garantir un comportement d’attribut pointeur non ambigu, utilisez toujours des attributs de pointeur explicites lors de la définition d’un pointeur.</span><span class="sxs-lookup"><span data-stu-id="fcaa9-113">To ensure unambiguous pointer-attribute behavior, always use explicit pointer attributes when defining a pointer.</span></span>

<span data-ttu-id="fcaa9-114">Il est recommandé d' **\[** **\]** utiliser PTR uniquement lorsque des alias de pointeur sont requis.</span><span class="sxs-lookup"><span data-stu-id="fcaa9-114">It is recommended that **\[** ptr **\]** is used only when pointer aliasing is required.</span></span>

 

 