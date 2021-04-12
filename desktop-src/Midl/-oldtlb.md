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
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381841"
---
# <a name="oldtlb-switch"></a>commutateur/oldtlb

Le commutateur **/oldtlb** indique au compilateur MIDL de générer une bibliothèque de types de format ancien.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Le commutateur **/oldtlb** remplace la valeur par défaut et indique au compilateur MIDL de générer des bibliothèques de types anciennes, même sur les versions actuelles de Windows, à l’aide de [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) au lieu de [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).

## <a name="examples"></a>Exemples

**MIDL/oldtlb NomFichier. idl**

**MIDL/oldtlb myoldodl. ODL**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 