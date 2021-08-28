---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Lecteur Windows Media des magasins en ligne, list.csv
- magasins en ligne, list.csv
- tapez 1 magasins en ligne, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7237afb37b30ccf8c96ddac95f0e81e148703d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480785"
---
# <a name="listcsv"></a>list.csv

Ce fichier contient une entrée pour chacune des listes contenues dans le catalogue. Les listes peuvent être des listes de pistes, d’albums, d’artistes, de genres, de sous-genres ou de flux radio. ou ils peuvent être des listes d’autres listes. Chaque entrée de liste est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.




| Champ | Obligatoire | Format | Description | 
|-------|----------|--------|-------------|
| ListID | Yes | Entier non négatif. | Identificateur de liste, unique dans list.csv. Doit être non négatif et inférieur à 2 ^ 32. <strong>Affichage d’un nœud de liste dans un contrôle Tree View :</strong> Si la valeur de ListID est 0, 1, 2, 3, 4, 5, 6 ou 7, la liste apparaît comme un nœud personnalisé sous le nœud de niveau supérieur de votre magasin en ligne dans le contrôle d’arborescence du lecteur. Les nœuds personnalisés apparaissent avant les nœuds standard sous le nœud de niveau supérieur du magasin en ligne et sont positionnés par ListID dans l’ordre croissant. Par exemple, s’il existe trois nœuds personnalisés, avec ListId de 1, 3 et 5, ils sont affichés en premier, deuxième et troisième sous le nœud de niveau supérieur de la boutique en ligne.<br /> | 
| ListTitle | No | Chaîne Unicode. Exemple : 10 premiers résultats<br /> | Titre de la liste. | 
| ListSubtitle | No | chaîne Unicode | Autre titre de liste, affiché sur la deuxième ligne de l’affichage en mosaïque. | 
| ListDescription | Yes | chaîne Unicode | Afficher le texte convivial de liste (affiché dans les pages de propriétés). | 
| Linked_ItemType | Yes | Chaîne Unicode. Format : [T|P|A|L|G|S|R<br /> Exemple : T<br /> | Indique le type des éléments liés.<ul><li>T = Track</li><li>P = l’intervenant</li><li>A = album</li><li>L = liste</li><li>G = genre</li><li>S = sous-genre</li><li>R = radio</li></ul> | 
| ListPrice | Yes | Chaîne Unicode. Exemple : $9,99<br /> | Prix de la liste. Le symbole monétaire doit être inclus. Une valeur zéro signifie que la liste est libre. Aucune valeur signifie que le prix est inconnu. Un trait d’Union signifie que la liste ne peut pas être achetée.<br /> | 
| Popularité | Yes | Valeur entière ou décimale. Exemple : 1259,3<br /> | Indique le classement de la popularité lorsque cette liste apparaît dans d’autres listes. Peut être zéro s’il n’est pas applicable. | 
| IsRecentlyAdded | Yes | Booléen. format : [0|1]<br /> Exemple : 0<br /> | Indique si la liste a été récemment ajoutée. | 
| IsFeatured | Yes | Booléen. format : [0|1]<br /> Exemple : 0<br /> | Indique si la liste est proposée. Peut être utilisé pour déterminer l’ordre de tri. | 
| EditorialGlyph | Yes | Entier non négatif. Doit correspondre à 0. | Non utilisé dans cette version. Doit correspondre à 0. | 
| ViewType | Yes | Chaîne Unicode. Format : [I|T|R|L|O] exemple : T<br /> | Indique le type d’affichage à utiliser pour la liste.<ul><li>I = icône</li><li>T = vignette</li><li>R = rapport</li><li>L = liste</li><li>O = liste triée</li></ul> | 
| ViewImageSize | Yes | Entier non négatif. Exemple : 180<br /> | Taille à laquelle l’image de liste est affichée. Si la valeur est 0, la taille est déterminée automatiquement. | 
| GroupBy | Yes | Chaîne Unicode. Format : [-|P|A|C|R|E<br /> Exemple : P<br /> | Indique quel champ est utilisé pour regrouper les éléments de la liste.<ul><li>-= Automatique</li><li>P = l’intervenant</li><li>A = album</li><li>C = Composer</li><li>R = évaluation</li><li>D = date</li></ul> | 
| ListItemsAreDynamic | Yes | Propriété booléenne. Peut avoir la valeur 0 ou 1. | Indique si la liste est générée dynamiquement. Les listes dynamiques n’ont pas d’éléments dans listitem.csv. Si une liste est marquée comme dynamique, ses éléments sont fournis par <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner :: GetListContents</a> | 




 

 

 





