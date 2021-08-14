---
description: ICE95 vérifie la table de contrôle et la table BBControl pour vérifier que les contrôles de tableau blanc s’intègrent à tous les panneaux.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f0f7d44554385c33648036f314406971193afc079b5aa8e72cf595695797ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315259"
---
# <a name="ice95"></a>ICE95

ICE95 vérifie la table de contrôle et la [table BBControl](bbcontrol-table.md) pour vérifier que les contrôles de [tableau](control-table.md) blanc s’intègrent à tous les panneaux.

## <a name="result"></a>Résultat

Si l’une des conditions suivantes est vraie, un contrôle d’affichage des panneaux ne peut pas être contenu dans un panneau. ICE95 publie les avertissements suivants.



| AVERTISSEMENT ICE95                                                                                                                                                                                                              | Description                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Élément BBControl' \[ 1 \] . \[ 2 \] 'dans la table BBControl ne tient pas dans tous les contrôles de tableau blanc de la table de contrôle. La coordonnée X dépasse la limite de la largeur minimale du contrôle de tableau blanc% s                   | La coordonnée X du contrôle est en dehors de la largeur du panneau.                          |
| Élément BBControl' \[ 1 \] . \[ 2 \] 'dans la table BBControl ne tient pas dans tous les contrôles de tableau blanc de la table de contrôle. La coordonnée Y dépasse la limite de la hauteur minimale du contrôle de tableau blanc% s                  | La coordonnée Y du contrôle est en dessous du bas du panneau.                           |
| Élément BBControl' \[ 1 \] . \[ 2 \] 'dans la table BBControl ne tient pas dans tous les contrôles de tableau blanc de la table de contrôle. La coordonnée X et la largeur combinés dépassent la largeur minimale du contrôle de tableau blanc% s   | La coordonnée X du contrôle plus la largeur du contrôle est en dehors de la largeur du panneau. |
| Élément BBControl' \[ 1 \] . \[ 2 \] 'dans la table BBControl ne tient pas dans tous les contrôles de tableau blanc de la table de contrôle. La coordonnée Y et la hauteur combinés dépassent la hauteur minimale du contrôle de tableau blanc% s | La coordonnée Y du contrôle plus la hauteur du contrôle se trouve en dessous du bas du panneau. |



 

## <a name="example"></a> Exemple

ICE95 signale les avertissements suivants pour l’exemple :

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

Table de contrôle (partielle) (partielle)



| Contrôler  | Type      | Largeur | Hauteur |
|----------|-----------|-------|--------|
| Control1 | Blanc | 300   | 100    |
| Control2 | Blanc | 100   | 300    |



 

[Table BBControl](bbcontrol-table.md)



| Blanc\_ | BBControl  | X   | O   | Largeur | Hauteur |
|-------------|------------|-----|-----|-------|--------|
| billboard1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| billboard1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| billboard1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| billboard1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



