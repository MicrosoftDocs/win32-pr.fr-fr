---
title: Gestionnaire de fenêtrage est toujours activé
description: Gestionnaire de fenêtrage est toujours activé
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b256b4270ab0bbeba588a4beff9bd1bd2bbe1c8166b40cd527f8b48a4f897df0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057359"
---
# <a name="desktop-window-manager-is-always-on"></a>Gestionnaire de fenêtrage est toujours activé

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**serveurs** – Windows Server 2012  


## <a name="description"></a>Description

dans Windows 8, la Gestionnaire de fenêtrage (DWM) est toujours activée et ne peut pas être désactivée par les utilisateurs finaux et les applications. comme dans Windows 7, DWM est utilisé pour composer le bureau. outre les expériences activées dans Windows 7, la composition du bureau DWM permet la composition du bureau pour tous les thèmes, la prise en charge de l’environnement 3d stéréoscopique, la gestion, la séparation et la protection de l’expérience avec les applications Windows Store.

**Composition du Bureau pour tous les thèmes**

dans Windows Vista et Windows 7, la composition du bureau est activée uniquement avec le thème AERO glass. par conséquent, les utilisateurs de Windows thèmes classiques et à contraste élevé ne peuvent pas utiliser les expériences activées par la composition du bureau, comme Windows Flip, la mise à l’échelle automatique pour la mise à l’échelle haute résolution (DPI), l’aperçu des miniatures et la loupe plein écran. en outre, dans ces versions antérieures de Windows, les développeurs d’applications doivent écrire et gérer plusieurs chemins de code : un où la composition du bureau est activée et une autre où la composition du bureau est désactivée.

avec Windows 8, la composition du bureau est activée pour tous les thèmes. les utilisateurs de Windows des thèmes classiques et à contraste élevé peuvent utiliser les expériences activées par la composition du bureau, comme Windows retourner, la mise à l’échelle automatique pour la mise à l’échelle de haute résolution, les aperçus de miniatures et la loupe plein écran. En outre, les développeurs n’ont pas besoin d’écrire et de gérer plusieurs chemins de code, ce qui simplifie le développement.

**Prise en charge de la 3D stéréoscopique**

La composition DWM Desktop prend en charge le rendu et la présentation du contenu de l’application 3D stéréoscopique en mode fenêtre et en plein écran.

**gestion, séparation et protection de l’expérience avec les applications Windows store**

la composition du bureau DWM permet de séparer et de protéger les fenêtres d’application de bureau des fenêtres des applications du nouveau Windows store en gérant et en séparant les fenêtres d’application de bureau des fenêtres de l’application Windows store. Étant donné que la composition du Bureau est responsable de la gestion de toutes les fenêtres d’application, la désactivation de la composition du Bureau peut entraîner un comportement inattendu. en outre, la composition du bureau est chargée de composer le nouveau menu Démarrer, ainsi que d’autres animations de fenêtre qui constituent la personnalité principale du nouveau système d’exploitation Windows.

## <a name="controlling-desktop-composition"></a>Contrôle de la composition du Bureau

dans Windows Vista et Windows 7, la composition du bureau est désactivée dans un certain nombre de scénarios. dans Windows 8, la composition du bureau DWM est un composant principal du système d’exploitation et ne peut pas être désactivée. À quelques exceptions près, la composition du Bureau est toujours activée ; Il est démarré avant l’ouverture de session de l’utilisateur et reste actif pendant la durée d’une session. cette section décrit comment Windows 8 traite les scénarios dans Windows 7 où la composition du bureau est désactivée.

**Référence SKU du serveur et certaines références client**

dans Windows 8, la composition du bureau est activée pour toutes les références serveur et client. Cela permet de s’assurer que les administrateurs et les utilisateurs du serveur peuvent tirer parti des expériences activées par la composition du bureau.

**Exigences fondamentales pour la composition du Bureau**

Windows 8 garantit que les spécifications de la carte graphique et de la profondeur de couleurs du système sont respectées via la prise en charge des pilotes WDDM et la profondeur des couleurs système.

**Prise en charge des pilotes WDDM**

si un système n’a pas de pilote graphique compatible WDDM, Windows 8 utilise la carte d’affichage Microsoft Basic comme adaptateur par défaut. Étant donné que DWM s’exécute toujours sur l’adaptateur par défaut, il choisit l’adaptateur d’affichage Microsoft Basic pour composer le bureau lorsqu’un pilote graphique compatible WDDM n’est pas disponible (s’il n’est pas installé ou désactivé) sur le système.

La carte d’affichage de base Microsoft est un rastériseur logiciel qui utilise l’UC plutôt que le GPU pour effectuer tout le dessin. Notez que les performances de la composition du Bureau sur la carte vidéo de base Microsoft (en particulier les animations) peuvent ne pas être aussi lisses que lors de l’exécution de la composition du Bureau sur un GPU.

**Profondeur de couleur système**

Impossible d’exécuter la composition du bureau, sauf si la profondeur de couleur est définie sur 32 bits par pixel. dans Windows 7, vous pouvez modifier la profondeur de couleur du système dans les scénarios suivants :

-   un utilisateur final utilise la Windows afficher le panneau de configuration ou un panneau de configuration tiers pour modifier la couleur système.
-   Un utilisateur final exécute une application qui modifie la profondeur de couleur du système par le biais d’une API publique.

contrairement à Windows 7, Windows 8 ne prend pas en charge la profondeur de couleur autre que 32 bits par pixel. L’utilisateur ne peut plus modifier la profondeur de couleur du système à l’aide du panneau de configuration.

En outre, les développeurs d’applications ne peuvent pas utiliser les API pour modifier la profondeur de couleur du système. Windows 8 détectera les applications qui essaient de modifier la profondeur de couleur du système à moins de 32 bits par pixel, et informez l’utilisateur qu’un shim de compatibilité des applications doit être appliqué pour exécuter les applications. Après confirmation de l’utilisateur, le shim de compatibilité des applications est appliqué et le shim virtualise le mode de couleur basse à l’application tout en conservant le système en cours d’exécution à 32 bits par pixel.

**WinSAT**

dans Windows 8, la composition du bureau ne dépend pas des scores winsat. En outre, WinSAT n’intègre plus l’évaluation DWM.

**Compatibilité des applications et action de l’utilisateur**

Dans Windows 8 :

-   Toutes les options de désactivation de la composition du bureau qui existent dans Windows 7 sont supprimées
-   La composition du Bureau est responsable de la composition de tous les thèmes
-   Les applications ne peuvent pas utiliser DwmEnableComposition pour désactiver la composition du bureau. Pour assurer la compatibilité descendante, un appel à cette API retourne la valeur Success ; Toutefois, la composition du Bureau n’est pas désactivée
-   Le shim « désactiver la composition du Bureau » est supprimé
-   L’option « désactiver la composition du Bureau » de l’onglet compatibilité de la boîte de dialogue Propriétés de l’application est supprimée.

**Une application utilise un pilote de mise en miroir pour la communication à distance**

Dans Windows 8 :

-   Ne prend pas en charge les pilotes miroirs pour les scénarios de communication à distance ; bien que la plupart des applications existantes qui utilisent des pilotes miroirs continuent de fonctionner, en raison de la modification de l’infrastructure nécessaire à la prise en charge des pilotes miroirs existants dans Windows 8 avec DWM, certaines fonctionnalités ou applications qui utilisent des pilotes miroirs peuvent ne pas fonctionner
-   Prend en charge les API de duplication de bureau pour les développeurs d’applications qui utilisent des pilotes miroirs pour les scénarios de communication à distance.
-   Ne prend pas en charge les pilotes de mise en miroir d’accessibilité existants
-   Les pilotes miroirs existants doivent être mis à jour pour s’assurer qu’ils sont compatibles avec Windows 8

**Connexion Bureau à distance**

dans Windows 8, la composition du bureau est toujours activée pour une connexion bureau à distance. un ordinateur client qui se connecte à un Windows 8 ordinateur distant obtient toujours la composition du bureau activée pour la session bureau à distance, quelle que soit la version du client Windows. La composition du Bureau est prise en charge pour plusieurs analyses sur l’ordinateur client, ainsi que pour la session d’application distante.

en outre, lors de la connexion à un ordinateur distant Windows 8, ces paramètres du client Connexion Bureau à distance ne prennent pas effet :

-   Profondeur de couleur
-   Case à cocher « Activer la composition »

La profondeur de couleur de la connexion est toujours définie sur 32 bits par pixel et la composition du Bureau est toujours activée.

 

 




