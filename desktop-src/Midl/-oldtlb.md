---
title: commutateur/oldtlb
description: Le commutateur/oldtlb indique au compilateur MIDL de générer une bibliothèque de types de format ancien.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- MIDL du commutateur/oldtlb
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b30a7bc905645523a81287eea2dfcdc408b8a4d172cc84282e0f1538e12cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895989"
---
# <a name="oldtlb-switch"></a>commutateur/oldtlb

Le commutateur **/oldtlb** indique au compilateur MIDL de générer une bibliothèque de types de format ancien.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

le commutateur **/oldtlb** remplace la valeur par défaut et indique au compilateur MIDL de générer des bibliothèques de types anciennes, même sur les versions actuelles de Windows à l’aide de [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) au lieu de [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).

## <a name="examples"></a>Exemples

**MIDL/oldtlb NomFichier. idl**

**MIDL/oldtlb myoldodl. ODL**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 