---
description: Concepts fondamentaux de MUI
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: Concepts fondamentaux de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88bd677d7a6b07bc4db78d733d81fc36624ddd06f9ad3014588b8e5fd0882aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390888"
---
# <a name="mui-fundamental-concepts-explained"></a>Concepts fondamentaux de MUI

-   [Prérequis pour MUI](#prerequisite-for-mui)
-   [Séparation du code source des ressources spécifiques à une langue](#separation-of-source-code-from-language-specific-resources)
    -   [Les premiers jours : le code et les ressources sont réunis](#the-early-days-code-and-resources-live-together)
    -   [Séparation logique du code et des ressources localisables](#logically-separating-code-and-localizable-resources)
    -   [Séparation physique du code et des ressources](#physically-separating-code-and-resources)
-   [Chargement dynamique des ressources spécifiques à une langue](#dynamically-loading-language-specific-resources)
-   [Création d’applications MUI](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Prérequis pour MUI

le prérequis de base pour la création d’une application compatible avec MUI pour Windows Vista et ultérieur consiste à concevoir l’application conformément aux [instructions de globalisation](https://msdn.microsoft.com/goglobal/bb688110.aspx)Windows.

## <a name="separation-of-source-code-from-language-specific-resources"></a>Séparation du code source des ressources spécifiques à une langue

L’un des locaux fondamentaux de la technologie MUI est la séparation du code source de l’application des ressources spécifiques à la langue, afin de permettre des scénarios multilingues dans les applications plus efficacement. La séparation du code et des ressources a été effectuée par le biais de différents mécanismes et de différents degrés dans le temps, comme indiqué dans les sections suivantes. Chaque méthode offrait des degrés de flexibilité variables dans la création, le déploiement et la maintenance de l’application.

La solution recommandée pour les applications compatibles avec MUI est la dernière méthode décrite ici, à savoir la séparation physique du code source de l’application et des ressources, avec les ressources elles-mêmes décomposées en un seul fichier par langue prise en charge pour une flexibilité maximale de la génération, du déploiement et de la maintenance.

### <a name="the-early-days-code-and-resources-live-together"></a>Les premiers jours : le code et les ressources sont réunis

Initialement, les applications localisées ont été créées en modifiant le code source et en modifiant les ressources (généralement des chaînes) dans le code lui-même et en recompilant les applications. Cela signifiait que pour produire une version localisée, il fallait copier le code source d’origine, traduire les éléments de texte (ressources) dans le code source et recompiler le code. L’illustration suivante montre le code d’application avec du texte qui doit être localisé.

![Diagramme conceptuel montrant une application qui contient des unités de ressources de texte incorporées](images/mui-fundamental-concepts-explained-fig3.gif)

Bien que cette approche permette de créer des applications localisées, elle présente également des inconvénients significatifs :

-   Il requiert plusieurs versions du code source, au moins une pour la langue source et une pour chacune des langues cibles. Cela permet de créer des problèmes importants pour synchroniser les différentes versions linguistiques de l’application. En particulier, lorsqu’une erreur doit être corrigée dans le code, l’erreur doit être corrigée dans chaque copie du code source (une par langue).
-   Elle est également extrêmement sujette aux erreurs, car les localisateurs, qui ne sont pas des développeurs, peuvent apporter des modifications au code source, créant ainsi un risque considérable en termes d’intégrité du code.

La combinaison de ces inconvénients rend cette proposition extrêmement inefficace, et un meilleur modèle était nécessaire.

### <a name="logically-separating-code-and-localizable-resources"></a>Séparation logique du code et des ressources localisables

Une amélioration significative par rapport au modèle précédent est la séparation logique du code et des ressources localisables pour une application. Cela permet d’isoler le code des ressources et de s’assurer que le code reste intact lorsque des ressources sont modifiées par la localisation. Du point de vue de l’implémentation, les chaînes et autres éléments d’interface utilisateur sont stockés dans des fichiers de ressources, qui sont relativement faciles à traduire et sont logiquement séparés des sections de code.

Idéalement, l’ajout de la prise en charge d’une langue donnée peut être aussi simple que la traduction des ressources localisables dans ce nouveau langage et l’utilisation de ces ressources traduites pour créer une nouvelle version localisée de l’application, sans nécessiter de modification du code. L’illustration suivante montre comment le code et les ressources localisables doivent être séparés logiquement au sein d’une application.

![Diagramme conceptuel qui montre une application qui contient des ressources localisables séparées du code](images/mui-fundamental-concepts-explained-fig4.gif)

Ce modèle permet de créer plus facilement des versions localisées d’une application et constitue une amélioration significative par rapport au modèle précédent. Ce modèle, implémenté par le biais de l’utilisation des outils de gestion des ressources, a été très performant au fil des années et est toujours couramment utilisé par de nombreuses applications aujourd’hui. Toutefois, il présente des inconvénients significatifs :

-   Bien qu’elles soient séparées logiquement, le code et les ressources localisées sont toujours physiquement joints dans un fichier exécutable. En particulier, la maintenance est toujours problématique, car la même erreur de code (identique dans toutes les versions linguistiques) requiert un correctif par langue. Par conséquent, s’il s’agit d’une application en 20 langues, un correctif de service doit être émis 20 fois (un pour chaque langue), même si le code n’est corrigé qu’une seule fois.
-   La distribution et l’utilisation des applications multilingues ne sont pas prises en charge de manière appropriée par ce modèle. Il peut s’agir d’un problème important dans les scénarios d’entreprise et d’OEM. Par exemple, si un ordinateur doit être partagé entre deux utilisateurs utilisant des langues différentes, les applications doivent être installées à deux reprises avec ce modèle, puis certains mécanismes devront être activés pour alterner entre les deux installations. Cela suppose qu’il n’existe aucune dépendance supplémentaire qui empêche même ce scénario d’être implémenté. L’illustration suivante montre un exemple d’une erreur de code unique nécessitant deux correctifs.

![Diagramme conceptuel qui montre deux applications localisées qui ont la même erreur de code](images/mui-fundamental-concepts-explained-fig5.gif)

Il est clair que, bien que ce modèle fonctionne bien dans certains scénarios, ses limites pour les applications multilingues et leurs déploiements peuvent être très problématiques.

Une variante de ce modèle qui atténue certains problèmes liés aux applications multilingues est le modèle dans lequel les ressources localisables contiennent un ensemble de ressources linguistiques différentes. Ce modèle a une base de code commune et plusieurs ressources pour différentes langues dans la même application. Par exemple, une application peut être livrée avec l’anglais, l’allemand, le français, l’espagnol, le néerlandais et l’italien dans le même package. L’illustration suivante montre une application qui contient plusieurs ressources de langue.

![Diagramme conceptuel montrant une application avec du code distinct de deux ressources spécifiques aux paramètres régionaux](images/mui-fundamental-concepts-explained-fig6.gif)

Ce modèle facilite la maintenance de l’application lorsqu’une erreur de code doit être corrigée (ce qui est une amélioration, mais n’améliore pas par rapport aux modèles précédents lorsqu’il s’agit de prendre en charge des langues supplémentaires). Dans ce cas, il faut toujours publier une nouvelle version de l’application (et cette version est potentiellement compliquée par la nécessité de s’assurer que toutes les ressources de langue sont synchronisées dans la même distribution).

### <a name="physically-separating-code-and-resources"></a>Séparation physique du code et des ressources

L’étape suivante consiste à séparer physiquement le code et les ressources. Dans ce modèle, les ressources sont extraites du code et séparées physiquement dans des fichiers d’implémentation différents. En particulier, cela signifie que le code peut devenir véritablement indépendant de la langue ; le même code physique est réellement fourni pour toutes les versions localisées d’une application. L’illustration suivante montre que le code et les ressources localisables doivent être physiquement séparés.

![Diagramme conceptuel qui montre une application séparée de ses ressources localisables](images/mui-fundamental-concepts-explained-fig7.gif)

Cette approche présente plusieurs avantages par rapport aux approches précédentes :

-   Le déploiement de solutions multilingues est considérablement simplifié. L’ajout de la prise en charge d’une langue donnée nécessite uniquement l’expédition et l’installation d’un nouvel ensemble de ressources de langue pour cette langue particulière. Cela est particulièrement important lorsque les ressources de langue ne sont pas toutes disponibles simultanément. Avec ce modèle, il est possible de déployer une application dans un ensemble de langages principaux et d’augmenter le nombre de langues prises en charge dans le temps sans avoir à modifier ou à redéployer le code réel. Cet avantage est encore étendu par un mécanisme de secours qui permet la localisation partielle d’applications et de composants système dans une langue donnée en veillant à ce que les ressources qui ne se trouvent pas dans ce langage préféré « repasse » à une autre langue que les utilisateurs comprennent également. En général, ce modèle permet de réduire la charge considérable que les sociétés internationales font face au déploiement d’applications dans plusieurs langues, car elle permet le déploiement d’une seule image de manière beaucoup plus efficace.
-   La facilité de maintenance est améliorée. Une erreur de code ne doit être corrigée et déployée qu’une seule fois, car le code est complètement indépendant de la localisation. Avec ce modèle, l’émission d’une correction pour une erreur de code, à condition que la modification ne soit pas liée à l’interface utilisateur, est bien plus simple et rentable que dans l’un des modèles précédents.

## <a name="dynamically-loading-language-specific-resources"></a>Chargement dynamique des ressources spécifiques à une langue

Les concepts fondamentaux de MUI en matière de [séparation physique du code source des ressources spécifiques à une langue](#physically-separating-code-and-resources), et de création d’un binaire de base indépendant du langage pour une application, configurent essentiellement une architecture qui est propice à l’implémentation du chargement dynamique des ressources spécifiques à la langue en fonction des paramètres de langue utilisateur et système.

le code source de l’Application fourni dans le fichier binaire de base indépendant du langage peut utiliser les api MUI dans la plateforme Windows pour abstraire la sélection de la langue d’interface utilisateur d’affichage appropriée pour un contexte donné. MUI prend en charge ce qui suit :

-   Construction d’une liste hiérarchisée de langues d’interface utilisateur d’affichage en fonction des paramètres système, utilisateur et au niveau de l’application, de l’utilisateur et du système.
-   Implémentation d’un mécanisme de secours qui choisit un candidat approprié à partir de cette liste de langues classée par ordre de priorité, en fonction de la disponibilité des ressources localisées.

Les avantages du chargement dynamique des ressources de l’interface utilisateur avec une priorité de secours sont les suivants :

-   Il permet la localisation partielle des applications et des composants système dans une langue donnée, car les ressources qui ne se trouvent pas dans cette langue par défaut basculent automatiquement vers la langue suivante de la liste classée par ordre de priorité.
-   Cela permet des scénarios tels que le basculement dynamique d’un langage à un autre.
-   Il permet de créer des images de déploiement unique régionales ou mondiales qui couvrent un ensemble de langues pour les OEM et les entreprises.

## <a name="building-mui-applications"></a>Création d’applications MUI

les sections précédentes décrivaient les options permettant de séparer le code source des ressources spécifiques à une langue, ainsi que l’avantage résultant de pouvoir utiliser les api core Windows platform pour charger dynamiquement des ressources localisées. bien qu’il s’agit d’instructions, il est également important de noter qu’il n’existe pas de moyen normatif spécifique pour développer une application MUI pour la plateforme Windows.

Les développeurs d’applications ont un choix complet quant à la façon dont ils gèrent différents paramètres de langue de l’interface utilisateur, les options de création des ressources et les méthodes de chargement des ressources. Les développeurs peuvent évaluer les instructions fournies dans ce document et choisir une combinaison qui correspond à leurs besoins et à l’environnement de développement.

le tableau suivant récapitule les différentes options de conception disponibles pour les développeurs d’applications qui cherchent à créer une application MUI pour la plateforme Windows.



<table>
<thead>
<tr class="header">
<th>Paramètres de langue de l’interface utilisateur</th>
<th>Création de ressources</th>
<th>Chargement des ressources</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">Suivre les paramètres de langue de l’interface utilisateur dans le système d’exploitation $ {REMOVE} $<br />
</td>
<td>Une seule langue dans un fichier binaire de ressources fractionnées (technologie de ressources MUI)<br/> -ou-<br/> Plusieurs langues dans un binaire de ressource non fractionnée<br/></td>
<td>L’application appelle des fonctions de chargement de ressources standard. Les ressources sont retournées dans les langues correspondant aux paramètres du système d’exploitation.<br/></td>
</tr>
<tr class="even">
<td>Mécanisme de ressources spécifique à l’application<br/></td>
<td>L’application appelle l’API MUI pour récupérer les langages d’interface utilisateur préférés aux threads ou les langages de l’interface utilisateur préférés du processus à partir du système d’exploitation et utiliser ces paramètres pour charger ses propres ressources.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Paramètres de langue de l’interface utilisateur spécifiques à l’application $ {REMOVE} $<br />
</td>
<td>Langue unique dans un fichier binaire de ressources fractionnées<br/> -ou-<br/> Plusieurs langues dans un binaire de ressource non fractionnée<br/></td>
<td>L’application appelle l’API MUI pour définir des langages d’interface utilisateur spécifiques aux applications ou des langages d’interface utilisateur préférés aux processus, puis appelle des fonctions de chargement de ressources standard. Les ressources sont retournées dans les langues définies par l’application ou les langues du système.<br/> -ou-<br/> L’application sonde les ressources dans un langage spécifique et gère sa propre extraction de ressources à partir des données binaires récupérées.<br/></td>
</tr>
<tr class="even">
<td>Mécanisme de ressources spécifique à l’application<br/></td>
<td>L’application gère son propre chargement des ressources.<br/></td>

</tr>
</tbody>
</table>



 

 

 




