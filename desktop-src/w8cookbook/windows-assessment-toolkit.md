---
title: Kit d’évaluation Windows
description: Kit d’évaluation Windows
ms.assetid: 9D0A4F42-F027-4032-8297-045937BD2B6E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6eff172a59a7f0ee00f85a0cd8f237387aaa78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404529"
---
# <a name="windows-assessment-toolkit"></a>Kit d’évaluation Windows

## <a name="platforms"></a>Plateformes

**Clients** -Windows 7 \| Windows 8  

## <a name="description"></a>Description

l’évaluation de la Windows Shared Computer Toolkit et les performances de Windows Shared Computer Toolkit composent le Kit de déploiement et d’évaluation Windows (ADK). ensemble, ils fournissent une solution complète pour évaluer les performances globales de l’ordinateur et automatiser le déploiement du système d’exploitation Windows sur de nouveaux ordinateurs.

cette rubrique se concentre sur le **Shared Computer Toolkit d’évaluation**. Les résultats de l’évaluation sont utilisés pour diagnostiquer les problèmes potentiels, afin que le matériel et les logiciels que vous développez soient réactifs et aient un impact minimal sur la durée de vie de la batterie, les performances de démarrage et l’heure d’arrêt. Les mêmes évaluations sont disponibles pour les partenaires OEM, les partenaires ISV/IHV, les passionnés et les autres membres de la Communauté, afin d’établir un cadre commun pour mesurer, comparer et examiner les aspects de la qualité.

à l’aide des outils d’évaluation de Windows, vous pouvez mesurer différents aspects des performances dans divers scénarios, du temps de démarrage aux performances de la durée de vie de la batterie à la diffusion vidéo haute définition. Les évaluations permettent d’identifier les problèmes potentiels, les comportements incohérents et de mettre en évidence les zones à examiner.

dans les versions précédentes de Windows, plusieurs outils étaient disponibles pour mesurer la qualité, notamment velocity Test suite (stm/VOS), Fundamental quality tools suite (FQTS) et System Power and Performance tools suite (SPPTS). l’Shared Computer Toolkit d’évaluation associe les fonctionnalités de ces outils de diagnostic des performances à un ensemble intégré d’outils qui est plus facile à utiliser et fournit des résultats plus larges et plus significatifs.

l’évaluation de la Windows Shared Computer Toolkit optimise la satisfaction des consommateurs en :

-   vous aider à évaluer l’expérience globale des Windows, des logiciels et des pilotes à valeur ajoutée, ainsi que des configurations matérielles
-   Fournir des données système détaillées qui peuvent vous aider à identifier les causes racines des problèmes de qualité
-   Réduction des coûts en révélant les problèmes pendant le développement
-   Génération de comparaisons de résultats à partir de différents ordinateurs ou du même ensemble d’ordinateurs dans le temps en créant des graphiques de comparaison à partir de plusieurs jeux de résultats
-   Génération de commentaires dans un format standardisé que vous pouvez utiliser pour améliorer la qualité de vos produits

des objectifs d’entreprise importants peuvent être atteints à l’aide des évaluations Shared Computer Toolkit :

-   **Mesurer & comparer** : vous pouvez utiliser les données pour comparer des composants (logiciels, pilotes ou les deux) à d’autres composants similaires afin de faciliter la prise de décision, les recommandations et le marquage des bancs d’essai compétitifs.
-   **Amélioration** de la qualité : vous pouvez travailler indépendamment ou avec des partenaires concernés pour créer un composant (logiciel, pilote ou les deux) conformément aux critères de qualité prédéfinis
-   **Suivre la qualité**   Vous pouvez créer un processus pour suivre efficacement la qualité des versions des composants et détecter les régressions après chaque itération.

## <a name="usage-and-best-practices"></a>Utilisation et meilleures pratiques

Les évaluations sont une combinaison de fichiers XML et binaires qui induit un ensemble spécifique d’États sur un ordinateur, mesurent et enregistrent l’activité et conservent les résultats enregistrés. Un travail est un regroupement d’une ou plusieurs évaluations et de leurs paramètres, exécutés simultanément sur un ordinateur. La plateforme d’évaluation fournit l’infrastructure permettant d’exécuter et d’afficher de manière cohérente les travaux, les évaluations et les résultats. Les résultats incluent souvent des informations de diagnostic et de correction qui vous aident à déterminer les zones nécessitant une investigation supplémentaire et une action corrective. Vous pouvez :

-   exécuter des évaluations sur un seul ordinateur ou une petite collection d’ordinateurs avec la **Console d’évaluation de Windows** (Windows AC) <dl> Ce scénario est destiné aux utilisateurs qui souhaitent afficher les caractéristiques des performances sur une ou plusieurs configurations d’ordinateur différentes. Windows AC est une interface graphique utilisateur utilisée pour regrouper les évaluations, créer un travail, empaqueter un travail, exécuter le travail et gérer les résultats de la tâche. Les résultats incluent souvent des actions recommandées.  
    </dl>
-   Run assessments against multiple computers in a lab environment with **Windows Assessment Services** (Windows AS) <dl> Ce scénario est principalement destiné aux utilisateurs qui souhaitent exécuter une suite d’évaluations qualitatives sur une gamme complète de postes de travail, d’ordinateurs portables ou de tablettes dans un environnement de développement.  
    </dl>

l’Shared Computer Toolkit d’évaluation offre les fonctionnalités suivantes :

-   Une interface utilisateur graphique simple et des évaluations qui peuvent être utilisées pour évaluer un ordinateur sans aucune connaissance technique approfondie du système
-   Résultats de l’évaluation, affichés dans la console ou l’interface utilisateur, qui incluent souvent des recommandations pour vous aider à améliorer le système
-   La possibilité d’exécuter une tâche préconfigurée en un seul clic
-   Paramètres d’évaluation prédéfinis dans chaque évaluation de travail préconfigurée pour pouvoir exécuter un travail sur plusieurs ordinateurs et être certain que les résultats sont comparables
-   Travaux pouvant être personnalisés pour inclure les évaluations que vous souhaitez utiliser et les paramètres que vous souhaitez utiliser
-   Syntaxe de ligne de commande de la plateforme d’évaluation pour l’écriture de scripts et l’automatisation des tâches
-   La possibilité d’exécuter un travail, d’afficher les résultats, de prendre des mesures de correction pour améliorer le système, puis de réexécuter la tâche et de comparer les nouveaux résultats côte à côte avec les anciens résultats pour voir comment le système a été amélioré

le Shared Computer Toolkit d’évaluation est généralement utilisé dans les scénarios suivants :




| Scénario | Description | 
|----------|-------------|
| « Boîte noire » | Exécutez une tâche prédéfinie et examinez les résultats pour toutes les valeurs inhabituelles ou les indications de problèmes relatifs aux pilotes, à l’utilisation de la mémoire ou à d’autres zones que l’évaluation adresse. | 
| Comparaison des résultats | <ol><li>Exécutez une évaluation unique à l’aide des paramètres recommandés sur tout ordinateur qui exécute un système d’exploitation pris en charge.</li><li>utilisez la Windows AC pour empaqueter le travail à exécuter sur un autre ordinateur.</li><li>Enregistrez les résultats dans un partage afin de pouvoir comparer les résultats.</li><li>comparez les résultats de n’importe quel ordinateur Windows à ceux de tout autre système d’exploitation pris en charge pour identifier les différences.</li></ol><br /> | 
| Nettoyer l’ordinateur | Exécutez des évaluations sur un ordinateur propre qui comprend uniquement le système d’exploitation pour établir les résultats du système de base. | 
| Ordinateur avec des composants matériels ou logiciels ajoutés | Ajoutez du nouveau matériel ou logiciel au système de l’ordinateur propre, puis réexécutez les évaluations pour comparer les résultats avec les résultats propres à l’ordinateur. | 
| Création d’évaluations | Utilisez des API publiques pour développer ou étendre une évaluation, ou intégrer des évaluations à vos outils et à votre infrastructure. | 




 

Ces évaluations peuvent être utilisées :



| Évaluation                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pré-validation de la certification du pilote          | l’évaluation de la **pré-validation de Certification de pilote** vérifie que les pilotes sur un système d’exploitation en cours d’exécution Windows qualifiés pour le programme de Certification Windows. Les résultats incluent des recommandations qui vous aident à résoudre les problèmes détectés par l’évaluation, tels que des pilotes non signés ou des signatures expirées.                                                                                                                                                                                                                                                            |
| Vérification du pilote                          | l’évaluation de la **vérification du pilote** vérifie qu’une image de Windows hors connexion ou un système d’exploitation Windows en cours d’exécution contient le jeu de pilotes approprié. Les résultats incluent des recommandations pour vous aider à résoudre les problèmes trouvés par l’évaluation. Ces problèmes peuvent inclure des pilotes manquants, dupliqués, anciens ou inutiles.                                                                                                                                                                                                                                         |
| Gestion de fichiers                                | L’évaluation de la **gestion des fichiers** offre un moyen automatisé d’effectuer des opérations de fichiers courantes et de capturer des métriques. Les métriques mesurent les durées et le débit pour vous aider à comprendre le fonctionnement d’un ordinateur dans les scénarios de gestion de fichiers des utilisateurs finaux. L’évaluation de la gestion des fichiers utilise un ensemble de charges de travail pour simuler un utilisateur qui copie, déplace, compresse, décompresse et supprime des fichiers et des dossiers sur les systèmes clients.                                                                                                                                       |
| Gestion des photos                               | L’évaluation de la **gestion des photos** mesure les performances de l’ordinateur et la durée de vie de la batterie en simulant un utilisateur final qui visualise et manipule des photos.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Lancer/créer un onglet dans Internet Explorer          | L’évaluation des **performances de démarrage d’Internet Explorer** permet d’identifier les composants qui peuvent affecter le temps nécessaire au démarrage d’Internet Explorer. L’évaluation mesure le temps nécessaire pour restituer entièrement une page vierge, y compris le temps de chargement du processus de IExplore.exe et les intervalles de création de trame et de création de tabulation. Elle mesure également l’effet de toutes les extensions, compléments et barres d’outils installés sur le système. Il ne mesure pas les performances du réseau ou de navigation.                                                                                         |
| Actif/inactif                                       | l’évaluation **de la Transition activée/désactivée** mesure les performances des scénarios de performances de démarrage, Windows 8 de mise en veille et de veille prolongée.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Performances de navigation dans Internet Explorer       | L’évaluation des **performances de navigation Internet Explorer** mesure la qualité de l’expérience de navigation dans Internet Explorer et évalue les capacités de l’UC et du matériel graphique. Trois charges de travail de navigation distinctes sont fournies pour insister sur l’ordinateur de différentes façons.                                                                                                                                                                                                                                                                                                  |
| Performances du transcodage multimédia                | L’évaluation de la **vidéo de transcodage** mesure le processus de modification d’un fichier vidéo vers un format ou une vitesse de transmission différents. Cette évaluation exécute une série d’opérations de transcodage avec des formats et des résolutions de fichiers d’entrée et de sortie courants.                                                                                                                                                                                                                                                                                                                                           |
| Windows Performances de l’interface utilisateur                       | l’évaluation des performances de l' **interface utilisateur Windows** évalue les performances de certaines expériences de base au sein de l’interface utilisateur Windows. l’évaluation mesure la réactivité et la qualité du rendu, tandis que l’évaluation exerce des charges de travail qui simulent des activités de l’utilisateur, telles que l’utilisation de la recherche et de la transition de Windows environnement de l’application Store sur le bureau. Les résultats de réactivité sont mesurés en millisecondes. Un nombre faible signifie que l’ordinateur est plus rapide et plus réactif. Pour le rendu, les résultats indiquent la fréquence d’images et le nombre de problèmes qui se produisent. |
| Encombrement mémoire                             | Vous pouvez utiliser l’évaluation de l' **encombrement mémoire** pour comparer quantitativement une image de base du système d’exploitation à une autre image du système d’exploitation. Vous pouvez ensuite identifier les composants spécifiques qui affectent l’encombrement mémoire du système physique. Ces composants peuvent inclure des pilotes, des applications de complément, des packages de logiciels préchargés et des programmes antivirus.                                                                                                                                                                                                           |
| Performances du premier démarrage                       | la **première** évaluation des performances de démarrage identifie les problèmes qui affectent la Windows durée de démarrage et d’affichage de l’écran d’accueil lors du premier démarrage de l’ordinateur. Les résultats aident les fabricants OEM à diagnostiquer ce qui provoque des retards et à fournir des recommandations pour améliorer l’expérience.                                                                                                                                                                                                                                                                                      |
| Diffusion multimédia en continu                              | L’évaluation des **performances de diffusion multimédia en continu** vous aide à évaluer les performances d’une configuration d’ordinateur lors de la diffusion en continu de médias à l’aide d’Internet Explorer. Vous pouvez utiliser les résultats de l’évaluation pour comprendre, comparer et améliorer l’expérience de diffusion multimédia en continu.                                                                                                                                                                                                                                                                                                                 |
| Complète WinSAT                         | l' **évaluation du système Windows (winsat)** est utilisée pour évaluer et améliorer les performances d’un ordinateur dans plusieurs composants système, notamment l’uc, la mémoire, le disque et les graphiques. Les résultats de l’évaluation complète WinSAT expriment la capacité d’une configuration matérielle de l’ordinateur en chiffres. Des scores plus élevés signifient généralement que l’ordinateur évalué est plus performant et plus rapide qu’un ordinateur dont le score est inférieur.                                                                                                                                                        |
| Efficacité énergétique                            | La tâche d' **efficacité énergétique** offre un moyen automatique d’évaluer la durée de vie de la batterie d’un ordinateur. À l’aide de charges de travail, la tâche d’efficacité énergétique effectue également des diagnostics qui évaluent si les composants système utilisent de l’alimentation lorsqu’ils doivent être inactifs.                                                                                                                                                                                                                                                                                                               |
| Paramètres de Diagnostic du minifiltre               | l’option de **Diagnostic minifiltre** s’exécute au cours de l’évaluation des performances de démarrage d’Internet Explorer, de l’évaluation de la gestion des fichiers et de l’évaluation des performances de démarrage (Windows 8). La sélection de cette option dans les évaluations qui offrent l’option de diagnostic minifiltre produit des métriques qui vous aident à évaluer l’impact des opérations de minifiltre sur différents scénarios d’évaluation.                                                                                                                                                                                  |
| Lecteur Windows Media Performances et qualité | l’évaluation des **performances et de la qualité de Lecteur Windows Media** lance WMP et lit plusieurs clips multimédias l’un après l’autre pour capturer les performances et les mesures de qualité liées à la lecture du média.                                                                                                                                                                                                                                                                                                                                                                          |



 

d’autres outils, tels que les Shared Computer Toolkit de performances Windows, sont inclus dans le kit ADK. Ces outils fournissent des informations approfondies qui vous permettent d’analyser et de suivre les performances du système et des applications. Pour plus d’informations, consultez la section des ressources ci-dessous.

## <a name="resources"></a>Ressources

**Vidéosurveillance**

-   [Vidéos ADK channel9 BUILD](https://channel9.msdn.com/Events/BUILD/BUILD2011?sort=status&direction=asc&term=&t=assessment+and+deployment+kit)

  
**Correspondante**

-   [Kit de déploiement et d’évaluation Windows](/previous-versions/windows/hh825420(v=win.10))
-   [Windows informations techniques de référence sur l’évaluation Shared Computer Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh825508(v=win.10))
-   [Moteur d’exécution d’évaluation](/previous-versions/windows/desktop/axe/axe-access-portal)
-   [Windows Analyse des performances](https://msdn.microsoft.com/performance/default.aspx)

  


 

