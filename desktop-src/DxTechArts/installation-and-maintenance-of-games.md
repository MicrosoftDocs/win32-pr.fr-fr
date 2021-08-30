---
title: Installation et maintenance des jeux
description: Cet article décrit un ensemble de meilleures pratiques qui peuvent contribuer à réduire la frustration des utilisateurs quant au temps nécessaire à l’installation d’un jeu, à empêcher des appels de support inutiles et à permettre aux utilisateurs de commencer à jouer à votre jeu aussi rapidement et facilement que possible.
ms.assetid: c953165d-2318-ca06-a895-abedcbcb594c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57518a0eb2c0d9dc07497e8c530394469df0354c321414191e6d07385352992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830499"
---
# <a name="installation-and-maintenance-of-games"></a>Installation et maintenance des jeux

Cet article décrit un ensemble de meilleures pratiques qui peuvent contribuer à réduire la frustration des utilisateurs quant au temps nécessaire à l’installation d’un jeu, à empêcher des appels de support inutiles et à permettre aux utilisateurs de commencer à jouer à votre jeu aussi rapidement et facilement que possible.

-   [Installation initiale](#initial-installation)
    -   [Rationalisation de l’interface utilisateur d’installation](#streamlining-the-installation-ui)
    -   [Réduction du temps nécessaire à l’installation](#reducing-the-time-required-for-installation)
    -   [Installation minimale](#minimal-installation)
    -   [Installer à la demande](#install-on-demand)
-   [Jeu après l’installation](#post-installation-game-play)
    -   [AutoRun](#autorun)
    -   [Conversion d’une installation Install-on-demand en installation complète](#converting-an-install-on-demand-installation-to-a-full-installation)
    -   [Maintenance du logiciel de jeu et du contenu](#maintenance-of-game-software-and-content)
    -   [Vérification automatique des mises à jour](#checking-for-updates-automatically)
    -   [Téléchargement automatique des correctifs](#downloading-patches-automatically)
-   [Autres ressources](#other-resources)
-   [Rubriques connexes](#related-topics)

## <a name="initial-installation"></a>Installation initiale

Les utilisateurs achètent des jeux parce qu’ils aiment les lire, pas parce qu’ils apprécient de les installer. L’installation d’un jeu doit être aussi rapide, simple et facile que possible pour l’utilisateur final. Dans l’idéal, les utilisateurs finaux ne doivent même pas voir une interface utilisateur d’installation. ils doivent pouvoir simplement déposer le disque du jeu dans la barre d’État et commencer à jouer.

### <a name="streamlining-the-installation-ui"></a>Rationalisation de l’interface utilisateur d’installation

Les aspects courants des interfaces utilisateur d’installation de jeux existantes interfèrent avec l’expérience utilisateur final souhaitée :

-   Poser des questions à l’utilisateur.

    Par exemple, de nombreux jeux demandent si l’utilisateur souhaite installer DirectX. Si le jeu nécessite l’exécution de Microsoft DirectX et que la version appropriée de DirectX n’est pas déjà installée, le jeu doit simplement installer DirectX.

-   Demander aux utilisateurs de répondre de la même manière à la plupart des utilisateurs.

    pour les utilisateurs standard, les paramètres par défaut pour le chemin d’installation, l’emplacement du menu Démarrer, etc., sont tous corrects. Offre des options avancées pour les utilisateurs qui souhaitent modifier ces paramètres.

L’interface utilisateur de l’installation doit être conçue pour permettre à l’utilisateur standard de commencer à jouer le jeu le plus rapidement possible. Si l’exécution automatique est activée sur l’ordinateur de l’utilisateur, qui est la valeur par défaut, le programme d’installation doit supposer que l’utilisateur souhaite jouer le jeu le plus rapidement possible, en ignorant toutes les questions inutiles. Le programme d’installation de PROGRA à la[demande](#install-on-demand)m doit commencer à installer le jeu dans le chemin d’installation par défaut, de préférence à l’aide d’une configuration telle que décrite dans. Il convient de fournir aux utilisateurs la possibilité de modifier les paramètres d’installation avant de démarrer automatiquement l’installation. Toutefois, cette procédure doit être effectuée en invitant l’utilisateur à appuyer sur une touche pour les options d’installation avancées, puis à poursuivre automatiquement avec les options par défaut si l’utilisateur n’atteint pas cette clé dans un délai de cinq à dix secondes.

Si l’exécution automatique n’est pas activée sur l’ordinateur de l’utilisateur, le programme d’installation doit supposer que l’utilisateur ne souhaite pas que le programme d’installation commence à installer le jeu automatiquement. Si le programme d’installation démarre par d’autres moyens que l’exécution automatique, il doit lancer l’interface utilisateur d’installation avancée.

### <a name="reducing-the-time-required-for-installation"></a>Réduction du temps nécessaire à l’installation

la plupart des jeux de Windows Microsoft prennent aujourd’hui entre cinq minutes et une demi-heure pour terminer le processus d’installation. En revanche, la plupart des jeux de console ne prennent pas plus de trente secondes à partir du moment où l’utilisateur insère le CD-ROM de jeu au moment où il peut jouer le jeu. cette différence est due au fait que la plupart des Windows jeux sont conçus pour s’exécuter le plus souvent, s’ils ne sont pas tous, du contenu du disque dur de l’ordinateur ; les consoles, qui n’ont pas d’emplacement pour stocker de façon permanente de grandes quantités de contenu, nécessitent que le contenu soit exécuté à partir du média source. Lors du chargement du contenu à partir du disque dur local, le temps de chargement des jeux est plus rapide, mais l’inconvénient est que tout le contenu doit être copié à partir du média source vers le disque dur à un moment donné. la plupart des Windows jeux choisissent de copier tout le contenu sur le disque dur en une seule fois, dans le cadre d’un processus d’installation. Cela vous permet de passer de l’expérience initiale de l’utilisateur au jeu en faisant en sorte que l’utilisateur regarde une barre de progression pendant plusieurs minutes avant de pouvoir jouer au jeu.

Il existe deux approches qui peuvent être utilisées pour réduire le temps consacré à l’installation initiale du jeu : [installation minimale](#minimal-installation) et installation [à la demande](#install-on-demand).

### <a name="minimal-installation"></a>Installation minimale

Dans un scénario d’installation minimale, le jeu installe uniquement un jeu minimal de contenu sur le disque dur. En règle générale, cela se compose uniquement de l’exécutable du jeu et des dll. Le reste du contenu est accessible directement à partir du support source. Cela réduit considérablement le temps nécessaire à l’installation, puisque l’exécutable d’un jeu est rarement supérieur à 10-20 Mo. L’inconvénient est que le jeu met plus de temps à charger du contenu pendant le jeu, car il doit le charger à partir du média source plus lent.

pour créer une configuration d’installation minimale dans une installation basée sur Windows Installer :

-   Regroupez tous les composants à installer sur le disque dur dans une fonctionnalité marquée pour une installation locale.

    Cette fonctionnalité sera appelée « démarrage ».

-   Regroupez tous les composants qui doivent être exécutés à partir du média source dans une fonctionnalité marquée comme « exécuter à partir de la source ».
-   Lorsque vous ouvrez un fichier qui peut se trouver sur le média source, utilisez la fonction [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) pour déterminer le chemin d’accès au fichier, au lieu de coder en dur le chemin d’accès.

    Cela permet de s’assurer que le fichier peut être trouvé même si la lettre de lecteur du lecteur de CD/DVD de l’utilisateur change.

-   Compressez le contenu qui reste sur le CD/DVD.

    La quantité de temps processeur passée à décompresser le contenu est généralement masquée par le taux de transfert lent des données à partir du lecteur de CD/DVD.

-   Regroupez le contenu dans des fichiers volumineux et contigus et accédez-y dans un ordre séquentiel.

    Les heures de recherche de lecteurs de CD/DVD sont Abysmal par rapport à celles des disques durs, et la plupart des lecteurs de CD/DVD n’atteignent pas les taux de transfert maximal, sauf s’ils lisent un fichier de grande taille et contigu.

-   Posez le contenu sur le CD/DVD dans l’ordre dans lequel il est susceptible d’être accédé.

    Les temps de recherche sont très réduits lorsque les fichiers sont accessibles dans le même ordre que la disposition sur disque.

### <a name="install-on-demand"></a>Installer à la demande

Dans un scénario d’installation à la demande, comme pour une installation minimale, le jeu installe initialement sur le disque dur uniquement les fichiers nécessaires pour démarrer le jeu. Toutefois, au lieu d’accéder au contenu restant à partir du média source chaque fois que cela est nécessaire, le jeu installe en fait chaque morceau de contenu sur le disque dur, tel qu’il est nécessaire pour la première fois, puis accède au disque dur local à chaque utilisation suivante. Le temps nécessaire à l’installation initiale est aussi réduit que dans pour une installation minimale, mais après la première fois que vous accédez à chaque élément de contenu, les temps de chargement s’améliorent.

pour créer une configuration à la demande install-on-demand dans une installation basée sur un Windows Installer :

-   Regroupez tous les composants à installer initialement sur le disque dur dans une fonctionnalité marquée pour une installation locale.

    Notez que cela est identique à la fonctionnalité bootstrap pour une installation minimale.

-   Regroupez le contenu restant en plusieurs fonctionnalités basées sur les composants susceptibles d’être utilisés ensemble.

    Par exemple, dans un jeu basé sur le niveau, regroupez tout le contenu utilisé à un niveau donné en une seule fonctionnalité. notez que Windows Installer permet à un composant d’être partagé par plusieurs fonctionnalités. par conséquent, si vous disposez d’un contenu qui est utilisé sur plusieurs niveaux, vous pouvez ajouter ce contenu aux fonctionnalités pour tous les niveaux nécessaires sans répliquer le contenu. Toutes ces fonctionnalités doivent être marquées comme « publiées », ce qui signifie qu’elles ne seront pas installées au début, mais peuvent être installées ultérieurement si nécessaire.

-   Lorsqu’un fichier est nécessaire, vérifiez d’abord si le fichier est déjà installé à l’aide de la fonction [**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea).

    S’il n’est pas encore installé (c’est-à-dire que son état est INSTALLSTATE \_ publié), appelez la fonction [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) pour installer la fonctionnalité localement. Lorsque vous ouvrez le fichier après son installation, appelez [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) pour déterminer le chemin d’accès au fichier. Bien que cela ne soit pas strictement nécessaire pour ce scénario (puisque le contenu sera toujours installé sur le disque dur avant son utilisation), cela facilite la prise en charge de l’installation minimale en plus de l’installation à la demande.

-   Si possible, anticipez le contenu qui sera probablement nécessaire, puis installez-le en arrière-plan pendant la durée d’inactivité.

    L’installation en arrière-plan est plus appropriée lorsque le jeu est à un point qui n’a pas besoin de toutes les performances de l’ordinateur. par exemple, lors de l’affichage d’un film de présentation, d’un couper-scène, d’un menu, etc.

-   Créez une option dans le menu options du jeu pour forcer l’installation de tout le reste du contenu.

    Pour l’implémenter, créez une fonctionnalité qui est un parent de toutes les fonctionnalités d’installation à la demande, puis appelez [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) pour installer cette fonctionnalité maître localement. Cela entraîne également l’installation des sous-fonctionnalités localement.

-   La disposition du contenu doit être similaire à celle d’une installation minimale, sauf que le contenu doit être mis en cluster uniquement avec un autre contenu qui est susceptible d’être nécessaire en même temps (par exemple, tout le contenu d’un niveau doit être ensemble).

## <a name="post-installation-game-play"></a>Game-Play après l’installation

### <a name="autorun"></a>AutoRun

Pour jouer un jeu déjà installé, l’utilisateur doit seulement déposer le disque d’installation dans le plateau du lecteur. La première chose que doit faire l’exécutable d’exécution automatique sur le disque consiste à vérifier si le jeu a déjà été installé et, le cas échéant, à lancer le jeu. en supposant que le jeu a été installé à l’aide d’une configuration Windows Installer, la vérification pour déterminer si le jeu est installé peut être effectuée avec un seul appel à la fonction [**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea).

### <a name="converting-an-install-on-demand-installation-to-a-full-installation"></a>Conversion d’une installation Install-on-demand en installation complète

Bien qu’une installation à la demande permette à l’utilisateur de commencer à jouer le jeu plus tôt qu’une installation complète, un utilisateur peut souhaiter installer explicitement le reste du contenu du jeu sur le disque dur local. L’utilisateur peut vouloir jouer au jeu sans avoir besoin du média source, ou il souhaite simplement éviter les temps de chargement en jeu plus longs qui résultent de l’installation du contenu à la demande. si la configuration du jeu utilise Windows Installer, le jeu peut fournir une option dans l’interface utilisateur des options de jeu pour terminer l’installation du contenu restant. Lorsque l’utilisateur sélectionne cette option, le jeu peut appeler [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) pour forcer l’installation locale des fonctionnalités restantes. Il n’est pas nécessaire de générer une application d’installation distincte pour ce faire.

### <a name="maintenance-of-game-software-and-content"></a>Maintenance du logiciel de jeu et du contenu

l’un des avantages que Windows jeux ont sur les jeux de console est la simplicité relative avec laquelle le serveur de publication peut publier des mises à jour du jeu après sa publication initiale. Que ces mises à jour introduisent du nouveau contenu ou résolvent simplement des bogues, il est important de rendre le processus de mise à jour aussi simple que possible pour l’utilisateur final. Le processus de mise à jour est encore plus important pour les jeux en ligne, qui requièrent généralement que tous les utilisateurs exécutent la dernière version du jeu pour se connecter.

### <a name="checking-for-updates-automatically"></a>Vérification automatique des mises à jour

Les utilisateurs n’ont pas à se souvenir de trouver les correctifs. Si une mise à jour est disponible pour le jeu, l’utilisateur doit au moins être averti et, idéalement, le correctif doit déjà être téléchargé.

Un moyen simple de vérifier la disponibilité de mises à jour consiste à se connecter à un serveur Web hébergé par le serveur de publication à l’aide d’une URL spécifique et à télécharger un fichier texte qui spécifie le numéro de version de la dernière version disponible du jeu, ainsi qu’une URL à partir de laquelle télécharger un package qui mettra à jour le jeu vers la dernière version.

La recherche de mises à jour chaque fois que l’utilisateur joue le jeu est suffisante pour s’assurer que l’utilisateur exécute la dernière version. Toutefois, si l’existence d’une nouvelle mise à jour est détectée immédiatement avant que l’utilisateur tente de jouer au jeu, l’utilisateur peut être contraint de retarder le jeu jusqu’à la fin du téléchargement de la mise à jour. Pour les mises à jour volumineuses ou les connexions lentes, ce délai peut être de l’ordre des heures. Pour éviter de forcer l’utilisateur à attendre avant de jouer au jeu, le jeu peut utiliser Planificateur de tâches pour planifier des vérifications périodiques des nouvelles mises à jour. Si une mise à jour est détectée, le jeu peut commencer à télécharger la mise à jour immédiatement, afin qu’elle soit entièrement téléchargée et prête à être installée lors de la prochaine exécution du jeu par l’utilisateur.

### <a name="downloading-patches-automatically"></a>Téléchargement automatique des correctifs

Une fois que le jeu a détecté qu’une nouvelle mise à jour est disponible, il doit immédiatement commencer à télécharger la mise à jour. Étant donné que la tâche qui vérifie les mises à jour s’exécute en mode silencieux en arrière-plan, le téléchargement doit être le plus discret possible. Le Service de transfert intelligent en arrière-plan (BITS) est une fonctionnalité du système d’exploitation qui permet aux applications de télécharger des fichiers à partir d’Internet, même si l’application elle-même n’est pas en cours d’exécution. Les tâches de téléchargement BITS s’exécutent uniquement lorsque l’utilisateur a ouvert une session et uniquement lorsque l’ordinateur est déjà connecté au réseau. Le service BITS ne tentera pas de forcer la connexion de l’ordinateur au réseau. Si l’utilisateur se déconnecte du réseau, ou se déconnecte, le travail BITS est suspendu et reprend le téléchargement la prochaine fois que l’utilisateur se connecte et se connecte au réseau. L’application peut configurer ses travaux BITS pour qu’elle utilise uniquement la bande passante réseau qui, sinon, ne serait pas utilisée, afin d’éviter que la tâche n’affecte les performances de toutes les autres applications susceptibles d’utiliser le réseau (par exemple, un jeu en ligne). le service BITS est disponible sur Windows XP et Windows 2000 Service Pack 3.

## <a name="other-resources"></a>Autres ressources

Pour plus d’informations sur les technologies référencées dans cet article, reportez-vous aux sections correspondantes de MSDN Library :

-   [Windows Installer](/windows/desktop/Msi/windows-installer-portal)
-   [Planificateur de tâches](/windows/desktop/TaskSchd/task-scheduler-start-page)
-   [Service de transfert intelligent en arrière-plan](/windows/desktop/Bits/background-intelligent-transfer-service-portal) (bits)

pour plus d’informations sur l’utilisation de Windows Installer pour les jeux, connectez-vous à l’article DirectX du mois suivant, « Introduction aux Windows Installer pour les développeurs de jeux ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea)
</dt> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea)
</dt> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 