---
title: Points de restauration
description: Des points de restauration sont créés pour permettre aux utilisateurs de choisir les États système précédents. Chaque point de restauration contient les informations nécessaires à la restauration de l’État choisi par le système. Des points de restauration sont créés avant que les modifications de clé ne soient apportées au système.
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 6ef1aba7d1cb018bb3fa4f32d868828ef2ac4d1b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316092"
---
# <a name="restore-points"></a>Points de restauration

Des points de restauration sont créés pour permettre aux utilisateurs de sélectionner un état système précédent. Chaque point de restauration contient les informations nécessaires pour restaurer le système à l’état sélectionné. Des points de restauration sont créés avant que les modifications de clé ne soient apportées au système.

La restauration du système gère automatiquement l’espace disque alloué aux points de restauration. Il purge les points de restauration les plus anciens pour faire de la place à de nouveaux. La restauration du système alloue de l’espace en fonction de la taille du disque dur et de la version de Windows que l’ordinateur exécute, comme indiqué dans le tableau suivant.

|Version de Windows |&nbsp;Taille du disque dur |Espace de restauration du système |
| --- | --- | --- |
|Windows 7 et versions ultérieures | > 64 GO |Jusqu’à 5% de l’espace disque total ou un maximum de 10 Go, la valeur la plus petite étant retenue |
|  | &le; 64 GO |Jusqu’à trois% de l’espace disque total |
|Windows Vista |  |Jusqu’à 15% de l’espace disque total ou un maximum de 30% d’espace disque disponible, selon la valeur la plus faible |
|Windows XP | >4 GO |Jusqu’à 12% de l’espace disque total<br /><br />Pour modifier la limite de stockage maximale dans Windows XP, utilisez l’élément **système** dans le panneau de configuration. |
|  | \< 4 GO |Jusqu’à 400 Mo |

## <a name="event-triggered-restore-points"></a>Points de restauration déclenchés par un événement

La restauration du système crée automatiquement un point de restauration avant qu’un des événements suivants se produise :

- **Installation d’application** (s’applique uniquement aux applications qui utilisent un programme d’installation conforme à la restauration du système). Si l’installation de l’application entraîne des problèmes système, l’utilisateur peut restaurer le système à un état antérieur à l’installation.
- **Windows Update ou l’installation de la mise à jour AutoUpdate**. Windows Update (anciennement mise à jour automatique) télécharge et installe automatiquement les mises à jour Windows. En outre, il offre aux utilisateurs un moyen simple de télécharger et d’installer manuellement les mises à jour. La restauration du système crée un point de restauration avant l’installation d’une mise à jour, que ce soit automatiquement ou manuellement.
- **Opération de restauration du système**. La restauration du système crée automatiquement un point de restauration en tant que sauvegarde avant le démarrage d’une opération de restauration. Par exemple, supposons qu’un utilisateur restaure accidentellement Windows à un point de restauration incorrect. Pour annuler cette restauration, l’utilisateur peut restaurer Windows à un point de restauration qui est antérieur au premier point de restauration. Une fois que Windows a été restauré à son état initial, l’utilisateur peut répéter le processus, en sélectionnant cette fois le point de restauration approprié.

## <a name="scheduled-restore-points"></a>Points de restauration planifiés

Les utilisateurs peuvent configurer la restauration du système pour créer des points de restauration à intervalles réguliers. Les utilisateurs peuvent également créer et nommer manuellement un point de restauration à tout moment à partir de l’interface utilisateur de la restauration du système. Ces points de restauration sont enregistrés et compressés et sont disponibles dans la liste des points de restauration.

Dans Windows 7 et versions ultérieures, la restauration du système crée un point de restauration planifié uniquement si aucun autre point de restauration n’a été créé au cours des sept derniers jours. Dans Windows Vista, la restauration du système crée un point de contrôle toutes les 24 heures si aucun autre point de restauration n’a été créé ce jour-là. Dans Windows XP, la restauration du système crée un point de contrôle toutes les 24 heures, indépendamment des autres opérations.

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a>Problème connu : vous ne pouvez pas restaurer le système à un point de restauration après avoir installé une mise à jour de Windows 10

Examinez le cas suivant :

1. Vous installez Windows 10 sur un ordinateur propre.
1. Vous activez la protection du système, puis créez un point de restauration système nommé « R1 ».
1. Vous installez une ou plusieurs mises à jour de Windows 10.
1. Une fois l’installation des mises à jour terminée, vous restaurez le système jusqu’au point de restauration « R1 ».

Dans ce scénario, le système n’est pas restauré sur le point de restauration « R1 ». Au lieu de cela, l’ordinateur rencontre une erreur d’arrêt (0xC000021A). Vous redémarrez l’ordinateur, mais le système ne peut pas revenir au bureau Windows.

### <a name="cause"></a>Cause

Il s’agit d’un problème connu dans Windows 10.

Pendant le processus de restauration du système, Windows effectue temporairement la restauration des fichiers en cours d’utilisation. Il enregistre ensuite les informations dans le registre. Lorsque l’ordinateur redémarre, il termine l’opération intermédiaire.

Dans ce cas, Windows restaure les fichiers de catalogue et transfère les fichiers de pilote (. sys) à restaurer au redémarrage de l’ordinateur. Toutefois, lorsque l’ordinateur redémarre, Windows charge les pilotes existants avant de restaurer les versions ultérieures des pilotes. Étant donné que les versions de pilote ne correspondent pas aux versions des fichiers de catalogue restaurés, le processus de redémarrage s’arrête.

### <a name="workaround"></a>Solution de contournement

**Pour effectuer une récupération après un échec de redémarrage et poursuivre le processus de restauration**

Une fois l’erreur survenue, redémarrez l’ordinateur jusqu’à ce qu’il pénètre dans l’environnement de récupération Windows (WinRE). Pour ce faire, vous devrez peut-être utiliser un commutateur de redémarrage matériel et vous devrez peut-être redémarrer plusieurs fois.

Dans l’environnement de récupération Windows :

1. Sélectionnez **résoudre les problèmes** d'  >  **Options avancées**  >  paramètres de démarrage **options de récupération**  >  , puis sélectionnez **redémarrer maintenant**.
1. Dans la liste des paramètres de démarrage, sélectionnez **désactiver la mise en application des signatures de pilotes**.
   > [!NOTE]  
   > Vous devrez peut-être utiliser la touche F7 pour sélectionner ce paramètre.
1. Laissez le processus de démarrage se poursuivre. Lors du redémarrage de Windows, le processus de restauration du système doit reprendre et se terminer.

Ces étapes permettent de restaurer l’ordinateur à son état « R1 ».

**Pour effectuer une récupération suite à un échec de redémarrage**

Pour effectuer une récupération après un échec de redémarrage et annuler le processus de restauration, procédez comme suit :

1. Comme décrit dans la procédure précédente, redémarrez l’ordinateur, puis entrez WinRE.  
1. Dans l’environnement de récupération Windows, sélectionnez **résoudre les problèmes** d'  >  **Options avancées**  >  **restauration du système**, puis sélectionnez annuler la restauration du **système**.

Ces étapes retournent l’ordinateur à l’État dans lequel il se trouvait avant le démarrage du processus de restauration.

**Pour restaurer Windows sur un point de restauration à l’aide de WinRE**

Pour démarrer l’Assistant Restauration du système sur un ordinateur affecté, utilisez WinRE à la place de la boîte de dialogue **paramètres** . Pour ce faire, procédez comme suit :

1. Sélectionnez Paramètres de **démarrage**  >    >  **mettre à jour &** la  >  **récupération** de sécurité.
1. Sous **Options avancées**, sélectionnez **redémarrer maintenant**.
1. Après le démarrage de WinRE, sélectionnez **résoudre les problèmes** d'  >  **Options avancées**  >  **restauration du système**.
1. Entrez votre clé de récupération telle qu’elle est affichée à l’écran, puis suivez les instructions de l’Assistant Restauration du système.

### <a name="references"></a>Références

Pour plus d’informations sur l’utilisation de WinRE, consultez les articles suivants :

- [Environnement de récupération Windows (Windows RE)](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [Démarrer votre ordinateur en mode sans échec dans Windows 10](https://support.microsoft.com/help/12376) 