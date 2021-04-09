---
title: commutateur/cstruct_out
description: Le commutateur/cstruct_out modifie la définition C d’une interface COM qui retourne des structures pour qu’elles correspondent à l’ABI qu’un implémenteur C++ peut fournir.
keywords:
- /commutateur cstruct_out MIDL
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844506"
---
# <a name="cstruct_out-switch"></a>\_commutateur/cstruct out

Ce commutateur modifie la définition C d’une interface COM qui retourne des structures correspondant à l’ABI qu’un implémenteur C++ peut fournir.

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Certaines définitions d’interface (notamment celles de `d3d12.idl` ) contiennent des `__stdcall` méthodes qui retournent des structures. Les Abi C et C++ de MSVC diffèrent dans la manière dont ils implémentent les fonctions suivantes :

* C les traite comme des fonctions brutes qui prennent un `this` pointeur masqué comme premier paramètre. Le compilateur applique une petite optimisation de struct qui autorise les structs inférieurs à 8 octets (ou plus si toutes les valeurs sont à virgule flottante) d’être retournés dans les registres. Seules les structures plus grandes sont promues pour utiliser un paramètre masqué et une valeur de retour allouée par l’appelant.
* C++ les traite comme des fonctions membres. Le compilateur effectue *toujours* cela en insérant un paramètre masqué (pointeur vers une valeur de retour allouée par l’appelant) en tant que deuxième paramètre, après le `this` pointeur. Elle retourne également le même pointeur que sa valeur de retour.

Ce commutateur force la définition C des interfaces dans l’en-tête résultant à supposer que l’implémenteur utilisait C++ et que le code C doit utiliser à la place explicitement l’ABI C++. Cela implique que la fonction inclue un paramètre masqué pour le pointeur de valeur de retour et retourne ce pointeur au lieu de la structure directement.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> </dl>
