---
description: Cette section répertorie les codes d’opération Raster binaires utilisés par les fonctions GetROP2 et SetROP2. Les codes d’opération Raster définissent la façon dont GDI combine les bits du stylet sélectionné avec les bits dans le bitmap de destination.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Opérations raster binaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114739"
---
# <a name="binary-raster-operations"></a>Opérations raster binaires

Cette section répertorie les codes d’opération Raster binaires utilisés par les fonctions [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) et [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) . Les codes d’opération Raster définissent la façon dont GDI combine les bits du stylet sélectionné avec les bits dans le bitmap de destination.

Chaque code d’opération Raster représente une opération booléenne dans laquelle les valeurs des pixels dans le stylet sélectionné et le bitmap de destination sont combinées. Voici les deux opérandes utilisés dans ces opérations.



| Opérande | Signification            |
|---------|--------------------|
| P       | Stylo sélectionné       |
| D       | Bitmap de destination |



 

Les opérateurs booléens utilisés dans ces opérations suivent.



| Opérateur | Signification                    |
|----------|----------------------------|
| a        | ET au niveau du bit                |
| n        | NOT au niveau du bit (inverse)      |
| o        | Opération de bits OR                 |
| x        | Or exclusif au niveau du bit (XOR) |



 

Toutes les opérations booléennes sont présentées en notation polonais inverse. Par exemple, l’opération suivante remplace les valeurs des pixels de l’image bitmap de destination par une combinaison des valeurs de pixel du stylet et du pinceau sélectionné :


```C++
DPo 
```



Chaque code d’opération Raster est un entier 32 bits dont le mot de poids fort est un index d’opération booléen et dont le mot de poids faible est le code d’opération. L’index d’opération 16 bits est une valeur 8 bits étendue de zéro qui représente tous les résultats possibles résultant de l’opération booléenne sur deux paramètres (dans ce cas, les valeurs de stylet et de destination). Par exemple, les index d’opération pour les opérations DPo et DPan sont affichés dans la liste suivante.



| P   | D   | DPo | Dpan |
|-----|-----|-----|------|
| 0   | 0   | 0   | 1    |
| 0   | 1   | 1   | 1    |
| 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0    |



 

La liste suivante présente les modes de dessin et les opérations booléennes qu’ils représentent.



| Opération Raster | Opération booléenne |
|------------------|-------------------|
| R2 \_ noir        | 0                 |
| \_COPYPEN R2      | P                 |
| \_MASKNOTPEN R2   | DPna              |
| \_MASKPEN R2      | DPa               |
| \_MASKPENNOT R2   | PDna              |
| \_MERGENOTPEN R2  | DPno              |
| \_MERGEPEN R2     | DPo               |
| \_MERGEPENNOT R2  | PDno              |
| R2 \_ NOP          | D                 |
| R2 \_ non          | Nom unique                |
| \_NOTCOPYPEN R2   | PN                |
| \_NOTMASKPEN R2   | DPan              |
| \_NOTMERGEPEN R2  | DPon              |
| \_NOTXORPEN R2    | DPxn              |
| \_Blanc R2        | 1                 |
| \_XORPEN R2       | DPx               |



 

Pour un appareil monochrome, GDI mappe la valeur de zéro au noir et la valeur 1 à blanc. Si une application tente de dessiner avec un stylet noir sur une destination blanche à l’aide des opérations raster binaires disponibles, les résultats suivants se produisent.



| Opération Raster | Résultats             |
|------------------|--------------------|
| R2 \_ noir        | Ligne noire visible |
| \_COPYPEN R2      | Ligne noire visible |
| \_MASKNOTPEN R2   | Aucune ligne visible    |
| \_MASKPEN R2      | Ligne noire visible |
| \_MASKPENNOT R2   | Ligne noire visible |
| \_MERGENOTPEN R2  | Aucune ligne visible    |
| \_MERGEPEN R2     | Ligne noire visible |
| \_MERGEPENNOT R2  | Ligne noire visible |
| R2 \_ NOP          | Aucune ligne visible    |
| R2 \_ non          | Ligne noire visible |
| \_NOTCOPYPEN R2   | Aucune ligne visible    |
| \_NOTMASKPEN R2   | Aucune ligne visible    |
| \_NOTMERGEPEN R2  | Ligne noire visible |
| \_NOTXORPEN R2    | Ligne noire visible |
| \_Blanc R2        | Aucune ligne visible    |
| \_XORPEN R2       | Aucune ligne visible    |



 

Pour un périphérique de couleur, GDI utilise des valeurs RVB pour représenter les couleurs du stylet et de la destination. Une valeur de couleur RVB est un entier long qui contient un champ de couleur rouge, vert et bleu, chacun spécifiant l’intensité de la couleur spécifiée. Les intensités sont comprises entre 0 et 255. Les valeurs sont compressées dans les trois octets de poids faible de l’entier long. La couleur d’un stylet est toujours une couleur unie, mais la couleur de la destination peut être un mélange de deux ou trois couleurs. Si une application tente de dessiner avec un stylet blanc sur une destination bleue à l’aide des opérations raster binaires disponibles, les résultats suivants se produisent.



| Opération Raster | Résultats                 |
|------------------|------------------------|
| R2 \_ noir        | Ligne noire visible     |
| \_COPYPEN R2      | Ligne blanche visible     |
| \_MASKNOTPEN R2   | Ligne noire visible     |
| \_MASKPEN R2      | Ligne bleue invisible    |
| \_MASKPENNOT R2   | Trait rouge/vert visible |
| \_MERGENOTPEN R2  | Ligne bleue invisible    |
| \_MERGEPEN R2     | Ligne blanche visible     |
| \_MERGEPENNOT R2  | Ligne blanche visible     |
| R2 \_ NOP          | Ligne bleue invisible    |
| R2 \_ non          | Trait rouge/vert visible |
| \_NOTCOPYPEN R2   | Ligne noire visible     |
| \_NOTMASKPEN R2   | Trait rouge/vert visible |
| \_NOTMERGEPEN R2  | Ligne noire visible     |
| \_NOTXORPEN R2    | Ligne bleue invisible    |
| \_Blanc R2        | Ligne blanche visible     |
| \_XORPEN R2       | Trait rouge/vert visible |



 

 

 



