---
title: Modèle objet
description: Le tableau suivant répertorie les types d’objets qui peuvent être manipulés à l’aide des divers jeux d’API fournis par la plateforme de filtrage Windows (WFP).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030848"
---
# <a name="object-model"></a>Modèle objet

Le tableau suivant répertorie les types d’objets qui peuvent être manipulés à l’aide des divers jeux d’API fournis par la plateforme de filtrage Windows (WFP).



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Type d'objet</th>
<th>Description</th>
<th>Exemples de propriétés</th>
<th>Exemple</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Filtrer</td>
<td>Règle qui régit la classification. Si les conditions sont remplies, l’action est appelée. <br/> Il s’agit de l’objet le plus complexe exposé par WFP, car il associe tous les autres types d’objets. <br/></td>
<td><ul>
<li>Tableau de conditions</li>
<li>Action (autorisation, bloc, légende)</li>
<li><a href="filter-weight-assignment.md">Poids</a></li>
<li>Context</li>
</ul></td>
<td>&quot;Bloquez le trafic avec un port TCP supérieur à 1024.&quot; <br/> &quot;Appel à des ID pour tout le trafic qui n’est pas sécurisé.&quot;<br/></td>
</tr>
<tr class="even">
<td>Légende</td>
<td>Ensemble de fonctions qui participent au processus de classification.<br/> Cela permet d’effectuer un traitement personnalisé des paquets lorsque certaines conditions sont remplies.<br/></td>
<td><ul>
<li>id</li>
<li>Couche applicable</li>
</ul></td>
<td>Le pilote NAT<br/></td>
</tr>
<tr class="odd">
<td>Couche</td>
<td>Conteneur de filtre dans le moteur de filtre. <br/> Représente un point spécifique dans le traitement du trafic réseau où le moteur de filtre est appelé.<br/></td>
<td><ul>
<li>Schéma pour les filtres qui peuvent être ajoutés à la couche</li>
</ul></td>
<td>Couche de transport entrante<br/></td>
</tr>
<tr class="even">
<td>Sous-couche</td>
<td>Sous-composant d’une couche, utilisé dans un <a href="filter-arbitration.md">arbitrage de filtre</a>.<br/></td>
<td><ul>
<li>Poids</li>
</ul></td>
<td>Sous-couche du tunnel IPsec<br/></td>
</tr>
<tr class="odd">
<td>Fournisseur</td>
<td>Un fournisseur de stratégie qui a créé une solution sur WFP.<br/> Il est utilisé uniquement à des fins de gestion ; elle n’affecte pas le traitement des paquets au moment de l’exécution.<br/></td>
<td><ul>
<li>id</li>
<li>Nom du service</li>
</ul></td>
<td>Pare-feu Windows avec fonctions avancées de sécurité<br/> Application tierce de filtrage d’URL<br/></td>
</tr>
<tr class="even">
<td>Contexte du fournisseur</td>
<td>Objet blob de données utilisé par un fournisseur de stratégie pour stocker des informations de contexte arbitraires. <br/> Il est utilisé pour passer des informations de configuration personnalisées à une légende.<br/> La façon la plus courante d’utiliser les informations de contexte est d’avoir des filtres qui référencent un contexte de fournisseur. <br/></td>
<td><ul>
<li>id</li>
<li>Objet blob de données</li>
</ul></td>
<td>IPsec stocke les paramètres d’authentification dans le moteur de filtrage de base (BFE). La &quot; &quot; propriété de contexte d’un filtre indique les paramètres d’authentification à utiliser pour le trafic décrit par le filtre.<br/> Le shim de sélection de certification SSL stocke les informations de certification dans un contexte de fournisseur. <br/></td>
</tr>
</tbody>
</table>



 

Les types d’objets exposés par l’API WFP ont une sémantique cohérente. Les actions d’ajout, d’énumération, d’abonnement, etc. sont similaires pour tous les types d’objets.

Chaque type d’objet est représenté par une structure de données (par exemple, [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)). Afin de réduire le nombre de structures de données différentes exposées par l’API WFP, la même structure de données est utilisée pour l’ajout de nouveaux objets et la récupération de ceux existants. Par conséquent, il peut y avoir des champs dans chaque structure de données qui sont ignorés lors de l’ajout d’un nouvel objet, car ces champs sont renseignés par le moteur de filtrage de base (BFE) et non par l’appelant. Par exemple, une structure de données **FWPM \_ FILTER0** a un champ **FilterId** qui contient le **LUID** du **\_ FILTER0 FWPS** correspondant. Ce **LUID** est assigné par BFE, ce qui signifie que ce champ est ignoré dans l’appel à [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des objets](object-management.md)
</dt> </dl>

 

 





