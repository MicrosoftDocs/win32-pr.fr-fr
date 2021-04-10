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
ms.openlocfilehash: 469802434d54319aa55c1e409ccb8d64e942836f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678309"
---
# <a name="zs-switch"></a>Commutateur/ZS

Le commutateur **/ZS** indique que le compilateur vérifie la syntaxe uniquement et ne génère pas de fichiers de sortie.

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

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

 

 




