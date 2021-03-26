---
description: À compter de Windows XP, le panneau de configuration prend en charge la catégorisation des éléments du panneau de configuration. Les éléments sont inscrits pour apparaître dans une ou plusieurs catégories. Impossible de créer des catégories.
title: Affectation des catégories du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972075"
---
# <a name="assigning-control-panel-categories"></a>Affectation des catégories du panneau de configuration

À compter de Windows XP, le panneau de configuration prend en charge la catégorisation des éléments du panneau de configuration. Les éléments sont inscrits pour apparaître dans une ou plusieurs catégories. Impossible de créer des catégories.

Pour inscrire un élément du panneau de configuration dans une ou plusieurs catégories, ajoutez des valeurs comme expliqué dans la section inscription de l’élément du panneau de configuration de l' [exécutable](registering-control-panel-items.md) ou [inscription](registering-control-panel-items.md) de l’élément du panneau de configuration de l’enregistrement des éléments du panneau de [configuration, le](registering-control-panel-items.md)cas échéant.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>ID de la catégorie</th>
<th>Nom de la catégorie (Windows 7)</th>
<th>Nom de la catégorie (Windows Vista)</th>
<th>Nom de la catégorie (Windows XP)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>&quot;Tous les éléments du panneau de configuration&quot;</td>
<td>&quot;Options supplémentaires&quot;
<blockquote>
[!Note]<br />
Tout élément du panneau de configuration qui ne spécifie pas d’ID de catégorie apparaît dans cette catégorie.
</blockquote>
<br/></td>
<td>&quot;Autres options du panneau de configuration&quot;
<blockquote>
[!Note]<br />
Tout élément du panneau de configuration qui ne spécifie pas d’ID de catégorie apparaît dans cette catégorie.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>1</td>
<td>&quot;Apparence et personnalisation&quot;</td>
<td>&quot;Apparence et personnalisation&quot;</td>
<td>&quot;Apparence et thèmes&quot;</td>
</tr>
<tr class="odd">
<td>2</td>
<td>&quot;Matériel et audio&quot;</td>
<td>&quot;Matériel et audio&quot;</td>
<td>&quot;Imprimantes et autres matériels&quot;</td>
</tr>
<tr class="even">
<td>3</td>
<td>&quot;Réseau et Internet&quot;</td>
<td>&quot;Réseau et Internet&quot;</td>
<td>&quot;Connexions réseau et Internet&quot;</td>
</tr>
<tr class="odd">
<td>4</td>
<td>N'est plus utilisé. Tout élément qui s’ajoute uniquement à la catégorie 4 apparaît dans la catégorie 2 (matériel et audio).</td>
<td>N'est plus utilisé. Tout élément qui s’ajoute uniquement à la catégorie 4 apparaît dans la catégorie 2 (matériel et audio).</td>
<td>&quot;Sons, voix et périphériques audio&quot;</td>
</tr>
<tr class="even">
<td>5</td>
<td>&quot;Système et sécurité&quot;</td>
<td>&quot;Système et maintenance&quot;</td>
<td>&quot;Performances et maintenance&quot;</td>
</tr>
<tr class="odd">
<td>6</td>
<td>&quot;Horloge, langue et région&quot;</td>
<td>&quot;Horloge, langue et région&quot;</td>
<td>&quot;Options de date, d’heure, de langue et régionales&quot;</td>
</tr>
<tr class="even">
<td>7</td>
<td>&quot;Options d’ergonomie&quot;</td>
<td>&quot;Options d’ergonomie&quot;</td>
<td>&quot;Options d’accessibilité&quot;</td>
</tr>
<tr class="odd">
<td>8</td>
<td>&quot;Programmes&quot;</td>
<td>&quot;Programmes&quot;</td>
<td>&quot;Ajouter ou supprimer des programmes&quot;</td>
</tr>
<tr class="even">
<td>9</td>
<td>&quot;Comptes d’utilisateur&quot;
<blockquote>
[!Note]<br />
Lorsque vous n’êtes pas connecté à un domaine, cela s’appelle &quot; comptes d’utilisateur et sécurité de famille &quot; .
</blockquote>
<br/></td>
<td>&quot;Comptes d’utilisateur&quot;
<blockquote>
[!Note]<br />
Lorsque vous n’êtes pas connecté à un domaine, cela s’appelle &quot; comptes d’utilisateur et sécurité de famille &quot; .
</blockquote>
<br/></td>
<td>&quot;Comptes d’utilisateur&quot;</td>
</tr>
<tr class="odd">
<td>10</td>
<td>N'est plus utilisé. Les éléments inscrits dans cette catégorie s’affichent dans la catégorie 5 (système et sécurité).</td>
<td>&quot;Sécurité&quot;</td>
<td>&quot;Centre de sécurité&quot;
<blockquote>
[!Note]<br />
Disponible uniquement dans Windows XP Service Pack 2 (SP2) ou version ultérieure.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>11</td>
<td>N'est plus utilisé. Les éléments inscrits dans cette catégorie s’affichent dans la catégorie 0 (tous les éléments du panneau de configuration).</td>
<td>&quot;ORDINATEUR portable&quot;
<blockquote>
[!Note]<br />
Cette catégorie est visible uniquement sur les ordinateurs portables.
</blockquote>
<br/></td>
<td>Non utilisé.</td>
</tr>
</tbody>
</table>



 

Dans Windows XP, les catégories **Ajouter ou supprimer des programmes** et des **comptes d’utilisateur** fonctionnent différemment des autres catégories dans le panneau de configuration. Lorsqu’un ou plusieurs éléments sont ajoutés à l’une de ces deux catégories, le lien associé dans le panneau de configuration ouvre une page de catégorie. Les éléments inscrits s’affichent dans la partie inférieure de la page sous le titre « ou sélectionnent une icône du panneau de configuration ». Quand aucun élément n’est inscrit pour l’une de ces catégories, le lien associé dans le panneau de configuration appelle directement l’élément Windows standard pour cette catégorie. Dans Windows Vista et versions ultérieures, la catégorie **programmes** et **compte d’utilisateur** n’a pas cette propriété.

La catégorie **Security Center** , disponible uniquement dans Windows XP SP2, est également un peu non standard. Cliquez sur cette catégorie pour ouvrir la page **Security Center** dans une nouvelle fenêtre. Les éléments inscrits pour **Security Center** s’affichent dans la partie inférieure de cette page sous le titre **gérer les paramètres de sécurité pour :**. Cliquer sur une icône ouvre l’élément du panneau de configuration.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments du panneau de configuration](control-panel-applications.md)
</dt> <dt>

[Conseils sur l’expérience utilisateur](user-experience-guidelines.md)
</dt> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Utilisation de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Traitement des messages du panneau de configuration](message-processing.md)
</dt> <dt>

[Exécution des éléments du panneau de configuration](executing-control-panel-items.md)
</dt> <dt>

[Extension des éléments du panneau de configuration système](extending-system-control-panel-items.md)
</dt> <dt>

[Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md)
</dt> <dt>

[Accès au panneau de configuration en mode sans échec sous Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




