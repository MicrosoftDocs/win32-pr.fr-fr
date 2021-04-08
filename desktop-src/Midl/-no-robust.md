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
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678714"
---
# <a name="no_robust-switch"></a>\_Sélecteur de commutateur robuste

Le commutateur de la **\_ robustesse de/non** indique au compilateur MIDL de désactiver explicitement la fonctionnalité de ligne de commande [**/Robust**](-robust.md) . Le commutateur de ligne de commande **/Robust** et les fonctionnalités qui lui sont associées sont le paramètre de compilateur par défaut pour MIDL version 6.0.359 et versions ultérieures.

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Avec MIDL version 6.0.359 et ultérieure, le compilateur MIDL définit [**/Robust**](-robust.md) par défaut. Le commutateur de ligne de commande **\_ fiable/non** doit être utilisé pour désactiver la fonctionnalité **/Robust** si des stubs générés doivent s’exécuter sur Microsoft WindowsÂ NT, WindowsÂ 95/98 ou sur WindowsÂ me.

## <a name="examples"></a>Exemples

**MIDL \_ . idl de nom de fichier fiable**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> </dl>

 

 




