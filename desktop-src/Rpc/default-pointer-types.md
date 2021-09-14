---
title: Types de pointeurs par défaut
description: Il n’est pas nécessaire que les pointeurs aient une description explicite de l’attribut. Lorsqu’un attribut explicite n’est pas fourni, le compilateur MIDL utilise un attribut de pointeur par défaut.
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c565fe8019567fd1fe319d7b34287d9729bbe1d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009150"
---
# <a name="default-pointer-types"></a>Types de pointeurs par défaut

Il n’est pas nécessaire que les pointeurs aient une description explicite de l’attribut. Lorsqu’un attribut explicite n’est pas fourni, le compilateur MIDL utilise un attribut de pointeur par défaut.

Les cas par défaut des pointeurs sans attributs sont les suivants :

-   Les pointeurs de niveau supérieur qui apparaissent dans les listes de paramètres sont par défaut des \[ [](/windows/desktop/Midl/ref) \] pointeurs Ref.
-   Tous les autres pointeurs ont comme valeur par défaut le type spécifié par l' \[ attribut [**\_ par défaut du pointeur**](/windows/desktop/Midl/pointer-default) \] . Quand aucun \[ **attribut \_ par défaut** \] de pointeur n’est fourni, ces pointeurs sont définis par défaut sur l' \[ [](/windows/desktop/Midl/unique) \] attribut unique lorsque le compilateur MIDL est en mode [extensions Microsoft](microsoft-rpc-binding-handle-extensions.md) ou en tant \[ [](/windows/desktop/Midl/ptr) \] qu’attribut PTR lorsque le compilateur MIDL est en mode compatible DCE.

Lorsqu’une procédure distante retourne un pointeur, la valeur de retour doit être un \[ pointeur [**unique**](/windows/desktop/Midl/unique) \] ou complet ( \[ [**ptr**](/windows/desktop/Midl/ptr) \] ).

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

### <a name="remarks"></a>Remarques

Pour garantir un comportement d’attribut pointeur non ambigu, utilisez toujours des attributs de pointeur explicites lors de la définition d’un pointeur.

Il est recommandé d' **\[** **\]** utiliser PTR uniquement lorsque des alias de pointeur sont requis.

 

 