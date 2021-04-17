---
title: Gestionnaire de fenêtrage est toujours activé
description: Gestionnaire de fenêtrage est toujours activé
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f855635615dee734b9a719d4e51d3ead663d144e
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316590"
---
# <a name="desktop-window-manager-is-always-on"></a>Gestionnaire de fenêtrage est toujours activé

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Dans Windows 8, Gestionnaire de fenêtrage (DWM) est toujours activé et ne peut pas être désactivé par les utilisateurs finaux et les applications. Comme dans Windows 7, DWM est utilisé pour composer le bureau. Outre les expériences activées dans Windows 7, la composition du Bureau DWM permet la composition du Bureau pour tous les thèmes, la prise en charge de la gestion stéréoscopique et la gestion, la séparation et la protection de l’expérience avec les applications du Windows Store.

**Composition du Bureau pour tous les thèmes**

Dans Windows Vista et Windows 7, la composition du Bureau est activée uniquement avec le thème AERO Glass. Par conséquent, les utilisateurs des thèmes Windows classique et à contraste élevé ne peuvent pas utiliser les expériences activées par la composition du poste de travail, telles que le basculement Windows, la mise à l’échelle automatique pour la mise à l’échelle haute résolution, l’aperçu de la miniature et la loupe plein En outre, dans ces versions antérieures de Windows, les développeurs d’applications doivent écrire et gérer plusieurs chemins de code : un où la composition du Bureau est activée et une autre où la composition du Bureau est désactivée.

Avec Windows 8, la composition du Bureau est activée pour tous les thèmes. Les utilisateurs des thèmes Windows classique et à contraste élevé peuvent utiliser les expériences activées par la composition du bureau, telles que le basculement Windows, la mise à l’échelle automatique pour la mise à l’échelle avec résolution élevée (DPI), les aperçus de miniatures et la loupe plein écran. En outre, les développeurs n’ont pas besoin d’écrire et de gérer plusieurs chemins de code, ce qui simplifie le développement.

**Prise en charge de la 3D stéréoscopique**

La composition DWM Desktop prend en charge le rendu et la présentation du contenu de l’application 3D stéréoscopique en mode fenêtre et en plein écran.

**Gestion, séparation et protection de l’expérience avec les applications du Windows Store**

La composition du Bureau DWM permet de séparer et de protéger les fenêtres d’application de bureau des nouvelles fenêtres d’application du Windows Store en gérant et en séparant les fenêtres d’application de bureau des fenêtres d’application du Windows Store. Étant donné que la composition du Bureau est responsable de la gestion de toutes les fenêtres d’application, la désactivation de la composition du Bureau peut entraîner un comportement inattendu. En outre, la composition du Bureau est chargée de composer le nouveau menu Démarrer, ainsi que d’autres animations de fenêtre qui constituent la principale personnalité du nouveau système d’exploitation Windows.

## <a name="controlling-desktop-composition"></a>Contrôle de la composition du Bureau

Dans Windows Vista et Windows 7, la composition du Bureau est désactivée dans un certain nombre de scénarios. Dans Windows 8, la composition du Bureau DWM est un composant principal du système d’exploitation et ne peut pas être désactivée. À quelques exceptions près, la composition du Bureau est toujours activée ; Il est démarré avant l’ouverture de session de l’utilisateur et reste actif pendant la durée d’une session. Cette section décrit comment Windows 8 traite les scénarios dans Windows 7 où la composition du Bureau est désactivée.

**Référence SKU du serveur et certaines références client**

Dans Windows 8, la composition du Bureau est activée pour toutes les références serveur et client. Cela permet de s’assurer que les administrateurs et les utilisateurs du serveur peuvent tirer parti des expériences activées par la composition du bureau.

**Exigences fondamentales pour la composition du Bureau**

Windows 8 garantit que les spécifications de la carte graphique et de la profondeur de couleurs du système sont respectées via la prise en charge des pilotes WDDM et la profondeur des couleurs système.

**Prise en charge des pilotes WDDM**

Si un système n’a pas de pilote graphique compatible WDDM, Windows 8 utilise l’adaptateur d’affichage de base Microsoft comme adaptateur par défaut. Étant donné que DWM s’exécute toujours sur l’adaptateur par défaut, il choisit l’adaptateur d’affichage Microsoft Basic pour composer le bureau lorsqu’un pilote graphique compatible WDDM n’est pas disponible (s’il n’est pas installé ou désactivé) sur le système.

La carte d’affichage de base Microsoft est un rastériseur logiciel qui utilise l’UC plutôt que le GPU pour effectuer tout le dessin. Notez que les performances de la composition du Bureau sur la carte vidéo de base Microsoft (en particulier les animations) peuvent ne pas être aussi lisses que lors de l’exécution de la composition du Bureau sur un GPU.

**Profondeur de couleur système**

Impossible d’exécuter la composition du bureau, sauf si la profondeur de couleur est définie sur 32 bits par pixel. Dans Windows 7, la profondeur de couleur du système peut être modifiée dans les scénarios suivants :

-   Un utilisateur final utilise le panneau de configuration Affichage Windows ou un panneau de configuration tiers pour modifier la couleur système.
-   Un utilisateur final exécute une application qui modifie la profondeur de couleur du système par le biais d’une API publique.

Contrairement à Windows 7, Windows 8 ne prend pas en charge la profondeur de couleur autre que 32 bits par pixel. L’utilisateur ne peut plus modifier la profondeur de couleur du système à l’aide du panneau de configuration.

En outre, les développeurs d’applications ne peuvent pas utiliser les API pour modifier la profondeur de couleur du système. Windows 8 détecte les applications qui essaient de modifier la profondeur de couleur du système pour qu’elle soit inférieure à 32 bits par pixel et informe l’utilisateur qu’un shim de compatibilité des applications doit être appliqué pour exécuter les applications. Après confirmation de l’utilisateur, le shim de compatibilité des applications est appliqué et le shim virtualise le mode de couleur basse à l’application tout en conservant le système en cours d’exécution à 32 bits par pixel.

**WinSAT**

Dans Windows 8, la composition du Bureau ne dépend pas des scores WinSAT. En outre, WinSAT n’intègre plus l’évaluation DWM.

**Compatibilité des applications et action de l’utilisateur**

Dans Windows 8 :

-   Toutes les options de désactivation de la composition du bureau qui existent dans Windows 7 sont supprimées
-   La composition du Bureau est responsable de la composition de tous les thèmes
-   Les applications ne peuvent pas utiliser DwmEnableComposition pour désactiver la composition du bureau. Pour assurer la compatibilité descendante, un appel à cette API retourne la valeur Success ; Toutefois, la composition du Bureau n’est pas désactivée
-   Le shim « désactiver la composition du Bureau » est supprimé
-   L’option « désactiver la composition du Bureau » de l’onglet compatibilité de la boîte de dialogue Propriétés de l’application est supprimée.

**Une application utilise un pilote de mise en miroir pour la communication à distance**

Dans Windows 8 :

-   Ne prend pas en charge les pilotes miroirs pour les scénarios de communication à distance ; Bien que la plupart des applications existantes qui utilisent des pilotes miroirs continuent de fonctionner, en raison de la modification de l’infrastructure nécessaire à la prise en charge des pilotes miroirs existants dans Windows 8 avec DWM, certaines fonctionnalités ou applications qui utilisent des pilotes miroirs peuvent ne pas fonctionner
-   Prend en charge les API de duplication de bureau pour les développeurs d’applications qui utilisent des pilotes miroirs pour les scénarios de communication à distance.
-   Ne prend pas en charge les pilotes de mise en miroir d’accessibilité existants
-   Les pilotes miroirs existants doivent être mis à jour pour s’assurer qu’ils sont compatibles avec Windows 8

**Connexion Bureau à distance**

Dans Windows 8, la composition du Bureau est toujours activée pour une connexion Bureau à distance. Un ordinateur client qui se connecte à un ordinateur distant Windows 8 obtient toujours la composition du Bureau activée pour la session Bureau à distance, quelle que soit la version du client Windows. La composition du Bureau est prise en charge pour plusieurs analyses sur l’ordinateur client, ainsi que pour la session d’application distante.

En outre, lors de la connexion à un ordinateur distant Windows 8, ces paramètres du client Connexion Bureau à distance n’entrent pas en vigueur :

-   Profondeur de couleur
-   Case à cocher « Activer la composition »

La profondeur de couleur de la connexion est toujours définie sur 32 bits par pixel et la composition du Bureau est toujours activée.

 

 




