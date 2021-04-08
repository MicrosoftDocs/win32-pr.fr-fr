---
title: attribut Switch
description: Le mot clé Switch sélectionne le discriminante pour une Union encapsulée \_ .
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- MIDL d’attribut de commutateur
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940469"
---
# <a name="switch-attribute"></a>attribut Switch

Le mot clé **switch** sélectionne le discriminante pour une [**\_ Union encapsulée**](encapsulated-unions.md).

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type de commutateur* 
</dt> <dd>

Spécifie un type [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) ou un identificateur qui correspond à l’un de ces types.

</dd> <dt>

*nom du commutateur* 
</dt> <dd>

Spécifie le nom de la variable de type *switch-type* qui agit en tant que discriminante d’Union.

</dd> </dl>

## <a name="examples"></a>Exemples

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Unions qui ne sont pas encapsulées](nonencapsulated-unions.md)
</dt> <dt>

[**le commutateur \_ est**](switch-is.md)
</dt> <dt>

[**type de commutateur \_**](switch-type.md)
</dt> <dt>

[**UE**](union.md)
</dt> </dl>

 

 




