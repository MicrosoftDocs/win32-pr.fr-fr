---
title: size_is (attribut)
description: Utilisez l’attribut \ size \_ is \ pour spécifier la taille de la mémoire, en éléments, allouée aux pointeurs dimensionnés, aux pointeurs dimensionnés aux pointeurs dimensionnés et aux tableaux à une ou plusieurs dimensions.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd57748d3ad92407fd65f3a6af7fc1ebb68321b576d57a50b6ba6f5546f8d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066699"
---
# <a name="size_is-attribute"></a>la taille \_ est un attribut

Utilisez l' \[ **attribut \_ Size** \] pour spécifier la taille de la mémoire, en éléments, allouée aux pointeurs dimensionnés, aux pointeurs dimensionnés aux pointeurs dimensionnés et aux tableaux à une ou plusieurs dimensions.

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Limited-expression-List* 
</dt> <dd>

Spécifie une ou plusieurs expressions en langage C. Chaque expression prend la valeur d’un entier non négatif qui représente la quantité de mémoire allouée à un pointeur dimensionné ou à un tableau. Dans le cas d’un tableau, spécifie une expression unique qui représente la taille d’allocation, en éléments, de la première dimension de ce tableau. Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques. MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation. Utilisez des virgules comme espaces réservés pour les paramètres implicites ou pour séparer plusieurs expressions.

</dd> </dl>

## <a name="remarks"></a>Remarques

Si vous utilisez l’attribut \[ **size \_ is** \] pour allouer de la mémoire pour un tableau multidimensionnel et que vous utilisez la notation de tableau \[ \] , gardez à l’esprit que seule la première dimension d’un tableau multidimensionnel peut être déterminée dynamiquement au moment de l’exécution. Les autres dimensions doivent être spécifiées de manière statique. Pour plus d’informations sur l’utilisation de l' \[ attribut **size \_** \] avec plusieurs niveaux de pointeurs pour permettre à un serveur de retourner un tableau de données de taille dynamique à un client, comme illustré dans l’exemple Proc7, consultez [plusieurs niveaux de pointeurs](/windows/desktop/Rpc/multiple-levels-of-pointers).

Vous pouvez utiliser l’une ou l’autre \[ **taille \_** est \] ou [**Max \_ est**](max-is.md) (mais pas les deux dans la même liste d’attributs) pour spécifier la taille d’un tableau dont les limites supérieures sont déterminées au moment de l’exécution. Notez, toutefois, que l' \[ attribut **size \_ is** \] ne peut pas être utilisé sur des dimensions de tableau fixes. L' \[ attribut **Max \_ is** \] spécifie l’index de tableau valide maximal. Par conséquent, la spécification de \[ Size a la valeur \_ (n) \] équivaut à spécifier \[ Max \_ is (n-1) \] .

Un \[ paramètre de tableau conforme [**dans**](in.md) \] ou \[ dans, [**out**](out-idl.md) \] avec l’attribut de \[ [**chaîne**](string.md) n' \] a pas besoin de l' \[ attribut **size \_ is** \] ou \[ [**Max \_ is**](max-is.md) \] . Dans ce cas, la taille de l’allocation est déterminée à partir de la marque de fin NULL de la chaîne d’entrée. Tous les autres tableaux conformes avec l’attribut de \[ chaîne \] doivent avoir une \[ **taille \_** \] ou un attribut \[ **Max \_ est** un \] attribut.

Bien qu’il soit possible d’utiliser l' \[ attribut **\_ Size** \] avec une constante, cette opération est inefficace et inutile. Par exemple, utilisez un tableau de taille fixe :

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

plutôt que :

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

Vous pouvez utiliser la \[ **taille \_** \] et les \[ [**\_**](length-is.md) \] attributs en même temps. Dans ce cas, la \[ **taille \_ est** l' \] attribut qui contrôle la quantité de mémoire allouée pour les données. La \[ **longueur \_ est** \] attribute spécifie le nombre d’éléments transmis. La quantité de mémoire spécifiée par la \[ **taille \_ est** \] et la \[ **longueur \_ est** que \] les attributs n’ont pas besoin d’être identiques. Par exemple, votre client peut passer un \[ paramètre in, out \] à un serveur et spécifier une allocation de mémoire importante avec \[ **size \_ is**, bien qu' \] il spécifie un petit nombre d’éléments de données à passer avec \[ **Length \_** \] . Cela permet au serveur de remplir le tableau avec plus de données qu’il n’en a reçu, qu’il peut ensuite renvoyer au client.

En général, il n’est pas utile de spécifier à la fois la \[ **taille \_** \] et les \[ [**\_**](length-is.md) \] \[ \] paramètres in ou \[ out \] . Dans les deux cas, la \[ **taille \_ est** le contrôle de l' \] allocation de mémoire. Votre application peut utiliser la \[ **taille \_** \] pour allouer plus d’éléments de tableau qu’elle ne le transmet (comme spécifié par \[ **Length \_** \] ). Toutefois, cela serait inefficace. Il serait également inefficace de spécifier des valeurs identiques pour la \[ **taille \_** \] , et la \[ **longueur \_ est** \] . Cela créerait une surcharge supplémentaire pendant le marshaling de paramètres. Si les valeurs de \[ **size \_ is** \] et \[ **Length \_** \] sont toujours les mêmes, omettez la \[ **longueur \_ est** \] attribute.

## <a name="examples"></a>Exemples

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Attributs de champ](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**tout d’abord, \_**](first-is.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**la dernière \_ est**](last-is.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**le nombre maximal \_ est**](max-is.md)
</dt> <dt>

[**min \_ est**](min-is.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> </dl>

 

 