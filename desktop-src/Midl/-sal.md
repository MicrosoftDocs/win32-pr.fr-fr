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
ms.openlocfilehash: 80097cbfbb7bebae3b84b65c9c228dd29992821a5bafa61830961f752c452950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067489"
---
# <a name="sal-switch"></a>commutateur/SAL

Le commutateur **/SAL** dirige MIDL pour générer des annotations SAL dans les fichiers stub générés.

``` syntax
midl /sal
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

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

 

 




