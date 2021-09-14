---
description: Transition de réinitialisation SMPTE
ms.assetid: 9271bd4b-57b1-4b1b-bfee-d6ae5f49a154
title: Transition de réinitialisation SMPTE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47de62c450ff0d75f72e5fac466801991b987834
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240696"
---
# <a name="smpte-wipe-transition"></a>Transition de réinitialisation SMPTE

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La transition de réinitialisation SMPTE produit l’une des réinitialisations standard définies par la société des ingénieurs d’images et de télévision (SMPTE) dans le document SMPTE 258M-1993, à l’exception de la fonction Quad Split.

![transition de réinitialisation en cours](images/trans-wipe.png)

ID de classe (CLSID) : {DE75D012-7A65-11D2-8CEA-00A0C9441E20}

Nom de la variable CLSID : CLSID \_ DxtJpeg

Nom convivial : « DxtJpeg »

Propriétés



| Propriété       | Type   | Default  | Description                                                                                                                                                                                                                                                                                                      |
|----------------|--------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BorderColor    | long   | 0x000000 | Couleur de la bordure autour des bords du motif de la réinitialisation. La valeur de cet attribut est un nombre hexadécimal au format 0x *RRVVBB*, où *RR* est la valeur rouge, *GG* est la valeur verte et *BB* est la valeur bleue. (Par conséquent, le rouge pur, le vert et le bleu sont 0xFF000, 0x00FF00 et 0x0000FF, respectivement). |
| BorderSoftness | long   | 0        | Largeur de la zone floue autour des bords du modèle de réinitialisation. Spécifiez zéro pour aucune zone floue.                                                                                                                                                                                                              |
| BorderWidth    | long   | 0        | Largeur de la bordure unie le long des bords du motif de la réinitialisation. Spécifiez zéro pour aucune bordure.                                                                                                                                                                                                                       |
| MaskName       | BSTR   | **NULL** | Si la **valeur** n’est pas null, spécifie le nom d’un fichier JPEG à utiliser comme masque de réinitialisation au lieu d’une réinitialisation standard intégrée. Le fichier doit contenir un dégradé monochrome, 8 bits par pixel. Le dégradé est utilisé comme masque pour définir la progression de la réinitialisation.                                                                 |
| MaskNum        | long   | 1        | Code de réinitialisation SMPTE standard spécifiant le style de réinitialisation à utiliser. Pour obtenir la liste des codes de réinitialisation et des schémas associés, consultez le document SMPTE 258M-1993.                                                                                                                                                            |
| OffsetX        | long   | 0        | Décalage horizontal de l’origine de la réinitialisation à partir du centre de l’image. Valide uniquement pour les valeurs de **MaskNum** allant de 101 à 131.                                                                                                                                                                                         |
| OffsetY        | long   | 0        | Décalage Verical de l’origine de la réinitialisation à partir du centre de l’image. Valide uniquement pour les valeurs de **MaskNum** allant de 101 à 131.                                                                                                                                                                                            |
| ReplicateX     | long   | 0        | Nombre de fois où le modèle de réinitialisation doit être répliqué horizontalement. Valide uniquement pour les valeurs de **MaskNum** allant de 101 à 131.                                                                                                                                                                                                |
| À répliquer     | long   | 0        | Nombre de réplications verticales du modèle de réinitialisation. Valide uniquement pour les valeurs de **MaskNum** allant de 101 à 131.                                                                                                                                                                                                  |
| Scale         | double | 1.0      | Quantité d’étirement horizontal de la réinitialisation, en pourcentage de la définition de la réinitialisation d’origine. Valide uniquement pour les valeurs de **MaskNum** allant de 101 à 131.                                                                                                                                                         |
| ScaleY         | double | 1.0      | Quantité d’étirement de la réinitialisation verticale, en pourcentage de la définition de la réinitialisation d’origine. Valide uniquement pour les valeurs de **MaskNum** allant de 101 à 131.                                                                                                                                                           |



 

## <a name="remarks"></a>Notes

Cette transition prend en charge les réinitialisations SMPTE standard suivantes :



| Number | Description                   | Number | Description                                 |
|--------|-------------------------------|--------|---------------------------------------------|
| 1      | Horizontal                    | 211    | Radial, gauche à droite, haut                     |
| 2      | Vertical                      | 212    | Radial, haut-haut, droite                      |
| 3      | En haut à gauche                    | 213    | Radial, de gauche à droite, en haut en bas              |
| 4      | En haut à droite                   | 214    | Radial, haut-descendant, gauche à droite                 |
| 5      | En bas à droite                   | 221    | Radial, haut                                 |
| 6      | En bas à gauche                    | 222    | Radial, droite                               |
| 7      | Quatre coins                  | 223    | Radial, bas                              |
| 8      | Quatre carrés                  | 224    | Radial, gauche                                |
| 21     | Portes de poules, verticales          | 225    | Radial, en haut à gauche, en bas à gauche     |
| 22     | Portes de poule, horizontale        | 226    | Radial, gauche dans le sens des aiguilles d’une montre     |
| 23     | Centre en haut                    | 227    | Radial, en haut à gauche, en bas à gauche |
| 24     | Au centre à droite                  | 228    | Radial, à gauche, à droite dans le sens inverse des aiguilles d’une montre |
| 25     | En bas au centre                 | 231    | Radial, fractionnement supérieur                           |
| 26     | Au centre à gauche                   | 232    | Radial, fractionnement à droite                         |
| 41     | Diagonale, NW à SE            | 233    | Fractionnement radial, bas                        |
| 42     | Diagonale, ne to SW            | 234    | Fractionnement radial, à gauche                          |
| 43     | Triangles, haut/bas         | 235    | Fractionnement radial, haut en bas                    |
| 44     | Triangles, gauche/droite         | 236    | Fractionnement radial, gauche-droite                    |
| 45     | Bande diagonale, SW vers ne     | 241    | Radial, coin supérieur gauche                     |
| 46     | Bande diagonale, NW à SE     | 242    | Radial, angle inférieur gauche                  |
| 47     | Croix                         | 243    | Radial, en bas à droite                 |
| 48     | Zone losange                   | 244    | Radial, coin supérieur droit                    |
| 61     | Coin, haut                    | 245    | Radial, en haut à gauche, en bas à droite              |
| 62     | Coin, droite                  | 246    | Radial, en bas à gauche, en haut à droite              |
| 63     | Coin, bas                 | 251    | Centrer radial, haut                          |
| 64     | Coin gauche                   | 252    | Radial Center, gauche                         |
| 65     | V                             | 253    | Centrer radial, bas                       |
| 66     | V, droite                      | 254    | Centrer radial, droite                        |
| 67     | V, inversé                   | 261    | Box radial, droite                           |
| 68     | V, gauche                       | 262    | Box radial, haut                             |
| 71     | Scie, gauche                | 263    | Centrer radial, haut, bas                  |
| 72     | Scie, haut                 | 264    | Centrer radial, gauche, droite                  |
| 73     | Scie, vertical            | 301    | Matrice, horizontal                          |
| 74     | Scie, horizontal          | 302    | Matrice, vertical                            |
| 101    | Box                           | 303    | Matrice, diagonale, haut à gauche                  |
| 102    | Losange                       | 304    | Matrice, diagonale, en haut à droite                 |
| 103    | Triangle, haut                  | 305    | Matrice, diagonale, bas à droite              |
| 104    | Triangle, droite               | 306    | Matrice, diagonale, bas à gauche               |
| 105    | Triangle, bas              | 310    | Matrice, en haut à gauche                  |
| 106    | Triangle, gauche                | 311    | Matrix, en haut à droite                 |
| 107    | Tête de flèche, haut                | 312    | Matrice, en bas à droite              |
| 108    | En-tête de flèche, droite             | 313    | Matrix, en bas à gauche               |
| 109    | Tête de flèche, bas              | 314    | Matrice, antihoraire en haut à gauche              |
| 110    | En-tête de flèche, à gauche              | 315    | Matrice, antihoraire en haut à droite             |
| 111    | Pentagone, haut                  | 316    | Matrice, antihoraire en bas à droite          |
| 112    | Pentagone, vers le                | 317    | Matrice, antihoraire en bas à gauche           |
| 113    | Hexagone                       | 320    | Matrice, vertical en haut à gauche, en haut à droite        |
| 114    | Hexagone, pivoté              | 321    | Matrice, vertical en bas à gauche, en bas à droite  |
| 119    | Circle                        | 322    | Matrice, vertical en haut à gauche, en bas à droite     |
| 120    | Ovale, horizontal              | 323    | Matrice, vertical en bas à gauche, en haut à droite     |
| 121    | Ovale, vertical                | 324    | Matrice, horizontal en haut à gauche, en bas à gauche    |
| 122    | Œil, horizontal               | 325    | Matrice, horizontal en haut à droite, en bas à droite  |
| 123    | Œil, vertical                 | 326    | Matrice, horizontal en haut à gauche, en bas à droite   |
| 124    | Rectangle à coins arrondis, horizontal | 327    | Matrice, horizontal en haut à droite, en bas à gauche   |
| 125    | Rectangle à coins arrondis, vertical   | 328    | Matrice, diagonale en bas à gauche, en haut à droite     |
| 127    | étoile à 4 branches                  | 329    | Matrice, diagonale en haut à gauche, en bas à droite     |
| 128    | étoile à 4 branches                  | 340    | Matrice, double spirale                   |
| 129    | étoile à 6 branches                  | 341    | Matrice, bas double spirale                |
| 130    | Cœur                         | 342    | Matrice, double spirale gauche                  |
| 131    | Keyhole                       | 343    | Matrix, double spirale droite                 |
| 201    | Radial, 12 heures            | 344    | Matrice, quadruple spirale, haut en bas             |
| 202    | Radial, 3 heures             | 345    | Matrice, quadruple spirale, gauche à droite             |
| 203    | Radial, 6 heures             | 350    | En cascade, à gauche                             |
| 204    | Radial, 9 heures             | 351    | En cascade, à droite                            |
| 205    | Radial, 12 + 6 heures        | 352    | Cascade, horizontal, gauche                 |
| 206    | Radial, 3 + 9 heures         | 353    | Cascade, horizontal, droite                |
| 207    | Radial, 4 voies                 | 409    | Masque aléatoire                                 |



 

 

 



