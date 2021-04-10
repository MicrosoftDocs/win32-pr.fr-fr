---
title: commutateur/ms_union
description: Le \_ commutateur/ms. Union contrôle l’alignement du rapport de non-remise des unions non encapsulées. Notez que cet attribut est fourni à des fins de compatibilité descendante.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /commutateur ms_union MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841433"
---
# <a name="ms_union-switch"></a>\_commutateur/ms. Union

Le commutateur **/ms. \_ Union** contrôle l’alignement du rapport de non-remise des unions non encapsulées.

> [!Note]  
> Cet attribut est fourni à des fins de compatibilité descendante. Il n’est pas recommandé de l’utiliser dans une nouvelle interface.

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Le compilateur MIDL reflète le comportement du compilateur IDL OSF-DCE pour les unions non encapsulées. Toutefois, étant donné que les versions antérieures du compilateur MIDL ne l’ont pas fait, le commutateur d' **\_ Union/ms.** fournit la compatibilité avec les interfaces générées sur les versions précédentes du compilateur MIDL.

La \_ fonctionnalité MS Union peut être utilisée en tant que commutateur de ligne de commande (**/ms. \_ Union**), en tant qu’attribut d’interface IDL ou en tant qu’attribut de type IDL.

## <a name="examples"></a>Exemples

**MIDL/ms. \_ Union fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




