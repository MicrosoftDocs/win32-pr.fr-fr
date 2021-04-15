---
title: Attributs de structure et d’Union
description: Utilisez les \_ attributs Switch \ pour spécifier la caractéristique d’une Union dans un appel de procédure distante. Utilisez l’attribut ignore pour désigner certains membres de structure ou d’Union comme locaux pour l’application cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL MIDL, attributs, structure et Union
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462158"
---
# <a name="structure-and-union-attributes"></a>Attributs de structure et d’Union

Utilisez les attributs de **commutateur \_** \* pour spécifier la caractéristique d’une Union dans un appel de procédure distante. Utilisez l’attribut [**ignore**](ignore.md) pour désigner certains membres de structure ou d’Union comme locaux pour l’application cliente.



| Attribut                           | Utilisation                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Utilisez**](switch.md)            | Sélectionne le discriminante pour une Union encapsulée.                                                                           |
| [**le commutateur \_ est**](switch-is.md)     | Identifie le discriminante pour une Union qui n’est pas encapsulée.                                                                      |
| [**type de commutateur \_**](switch-type.md) | Identifie le type du discriminante pour une Union non encapsulée.                                                          |
| [**tenir**](ignore.md)            | Désigne un pointeur contenu dans une structure ou une Union, et l’objet indiqué par le pointeur ne doit pas être transmis. |



 

Vous pouvez également utiliser les [attributs de pointeur de tableau et de dimensionnement](array-and-sized-pointer-attributes.md) pour spécifier les caractéristiques des membres de structure ou d’Union.

 

 




