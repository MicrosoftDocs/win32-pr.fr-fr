---
title: int (attribut)
description: Le mot clé int spécifie un entier signé 32 bits sur les plateformes 32 bits. Sur les plateformes 16 bits, le mot clé int est un mot clé facultatif qui peut accompagner les mots clés Small, Short et long.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- MIDL d’attribut int
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678242"
---
# <a name="int-attribute"></a>int (attribut)

Le mot clé **int** spécifie un entier signé 32 bits sur les plateformes 32 bits. Sur les plateformes 16 bits, le mot clé **int** est un mot clé facultatif qui peut accompagner les mots clés [**Small**](small.md), [**short**](short.md)et [**long**](long.md).

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*modificateur entier* 
</dt> <dd>

Spécifie le mot clé [**Small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)ou [**\_ \_ Int64**](--int64.md), qui sélectionne la taille des données de type entier. Sur les plateformes 16 bits, le qualificateur de taille doit être présent.

</dd> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. (Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante. Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

Les types d’entiers sont parmi les types de base du langage IDL (Interface Definition Language). Ils peuvent apparaître en tant que spécificateurs de type dans les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type de retour de fonction et en tant que spécificateur de type de paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

Si aucune spécification de signe entier n’est fournie, le type entier est [**signé**](signed.md)par défaut.

Les compilateurs IDL DCE n’autorisent pas le [**mot clé signed**](signed.md) à spécifier le signe des types entiers. Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur [**/OSF**](-osf.md) du compilateur MIDL.

Microsoft ne recommande pas l’utilisation de \_ \_ int3264 pour la communication à distance si cela peut être évité. Pour plus d’informations sur l’utilisation et les limitations, consultez la rubrique sur [**\_ \_ int3264**](--int3264.md) .

## <a name="examples"></a>Exemples

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[**consolidation**](hyper.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**abonné**](signed.md)
</dt> <dt>

[**Small**](small.md)
</dt> <dt>

[**modélis**](struct.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**UE**](union.md)
</dt> </dl>

 

 




