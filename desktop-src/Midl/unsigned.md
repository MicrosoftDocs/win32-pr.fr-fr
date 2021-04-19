---
title: attribut non signé
description: Le mot clé unsigned indique que le bit le plus significatif d’une variable de type entier représente un bit de données plutôt qu’un bit signé.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- MIDL d’attribut non signé
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106545734"
---
# <a name="unsigned-attribute"></a>attribut non signé

Le mot clé **unsigned** indique que le bit le plus significatif d’une variable de type entier représente un bit de données plutôt qu’un bit signé.

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Peut être de [**type char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md)et [**Small**](small.md).

</dd> <dt>

*identificateur-nom* 
</dt> <dd>

Spécifie un identificateur MIDL valide. Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.

</dd> </dl>

## <a name="remarks"></a>Notes

Ce mot clé est facultatif et peut être utilisé avec l’un des types caractère et entier [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)et [**Small**](small.md). Vous pouvez éventuellement inclure le mot clé [**int**](int.md) après les qualificateurs de type **long**, **short** et **Small**.

Quand vous utilisez le commutateur de compilateur MIDL [**/char**](-char.md), les types caractère et entier qui apparaissent dans le fichier IDL sans mots clés de signe explicite peuvent apparaître avec le mot clé [**signé**](signed.md) ou **non signé** dans le fichier d’en-tête généré. Pour éviter toute confusion, spécifiez le signe de l’entier et des types de caractères.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**abonné**](signed.md)
</dt> <dt>

[**Small**](small.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




