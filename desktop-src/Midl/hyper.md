---
title: Hyper Attribute
description: Le mot clé hyper indique un entier 64 bits qui peut être déclaré comme étant signé ou non signé.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- MIDL hyper-attribut
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f202890d2d81dcd7916f29c0330bf8e7093a7cf189e7b76a8af64dd2f0d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895259"
---
# <a name="hyper-attribute"></a>Hyper Attribute

Le mot clé **hyper** indique un entier 64 bits qui peut être déclaré comme étant signé ou non signé.

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*déclarateur-liste* 
</dt> <dd>

Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. (Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante. Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le type **hyper** est l’un des types de base du langage IDL (Interface Definition Language). Le type **hyper** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type de retour de fonction et en tant que spécificateur de type de paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

> [!Note]  
> Pour les plateformes 16 bits, le compilateur MIDL remplace les entiers hyper signés par des **\_ uhyper MIDL**. Cela permet de définir des interfaces avec des entiers hyper signés sur des plateformes qui ne prennent pas directement en charge les entiers 64 bits. **Le \_ uhyper MIDL** est défini dans les fichiers d’en-tête RPC.

 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




