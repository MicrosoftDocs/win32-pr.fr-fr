---
description: Les techniques fournissent le muscle de rendu. Une technique encapsule l’état d’effet qui détermine un style de rendu. Une technique est constituée d’une ou de plusieurs passes.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Techniques et passes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095277"
---
# <a name="techniques-and-passes-direct3d-9"></a>Techniques et passes (Direct3D 9)

Les techniques fournissent le muscle de rendu. Une technique encapsule l’état d’effet qui détermine un style de rendu. Une technique est constituée d’une ou de plusieurs passes.

## <a name="techniques"></a>Technologie

La syntaxe d’appel d’une technique est la suivante :


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



Où :

-   ID est un nom unique facultatif.
-   l’annotation est égale à zéro, un ou plusieurs éléments facultatifs d’informations spécifiques à l’utilisateur. Consultez [Ajouter des informations pour appliquer des paramètres avec des \_ Annotations](using-an-effect.md).
-   Pass (es) est égal à zéro ou plusieurs passes. Chaque passe contient des attributions d’État. Voir ci-dessous.

## <a name="passes"></a>Mettent

Une passe contient les assignations d’État requises pour effectuer le rendu.


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



Où :

-   ID est un nom unique facultatif.
-   l’annotation est une partie facultative d’informations spécifiques à l’utilisateur. Consultez [Ajouter des informations pour appliquer des paramètres avec des \_ Annotations](using-an-effect.md).
-   les affectations assignent zéro ou plusieurs valeurs d’État, ou évaluent une ou plusieurs expressions. Consultez [États d’effet (Direct3D 9)](effect-states.md) et [expressions (Direct3D 9)](expressions.md).

Les passes ignorent toutes les affectations, sauf la dernière, dans un ensemble d’affectations répétées au même État.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



