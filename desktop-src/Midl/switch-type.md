---
title: switch_type (attribut)
description: L’attribut \ Switch \_ type \ identifie le type de la variable utilisée en tant qu’Union discriminante. Le type de commutateur peut être un type entier, caractère, booléen ou énumération.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type MIDL de l’attribut
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093157"
---
# <a name="switch_type-attribute"></a>\_attribut type de commutateur

L’attribut **\[ \_ type \] de commutateur** identifie le type de la variable utilisée en tant qu’Union discriminante. Le type de commutateur peut être un type entier, caractère, booléen ou énumération.

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*spécificateur de type Switch* 
</dt> <dd>

Spécifie un type [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md)ou [**enum**](enum.md) , ou un identificateur de ce type.

</dd> </dl>

## <a name="remarks"></a>Notes

Tandis que l’attribut **\[ \_ type \] de commutateur** identifie le type de variable, le **\[** [**commutateur \_ est**](switch-is.md) **\]** attribute spécifie le nom du paramètre qui est l’Union discriminante. L’attribut **\[ \_ type \] de commutateur** s’applique aux paramètres ou aux membres de structures ou d’unions.

L’Union et son discriminante doivent être spécifiés au même niveau logique. Lorsque l’Union est un paramètre, l’Union discriminante doit être un autre paramètre. Lorsque l’Union est un champ d’une structure, discriminante doit être un autre champ de la structure au même niveau que le champ Union.

## <a name="examples"></a>Exemples

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Booléen**](boolean.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[Unions encapsulées](encapsulated-unions.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[Unions qui ne sont pas encapsulées](nonencapsulated-unions.md)
</dt> <dt>

[**le commutateur \_ est**](switch-is.md)
</dt> <dt>

[**union**](union.md)
</dt> </dl>

 

 




