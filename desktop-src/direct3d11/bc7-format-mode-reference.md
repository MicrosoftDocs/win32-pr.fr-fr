---
title: Référence du mode de format BC7
description: Cette documentation contient la liste des 8 modes de blocage et des allocations de bits pour les blocs de format de compression de texture BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f96bfd9c90697b47587048684239ecf084dd43a76e0ef76b9717fe09d3b3630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126164"
---
# <a name="bc7-format-mode-reference"></a>Référence du mode de format BC7

Cette documentation contient la liste des 8 modes de blocage et des allocations de bits pour les blocs de format de compression de texture BC7.

Les couleurs de chaque sous-ensemble au sein d’un bloc sont représentées par deux couleurs de point de terminaison explicites et un ensemble de couleurs interpolées entre elles. Selon la précision de l’index du bloc, chaque sous-ensemble peut avoir 4, 8 ou 16 couleurs possibles.

-   [Mode 0](#mode-0)
-   [Mode 1](#mode-1)
-   [Mode 2](#mode-2)
-   [Mode 3](#mode-3)
-   [Mode 4](#mode-4)
-   [Mode 5](#mode-5)
-   [Mode 6](#mode-6)
-   [Mode 7](#mode-7)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="mode-0"></a>Mode 0

Le mode BC7 0 présente les caractéristiques suivantes :

-   Composants de couleur uniquement (sans alpha)
-   3 sous-ensembles par bloc
-   Points de terminaison RGBP 4.4.4.1 avec un bit P unique par point de terminaison
-   index 3 bits
-   16 partitions

![disposition en mode 0 bits](images/bc7-mode0.png)

## <a name="mode-1"></a>Mode 1

BC7 mode 1 présente les caractéristiques suivantes :

-   Composants de couleur uniquement (sans alpha)
-   2 sous-ensembles par bloc
-   Points de terminaison RGBP 6.6.6.1 avec un bit P partagé par sous-ensemble)
-   index 3 bits
-   64 partitions

![disposition 1 bit mode](images/bc7-mode1.png)

## <a name="mode-2"></a>Mode 2

Le mode BC7 2 présente les caractéristiques suivantes :

-   Composants de couleur uniquement (sans alpha)
-   3 sous-ensembles par bloc
-   Points de terminaison 5.5.5 RVB
-   index 2 bits
-   64 partitions

![disposition en mode 2 bits](images/bc7-mode2.png)

## <a name="mode-3"></a>Mode 3

Le mode BC7 3 présente les caractéristiques suivantes :

-   Composants de couleur uniquement (sans alpha)
-   2 sous-ensembles par bloc
-   Points de terminaison RGBP 7.7.7.1 avec un bit P unique par sous-ensemble)
-   index 2 bits
-   64 partitions

![disposition en mode 3 bits](images/bc7-mode3.png)

## <a name="mode-4"></a>Mode 4

Le mode BC7 4 présente les caractéristiques suivantes :

-   Composants de couleur avec composant alpha distinct
-   1 sous-ensemble par bloc
-   Points de terminaison de couleur RVB 5.5.5
-   points de terminaison alpha 6 bits
-   16 x index 2 bits
-   16 x index 3 bits
-   rotation des composants 2 bits
-   sélecteur d’index 1 bit (si les index à 2 ou 3 bits sont utilisés)

![disposition en mode 4 bits](images/bc7-mode4.png)

## <a name="mode-5"></a>Mode 5

Le mode BC7 5 présente les caractéristiques suivantes :

-   Composants de couleur avec composant alpha distinct
-   1 sous-ensemble par bloc
-   Points de terminaison de couleur RVB 7.7.7
-   points de terminaison alpha 8 bits
-   16 x index de couleurs 2 bits
-   16 x index alpha 2 bits
-   rotation des composants 2 bits

![disposition en mode 5 bits](images/bc7-mode5.png)

## <a name="mode-6"></a>Mode 6

Le mode BC7 6 présente les caractéristiques suivantes :

-   Composants de couleur et alpha combinés
-   Un seul sous-ensemble par bloc
-   Points de terminaison de couleur RGBAP 7.7.7.7.1 (et alpha) (P-bit unique par point de terminaison)
-   16 x index 4 bits

![disposition en mode 6 bits](images/bc7-mode6.png)

## <a name="mode-7"></a>Mode 7

Le mode BC7 7 présente les caractéristiques suivantes :

-   Composants de couleur et alpha combinés
-   2 sous-ensembles par bloc
-   Points de terminaison de couleur RGBAP 5.5.5.5.1 (et alpha) (P-bit unique par point de terminaison)
-   index 2 bits
-   64 partitions

![disposition en mode 7 bits](images/bc7-mode7.png)

## <a name="remarks"></a>Remarques

Le mode 8 (l’octet le moins significatif est défini sur 0x00) est réservé. Ne l’utilisez pas dans votre encodeur. Si vous transmettez ce mode au matériel, un bloc initialisé à tous les zéros est retourné.

Dans BC7, vous pouvez encoder le composant alpha de l’une des manières suivantes :

-   Types de bloc sans encodage de composant alpha explicite. Dans ces blocs, les points de terminaison de couleur ont un encodage RVB uniquement, le composant alpha étant décodé sur 1,0 pour tous les éléments de texture.
-   Types de blocs avec des composants alpha et de couleur combinés. Dans ces blocs, les valeurs de couleur du point de terminaison sont spécifiées au format RVBA et les valeurs des composants alpha sont interpolées avec les valeurs de couleur.
-   Types de bloc avec des composants alpha et de couleur séparés. Dans ces blocs, les valeurs de couleur et alpha sont spécifiées séparément, chacune avec son propre jeu d’index. Par conséquent, ils ont un vecteur effectif et un canal scalaire qui sont encodés séparément, où le vecteur spécifie généralement les canaux \[ de couleur R, G, B \] et le scalaire spécifie le canal alpha \[ a \] . Pour prendre en charge cette approche, un champ 2 bits distinct est fourni dans l’encodage, qui permet la spécification de l’encodage de canal distinct comme valeur scalaire. Par conséquent, le bloc peut avoir l’une des quatre représentations suivantes de cet encodage alpha (comme indiqué par le champ de 2 bits) :
    -   RVB \| A : canal alpha distinct
    -   AGB \| R : canal de couleur « rouge » distinct
    -   RAB \| G : canal de couleur « vert » distinct
    -   RGA \| B : canal de couleur « bleu » distinct

    Le décodeur réorganise l’ordre des canaux à la valeur RVBA après le décodage, de sorte que le format de bloc interne est invisible pour le développeur. Les blocs avec des composants alpha et de couleur distincts ont également deux jeux de données d’index : un pour l’ensemble vectorisé de canaux et un pour le canal scalaire. (Dans le cas du mode 4, ces index sont de largeur différente de \[ 2 ou 3 bits \] . Le mode 4 contient également un sélecteur 1 bit qui spécifie si le vecteur ou le canal scalaire utilise les index 3 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format BC7](bc7-format.md)
</dt> </dl>

 

 




