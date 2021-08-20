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
ms.openlocfilehash: 8c6b7a1e70804bc3c9c277f3d46ac6a8ad20fc0f98b370f93fe9fd09b0b1bb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013857"
---
# <a name="ignore-attribute"></a>ignorer l’attribut

L’attribut **\[ ignore \]** désigne qu’un pointeur contenu dans une structure ou une Union et l’objet indiqué par le pointeur ne sont pas transmis. L’attribut **\[ ignore \]** est limité aux membres de pointeur de structures ou d’unions.

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type de membre de pointeur* 
</dt> <dd>

Spécifie le type du membre pointeur de la structure ou de l’Union.

</dd> <dt>

*nom du pointeur* 
</dt> <dd>

Spécifie le nom du membre pointeur qui doit être ignoré pendant le marshaling.

</dd> </dl>

## <a name="remarks"></a>Remarques

La valeur d’un membre de structure avec l’attribut **\[ ignore \]** est non définie au niveau de la destination. Un **\[** paramètre [**in**](in.md) **\]** n’est pas défini sur l’ordinateur distant. Un **\[** [](out-idl.md) **\]** paramètre de sortie n’est pas défini sur l’ordinateur local.

L’attribut **\[ ignore \]** vous permet d’empêcher la transmission de données. Cela est utile dans des situations telles qu’une liste à double liaison. L’exemple suivant inclut une liste à double liaison qui introduit l’alias de données :

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

L’alias se produit dans l’exemple précédent, car la même zone mémoire est disponible à partir de deux pointeurs différents dans la fonction **p** et **p->suivant->précédent**.

Notez que l’option **\[ Ignorer \]** ne peut pas être utilisée en tant qu’attribut de type.

## <a name="examples"></a>Exemples

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs de tableau et de Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Tableaux et pointeurs](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 