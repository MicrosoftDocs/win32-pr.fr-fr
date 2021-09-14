---
description: ICE08 vérifie que la table des composants ne contient pas de GUID en double. Chaque composant doit avoir un GUID unique. Aucune validation n’est effectuée si la table de composants n’existe pas.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021623"
---
# <a name="ice08"></a>ICE08

ICE08 vérifie que la [table des composants](component-table.md) ne contient pas de [GUID](guid.md)en double. Chaque composant doit avoir un GUID unique. Aucune validation n’est effectuée si la table de composants n’existe pas.

## <a name="result"></a>Résultats

ICE08 publie un message d’erreur si au moins deux entrées de la colonne ComponentId de la table des composants contiennent le même GUID.

## <a name="example"></a>Exemple

Dans l’exemple suivant, ICE08 publie un message indiquant que les composants Red et Green comportent des GUID en double.

[Table des composants](component-table.md) (partielle)



| Composant | ComponentId                            |
|-----------|----------------------------------------|
| Rouge       | {0000000A-0003-0000-0000-624474736554} |
| Blue      | {0000000A-0003-0000-0000-624474736354} |
| Vert     | {0000000A-0003-0000-0000-624474736554} |



 

Pour corriger cette erreur, modifiez l’un des GUID dupliqués.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



