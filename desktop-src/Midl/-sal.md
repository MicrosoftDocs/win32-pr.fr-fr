---
title: commutateur/SAL
description: Le commutateur/SAL dirige MIDL pour générer des annotations SAL dans les fichiers stub générés.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- MIDL du commutateur/SAL
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509012"
---
# <a name="sal-switch"></a>commutateur/SAL

Le commutateur **/SAL** dirige MIDL pour générer des annotations SAL dans les fichiers stub générés.

``` syntax
midl /sal
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

MIDL marquera les paramètres de pointeur et de tableau avec des annotations qui reflètent la description de paramètre dans le fichier IDL, telle qu’elle est appliquée par RPC et le moteur de conversion de NDR. MIDL ne crée pas d’annotations pour les paramètres dans les méthodes d’interface marquées avec l’attribut [**\[ local \]**](local.md), sauf si [**/SAL \_ local**](-sal-local.md) est également présent sur la ligne de commande. Pour remplacer l’annotation générée par MIDL, utilisez l’attribut [**\[ annoter \]**](annotate.md) .

Les annotations générées par MIDL ont toujours le préfixe \_ \_ RPC \_ et nécessitent l’utilisation de l’en-tête **rpcsal. h** pour convertir l’annotation en annotations SAL standard.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/SAL \_ local**](-sal-local.md)
</dt> <dt>

[**\[annoter\]**](annotate.md)
</dt> </dl>

 

 




