---
description: Pour bien comprendre un nuanceur qui implémente PRT, il est utile de dériver la formule utilisée par le nuanceur pour calculer Exit luminance.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Équations PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd3dc716349ce46d4e678f0e408e5c964eb5f01d633649e3d512db6115c0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798170"
---
# <a name="prt-equations-direct3d-9"></a>Équations PRT (Direct3D 9)

Pour bien comprendre un nuanceur qui implémente PRT, il est utile de dériver la formule utilisée par le nuanceur pour calculer Exit luminance.

Pour commencer, l’équation suivante est l’équation générale permettant de calculer les luminance de sortie résultant d’un éclairage direct sur un objet diffus avec un éclairage distant arbitraire.

![équation de l’luminance de sortie résultant d’un éclairage direct sur un objet diffus avec un éclairage distant arbitraire](images/prt-theory-eq1.png)

où :



| Paramètre     | Description                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| PR            | Luminance de sortie au sommet p. Évalué à chaque vertex sur la maille.                                   |
| p<sub>d</sub> | Albedo de l’aire.                                                                              |
| pi            | Constante, utilisée comme facteur de normalisation de la conservation de l’énergie.                                        |
| L (s)          | Environnement d’éclairage (source luminance).                                                             |
| VP ₍ s ₎         | Fonction de visibilité binaire pour le point p. La valeur est 1 si le point peut voir la lumière, 0 dans le cas contraire.             |
| HNP ₍ s ₎        | Terme cosinus de la Loi de Lambert. Égal à Max ((NP · s), 0) où NP correspond à la surface normale au point p. |
| s             | Variable qui s’intègre sur la sphère.                                                           |



 

À l’aide de fonctions sphériques, telles que les harmoniques sphériques, l’équation suivante est proche de l’environnement d’éclairage.

![équation de l’environnement d’éclairage](images/prt-theory-eq2.png)

où :



| Paramètre        | Description                                              |
|------------------|----------------------------------------------------------|
| L (s)             | Environnement d’éclairage (source luminance).              |
| i                | Entier qui totalise le nombre de fonctions de base. |
| O                | Ordre des harmoniques sphériques.                        |
| l<sub></sub>    | Un coefficient.                                           |
| Y<sub>(s)</sub> | Certaines fonctions de base sur la sphère.                     |



 

La collection de ces coefficients, L', fournit la approximation optimale pour la ou les fonctions L avec les fonctions de base Y (s). Le remplacement et la distribution produisent l’équation suivante.

![équation de l’luminance de sortie après remplacement de l (s) et distribution](images/prt-theory-eq3.png)

L’intégrale de Y<sub>i (s)</sub>VP ₍ s ₎ HNP ₍ s ₎ est un coefficient de transfert t<sub>pi</sub> que le simulateur Précalcule pour chaque vertex sur la maille. La substitution de ce code génère l’équation suivante.

![équation de Exit luminance après avoir remplacé le coefficient de transfert](images/prt-theory-eq4.png)

La modification de cette notation vectorielle produit l’équation non compressée suivante pour calculer les luminance de sortie pour chaque canal.

![équation de Exit luminance après avoir changé en notation Vector](images/prt-theory-eq5.png)

où :



| Paramètre     | Description                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PR            | Luminance de sortie au sommet p.                                                                                                                                                      |
| p<sub>d</sub> | Albedo de l’aire.                                                                                                                                                          |
| Budget            | Le vecteur de l<sub>i</sub>et est la projection de la source luminance dans les fonctions de base d’harmoniques sphériques. Il s’agit d’un vecteur de commande ² de coefficients d’harmonique sphérique. |
| PM            | Vecteur de transfert de commande ² pour le vertex p. Le simulateur divise les coefficients de transfert par p.                                                                                       |



 

Ces deux vecteurs sont un vecteur de commande ² de coefficients d’harmonique sphérique. Notez donc qu’il s’agit simplement d’un point. En fonction de la commande, le point peut être coûteux afin que la compression puisse être utilisée. Un algorithme appelé CPCA (cluster principal Component Analysis) compresse efficacement les données. Cela permet l’utilisation d’une approximation d’harmonique sphérique d’ordre supérieur qui produit des ombres plus nettes.

CPCA fournit l’équation suivante pour rapprocher le vecteur de transfert.

![équation du vecteur de transfert approximatif](images/prt-theory-eq6.png)

où :



| Paramètre      | Description                                          |
|----------------|------------------------------------------------------|
| PM             | Vecteur de transfert pour le vertex p.                    |
| MK             | Moyenne du cluster k.                              |
| j              | Entier qui additionne le nombre de vecteurs PCA. |
| N              | Nombre de vecteurs PCA.                           |
| w<sub>PJ</sub> | Poids de JTH PCA pour le point p.                      |
| B<sub>kJ</sub> | Le vecteur de base JTH PCA pour le cluster k.              |



 

Un cluster est tout simplement un nombre de vertex qui partagent le même vecteur de moyenne. L’obtention de la moyenne du cluster, des pondérations de l’APC, des vecteurs de base de l’APC et des ID de cluster pour les vertex est décrite ci-dessous.

Le remplacement de ces deux équations donne :

![équation de Exit luminance après avoir remplacé le vecteur de transfert](images/prt-theory-eq7.png)

Ensuite, la distribution du produit scalaire produit l’équation suivante.

![équation de l’luminance de sortie après la distribution du produit scalaire](images/prt-theory-eq8.png)

Parce que les deux (MK · L') et (B<sub>kJ</sub>· L') sont des constantes par vertex, l’exemple calcule ces valeurs avec l’UC et les passe comme constantes dans le nuanceur de sommets. étant donné que w<sub>PJ</sub> change pour chaque vertex, l’exemple stocke ces données par vertex dans la mémoire tampon de vertex.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transfert de luminance précalculé](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



