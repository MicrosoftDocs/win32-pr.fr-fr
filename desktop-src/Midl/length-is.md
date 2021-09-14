---
title: length_is (attribut)
description: L’attribut \ Length \_ est \ spécifie le nombre d’éléments de tableau à transmettre. Vous devez spécifier une valeur non négative.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093450"
---
# <a name="length_is-attribute"></a>la longueur \_ est Attribute

La **\[ longueur \_ est \]** attribute spécifie le nombre d’éléments de tableau à transmettre. Vous devez spécifier une valeur non négative.

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Limited-expression-List* 
</dt> <dd>

Spécifie une ou plusieurs expressions en langage C. Chaque expression prend la valeur d’un entier qui représente le nombre d’éléments de tableau à transmettre. Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques. MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation. Séparez plusieurs expressions par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

La **\[ longueur \_ est \]** un attribut qui détermine la valeur des index de tableau correspondant au **\[** [**\_**](last-is.md) **\]** **\[ \_ \]** dernier attribut is lorsque l’argument Last n’est pas spécifié. La relation entre ces index de tableau est la suivante : longueur = Last-First + 1.

La **\[ longueur \_ est \]** l’attribut ne peut pas être utilisé en même temps que le **\[** [**dernier attribut \_ est**](last-is.md) **\]** ou l’attribut de **\[** [**chaîne**](string.md) **\]** .

Pour définir une chaîne comptée avec une **\[ longueur égale \_ \]** à ou **\[** [**Last \_ est**](last-is.md) **\]** attribute, utilisez un tableau de caractères ou un pointeur sans l’attribut de **\[** [**chaîne**](string.md) **\]** .

L’utilisation d’une expression constante avec la **\[ longueur \_ est \]** l’attribut est une utilisation inappropriée de l’attribut. Il est légal, mais inefficace, et se traduira par un code de marshaling plus lent.

Vous pouvez utiliser la **\[** [**taille \_**](size-is.md) **\]** **\[ \_ et \]** les attributs en même temps. Dans ce cas, la **\[ taille \_ est \]** l’attribut qui contrôle la quantité de mémoire allouée pour les données. La **\[ longueur \_ est \]** attribute spécifie le nombre d’éléments transmis. La quantité de mémoire spécifiée par la **\[ taille \_ est \]** et la **\[ longueur \_ est \]** que les attributs n’ont pas besoin d’être identiques. Par exemple, votre client peut passer un paramètre **\[ in**, **out \]** à un serveur et spécifier une allocation de mémoire importante avec **\[ size \_ is \]**, bien qu’il spécifie un petit **\[ \_ \]** nombre d’éléments de données à passer avec length. Cela permet au serveur de remplir le tableau avec plus de données qu’il n’en a reçu, qu’il peut ensuite renvoyer au client.

En général, il n’est pas utile de spécifier à la fois la **\[** [**taille \_**](size-is.md) **\]** **\[ \_ \]** et les **\[** paramètres [**in**](in.md) **\]** ou **\[** [**out**](out-idl.md) **\]** . Dans les deux cas, la **\[ taille \_ est \]** le contrôle de l’allocation de mémoire. Votre application peut utiliser la **\[ taille \_ \]** pour allouer plus d’éléments de tableau qu’elle ne le transmet (comme **\[ \_ \]** spécifié par Length). Toutefois, cela serait inefficace. Il serait également inefficace de spécifier des valeurs identiques pour la **\[ taille \_ \]** , et la **\[ longueur \_ est \]**. Car cela entraînerait une surcharge supplémentaire pendant le marshaling des paramètres. Lorsque les valeurs de **\[ taille \_ \]** sont et que la **\[ longueur \_ est \]** toujours la même, omettez la **\[ longueur \_ est \]** attribut.

## <a name="examples"></a>Exemples

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs de champ](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**tout d’abord, \_**](first-is.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**la dernière \_ est**](last-is.md)
</dt> <dt>

[**le nombre maximal \_ est**](max-is.md)
</dt> <dt>

[**min \_ est**](min-is.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> </dl>

 

 