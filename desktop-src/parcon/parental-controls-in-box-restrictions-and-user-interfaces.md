---
description: Plusieurs implémentations de restrictions sont fournies.
ms.assetid: a00d9a3a-d052-492c-b9e7-3ecb1455a392
title: Contrôle parental In-Box des restrictions & des interfaces utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9cb430a05d6e23b5ffa736398d30197aaec1dbbcdf6d1610ec8bc2db50d6556
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846642"
---
# <a name="parental-controls-in-box-restrictions--user-interfaces"></a>Contrôle parental In-Box des restrictions & des interfaces utilisateur

Plusieurs implémentations de restrictions sont fournies.

-   [Restrictions Web](#web-restrictions)
-   [Limites de temps](#time-limits)
-   [Jeux](#games)
-   [Autoriser et bloquer des programmes spécifiques](#allow-and-block-specific-programs)

## <a name="web-restrictions"></a>Restrictions Web

-   Filtre de contenu Web intégré à l’aide d’un service d’évaluation dynamique gratuit. Configurable individuellement par utilisateur contrôlé.
-   Filtre tout le trafic HTTP lorsqu’il est activé, retourne la page mise en forme personnalisée si elle est bloquée. Autorise des fonctionnalités acceptables avec tous les principaux navigateurs. En surveillant toutes les demandes HTTP et HTTPs pour une page, permet de bloquer des parties de page Web individuelles.
-   hautement configurable à l’aide de l’interface utilisateur qui autorise ou bloque les listes d’URL, les présélections de catégories d’évaluation simplifiées, ou ActiveX contrôle de plus de 12 catégories, ainsi qu’une stratégie de blocage des téléchargements de fichiers.

> [!Note]  
> Le blocage réel du téléchargement de fichiers requiert que les applications implémentent la restriction, en respectant le paramètre fourni.

 

-   implémenté comme un pilote de plateforme de filtrage Windows (WFP) communiquant avec le processus de surveillance de la sécurité des familles en cours d’exécution dans les sessions des utilisateurs. l’implémentation est passée d’un filtre de fournisseur de services en couche (LSP) à un pilote de plateforme de filtrage Windows (WFP) communiquant avec le processus de surveillance de la sécurité des familles en cours d’exécution dans les sessions des utilisateurs.

    **Windows 7 et Windows Vista :** Implémenté comme un filtre LSP (Layered Service Provider) qui communique avec un service à droits limités pour la gestion et la surveillance globales. Le filtre reste dans la chaîne LSP lorsqu’il est désactivé, mais passe tout le trafic via. Cette implémentation est prise en charge uniquement pour les systèmes d’exploitation listés.

-   Les applications peuvent fournir une interface utilisateur pour afficher les blocages de page partiels et honorer la stratégie de blocage des téléchargements de fichiers. Ils peuvent également appeler une API pour permettre à l’utilisateur de demander l’autorisation d’afficher une page bloquée. Cette substitution administrative appelle une petite application qui affiche les URL tentées et qui demande des informations d’identification pour les autoriser.
-   Une API est fournie pour les cas spéciaux où une application doit s’inscrire pour contourner le filtrage, ou si des URL spécifiques doivent toujours être autorisées.
-   Étant donné qu’un seul filtre de contenu Web doit être en cours d’exécution à la fois, des tiers peuvent s’inscrire comme filtre actif et désactiver le filtre intégré. Cette extensibilité, couplée à la possibilité d’afficher un filtre tiers dans l’interface utilisateur, permet un remplacement simple. Les filtres doivent supprimer leur inscription lorsqu’ils sont désinstallés.

## <a name="time-limits"></a>Limites de temps

-   Les restrictions de temps intégrées ont été améliorées grâce à la possibilité de contrôler la durée totale d’utilisation de l’ordinateur par jour (durée), en plus de la possibilité de contrôler les heures d’utilisation de l’ordinateur (curfew) disponibles dans les versions précédentes de Windows.
-   L’interface utilisateur pour curfew permet un contrôle indépendant pour chaque jour de la semaine avec une granularité de demi-heure
-   L’interface utilisateur pour l’allocation de temps autorise les contrôles pour les jours de la semaine et les week-ends ou le contrôle indépendant pour chaque jour de la semaine avec une granularité de 15 minutes.
-   Le mécanisme de changement rapide d’utilisateur n’est plus utilisé pour forcer le verrouillage ou bloquer la connexion de l’utilisateur contrôlé en cas de délai de blocage. Un basculement vers un bureau distinct est utilisé à ces fins. Notez que le changement de passe rapide conserve l’état de l’utilisateur lorsqu’il est verrouillé.

## <a name="games"></a>Jeux

-   Fonctionne conjointement avec l’Explorateur de jeux.
-   Permet aux administrateurs de contrôler les jeux qui peuvent être lus par le biais d’une interface utilisateur riche pour sélectionner un système et un niveau de classification des jeux (plus les descripteurs, le cas échéant), et/ou en autorisant ou bloquant spécifiquement les titres.
-   Les métadonnées sur les évaluations de jeux sont obtenues de l’une des deux manières suivantes :
    -   Les titres pris en charge déploient leurs propres fichiers de définition de jeu (GDFs).
    -   Environ 2000 titres hérités sont couverts par une base de données intégrée.
-   Trois mécanismes sont utilisés pour la mise en œuvre :
    -   Refuser les listes de contrôle d’accès pour l’utilisateur contrôlé accès en écriture au dossier du jeu.
    -   Processus d’arrêt des titres hérités à l’aide de la technologie de shim de compatibilité des applications.
    -   L’API Auto-Check utilise des titres pris en charge pour bloquer l’exécution.
-   Il est recommandé de connaître les limites de temps des événements expliqués dans la section ci-dessus.
-   La documentation de GDFs et de l’Explorateur de jeux sera fournie principalement par le biais des versions du kit de développement logiciel (SDK) DirectX.

## <a name="allow-and-block-specific-programs"></a>Autoriser et bloquer des programmes spécifiques

-   Également appelés restrictions générales relatives aux applications (GAR).
-   Désactivée par défaut. S’il est activé, il permet uniquement à un utilisateur contrôlé d’exécuter des applications approuvées par un administrateur, avec des exceptions raisonnables.
-   L’interface utilisateur fournit une liste de noms de programme avec les chemins d’accès correspondants, chacun avec une case à cocher Autoriser. Un bouton Parcourir est également fourni.
-   Implémenté à l’aide de stratégies de restriction logicielle (SRP), également appelé sécurité :
    -   Empêche l’exécution de tous les supports (clés USB, disquettes, etc.).
    -   Utilise des règles de chemin d’accès pour spécifier les programmes autorisés à s’exécuter.
    -   Les autorisations d’écriture de la liste de contrôle d’accès NTFS sont révoquées de tout ce qui est autorisé pour l’exécution de l’utilisateur contrôlé.
    -   Si elle est bloquée et remplacée par la suite pour autoriser, l’application doit être redémarrée manuellement.
-   Voici certaines exceptions :
    -   tous les fichiers binaires requis pour un sous-ensemble de base de Windows fonctionnent.
    -   Tous les fichiers exécutables qui s’inscrivent à l’aide d’une API doivent être autorisés pour un utilisateur donné.
    -   Jeux spécifiés comme étant autorisés sous des restrictions de jeux.
-   Notez que la commande RunAs est bloquée par la conception d’un utilisateur quand GAR est activé.

 

 



