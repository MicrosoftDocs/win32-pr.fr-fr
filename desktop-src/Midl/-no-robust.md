---
title: commutateur/no_robust
description: Le commutateur de la \_ robustesse de/non indique au compilateur MIDL de désactiver explicitement la fonctionnalité de ligne de commande/Robust. Le commutateur de ligne de commande/Robust et les fonctionnalités qui lui sont associées sont le paramètre de compilateur par défaut pour MIDL version 6.0.359 et versions ultérieures.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /commutateur no_robust MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1078a3eec25d6b6fdf44268ae915c20e7a2a9cf0c07a29730461bd544a7a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808854"
---
# <a name="no_robust-switch"></a>\_Sélecteur de commutateur robuste

Le commutateur de la **\_ robustesse de/non** indique au compilateur MIDL de désactiver explicitement la fonctionnalité de ligne de commande [**/Robust**](-robust.md) . Le commutateur de ligne de commande **/Robust** et les fonctionnalités qui lui sont associées sont le paramètre de compilateur par défaut pour MIDL version 6.0.359 et versions ultérieures.

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Avec MIDL version 6.0.359 et ultérieure, le compilateur MIDL définit [**/Robust**](-robust.md) par défaut. Le commutateur de ligne de commande **\_ fiable/non** doit être utilisé pour désactiver la fonctionnalité **/Robust** si des stubs générés doivent s’exécuter sur Microsoft WindowsÂ NT, WindowsÂ 95/98 ou sur WindowsÂ me.

## <a name="examples"></a>Exemples

**MIDL \_ . idl de nom de fichier fiable**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> </dl>

 

 




