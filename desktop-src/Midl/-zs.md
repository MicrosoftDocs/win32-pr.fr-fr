---
title: Commutateur/ZS
description: Le commutateur/ZS indique que le compilateur vérifie la syntaxe uniquement et ne génère pas de fichiers de sortie.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- MIDL du commutateur/ZS
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92bd2321567bbc565d3198fe5ebf5c98a3d8df440ea967409830c8e73488609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014017"
---
# <a name="zs-switch"></a>Commutateur/ZS

Le commutateur **/ZS** indique que le compilateur vérifie la syntaxe uniquement et ne génère pas de fichiers de sortie.

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Ce commutateur remplace tous les autres commutateurs qui spécifient des informations sur les fichiers de sortie.

Vous pouvez également spécifier le mode de vérification de syntaxe avec le commutateur de compilateur MIDL [**/Syntax \_ Check**](-syntax-check.md).

## <a name="examples"></a>Exemples

**MIDL/ZS NomFichier. idl**

**/Syntax MIDL \_ vérifier filename. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**vérification de/Syntax \_**](-syntax-check.md)
</dt> </dl>

 

 




