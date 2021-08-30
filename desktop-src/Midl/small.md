---
title: attribut de petite taille
description: Le mot clé Small désigne un nombre entier 8 bits.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- MIDL d’attribut de petite taille
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec627a083d5f5186a4ce8b6b25b0ebbc7bd56afd3e334e46dc4e4901dde34201
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927399"
---
# <a name="small-attribute"></a>attribut de petite taille

Le mot clé **Small** désigne un nombre entier 8 bits.

``` syntax
small identifier-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*identificateur-nom* 
</dt> <dd>

Spécifie un identificateur MIDL valide. Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le mot clé **Small** peut être précédé [**du mot clé signed ou du**](signed.md) mot clé [**unsigned**](unsigned.md). Le mot clé [**int**](int.md) est facultatif et peut être omis. Pour le compilateur MIDL, un petit entier est **signé** par défaut et est synonyme de **Small int signé**.

Le type d’entier **petit** est l’un des types de base du langage IDL. Le **petit** type entier peut apparaître en tant que spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type Return-Function et en tant que spécificateur de type paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

Le signe du **petit** type peut être modifié par le commutateur du compilateur MIDL [**/char**](-char.md). Pour éviter toute confusion, spécifiez le signe du type entier avec les [**Mots clés signed**](signed.md) et [**unsigned**](unsigned.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/Char**](-char.md)
</dt> <dt>

[**const**](const.md)
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

[**non signé**](unsigned.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




