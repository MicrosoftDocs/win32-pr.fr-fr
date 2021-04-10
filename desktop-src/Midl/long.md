---
title: attribut long
description: Le mot clé long désigne un entier 32 bits.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- long, attribut MIDL
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940413"
---
# <a name="long-attribute"></a>attribut long

Le mot clé **long** désigne un entier 32 bits.

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. (Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante. Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

Le mot clé **long** peut être précédé du mot [**clé signed ou du**](signed.md) mot clé [**unsigned**](unsigned.md). Le mot clé [**int**](int.md) est facultatif et peut être omis. Pour le compilateur MIDL, un entier long est signé par défaut et est synonyme de **long int signé**. Sur les plateformes 32 bits, **long** est synonyme de **int**.

Le type entier **long** est l’un des types de base du langage IDL. Le type entier **long** peut apparaître en tant que spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type Return-Function et en tant que spécificateur de type paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**consolidation**](hyper.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**abonné**](signed.md)
</dt> <dt>

[**Small**](small.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> </dl>

 

 




