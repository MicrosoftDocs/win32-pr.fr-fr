---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player Online stores, track.csv
- magasins en ligne, track.csv
- tapez 1 magasins en ligne, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310370"
---
# <a name="trackcsv"></a>track.csv

Ce fichier contient une entrée pour chaque piste dans le catalogue. Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

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
<td>TrackID tel</td>
<td>Oui</td>
<td>Entier non négatif. Exemple : 32789<br/></td>
<td>Identificateur unique fourni par le fournisseur de contenu. Doit être inférieur à 2 ^ 32. Conseil en matière de performances : si les ID affectés aux pistes du même album sont numérotés consécutivement, la compression du catalogue est plus efficace. Toutefois, la numérotation consécutive des suivis d’albums n’est pas obligatoire.<br/></td>
</tr>
<tr class="even">
<td>TrackTitle</td>
<td>Oui</td>
<td>Chaîne Unicode. Exemple : Raygun Robbers’Blues</td>
<td>Nom de la piste.</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Oui</td>
<td>Entier non négatif. Exemple : 543<br/></td>
<td>Durée de la piste en secondes.</td>
</tr>
<tr class="even">
<td>TrackNumber</td>
<td>Oui</td>
<td>Entier non négatif. Exemple : 7<br/></td>
<td>Numéro de piste sur l’album de la piste. Le suivi des nombres commence à 1 et augmente sur les jeux de disques. Le numéro de piste doit être inférieur à 256. Un numéro de piste supérieur ou égal à 256 entraîne un comportement inattendu dans le lecteur Windows Media.</td>
</tr>
<tr class="odd">
<td>TrackPrice</td>
<td>Oui</td>
<td>Chaîne Unicode. Exemple : $0,99.</td>
<td>Suivre le prix. Le symbole monétaire doit être inclus. La chaîne vide, 0 et-ont une signification particulière. Une chaîne vide indique que le prix est inconnu. Un zéro dans ce champ signifie que la piste est libre et un trait d’Union (-) indique que la piste ne peut pas être achetée.</td>
</tr>
<tr class="even">
<td>CanStream</td>
<td>Oui</td>
<td>Propriété booléenne. Peut être 0 ou 1. exemple : 0<br/></td>
<td>Indique si la piste peut être diffusée en continu.</td>
</tr>
<tr class="odd">
<td>CanDownload</td>
<td>Oui</td>
<td>Propriété booléenne. Peut être 0 ou 1. exemple : 0<br/></td>
<td>Indique si la piste peut être téléchargée.</td>
</tr>
<tr class="even">
<td>HasPreviewClip</td>
<td>Oui</td>
<td>Propriété booléenne. Peut être 0 ou 1. exemple : 0<br/></td>
<td>Indique si la piste a un clip d’aperçu.</td>
</tr>
<tr class="odd">
<td>HasVideoClip</td>
<td>Oui</td>
<td>Propriété booléenne. Peut être 0 ou 1. exemple : 0<br/></td>
<td>Indique si la piste a un clip vidéo.</td>
</tr>
<tr class="even">
<td>ParentalRating</td>
<td>Oui</td>
<td>Énumération. Peut être N, E ou C. exemple : N<br/></td>
<td>Indique l’évaluation de l’avis parental. Les valeurs N, E et C sont pour normal, Explicit et Clean.</td>
</tr>
<tr class="odd">
<td>LinkedAlbumID</td>
<td>Oui</td>
<td>Entier non négatif. Doit être l’ID d’un album. Exemple : 32423</td>
<td>ID de l’album qui contient cette piste.
<blockquote>
[!Note]<br />
Chaque suivi doit appartenir à un album. Autrement dit, pour chaque piste, le champ LinkedAlbumID doit être égal à l’un des ID d’album figurant dans le fichier album.csv.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>LinkedTrackArtist_ArtistIDs</td>
<td>Oui</td>
<td>Liste d’entiers. La liste contient les ID d’artiste, séparés par des points-virgules. Exemple : 41322 ; 12321 ; 82123 ;</td>
<td>Liste d’ID correspondant aux artistes contributeurs.</td>
</tr>
<tr class="odd">
<td>Composer</td>
<td>Non</td>
<td>Chaîne Unicode. Exemple : Beethoven</td>
<td>Compositeur de la piste. Si le genre de la piste n’a pas le champ HasComposer défini, la valeur du champ compositeur sera ignorée. Généralement utilisé uniquement pour les pistes Jazz ou classiques.</td>
</tr>
<tr class="even">
<td>Popularité</td>
<td>Oui</td>
<td>Entier non négatif ou float. exemple : 1252,6<br/></td>
<td>Détermine la position de la piste dans la liste lorsqu’elle est triée par popularité. Un nombre inférieur indique une popularité plus élevée.</td>
</tr>
<tr class="odd">
<td>StarRating</td>
<td>Non</td>
<td>Float. exemple : 4,21<br/></td>
<td>L’évaluation de l’étoile sera arrondie à l’étoile 1/4 la plus proche par le lecteur Windows Media avant d’être affichée dans l’interface utilisateur du lecteur Windows Media.</td>
</tr>
</tbody>
</table>



 

 

 





