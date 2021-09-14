---
title: commutateur/mktyplib203
description: Le commutateur/mktyplib203 force le compilateur MIDL à analyser le fichier d’entrée.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- MIDL du commutateur/mktyplib203
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8fd972355c2f6d37300c60f4bf74e76bf4396
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093906"
---
# <a name="mktyplib203-switch"></a>commutateur/mktyplib203

Le commutateur **/mktyplib203** force le compilateur MIDL à analyser le fichier d’entrée.

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Pour pouvoir utiliser le commutateur **/mktyplib203** , le fichier d’entrée doit respecter la syntaxe ODL exactement, ce qui signifie que vous ne pouvez pas placer d’instructions en dehors du bloc de bibliothèque. Exemples

**MIDL/mktyplib203 myoldodl. ODL**

**MIDL/mktyplib203 oldhabit. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




