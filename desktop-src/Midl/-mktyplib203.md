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
ms.openlocfilehash: dc887560401986b9a7d5e0f0aa7c8b36d61874bf245a88ade7a149cd084f1ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014147"
---
# <a name="mktyplib203-switch"></a>commutateur/mktyplib203

Le commutateur **/mktyplib203** force le compilateur MIDL à analyser le fichier d’entrée.

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Pour pouvoir utiliser le commutateur **/mktyplib203** , le fichier d’entrée doit respecter la syntaxe ODL exactement, ce qui signifie que vous ne pouvez pas placer d’instructions en dehors du bloc de bibliothèque. Exemples

**MIDL/mktyplib203 myoldodl. ODL**

**MIDL/mktyplib203 oldhabit. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




