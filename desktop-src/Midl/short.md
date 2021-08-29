---
title: attribut Short
description: Le mot clé Short désigne un entier 16 bits.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- attribut MIDL Short
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb107b818d2d89717535996d95b580df5a2d49ad0a72aef97de5d6111a0e90d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066739"
---
# <a name="short-attribute"></a>attribut Short

Le mot clé **short** désigne un entier 16 bits.

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. (Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante. Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le mot clé **short** peut être précédé du mot [**clé signed ou du**](signed.md) mot clé [**unsigned**](unsigned.md). Le mot clé [**int**](int.md) est facultatif et peut être omis. Pour le compilateur MIDL, un entier Short est signé par défaut et est synonyme de **short int signé**.

Le type d’entier **short** est l’un des types de base du langage IDL. Le type entier **short** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et spécificateur de type de paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**abonné**](signed.md)
</dt> <dt>

[**Small**](small.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> </dl>

 

 




