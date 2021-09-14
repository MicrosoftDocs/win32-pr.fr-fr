---
description: Cette rubrique définit les \_ \* constantes INEG des paramètres régionaux utilisés par nls.
ms.assetid: 3a1e4a63-31bd-4ff9-a3ca-af357389e179
title: Constantes LOCALE_INEG *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5c40b2fc53e93653753eeb61048251a7fe55c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240203"
---
# <a name="locale_ineg-constants"></a>Paramètres régionaux \_ INEG \* constantes

Cette rubrique définit les \_ \* constantes INEG des paramètres régionaux utilisés par nls.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LOCALE_INEGCURR</td>
<td>Mode de devise négative. 
<table>
<thead>
<tr class="header">
<th>Mode</th>
<th>Format pour une devise négative</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Parenthèse ouvrante, symbole monétaire, nombre, parenthèse droite ; par exemple, ($1,1)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Signe négatif, symbole monétaire, nombre ; par exemple,-$1,1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Symbole monétaire, signe négatif, nombre ; par exemple, $-1,1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Symbole monétaire, nombre, signe négatif ; par exemple, $1,1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Parenthèse ouvrante, nombre, symbole monétaire, parenthèse droite ; par exemple, ($1,1)</td>
</tr>
<tr class="even">
<td>5</td>
<td>Signe négatif, nombre, symbole monétaire ; par exemple,-$1,1</td>
</tr>
<tr class="odd">
<td>6</td>
<td>Nombre, signe négatif, symbole monétaire ; par exemple, 1,1-$</td>
</tr>
<tr class="even">
<td>7</td>
<td>Nombre, symbole monétaire, signe négatif ; par exemple, $1,1-</td>
</tr>
<tr class="odd">
<td>8</td>
<td>Signe négatif, nombre, espace, symbole monétaire (comme #5, mais avec un espace avant le symbole monétaire); par exemple,-$1,1</td>
</tr>
<tr class="even">
<td>9</td>
<td>Le signe négatif, le symbole monétaire, l’espace, le nombre (comme #1, mais avec un espace après le symbole monétaire); par exemple,-$1,1</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Nombre, espace, symbole monétaire, signe négatif (comme #7, mais avec un espace avant le symbole monétaire); par exemple, $1,1-</td>
</tr>
<tr class="even">
<td>11</td>
<td>Symbole monétaire, espace, nombre, signe négatif (comme #3, mais avec un espace après le symbole monétaire); par exemple, $1,1-</td>
</tr>
<tr class="odd">
<td>12</td>
<td>Symbole monétaire, espace, signe négatif, nombre (comme #2, mais avec un espace après le symbole monétaire); par exemple, $-1,1</td>
</tr>
<tr class="even">
<td>13</td>
<td>Nombre, signe négatif, espace, symbole monétaire (comme #6, mais avec un espace avant le symbole monétaire); par exemple, 1,1-$</td>
</tr>
<tr class="odd">
<td>14</td>
<td>Parenthèse ouvrante, symbole monétaire, espace, nombre, parenthèse droite (comme #0, mais avec un espace après le symbole monétaire); par exemple, ($1,1)</td>
</tr>
<tr class="even">
<td>15</td>
<td>Parenthèse ouvrante, nombre, espace, symbole monétaire, parenthèse droite (comme #4, mais avec un espace avant le symbole monétaire); par exemple, ($1,1)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>LOCALE_INEGNUMBER</td>
<td>Mode de nombre négatif, autrement dit, le format d’un nombre négatif. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Format</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Parenthèse ouvrante, nombre, parenthèse droite ; par exemple, (1,1)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Signe négatif, nombre ; par exemple,-1,1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Signe négatif, espace, nombre ; par exemple,-1,1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Nombre, signe négatif ; par exemple, 1,1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Nombre, espace, signe négatif ; par exemple, 1,1-</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSEPBYSPACE</td>
<td>Séparation du signe négatif dans une valeur monétaire. Cette valeur est 1 si le symbole monétaire est séparé par un espace de la quantité négative, ou 0 dans le cas contraire.</td>
</tr>
<tr class="even">
<td>LOCALE_INEGSIGNPOSN</td>
<td>Index de mise en forme pour les valeurs de devise de la connexion négative. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Les parenthèses entourent le montant et le symbole monétaire.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Le signe précède le nombre.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Le signe suit le nombre.</td>
</tr>
<tr class="even">
<td>3</td>
<td>Le signe précède le symbole monétaire.</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Le signe suit le symbole monétaire.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSYMPRECEDES</td>
<td>Position du symbole monétaire dans une valeur monétaire négative. Cette valeur est 1 si le symbole monétaire précède la quantité négative, ou 0 si le symbole suit la valeur.</td>
</tr>
</tbody>
</table>



 

 

 



