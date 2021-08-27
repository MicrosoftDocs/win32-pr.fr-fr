---
description: Les sections suivantes décrivent comment Direct3D gère les conversions entre les types de données.
ms.assetid: 454d3fd0-fc0f-46a9-925e-13f8e3c39f02
title: Règles de conversion des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b5ba37305fb7cadc229a614b883519cf6c5f45
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626295"
---
# <a name="data-conversion-rules"></a>Règles de conversion des données

Les sections suivantes décrivent comment Direct3D gère les conversions entre les types de données.

-   [Terminologie des types de données](#data-type-terminology)
-   [Conversion à virgule flottante](#floating-point-conversion)
    -   [Conververting d’une représentation de plage supérieure à une représentation de plage inférieure](#conververting-from-a-higher-range-representation-to-a-lower-range-representation)
    -   [Conversion d’une représentation de plage inférieure en une représentation de plage supérieure](#converting-from-a-lower-range-representation-to-a-higher-range-representation)
-   [Conversion d’entier](#integer-conversion)
-   [Conversion d’entier à virgule fixe](#fixed-point-integer-conversion)
-   [Rubriques connexes](#related-topics)

## <a name="data-type-terminology"></a>Terminologie des types de données

Les termes suivants sont utilisés par la suite pour caractériser diverses conversions de format.



| Terme  | Définition                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RONFLEr | Entier normalisé signé, ce qui signifie que pour le numéro de complément de n bits 2, la valeur maximale correspond à 1,0 f (par exemple, la valeur de 5 bits 01111 correspond à 1.0 f), et la valeur minimale signifie-1.0 f (par exemple, la valeur 5 bits 10000 correspond à-1.0 f). En outre, le deuxième nombre minimal est mappé à-1.0 f (par exemple, la valeur 5 bits 10001 est mappée à-1.0 f). Il y a donc deux représentations entières pour-1.0 f. Il existe une représentation unique pour 0.0 f, et une représentation unique pour 1.0 f. Cela génère un ensemble de représentations entières pour les valeurs à virgule flottante uniformément espacées dans la plage (-1,0 f... 0.0 f) et également un ensemble complémentaire de représentations pour les nombres dans la plage (0.0 f... supérieures |
| UNORM | Entier normalisé non signé, ce qui signifie que pour un nombre n bits, tous les 0 signifient 0.0 f, et tous les 1 signifient 1,0 f. Une séquence de valeurs à virgule flottante uniformément espacées de 0.0 f à 1.0 f est représentée. par exemple, un UNORM de 2 bits représente 0.0 f, 1/3, 2/3 et 1,0 f.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Saint  | Entier signé. entier du complément 2. par exemple, un Saint-octet 3 bits représente les valeurs intégrales-4,-3,-2,-1, 0, 1, 2, 3.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| UINT  | Entier non signé. par exemple, un UINT de 3 bits représente les valeurs intégrales 0, 1, 2, 3, 4, 5, 6, 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| FLOAT | Valeur à virgule flottante dans l’une des représentations définies par Direct3D.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SRVB  | Semblable à UNORM, dans le cas d’un nombre n bits, les 0 signifient 0.0 f et tous les 1 signifient 1,0 f. Toutefois, contrairement à UNORM, avec sRVB, la séquence d’encodages d’entiers non signés entre tous les 0 de tous les 1 représente une progression non linéaire dans l’interprétation à virgule flottante des nombres, comprise entre 0.0 f et 1,0 f. En gros, si cette progression non linéaire, sRVB, est affichée sous la forme d’une séquence de couleurs, elle apparaît sous la forme d’une rampe linéaire des niveaux de luminosité pour un observateur « moyen », sous les conditions d’affichage « moyennes », sur un affichage « moyen ». Pour obtenir des détails complets, reportez-vous à la norme de couleurs sRVB, IEC 61996-2-1, à l’adresse CEI (Commission Électrotechnique Internationale).                |



 

## <a name="floating-point-conversion"></a>Conversion à virgule flottante

À chaque fois qu’une conversion à virgule flottante entre différentes représentations se produit, y compris vers ou à partir de représentations à virgule non flottante, les règles suivantes s’appliquent.

### <a name="conververting-from-a-higher-range-representation-to-a-lower-range-representation"></a>Conververting d’une représentation de plage supérieure à une représentation de plage inférieure

-   L’arrondi à zéro est utilisé lors de la conversion vers un autre format float. Si la cible est un format d’entier ou de point fixe, l’arrondi vers le le plus proche est utilisé, à moins que la conversion soit explicitement documentée comme utilisant un autre comportement d’arrondi, tel que l’arrondi au RONFLEment le plus proche de la virgule FLOTTante, la valeur float à UNORM ou la valeur FLOAT à sRVB. D’autres exceptions sont les instructions de nuanceur ftoi et ftou, qui utilisent l’arrondi à zéro. Enfin, les conversions de type float vers Fixed utilisées par l’échantillonneur de texture et le rastériseur ont une tolérance spécifiée mesurée en unités en dernier lieu à partir d’une solution idéale de précision infinie.
-   Pour les valeurs sources supérieures à la plage dynamique d’un format cible de plage inférieure (par exemple, une grande valeur flottante de 32 bits est écrite dans une RenderTarget flottante de 16 bits), la valeur maximale représentable (correctement signée), à l’exclusion de l’infini signé (en raison de l’arrondi à zéro décrit ci-dessus).
-   Une valeur NaN dans un format de plage plus élevé est convertie en représentation NaN dans le format de plage inférieure si la représentation NaN existe dans le format de plage inférieure. Si le format inférieur n’a pas de représentation NaN, le résultat sera 0.
-   Le fichier INF dans un format de plage plus élevé est converti en fichier INF au format de plage inférieure, s’il est disponible. Si le format inférieur n’a pas de représentation INF, il sera converti en valeur maximale pouvant être représentée. Le signe sera préservé s’il est disponible dans le format cible.
-   La dénorme dans un format de plage plus élevé est convertie en représentation dérespectee dans le format de plage inférieure, si elle est disponible dans le format de plage inférieur et que la conversion est possible ; sinon, le résultat est 0. Le bit de signe sera préservé s’il est disponible dans le format cible.

### <a name="converting-from-a-lower-range-representation-to-a-higher-range-representation"></a>Conversion d’une représentation de plage inférieure en une représentation de plage supérieure

-   La valeur NaN dans un format de plage inférieure est convertie en représentation NaN dans le format de plage supérieur, si elle est disponible dans le format de plage supérieur. Si le format de plage supérieur n’a pas de représentation NaN, il sera converti en 0.
-   Le fichier INF dans un format de plage inférieure est converti en une représentation INF dans le format de plage supérieur, s’il est disponible dans le format de plage supérieur. Si le format supérieur n’a pas de représentation INF, il sera converti en valeur maximale pouvant être représentée (MAX \_ float dans ce format). Le signe sera préservé s’il est disponible dans le format cible.
-   La dénorme dans un format de plage inférieure est convertie en une représentation normalisée dans le format de plage le plus élevé, si possible, ou en une représentation dénormalisée dans un format de plage supérieur si la représentation dénormalisée existe. En cas d’échec, si le format de plage supérieur n’a pas de représentation de dénorme, il sera converti en 0. Le signe sera préservé s’il est disponible dans le format cible. Notez que les nombres à virgule flottante 32 bits sont décomptés comme un format sans représentation dénormale (car les dénormes dans les opérations sur les Floats 32 bits se vident pour le signe préservé 0).

## <a name="integer-conversion"></a>Conversion d’entier

Le tableau suivant décrit les conversions de différentes représentations décrites ci-dessus vers d’autres représentations. Seules les conversions qui se produisent réellement dans Direct3D sont affichées.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Type de données source</th>
<th>Type de données de destination</th>
<th>Règle de conversion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RONFLEr</td>
<td>FLOAT</td>
<td>À partir d’une valeur entière n bits représentant la plage signée [-1.0 f à 1.0 f], la conversion en virgule flottante est la suivante.<br/>
<ul>
<li>La valeur la plus négative est mappée à-1.0 f. par exemple, la valeur de 5 bits 10000 est mappée à-1.0 f.</li>
<li>Chaque autre valeur est convertie en valeur float (appelez-la c), puis result = c * (1,0 f/(2 ⁽ ⁿ ⁻ ¹ ⁾-1)). Par exemple, la valeur 5 bits 10001 est convertie en-15 f, puis divisée par 15 15, produisant-1.0 f.</li>
</ul></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>RONFLEr</td>
<td>Étant donné un nombre à virgule flottante, la conversion en valeur entière n bits représentant la plage signée [-1.0 f à 1.0 f] est la suivante.<br/>
<ul>
<li>Supposons que c représente la valeur de départ.</li>
<li>Si c est NaN, le résultat est 0.</li>
<li>Si c > 1.0 f, y compris le fichier INF, il est ancré à 1.0 f.</li>
<li>Si c <-1.0 f, y compris-INF, il est ancré à-1.0 f.</li>
<li>Conversion d’une échelle flottante en échelle d’entier : c = c * (2 ⁿ ⁻ ¹-1).</li>
<li>Convertissez en entier comme suit.
<ul>
<li>Si c >= 0 Then c = c + 0,5 f, sinon, c = c-0,5 f.</li>
<li>Supprimer la fraction décimale, et la valeur à virgule flottante restante (intégrale) est convertie directement en entier.</li>
</ul></li>
</ul>
Cette conversion admet une tolérance de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit-Last-place Unit-Last-place (côté entier). Cela signifie qu’après la conversion de l’échelle float en Integer, toute valeur dans D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unité-Last-place d’une valeur de format cible représentable est autorisée à mapper à cette valeur. L’exigence supplémentaire d’inversion des données garantit que la conversion est nondecreasing dans la plage et que toutes les valeurs de sortie sont réalisables. (Dans les constantes indiquées ici, <em>XX</em> doit être remplacé par la version de Direct3D, par exemple 10, 11 ou 12.)<br/></td>
</tr>
<tr class="odd">
<td>UNORM</td>
<td>FLOAT</td>
<td>La valeur de départ n bits est convertie en valeur float (0.0 f, 1.0 f, 2.0 f, etc.), puis divisée par (2 ⁿ-1).<br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>UNORM</td>
<td>Supposons que c représente la valeur de départ.<br/>
<ul>
<li>Si c est NaN, le résultat est 0.</li>
<li>Si c > 1.0 f, y compris le fichier INF, il est ancré à 1.0 f.</li>
<li>Si c < 0.0 f, y compris-INF, il est ancré à 0.0 f.</li>
<li>Convertir à partir d’une échelle flottante en échelle entière : c = c * (2 ⁿ-1).</li>
<li>Convertir en entier.
<ul>
<li>c = c + 0,5 f.</li>
<li>La fraction décimale est supprimée, et la valeur à virgule flottante restante (intégrale) est convertie directement en entier.</li>
</ul></li>
</ul>
Cette conversion admet une tolérance de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unité-Last-place (côté entier). Cela signifie qu’après la conversion de l’échelle float en Integer, toute valeur dans D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unité-Last-place d’une valeur de format cible représentable est autorisée à mapper à cette valeur. L’exigence supplémentaire d’inversion des données garantit que la conversion est nondecreasing dans la plage et que toutes les valeurs de sortie sont réalisables.<br/></td>
</tr>
<tr class="odd">
<td>SRVB</td>
<td>FLOAT</td>
<td>L’exemple suivant est la conversion d’sRVB en valeur FLOAT idéale.<br/>
<ul>
<li>Prenez la valeur de départ n bits, convertissez-la en une valeur float (0.0 f, 1.0 f, 2.0 f, etc.). appelez ce c.</li>
<li>c = c * (1,0 f/(2 ⁿ-1))</li>
<li>Si (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD) Then : result = c/D3D<em>XX</em>_SRGB_TO_FLOAT_DENOMINATOR_1, Else : Result = ((c + D3D<em>xx</em>_SRGB_TO_FLOAT_OFFSET)/D3D<em>XX</em>_SRGB_TO_FLOAT_DENOMINATOR_2) D3D<em>XX</em>_SRGB_TO_FLOAT_EXPONENT</li>
</ul>
Cette conversion admet une tolérance de D3D<em>xx</em>_SRGB_TO_FLOAT_TOLERANCE_IN_ULP unité-Last-place (côté sRVB). <br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SRVB</td>
<td>Voici la conversion d’sRVB à virgule flottante idéale >.<br/> En supposant que le composant de couleur sRVB cible comporte n bits :<br/>
<ul>
<li>Supposons que la valeur de départ est c.</li>
<li>Si c est NaN, le résultat est 0.</li>
<li>Si c > 1.0 f, y compris le fichier INF, est ancré à 1.0 f.</li>
<li>Si c < 0.0 f, y compris-INF, il est ancré à 0.0 f.</li>
<li>Si (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD) Then : c = d3d<em>XX</em>_FLOAT_TO_SRGB_SCALE_1 * c, Else : c = D3D<em>XX</em>_FLOAT_TO_SRGB_SCALE_2 * c (D3D<em>XX</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/D3D<em>XX</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR)-D3D<em>XX</em>_FLOAT_TO_SRGB_OFFSET</li>
<li>Convertir à partir d’une échelle flottante en échelle entière : c = c * (2 ⁿ-1).</li>
<li>Convertir en entier :
<ul>
<li>c = c + 0,5 f.</li>
<li>La fraction décimale est supprimée, et la valeur à virgule flottante restante (intégrale) est convertie directement en entier.</li>
</ul></li>
</ul>
Cette conversion admet une tolérance de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unité-Last-place (côté entier). Cela signifie qu’après la conversion de l’échelle float en Integer, toute valeur dans D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unité-Last-place d’une valeur de format cible représentable est autorisée à mapper à cette valeur. L’exigence supplémentaire d’inversion des données garantit que la conversion est nondecreasing dans la plage et que toutes les valeurs de sortie sont réalisables.<br/></td>
</tr>
<tr class="odd">
<td>Saint</td>
<td>Saint-est avec plus de bits</td>
<td>Pour effectuer une conversion de Saint-vers-Saint-versa avec plus de bits, le bit le plus significatif (MSB) du numéro de départ est &quot; étendu &quot; aux bits supplémentaires disponibles dans le format cible.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>Saint-est avec plus de bits</td>
<td>Pour convertir un UINT en un Saint-nouveau avec plus de bits, le nombre est copié vers les bits les moins significatifs du format cible (LSBs) et les MSBs supplémentaires sont remplis avec 0.<br/></td>
</tr>
<tr class="odd">
<td>Saint</td>
<td>UINT avec plus de bits</td>
<td>Pour effectuer une conversion de Saint-vers-UINT avec plus de bits : si la valeur est négative, la valeur est ancrée à 0. Sinon, le nombre est copié dans le LSBs du format cible et les MSB supplémentaires sont remplis avec 0.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>UINT avec plus de bits</td>
<td>Pour convertir de UINT en UINT avec plus de bits, le nombre est copié dans le LSBs du format cible et les MSB supplémentaires sont remplis avec 0.<br/></td>
</tr>
<tr class="odd">
<td>Saint-ou-UINT</td>
<td>Saint-ou-UINT avec des bits inférieurs ou égaux</td>
<td>Pour convertir un Saint-ou un UINT en Saint-ou UINT avec des bits inférieurs ou égaux (et/ou modifier l’inscription), la valeur de départ est simplement ancrée à la plage du format cible.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="fixed-point-integer-conversion"></a>Conversion d’entier à virgule fixe

Les entiers à virgule fixe sont simplement des entiers d’une certaine taille de bit qui ont une virgule décimale implicite à un emplacement fixe.

Le type de données « Integer » omniprésent est un cas spécial d’un entier à virgule fixe avec la décimale à la fin du nombre.

Les représentations de nombre à virgule fixe sont caractérisées par : i. f, où i est le nombre de bits entiers et f est le nombre de bits fractionnaires. par exemple, 16,8 signifie 16 bits entier suivi de 8 bits de fraction. La partie entière est stockée dans le complément à 2, au moins comme défini ici (bien qu’elle puisse également être définie de la même façon pour les entiers non signés). La partie fractionnaire est stockée dans un format non signé. La partie fractionnaire représente toujours la fraction positive entre les deux valeurs intégrales les plus proches, en commençant par le plus négatif.

Les opérations d’addition et de soustraction sur les nombres à virgule fixe sont effectuées simplement à l’aide d’une opération arithmétique sur les entiers standard, sans tenir compte de l’endroit où se trouve la virgule implicite. L’ajout de 1 à un nombre à virgule fixe 16,8 signifie simplement l’ajout de 256, puisque la décimale est de 8 emplacements à partir de la fin la moins significative du nombre. D’autres opérations, telles que la multiplication, peuvent être effectuées tout simplement à l’aide d’une opération arithmétique sur les entiers, à condition que l’effet sur la décimale fixe soit pris en compte. Par exemple, la multiplication de deux entiers 16,8 à l’aide d’un nombre entier multiplie produit un résultat 32,16.

Les représentations d’entiers à virgule fixe sont utilisées de deux manières dans Direct3D.

-   Les positions de vertex après découpage dans le rastériseur sont alignées sur le point fixe, afin de répartir uniformément la précision dans la zone RenderTarget. De nombreuses opérations de rastérisation, y compris l’élimination de visage comme exemple, se produisent sur des positions alignées à virgule fixe, tandis que d’autres opérations, telles que la configuration de l’interpolateur d’attribut, utilisent des positions qui ont été reconverties en virgule flottante à partir des positions alignées à virgule fixe.
-   Les coordonnées de texture pour les opérations d’échantillonnage sont alignées sur le point fixe (après avoir été mises à l’échelle en fonction de la taille de la texture), afin de répartir uniformément la précision dans l’espace de texture, en choisissant les emplacements/poids du robinet de filtre. Les valeurs de pondération sont reconverties en virgule flottante avant l’exécution de l’arithmétique de filtrage réelle.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Type de données source</th>
<th>Type de données de destination</th>
<th>Règle de conversion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLOAT</td>
<td>Entier à virgule fixe</td>
<td>Voici la procédure générale de conversion d’un nombre à virgule flottante n en un entier à virgule fixe i. f, où i est le nombre de bits d’entier (signé) et f est le nombre de bits fractionnaires.<br/>
<ul>
<li>Compute FixedMin =-2 ⁽ ⁱ ⁻ ¹ ⁾</li>
<li>Compute FixedMax = 2 ⁽ ⁱ ⁻ ¹ ⁾-2<sup>(-f)</sup></li>
<li>Si n est un NaN, result = 0 ; Si n est + inf, résultat = FixedMax * 2<sup>f</sup>; Si n est-inf, résultat = FixedMin * 2<sup>f</sup></li>
<li>Si n >= FixedMax, result = Fixedmax * 2<sup>f</sup>; Si n <= FixedMin, result = FixedMin * 2 <sup> f</sup></li>
<li>Sinon calcul n * 2<sup>f</sup> et conversion en entier.</li>
</ul>
Les implémentations sont autorisées sur D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP la tolérance d’unité de dernier placement dans le résultat de type entier, au lieu de la valeur infiniment précise n * 2<sup>f</sup> après la dernière étape ci-dessus.<br/></td>
</tr>
<tr class="even">
<td>Entier à virgule fixe</td>
<td>FLOAT</td>
<td>Supposons que la représentation à virgule fixe spécifique qui est convertie en valeur float ne contient pas plus d’un total de 24 bits d’informations, pas plus de 23 bits de qui se trouve dans le composant fractionnaire. Supposons qu’un nombre à virgule fixe donné, FXP, se trouve dans la forme i. f (l’entier i bits, la fraction f bits). La conversion en valeur float est similaire au pseudo-code suivant.<br/> float Result = (float) (FXP >> f) +//extraire un entier<br/> <dl> ((float) (FXP & (2<sup>f</sup> - 1))/(2<sup>f</sup>));//extraire une fraction<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




