---
title: commutateur/syntax_check
description: Le \_ commutateur de vérification/Syntax indique que le compilateur vérifie uniquement la syntaxe et ne génère pas de fichiers de sortie.
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /commutateur syntax_check MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678518"
---
# <a name="syntax_check-switch"></a>commutateur de vérification de/Syntax \_

Le commutateur de **\_ vérification/Syntax** indique que le compilateur vérifie uniquement la syntaxe et ne génère pas de fichiers de sortie.

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Ce commutateur remplace tous les autres commutateurs qui spécifient des informations sur les fichiers de sortie.

Vous pouvez également spécifier le mode de vérification de syntaxe avec l’option de compilateur MIDL [**/ZS**](-zs.md).

## <a name="examples"></a>Exemples

**MIDL/ZS NomFichier. idl**

**/Syntax MIDL \_ vérifier filename. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ZS**](-zs.md)
</dt> </dl>

 

 




