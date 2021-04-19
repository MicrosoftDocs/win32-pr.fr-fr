---
title: commutateur/sal_local
description: Le \_ commutateur local/SAL dirige MIDL pour générer également des annotations SAL pour les paramètres des méthodes d’interface marquées \ local \. Le commutateur/SAL doit également être présent.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /commutateur sal_local MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510650"
---
# <a name="sal_local-switch"></a>\_commutateur local/SAL

Le **commutateur \_ local/SAL** dirige MIDL pour générer également des annotations SAL pour les paramètres de méthodes d’interface marquées comme [**\[ locales \]**](local.md). Le commutateur [**/SAL**](-sal.md) doit également être présent.

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Modifie le comportement du commutateur [**/SAL**](-sal.md) pour fournir également des annotations sur les paramètres des méthodes d’interface marquées avec l’attribut [**\[ local \]**](local.md) . Utilisez l’attribut [**\[ annoter \]**](annotate.md)pour remplacer l’annotation générée par MIDL par une autre chaîne d’annotation.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[annoter\]**](annotate.md)
</dt> </dl>

 

 




