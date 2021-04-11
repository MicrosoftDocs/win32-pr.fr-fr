---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player Online stores, list.csv
- magasins en ligne, list.csv
- tapez 1 magasins en ligne, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101237"
---
# <a name="listcsv"></a>list.csv

Ce fichier contient une entrée pour chacune des listes contenues dans le catalogue. Les listes peuvent être des listes de pistes, d’albums, d’artistes, de genres, de sous-genres ou de flux radio. ou ils peuvent être des listes d’autres listes. Chaque entrée de liste est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Champ</th>
<th>Obligatoire</th>
<th>Format</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ListID</td>
<td>Oui</td>
<td>Entier non négatif.</td>
<td>Identificateur de liste, unique dans list.csv. Doit être non négatif et inférieur à 2 ^ 32. <strong>Affichage d’un nœud de liste dans un contrôle Tree View :</strong> Si la valeur de ListID est 0, 1, 2, 3, 4, 5, 6 ou 7, la liste apparaît comme un nœud personnalisé sous le nœud de niveau supérieur de votre magasin en ligne dans le contrôle d’arborescence du lecteur. Les nœuds personnalisés apparaissent avant les nœuds standard sous le nœud de niveau supérieur du magasin en ligne et sont positionnés par ListID dans l’ordre croissant. Par exemple, s’il existe trois nœuds personnalisés, avec ListId de 1, 3 et 5, ils sont affichés en premier, deuxième et troisième sous le nœud de niveau supérieur de la boutique en ligne.<br/></td>
</tr>
<tr class="even">
<td>ListTitle</td>
<td>Non</td>
<td>Chaîne Unicode. Exemple : 10 premiers résultats<br/></td>
<td>Titre de la liste.</td>
</tr>
<tr class="odd">
<td>ListSubtitle</td>
<td>Non</td>
<td>chaîne Unicode</td>
<td>Autre titre de liste, affiché sur la deuxième ligne de l’affichage en mosaïque.</td>
</tr>
<tr class="even">
<td>ListDescription</td>
<td>Oui</td>
<td>chaîne Unicode</td>
<td>Afficher le texte convivial de liste (affiché dans les pages de propriétés).</td>
</tr>
<tr class="odd">
<td>Linked_ItemType</td>
<td>Oui</td>
<td>Chaîne Unicode. Format : [T | P | A | L | G | S | R<br/> Exemple : T<br/></td>
<td>Indique le type des éléments liés.
<ul>
<li>T = Track</li>
<li>P = l’intervenant</li>
<li>A = album</li>
<li>L = liste</li>
<li>G = genre</li>
<li>S = sous-genre</li>
<li>R = radio</li>
</ul></td>
</tr>
<tr class="even">
<td>ListPrice</td>
<td>Oui</td>
<td>Chaîne Unicode. Exemple : $9,99<br/></td>
<td>Prix de la liste. Le symbole monétaire doit être inclus. Une valeur zéro signifie que la liste est libre. Aucune valeur signifie que le prix est inconnu. Un trait d’Union signifie que la liste ne peut pas être achetée.<br/></td>
</tr>
<tr class="odd">
<td>Popularité</td>
<td>Oui</td>
<td>Valeur entière ou décimale. Exemple : 1259,3<br/></td>
<td>Indique le classement de la popularité lorsque cette liste apparaît dans d’autres listes. Peut être zéro s’il n’est pas applicable.</td>
</tr>
<tr class="even">
<td>IsRecentlyAdded</td>
<td>Oui</td>
<td>Booléen. format : [0 | 1]<br/> Exemple : 0<br/></td>
<td>Indique si la liste a été récemment ajoutée.</td>
</tr>
<tr class="odd">
<td>IsFeatured</td>
<td>Oui</td>
<td>Booléen. format : [0 | 1]<br/> Exemple : 0<br/></td>
<td>Indique si la liste est proposée. Peut être utilisé pour déterminer l’ordre de tri.</td>
</tr>
<tr class="even">
<td>EditorialGlyph</td>
<td>Oui</td>
<td>Entier non négatif. Doit correspondre à 0.</td>
<td>Non utilisé dans cette version. Doit correspondre à 0.</td>
</tr>
<tr class="odd">
<td>ViewType</td>
<td>Oui</td>
<td>Chaîne Unicode. Format : [I | T | R | L | O] exemple : T<br/></td>
<td>Indique le type d’affichage à utiliser pour la liste.
<ul>
<li>I = icône</li>
<li>T = vignette</li>
<li>R = rapport</li>
<li>L = liste</li>
<li>O = liste triée</li>
</ul></td>
</tr>
<tr class="even">
<td>ViewImageSize</td>
<td>Oui</td>
<td>Entier non négatif. Exemple : 180<br/></td>
<td>Taille à laquelle l’image de liste est affichée. Si la valeur est 0, la taille est déterminée automatiquement.</td>
</tr>
<tr class="odd">
<td>GroupBy</td>
<td>Oui</td>
<td>Chaîne Unicode. Format : [-| P | A | C | R | E<br/> Exemple : P<br/></td>
<td>Indique quel champ est utilisé pour regrouper les éléments de la liste.
<ul>
<li>- = Automatique</li>
<li>P = l’intervenant</li>
<li>A = album</li>
<li>C = compositeur</li>
<li>R = évaluation</li>
<li>D = date</li>
</ul></td>
</tr>
<tr class="even">
<td>ListItemsAreDynamic</td>
<td>Oui</td>
<td>Propriété booléenne. Peut avoir la valeur 0 ou 1.</td>
<td>Indique si la liste est générée dynamiquement. Les listes dynamiques n’ont pas d’éléments dans listitem.csv. Si une liste est marquée comme dynamique, ses éléments sont fournis par <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner :: GetListContents</a></td>
</tr>
</tbody>
</table>



 

 

 





