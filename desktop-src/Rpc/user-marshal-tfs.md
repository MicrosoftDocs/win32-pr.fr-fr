---
title: Marshal d’utilisateur
description: Utilisateur-Marshal dans l’appel de procédure distante (RPC).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840025"
---
# <a name="user-marshal"></a>Marshal d’utilisateur

Le Marshal utilisateur a une chaîne de format similaire à la transmission \_ en tant que :

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

Les indicateurs<1> octet se composent du Quartet indicateur supérieur et du Quartet alignement inférieur.

Les 2 bits supérieurs du Quartet d’indicateur sont utilisés pour décrire si le type de câble est défini comme pointeur unique, pointeur de référence ou sans pointeur (il ne peut pas être un PTR). Les manifestes suivants ont été définis pour définir/obtenir les indicateurs :

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

Le grignot d’alignement du mot d’indicateur conserve l’alignement filaire du type transmis.

L’index quadruple \_<2> est un index de la routine de rappel quadruple des fonctions de Marshal utilisateur. Les positions de routine sont les suivantes : dimensionnement, marshaling, démarshaling et routine de libération.

La \_ \_ taille de la mémoire de type utilisateur \_<2> fournit une taille pour le type spécifique de l’utilisateur, y compris les types inconnus.

La taille de la \_ mémoire tampon de type transmis \_ \_<2> est soit zéro lorsque la taille est variable, soit la taille fixe réelle. Il s’agit d’une optimisation qui permet à MIDL d’ignorer les rappels lors du dimensionnement de la mémoire tampon, ainsi que lors de la libération de.

## <a name="range"></a>Plage

La \[ \] vérification de plage fournit des moyens supplémentaires pour la validation d’argument au niveau de la couche NDR. Le \[ \] descripteur de plage a le format suivant :

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

Les indicateurs prennent le Quartet supérieur et le type le Quartet inférieur du deuxième octet. Les valeurs basse et haute dépendent du type de la variable à vérifier.

Les indicateurs sont conçus comme un véhicule d’expansion ; le compilateur a défini le Quartet sur zéro.

 

 




