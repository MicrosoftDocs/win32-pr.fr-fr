---
title: Char (attribut)
description: Le mot clé char spécifie un élément de données de 8 bits.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- attribut char MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093730"
---
# <a name="char-attribute"></a>Char (attribut)

Le mot clé **char** spécifie un élément de données de 8 bits.

``` syntax
char identifier-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*identificateur-nom* 
</dt> <dd>

Spécifie un identificateur MIDL valide. Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.

</dd> </dl>

## <a name="remarks"></a>Notes

Le mot clé **char** identifie un élément de données qui contient 8 bits. Pour le compilateur MIDL, un **caractère** est non signé par défaut et est synonyme de type [**unsigned**](unsigned.md) **char**.

Dans cette version de Microsoft RPC, les tables de conversion de caractères qui convertissent entre ASCII et EBCDIC sont intégrées dans les bibliothèques Runtime et ne peuvent pas être modifiées par l’utilisateur.

Le type **char** est l’un des types de base du langage IDL (Interface Definition Language). Le type **char** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et spécificateur de type de paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

Les compilateurs IDL DCE n’acceptent pas le mot clé [**signed**](signed.md) appliqué aux types **char** . Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur [**/OSF**](-osf.md) du compilateur MIDL.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**poids**](byte.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**abonné**](signed.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




