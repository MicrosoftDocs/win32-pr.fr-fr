---
description: Direct3D 10 prend en charge plusieurs représentations à virgule flottante différentes. Tous les calculs à virgule flottante fonctionnent sous un sous-ensemble défini du comportement à virgule flottante simple précision IEEE 754 32 bits.
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: Règles de point FFloating (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7f575810b1efb1bde65dd1c80de98837a0a0274c6b394207b612874f289054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100981"
---
# <a name="floating-point-rules-direct3d-10"></a>Règles à virgule flottante (Direct3D 10)

Direct3D 10 prend en charge plusieurs représentations à virgule flottante différentes. Tous les calculs à virgule flottante fonctionnent sous un sous-ensemble défini du comportement à virgule flottante simple précision IEEE 754 32 bits.

-   [Règles de Floating-Point bits 32](#32-bit-floating-point-rules)
    -   [Règles IEEE-754 honorées](#honored-ieee-754-rules)
    -   [Écarts ou exigences supplémentaires des règles IEEE-754](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [Règles de Floating-Point 16 bits](#16-bit-floating-point-rules)
-   [Règles de Floating-Point 11 bits et 10 bits](#11-bit-and-10-bit-floating-point-rules)
-   [Rubriques connexes](#related-topics)

## <a name="32-bit-floating-point-rules"></a>Règles de Floating-Point bits 32

Il existe deux ensembles de règles : ceux qui se conforment à IEEE-754 et ceux qui s’écartent de la norme.

### <a name="honored-ieee-754-rules"></a>Règles IEEE-754 honorées

Certaines de ces règles sont une option unique où IEEE-754 offre des choix.

-   La division par 0 produit +/-INF, à l’exception de 0/0, ce qui donne NaN.
-   le journal de (+/-) 0 produit-INF. le journal d’une valeur négative (autre que-0) produit une valeur NaN.
-   La racine carrée réciproque (rsq) ou la racine carrée (sqrt) d’un nombre négatif produit une valeur NaN. L’exception est-0 ; sqrt (-0) génère-0, et rsq (-0) produit-INF.
-   INF-INF = NaN
-   (+/-) INF/(+/-) INF = NaN
-   (+/-) INF \* 0 = Nan
-   NaN (any OP) any-value = NaN
-   Les comparaisons EQ, GT, GE, LT et LE, lorsque l’un ou l’autre ou les deux opérandes sont NaN, retourne **false**.
-   Les comparaisons ignorent le signe 0 (par conséquent + 0 est égal à-0).
-   La comparaison ne, lorsque l’un des opérandes ou les deux, est NaN retourne la **valeur true**.
-   Les comparaisons de toute valeur non NaN par rapport à +/-INF renvoient le résultat correct.

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>Écarts ou exigences supplémentaires des règles IEEE-754

-   IEEE-754 nécessite des opérations à virgule flottante pour produire un résultat qui est la valeur représentable la plus proche d’un résultat à précision infinie, connu sous le nom d’arrondi à le plus proche, même. Direct3D 10, cependant, définit une exigence plus faible : les opérations à virgule flottante 32 bits produisent un résultat qui se trouve dans une unité-Last-place (1 ULP) du résultat infini. Cela signifie que, par exemple, le matériel est autorisé à tronquer les résultats à 32 bits plutôt qu’à effectuer un arrondi vers le plus proche, même si cela entraînerait une erreur d’au plus un ULP.
-   Il n’existe aucune prise en charge des exceptions à virgule flottante, des bits d’État ou des interruptions.
-   Les dénormes sont vidées du zéro protégé contre la signature lors de l’entrée et de la sortie d’une opération mathématique à virgule flottante. Des exceptions sont faites pour toute opération de déplacement de données ou d’e/s qui ne manipule pas les données.
-   Les États qui contiennent des valeurs à virgule flottante, telles que Viewport MinDepth/MaxDepth, BorderColor Values, etc., peuvent être fournis comme valeurs de dénorme et peuvent ou non être vidés avant d’être utilisés par le matériel.
-   Les opérations min ou Max vident les dénormes pour la comparaison, mais le résultat peut ou non être vidé de la norme.
-   L’entrée NaN d’une opération produit toujours une valeur NaN à la sortie, mais le modèle binaire exact de la valeur NaN n’est pas requis pour rester le même (sauf si l’opération est une instruction Move brute, qui ne modifie pas les données du tout.)
-   Les opérations min ou Max pour lesquelles un seul opérande est NaN retournent l’autre opérande en tant que résultat (contrairement aux règles de comparaison ci-dessus). Il s’agit d’une nouvelle règle IEEE (IEEE 754R), requise dans Direct3D 10.
-   Une autre nouvelle règle IEEE 754R est que min (-0, + 0) = = min (+ 0,-0) = =-0, et Max (-0, + 0) = = max (+ 0,-0) = = + 0, ce qui respecte le signe, contrairement aux règles de comparaison pour le zéro signé (indiqué ci-dessus). Direct3D 10 recommande le comportement IEEE 754R, mais il ne sera pas appliqué. Il est possible que le résultat de la comparaison des zéros dépende de l’ordre des paramètres, à l’aide d’une comparaison qui ignore les signes.
-   x \* 1.0 f aboutit toujours à x (sauf denorme Flush).
-   x/1.0 a toujours pour résultat x (à l’exception de la dénorme Flush).
-   x +/-0.0 f produit toujours x (à l’exception de la dénorme Flush). Mais-0 + 0 = + 0.
-   Les opérations fusionnées (par exemple, Mad, DP3) produisent des résultats qui ne sont pas moins précis que le plus mauvais ordonnancement en série de l’évaluation de l’expansion déroutée de l’opération. Notez que la définition du pire ordonnancement possible, pour des raisons de tolérance, n’est pas une définition fixe pour une opération fusionnée donnée. elle dépend des valeurs particulières des entrées. Les étapes individuelles de l’expansion sans fusible sont chacune autorisées 1 tolérance ULP (ou pour toutes les instructions Direct3D 10 appelle avec une tolérance plus Lax que 1 ULP, la tolérance la plus LAX est autorisée).
-   Les opérations fusionnées adhèrent aux mêmes règles NaN que les opérations non fusionnées.
-   Multiplier et diviser chaque fonctionnent au niveau de précision à virgule flottante 32 bits (précision à 1 ULP).

## <a name="16-bit-floating-point-rules"></a>Règles de Floating-Point 16 bits

Direct3D 10 prend également en charge les représentations 16 bits des nombres à virgule flottante.

Format:

-   1 bit (s) de signe dans la position de bit du MSB
-   5 bits d’exposant biaisé (e)
-   10 bits de fraction (f), avec un bit masqué supplémentaire

Une valeur float16 (v) respecte les règles suivantes :

-   Si e = = 31 et f ! = 0, alors v est NaN indépendamment de s
-   Si e = = 31 et f = = 0, v = (-1) s \* infini (infini signé)
-   Si e est compris entre 0 et 31, v = (-1) s \* 2 (e-15) \* (1. f)
-   Si e = = 0 et f ! = 0, alors v = (-1) s \* 2 (e-14) \* (0. f) (nombres dénormalisés)
-   Si e = = 0 et f = = 0, v = (-1) s \* 0 (zéro signé)

les règles à virgule flottante 32 bits sont également conservées pour les nombres à virgule flottante 16 bits, ajustées pour la disposition en bits décrite ci-dessus. Les exceptions à cette règle sont les suivantes :

-   Précision : les opérations non ancrées sur les nombres à virgule flottante 16 bits produisent un résultat qui est la valeur représentable la plus proche d’un résultat à précision infinie (arrondi au plus proche pair, par IEEE-754, appliqué aux valeurs 16 bits). les règles à virgule flottante 32 bits adhèrent à 1 tolérance ULP, les règles à virgule flottante de 16 bits adhèrent à 0,5 ULP pour les opérations non fusionnées et 0,6 ULP pour les opérations fusionnées.
-   les nombres à virgule flottante 16 bits préservent les dénormes.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>Règles de Floating-Point 11 bits et 10 bits

Direct3D 10 prend également en charge les formats à virgule flottante 11 bits et 10 bits.

Format:

-   Aucun bit de signe
-   5 bits d’exposant biaisé (e)
-   6 bits de fraction (f) pour un format 11 bits, 5 bits de fraction (f) pour un format 10 bits, avec un bit masqué supplémentaire dans les deux cas.

Une valeur float11/float10 (v) respecte les règles suivantes :

-   Si e = = 31 et f ! = 0, alors v est NaN
-   Si e = = 31 et f = = 0, alors v = + Infinity
-   Si e est compris entre 0 et 31, v = 2 (e-15) \* (1. f)
-   Si e = = 0 et f ! = 0, alors v = \* 2 (e-14) \* (0. f) (nombres dénormalisés)
-   Si e = = 0 et f = = 0, alors v = 0 (zéro)

les règles à virgule flottante 32 bits contiennent également des nombres à virgule flottante de 11 et 10 bits, ajustés pour la disposition en bits décrite ci-dessus. Voici certaines exceptions :

-   Précision : les règles à virgule flottante 32 bits adhèrent à 0,5 ULP.
-   les nombres à virgule flottante 10/11 bits préservent les dénormes.
-   Toute opération qui aboutirait à un nombre inférieur à zéro est ancrée à zéro.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



