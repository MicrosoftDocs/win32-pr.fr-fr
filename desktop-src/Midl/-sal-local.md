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
ms.openlocfilehash: 666401cca482846fc2e6a9d5851a4da9d2d362279c9bc1496ab672a94ac9b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014087"
---
# <a name="sal_local-switch"></a>\_commutateur local/SAL

Le **commutateur \_ local/SAL** dirige MIDL pour générer également des annotations SAL pour les paramètres de méthodes d’interface marquées comme [**\[ locales \]**](local.md). Le commutateur [**/SAL**](-sal.md) doit également être présent.

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Modifie le comportement du commutateur [**/SAL**](-sal.md) pour fournir également des annotations sur les paramètres des méthodes d’interface marquées avec l’attribut [**\[ local \]**](local.md) . Utilisez l’attribut [**\[ annoter \]**](annotate.md)pour remplacer l’annotation générée par MIDL par une autre chaîne d’annotation.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[annoter\]**](annotate.md)
</dt> </dl>

 

 




