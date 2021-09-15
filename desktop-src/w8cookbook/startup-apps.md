---
title: Applications de démarrage
description: Applications de démarrage
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- application de démarrage
- tâche en arrière-plan
- Exécuter la clé
- RunOnce
- dossier de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404251"
---
# <a name="startup-apps"></a>Applications de démarrage

## <a name="platform"></a>Plateforme

**Clients** Windows 8     


## <a name="description"></a>Description

l’un des grands résultats de Windows est la capacité à éclairer différents facteurs de forme, des ordinateurs de bureau traditionnels et des ordinateurs portables aux tablettes de faible puissance. pour s’assurer que nos clients mutuels bénéficient d’une expérience remarquable sur n’importe quel facteur de forme qu’ils choisissent avec Windows, deux mesures de réussite clés qui doivent être traitées sont une autonomie de batterie accrue et une excellente réactivité du PC. pour ce faire, des améliorations ont été apportées dans plusieurs domaines de Windows notamment le cycle de vie des processus, les états de veille et les applications de démarrage (applications avec lancement automatisé après le démarrage de l’ordinateur). cette rubrique met en évidence certains des impacts des applications de démarrage sur un appareil Windows, et fournit des conseils aux développeurs (ISV/IHV) et aux oem pour repenser les modèles d’utilisation des applications de démarrage afin d’améliorer la durée de vie et la réactivité de la batterie pour nos clients mutuels. elle décrit également les modifications apportées à Windows qui permettent aux utilisateurs de déterminer les applications de démarrage qui sont réellement exécutées.

Windows les applications du Store sont conçues pour adhérer aux nouvelles normes en matière de consommation et de réactivité de la batterie, et Windows gère leur cycle de vie en les suspendant et/ou en les terminant. toutefois, les applications de bureau conçues pour les versions antérieures de Windows n’ont pas nécessairement été conçues pour préserver la durée de vie de la batterie ou être sensibles à l’activité des utilisateurs, et peuvent affecter la réactivité du système (par exemple, lorsqu’une application envoie une pulsation normale de 1 seconde pour rechercher des mises à jour cela peut créer une expérience médiocre pour l’utilisateur qui achète une Windows tablet pc avec une durée de vie de batterie longue et des semaines de secours, mais découvre que la durée de vie de la batterie des tablettes n’atteint pas ces objectifs. En outre, étant donné que les applications de démarrage s’exécutent en arrière-plan, le nombre d’applications en cours d’exécution sur le système peut être beaucoup plus important que ce que l’utilisateur sait et affecter la réactivité du système. Les applications de démarrage sont classées pour inclure celles tirant parti de ces mécanismes pour démarrer :

-   Exécuter des clés de Registre (HKLM, HKCU, nœuds WOW64 inclus)
-   Clés de Registre RunOnce
-   Dossiers de démarrage dans le menu Démarrer pour les emplacements publics et par utilisateur

de nouvelles fonctionnalités ont été ajoutées à Windows pour s’assurer que les utilisateurs finaux sont toujours en contrôle des applications qui s’exécutent sur leurs systèmes. L’onglet démarrage du gestionnaire des tâches affiche une liste des applications de démarrage, ainsi que des contrôles qui permettent aux utilisateurs de désactiver les applications de démarrage. Pour aider les utilisateurs à déterminer les éléments à désactiver, le gestionnaire des tâches affiche une mesure de chaque impact sur les applications de démarrage. L’impact est évalué en fonction de l’utilisation du processeur et du disque de l’application au démarrage. Les valeurs d’impact sont déterminées en appliquant les critères suivants :

-   **Impact élevé**   Applications qui utilisent plus de 1 seconde du temps processeur ou plus de 3 Mo d’e/s disque au démarrage
-   **Impact moyen**   Applications qui utilisent 300 ms-1000 ms du temps processeur ou 300 Ko-3 Mo d’e/s disque
-   **Impact faible**   Applications qui utilisent moins de 300 ms de temps processeur et moins de 300 Ko d’e/s disque

Microsoft fournit des outils pour aider les développeurs d’applications à évaluer, analyser et prendre des mesures pour réduire leur impact sur le démarrage et améliorer l’expérience utilisateur. Le kit de déploiement et d’évaluation offre la possibilité d’exécuter une évaluation des performances de démarrage et de mesurer l’impact des applications qui s’exécutent au démarrage. les résultats de l’évaluation contiennent des informations détaillées sur l’analyse et la correction, le cas échéant, pour les composants les plus importants au démarrage de Windows. à l’aide de l’analyseur de performances Windows, les développeurs d’applications peuvent effectuer une analyse détaillée afin de déterminer la cause racine de l’impact sur les performances et d’améliorer les performances de démarrage Windows. installez le kit de Windows ADK à partir d' [ici](/previous-versions/windows/hh825494(v=win.10)).

## <a name="guidance"></a>Guidance

Les applications de démarrage s’étendent sur plusieurs catégories, comme décrit dans le tableau ci-dessous. un ensemble de recommandations pour les développeurs est mappé aux catégories d’applications de démarrage pour les aligner sur les modifications fonctionnelles Windows décrites ci-dessus.



Catégories d’applications de démarrage

Description

Recommandation

**Programmes**

Surveiller et mettre à jour les utilisateurs pour les mises à jour en ligne

**Tâche de maintenance**

> [!Note]  
> Toutes les mises à jour doivent être des tâches de maintenance, sans aucune exigence d’interaction avec l’interface utilisateur. Les applications doivent simplement se mettre à jour en mode silencieux, et restaurer en cas d’échec

<br/>

$ {ROWSPAN2} $**assistance matérielle**$ {Remove} $  

Autres points d’accès

fournir un accès à des fonctionnalités de Windows et des applications accessibles via d’autres points d’accès dans Windows

**Remove**

> [!Note]  
> La clé est de réduire les fonctionnalités en double qui existent dans Windows

<br/>

Notificateurs

Fournir aux utilisateurs des notifications concernant leurs appareils

**Remove**

> [!Note]  
> Windows fournit des notifications aux utilisateurs sur leurs appareils

<br/>

**Pré-lanceurs**

Certaines activités préliminaires requises par les applications sont déchargées dans une application de démarrage pendant la connexion de l’utilisateur

**Remove**

> [!Note]  
> Windows 8 est optimisée pour une expérience rapide des lancements d’applications.

<br/>

$ {ROWSPAN4} $**utilitaire**$ {Remove} $  

Synchronisation de PC

Fournir des fonctionnalités de synchronisation sur plusieurs systèmes

**Démarrage** (mises à jour potentielles dans la version bêta)

Sauvegarde et récupération

Point d’entrée pour enregistrer et restaurer l’état des fichiers, des paramètres ou des systèmes entiers

**Windows Stocker l’application pour l’interfaçage avec les utilisateurs**

Télémétrie

Collecter et envoyer des informations sur l’environnement et l’expérience utilisateur

**Tâche de maintenance**

Surveillance de PC

Fournir une surveillance de l’état du système non sollicité et des notifications qui dupliquent les fonctionnalités existantes de la boîte de réception

**Remove**

> [!Note]  
> La clé est de réduire les fonctionnalités en double qui existent dans Windows

<br/>

$ {ROWSPAN2} $**sécurité**$ {Remove} $  

Filtres de & de contrôle parental

Appliquer les règles et restrictions établies pour l’accès Internet et l’utilisation

**Startup**

Configuration et gestion

Autoriser les utilisateurs à contrôler les options de diagnostic et de correction pour l’analyse de la sécurité du système notifier les utilisateurs des découvertes et des actions de sécurité

**Windows Stocker l’application pour l’interfaçage avec les utilisateurs**

**Communication & Internet** (mi & VoIP)

Envoyer et recevoir des messages et des appels

**Windows Application du Store**

**Musique & MP3**

Lire, stocker et gérer la musique

**Windows Application du Store**

**Vidéo photo &**

Détection, enregistrement, rendu, stockage et gestion des photos et des vidéos

**Windows Application du Store**

**Jeux de PC**

Lancer des jeux dans différents domaines

**Windows Application du Store**

**Vente incitative &**

Attirer l’attention sur les biens et services disponibles à l’achat

**Remove**



 

> [!Note]  
> Les instructions relatives aux applications d’accessibilité sont couvertes par des enmissionsments directs distincts avec les éditeurs de logiciels indépendants. Pour plus d’informations, consultez [*programmation pour faciliter l’accès*](../winauto/ease-of-access---assistive-technology-registration.md) .

 

**Windows Applications du Windows Store**

Windows les applications du Store améliorent l’expérience utilisateur en introduisant un espace de Windows avec de nouvelles coordonnées : un nouveau modèle d’application, une nouvelle interface utilisateur et un magasin de Windows. ces options d’infrastructure de langue et de présentation sont disponibles pour le développement d’applications Windows store :

-   HTML/JavaScript/CSS
-   XAML/C #
-   XAML/C++

des informations agrégées pour le développement d’applications Windows store sont disponibles sur le [Centre de développement Windows](https://msdn.microsoft.com/windows/apps/).

Exemples :

-   [développement de jeux Windows Store](/previous-versions/windows/apps/hh452744(v=win.10))
-   [développement d’applications Windows Store qui utilisent des médias](/previous-versions/windows/apps/hh465132(v=win.10))

**Tâches de maintenance automatiques**

L’activité en arrière-plan périodique doit être conçue comme des tâches de maintenance automatique. celles-ci sont planifiées au temps d’inactivité du système pour augmenter la réactivité et l’efficacité énergétique des pc Windows. Les tâches de maintenance peuvent être créées et configurées par une application de bureau au moment de l’installation, à l’aide du kit de développement logiciel (SDK). Pour plus d’informations, consultez la rubrique maintenance automatique suivante.

## <a name="resources"></a>Ressources

-   [Instructions d’accessibilité](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Centre de développement Windows](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

