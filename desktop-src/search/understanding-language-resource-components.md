---
description: Les ressources de langage consistent en des analyseurs lexicaux et des générateurs de formes dérivées qui étendent la création d’index et les fonctionnalités d’interrogation aux nouveaux langages et paramètres régionaux.
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: Fonctionnement des composants de ressources linguistiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03c9294eaf6e50de024b866372093a0359fc79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525443"
---
# <a name="understanding-language-resource-components"></a>Fonctionnement des composants de ressources linguistiques

Les ressources de langage consistent en des analyseurs lexicaux et des générateurs de formes dérivées qui étendent la création d’index et les fonctionnalités d’interrogation aux nouveaux langages et paramètres régionaux. Les analyseurs lexicaux sont utilisés lors de la création et de l’interrogation d’index. Les générateurs de formes dérivées sont utilisés uniquement pour l’interrogation. Windows Search utilise des dll de ressources de langage pour établir une liaison avec les implémentations [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) et [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) pour des paramètres régionaux de langue spécifiques.

Cette rubrique est organisée comme suit :

-   [À propos des ressources de langue](#about-language-resources)
-   [Césure de mots](#word-breaking)
-   [Recherche de radical](#stemming)
-   [Normalisation](#normalization)
-   [Mots parasites](#noise-words)
-   [Rubriques connexes](#related-topics)

## <a name="about-language-resources"></a>À propos des ressources de langue

Windows Search utilise un filtre (une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) et [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) pour accéder à un document dans son format natif. Le composant [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) extrait le contenu, les propriétés et la mise en forme du texte à partir du document. Le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) identifie les paramètres régionaux du document qu’il filtre. Le composant d’indexation appelle l’analyseur lexical approprié pour ces paramètres régionaux. Si aucun n’est disponible, le composant d’indexation appelle l’analyseur lexical neutre. Le séparateur de mots reçoit, à partir d’un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), un flux d’entrée de caractères Unicode que l’analyseur lexical analyse pour produire des mots et des expressions individuels. L’analyseur lexical normalise également les formats de date et d’heure. L’indexeur normalise les mots générés par l’analyseur lexical en convertissant les mots en lettres majuscules. L’indexeur enregistre les mots en majuscules dans l’index de recherche en texte intégral, à l’exception des mots parasites identifiés pour ces paramètres régionaux.

Le tableau suivant répertorie les actions et les résultats correspondants pour la phrase « la figure 1 illustre le rôle des ressources de langue pour la recherche Windows pendant le processus de création d’index ».



| Action                  | Texte obtenu                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Texte d’origine           | La figure 1 illustre le rôle des ressources de langue pour la recherche Windows pendant le processus de création d’index.                    |
| Filtrage               | La figure 1 illustre le rôle des ressources de langue pour la recherche Windows pendant le processus de création d’index.                    |
| Césure de mots           | Figure 1, illustre, le, le rôle, les, la langue, les ressources, pour, Windows, recherche, pendant, le, l’index, la création, le processus, EOS |
| Normalisation           | FIGURE 1, ILLUSTRE, LE, LE RÔLE, LES, LE LANGAGE, LES RESSOURCES, WINDOWS, RECHERCHE, PENDANT, LE, L’INDEX, LA CRÉATION, LE PROCESSUS           |
| Suppression des mots parasites      | FIGURE, ILLUSTRE, RÔLE, LANGAGE, RESSOURCES, FENÊTRES, RECHERCHE, PENDANT, INDEX, CRÉATION, PROCESSUS                            |
| Enregistrer dans l’index de recherche en texte intégral | FIGURE, ILLUSTRE, RÔLE, LANGAGE, RESSOURCES, FENÊTRES, RECHERCHE, PENDANT, INDEX, CRÉATION, PROCESSUS                            |



 

Les analyseurs lexicaux et les générateurs de formes dérivées sont utilisés pour étendre les requêtes [FREETEXT](-search-sql-freetext.md) au moment de la requête. Les paramètres régionaux de la requête sont les paramètres régionaux par défaut, sauf si un identificateur de code de langue (LCID) est passé en tant que paramètre de requête. Le composant de requête appelle l’analyseur lexical approprié sur les termes de la requête listés dans la clause [Where](-search-sql-where.md) de la requête. Par exemple, si la clause WHERE de la requête contient « FREETEXT (pommes, oranges et poires) », l’analyseur lexical reçoit le texte « pommes, oranges et poires ». Si la clause WHERE de la requête utilise le prédicat [contient](-search-sql-contains.md) du texte intégral, la sortie de texte de l’analyseur lexical est normalisée. Dans le cas contraire, le composant de requête passe chaque mot identifié par l’analyseur lexical au générateur de formes dérivées approprié pour cette langue et ces paramètres régionaux. Le générateur de formes dérivées génère une liste de formes alternatives ou fléchies pour ce mot. Le composant de requête normalise la liste développée des termes de requête et supprime les mots parasites.

Le tableau suivant répertorie les actions et les résultats correspondants pour la requête « pommes, oranges et poires ».



| Action                       | Texte obtenu                                            |
|------------------------------|-----------------------------------------------------------|
| Texte d’origine                | pommes, oranges et poires                                |
| Césure de mots                | pommes, oranges, et, poires, EOS                          |
| Recherche de radical                     | Apple, pommes, orange, orange, oranges, et, poires, poires |
| Normalisation                | APPLE, POMMES, ORANGE, ORANGE, ORANGES, ET, POIRES, POIRES |
| Suppression des mots parasites           | APPLE, POMMES, ORANGE, ORANGE, ORANGES, POIRES, POIRES      |
| Liste développée des termes de requête | APPLE, POMMES, ORANGE, ORANGE, ORANGES, POIRES, POIRES      |



 

Les termes de requête étendus augmentent la probabilité que la requête trouve des documents qui correspondent à l’intention de la requête d’origine. Le texte généré par l’analyseur lexical ou le générateur de formes dérivées au moment de la requête n’est pas stocké sur le disque.

## <a name="word-breaking"></a>Analyse lexicale

La césure des mots correspond à la séparation du texte en jetons de texte individuels ou en mots. De nombreux langages, en particulier ceux qui utilisent des alphabets romains, possèdent un tableau de séparateurs de mots (tels que des espaces blancs) et des signes de ponctuation utilisés pour discerner les mots, les expressions et les phrases. Les analyseurs lexicaux doivent s’appuyer sur des heuristiques de langage précis pour fournir des résultats fiables et précis. La césure des mots est plus complexe pour les systèmes de caractères d’écriture ou les alphabets basés sur des scripts, où la signification des caractères individuels est déterminée à partir du contexte. Pour plus d’informations sur les considérations linguistiques qui peuvent affecter votre implémentation de l’analyseur lexical, consultez [Considérations linguistiques et Unicode](linguistic-and-unicode-considerations.md).

## <a name="stemming"></a>Recherche de radical

Windows Search applique des générateurs de formes dérivées exclusivement au moment de la requête pour générer des formulaires de mot supplémentaires pour les termes du [FREETEXT](-search-sql-freetext.md) et des requêtes de propriété. Les générateurs de formes dérivées effectuent une analyse morphologique et appliquent des règles grammaticales pour générer une liste de formes alternatives ou fléchies pour les mots. Les autres formulaires ont souvent le même type de forme ou de base. En générant les formes fléchies d’un mot, le service d’indexation retourne les résultats de la requête qui sont statistiquement plus pertinents pour une requête. Par exemple, une requête de texte intégral pour « natation Meeting » correspond à des documents qui contiennent des « natation, des natations, des natations, des natations, des SWAM, des SWUM » ou des « réunions, des réunions, des réunions, des réunions, des réunions, des conditions réunies » et des combinaisons de ces termes.

Certains langages requièrent que les termes fléchis soient générés à la fois au moment de l’indexation et au moment de la requête pour les inflexions standard et de variantes. Dans ce cas, le radical se produit dans le composant analyseur lexical, avec un travail de radical minimal dans le générateur de formes dérivées. Par exemple, l’analyseur lexical japonais effectue un radical au cours de la création et de l’interrogation de l’index pour permettre à une requête de rechercher des formes fléchies différentes des termes de recherche.

## <a name="normalization"></a>Normalisation

Les documents de toutes les langues sont stockés dans un index unique. Bien que les mots et les règles linguistiques diffèrent considérablement, certaines considérations, telles que les nombres, les dates et les heures, sont gérées de manière cohérente sur tous les analyseurs lexicaux. Pour plus d’informations sur les considérations relatives à la normalisation qui peuvent affecter votre implémentation de l’analyseur lexical, consultez [normalisation des formes de surface](surface-form-normalization.md).

## <a name="noise-words"></a>Mots parasites

Les mots parasites, également appelés mots vides, sont des mots qui ne sont pas des indicateurs significatifs pour le contenu. Le service d’indexation supprime les mots parasites des termes de la requête et du contenu inclus dans l’index de recherche en texte intégral. Un *décalage* est l’occurrence d’un mot dans un document ou dans une liste de termes de requête. Le décalage des mots parasites dans un document ou une requête est enregistré comme vide. La suppression des mots parasites améliore les performances des requêtes en évitant la croissance inutile des index. Il améliore également la pertinence des résultats de la requête. Vous pouvez configurer la recherche Windows pour utiliser des listes de mots parasites pour des langues spécifiques. Ces listes sont utilisées lorsqu’un analyseur lexical est appelé pour cette langue. Par exemple, « le » dans la langue anglaise se produit si souvent qu’il a peu de valeur en tant que clé unique. « Le » se trouve dans la liste de mots parasites, n’est pas écrit dans l’index de contenu et, s’il est interrogé, ne retourne aucun résultat.

Les mots parasites jouent le rôle d’espaces réservés dans les requêtes d’expressions. Un document qui contient le texte « WAG the Dog » est stocké dans l’index avec « WAG » à l’occurrence 1 et « Dog » à l’occurrence 3. La requête d’expression « WAG Dog » ne correspond pas, mais la requête d’expression « WAG a Dog », car les informations d’occurrence correspondent. L’expression « WAG violet Dog » ne correspond pas, car « violet » est introuvable dans l’index à l’occurrence 2. Toutefois, une requête pour « WAG the Dog » renvoie des documents contenant « WAG Purple Dog », car il n’existe aucun moyen de déterminer efficacement si le document avait un mot non parasite entre « WAG » et « Dog ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Extension des ressources linguistiques](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Implémentation d’un analyseur lexical et du générateur de formes dérivées](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Considérations linguistiques et Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Ressources et meilleures pratiques pour la résolution des problèmes](troubleshooting-language-resources.md)
</dt> </dl>

 

 
