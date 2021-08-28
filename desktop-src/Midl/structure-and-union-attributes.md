---
title: Attributs de structure et d’Union
description: Utilisez les \_ attributs Switch \ pour spécifier la caractéristique d’une Union dans un appel de procédure distante. Utilisez l’attribut ignore pour désigner certains membres de structure ou d’Union comme locaux pour l’application cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL MIDL, attributs, structure et Union
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc179632bb7e0d64b777f3c8a08b9de2af7bbf818978d6bb0a7ee2ea8b515542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066669"
---
# <a name="structure-and-union-attributes"></a>Attributs de structure et d’Union

Utilisez les attributs de **commutateur \_** \* pour spécifier la caractéristique d’une Union dans un appel de procédure distante. Utilisez l’attribut [**ignore**](ignore.md) pour désigner certains membres de structure ou d’Union comme locaux pour l’application cliente.



| Attribut                           | Usage                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Utilisez**](switch.md)            | Sélectionne le discriminante pour une Union encapsulée.                                                                           |
| [**le commutateur \_ est**](switch-is.md)     | Identifie le discriminante pour une Union qui n’est pas encapsulée.                                                                      |
| [**type de commutateur \_**](switch-type.md) | Identifie le type du discriminante pour une Union non encapsulée.                                                          |
| [**tenir**](ignore.md)            | Désigne un pointeur contenu dans une structure ou une Union, et l’objet indiqué par le pointeur ne doit pas être transmis. |



 

Vous pouvez également utiliser les [attributs de pointeur de tableau et de dimensionnement](array-and-sized-pointer-attributes.md) pour spécifier les caractéristiques des membres de structure ou d’Union.

 

 




