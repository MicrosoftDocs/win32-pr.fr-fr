---
title: attribut signé
description: Le mot clé signed indique que le bit le plus significatif d’une variable de type entier représente un bit de signe plutôt qu’un bit de données.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- MIDL d’attribut signé
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3db15bc46d6d8ab3ec108c648d094ebf706d9286a8c4b0a823fa409e118e3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641332"
---
# <a name="signed-attribute"></a>attribut signé

Le mot clé **signed** indique que le bit le plus significatif d’une variable de type entier représente un bit de signe plutôt qu’un bit de données.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Peut être de [**type char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)et [**Small**](small.md).

</dd> <dt>

*identificateur-nom* 
</dt> <dd>

Spécifie un identificateur MIDL valide. Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ce mot clé est facultatif et peut être utilisé avec l’un des types caractère et entier [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)et [**Small**](small.md). Vous pouvez éventuellement inclure le mot clé [**int**](int.md) après les qualificateurs de type **long**, **short** et **Small**.

Lorsque vous utilisez le commutateur de compilateur MIDL, les types [**de caractères et**](char-idl.md)d’entiers qui apparaissent dans le fichier IDL sans mots clés de signe explicite peuvent apparaître avec les mots clés **signés** ou [**non signés**](unsigned.md) dans le fichier d’en-tête généré. Pour éviter toute confusion, spécifiez le signe de l’entier et des types de caractères.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
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

[**Small**](small.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




