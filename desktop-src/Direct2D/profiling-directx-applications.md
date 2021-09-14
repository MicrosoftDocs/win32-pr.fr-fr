---
title: Profilage d’applications DirectX
description: montre comment mesurer certaines des mesures les plus importantes en matière de temps de performances pour une application DirectX à l’aide des outils XPerf et GPUView fournis dans le cadre du Shared Computer Toolkit de performances Windows.
ms.assetid: 4B2F7273-C9B0-4DD3-B559-6220CDE62129
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0280389d4f8f2161e5e07f8906df7ea0484ad458
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112581"
---
# <a name="profiling-directx-apps"></a>Profilage d’applications DirectX

cela vous montre comment mesurer certaines des mesures les plus importantes en matière de temps de performances pour une application [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) à l’aide des outils **XPerf** et **GPUView** fournis dans le cadre du Shared Computer Toolkit de performances de Windows. Il ne s’agit pas d’un guide complet pour comprendre les outils, plutôt que leur applicabilité spécifique pour l’analyse des performances des applications DirectX. Alors que la plupart des techniques présentées ici s’appliquent à toutes les applications DirectX, elles sont particulièrement pertinentes pour les applications qui utilisent des chaînes de permutation et non pour les applications DirectX basées sur XAML qui utilisent SIS/outre et les animations XAML. Nous vous guidons tout au long des mesures de temps de performance clés, de l’acquisition et de l’installation des outils et des suivis de mesure des performances, puis les analysent pour comprendre les goulots d’étranglement des applications.

## <a name="about-the-tools"></a>À propos des outils

### <a name="xperf"></a>**XPerf**

**XPerf** est un ensemble d’outils d’analyse des performances basés sur Suivi d’v nements pour Windows (ETW) conçus pour mesurer et analyser les performances du système et des applications détaillées et l’utilisation des ressources. à partir de Windows 8 cet outil en ligne de commande a une interface utilisateur graphique et est appelé le Windows l’enregistreur de performances (WPR) et l’analyseur de performances Windows (WPA). pour plus d’informations sur ces outils, consultez la page web relative à [Windows performance Shared Computer Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)) (WPT) : [Windows performance Shared Computer Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)).

Un ETW collecte les événements de noyau demandés et les enregistre dans un fichier appelé fichier journal de suivi d’événements (ETL). Ces événements de noyau fournissent des informations complètes sur les caractéristiques d’une application et du système lors de l’exécution de l’application. Les données sont collectées en activant la capture de trace, en exécutant le scénario d’application souhaité qui nécessite une analyse, ce qui permet d’arrêter la capture qui enregistre les données dans un fichier ETL. Vous pouvez ensuite analyser le fichier sur le même ordinateur ou sur un autre ordinateur à l’aide de l’outil de ligne de commande **xperf.exe** ou de l’outil d’analyse de trace visuel **xperfview.exe**.

### <a name="gpuview"></a>GPUView

**GPUView** est un outil de développement pour déterminer les performances de l’unité de traitement graphique (GPU) et de l’UC. Il examine les performances en ce qui concerne le traitement de la mémoire tampon d’accès direct à la mémoire (DMA) et tout autre traitement vidéo sur le matériel vidéo.

Pour les applications [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) qui s’appuient fortement sur le GPU, **GPUView** est un outil puissant pour comprendre la relation entre le travail effectué sur le processeur et le GPU. Pour plus d’informations sur **GPUView**, consultez [utilisation de GPUView](/windows-hardware/drivers/display/using-gpuview).

Comme pour **Xperf**, une trace ETW est tout d’abord prise en démarrant le service de suivi, en exerçant le scénario nécessitant une analyse pour l’application en cours d’examen, en arrêtant le service et en enregistrant les informations dans un fichier ETL. **GPUView** présente les données présentes dans le fichier ETL dans un format graphique.

Après l’installation de l’outil **GPUView** , nous vous recommandons de lire la rubrique « affichage principal de **GPUView**» dans le menu « aide de **GPUView** ». Elle contient des informations utiles sur l’interprétation de l’interface utilisateur **GPUView** .

## <a name="installing-the-tools"></a>Installation des outils

**XPerf** et **GPUView** sont tous les deux inclus dans le Shared Computer Toolkit de Performance Windows (WPT).

**XPerf** est fourni dans le cadre du kit de développement logiciel (SDK) Windows pour Windows. [téléchargez le SDK Windows](https://dev.windows.com/downloads).

**GPUView** est disponible dans le Kit de déploiement et d’évaluation de Windows (Windows ADK). [téléchargez le kit de Windows ADK](/windows-hardware/get-started/adk-install).

Après l’installation, vous devez ajouter les répertoires contenant **Xperf** et **GPUView** à la variable système « Path ».

Cliquez sur le bouton Démarrer et tapez « variables système ». Le Fenêtre Propriétés système s’ouvre. Cliquez sur « modifier les variables d’environnement système ». Sélectionnez « variables d’environnement » dans la boîte de dialogue « Propriétés système ». La variable « PATH » se trouve sous « variables système ». Ajoutez le répertoire contenant **xperf.exe** et **GPUView.exe** au chemin d’accès. ces fichiers exécutables se trouvent dans le répertoire « Windows Performance Shared Computer Toolkit » à l’intérieur des « Kits Windows ». l’emplacement par défaut est : **C : \\ Program Files (x86) \\ Windows Kits \\ 10 \\ Windows Performance Shared Computer Toolkit**.

## <a name="performance-time-measurements"></a>Mesures de temps de performance

La plupart des applications s’exécutent correctement et sont réactives aux entrées d’utilisateur. Toutefois, selon le scénario que vous souhaitez, un aspect des performances peut être plus important qu’un autre. Par exemple, pour une application de lecteur d’actualités s’exécutant sur un Tablet PC tactile, l’aspect le plus important est d’afficher un article unique à la fois et de faire défiler/zoomer/faire défiler le même ou un autre article. Dans ce scénario, la possibilité d’afficher tout le contenu de chaque trame n’est pas nécessaire. Toutefois, la possibilité de faire défiler l’article sans heurts sur un mouvement tactile est extrêmement importante.

Dans une autre instance, un jeu ou une application de rendu vidéo qui utilise un grand nombre de problèmes d’animations si les trames sont supprimées. Dans ce cas, la possibilité de présenter du contenu à l’écran sans interuption à partir de l’entrée utilisateur est extrêmement importante.

Pour comprendre quelle partie de l’application pose problème, la première étape consiste à choisir les scénarios les plus importants. Une fois que les principaux aspects de l’application sont compris et comment ils seront testés, il est plus facile de rechercher des problèmes à l’aide des outils.

Voici quelques-unes des mesures de temps de performances les plus courantes :

### <a name="startup-time"></a>Au moment du démarrage

Temps mesuré à partir du lancement du processus jusqu’au premier sur l’écran. Cette mesure est plus utile lorsque le système est chaud et que la mesure est prise une fois que l’application a été lancée plusieurs fois.

### <a name="cpu-time-per-frame"></a>Temps processeur par frame

Durée pendant laquelle le processeur traite activement la charge de travail de l’application pour une trame. Si l’application s’exécute correctement, tout le traitement requis pour une trame se produit dans un intervalle de v-sync. Avec le taux d’actualisation du moniteur de 60 Hz, il s’agit de 16ms par trame. Si le temps processeur/le cadre est supérieur à 16ms, les optimisations du processeur peuvent être nécessaires pour produire une expérience d’application gratuite.

### <a name="gpu-time-per-frame"></a>Temps GPU par frame

Durée pendant laquelle le GPU traite activement la charge de travail de l’application pour une trame. Une application est liée au GPU lorsque le temps nécessaire pour traiter une image de données est supérieur à 16ms.

La possibilité de déterminer si une application est liée à l’UC ou au GPU réduit la partie problématique du code.

## <a name="taking-performance-time-measurement-trace"></a>Suivi de la mesure du temps de performance

Procédez comme suit pour effectuer une trace :

1.  Ouvrez une fenêtre de commande en tant qu’administrateur.
2.  Fermez l’application si elle est déjà en cours d’exécution.
3.  accédez au répertoire *gpuview* à l’intérieur du dossier Windows Performance Shared Computer Toolkit.
4.  Tapez « log. cmd » pour démarrer le suivi des événements. Cette option permet de consigner les événements les plus intéressants. Les autres options disponibles consignent différentes étendues des événements. Par exemple, le mode de journalisation Verbose ou « v » capture tous les événements dont le **GPUView** est conscient.
5.  Lancez l’exemple et exercez l’exemple de la manière qui couvre le chemin d’accès des performances que vous devez analyser.
6.  Revenez à la fenêtre de commande et tapez « log. cmd » à nouveau pour arrêter la journalisation.
7.  Cela génère un fichier appelé « fusionné. etl » dans le dossier *gpuview* . Vous pouvez enregistrer ce fichier dans un autre emplacement et l’analyser sur le même ordinateur ou sur un autre ordinateur. Pour afficher les détails de la capture de la pile, enregistrez le fichier de symboles (. pdb) associé à l’application.

## <a name="measurements"></a>Mesures


> [!Note]  
> Les mesures de l’exemple réalisation de la géométrie sont prises sur une machine à quatre cœurs avec une carte graphique DirectX11 intégrée. Les mesures varient en fonction de la configuration de l’ordinateur.

 

Cette section montre comment mesurer le temps de démarrage, le processeur et le temps GPU par mesure de trame. Vous pouvez capturer un suivi des performances pour le même échantillon sur votre ordinateur et voir les différences entre les différentes mesures.

Pour analyser le suivi dans **GPUView**, ouvrez le fichier « fusionné. ELT » à l’aide de **GPUView.exe**.

### <a name="startup-time"></a>Au moment du démarrage

Le temps de démarrage est mesuré en fonction du temps total passé par le démarrage de l’application jusqu’à ce que le contenu apparaisse pour la première fois à l’écran.

La mesure du temps de démarrage est recommandée en suivant les étapes indiquées dans la section précédente avec ces variations :

-   Si vous effectuez les mesures de démarrage la première fois que vous lancez l’application, elle est appelée démarrage à froid. Cela peut varier en fonction des mesures effectuées après le lancement de l’application plusieurs fois plus tard dans une courte durée. C’est ce que l’on appelle le démarrage à chaud. En fonction du nombre de ressources créées par une application au lancement, il peut y avoir une grande différence entre les deux temps de démarrage. En fonction des objectifs de l’application, il peut être souhaitable de mesurer l’un ou l’autre.
-   Lorsque vous consignez les informations de performance, arrêtez l’application dès que la première image s’affiche à l’écran.

### <a name="calculating-start-up-time-using-gpuview"></a>Calcul du temps de démarrage à l’aide de **GPUView**

1.  Dans **GPUView**, faites défiler jusqu’au processus approprié, dans ce cas GeometryRealization.exe.

    ![Capture d’écran montrant un exemple de processus dans GPUView.](images/profile1.png)

2.  La file d’attente de l’UC du contexte représente la charge de travail Graphics mise en file d’attente sur le matériel, mais pas nécessairement traitée par le matériel. Lorsque le fichier de trace est ouvert, il affiche tous les événements journalisés entre le moment où la trace a été effectuée. Pour calculer l’heure de démarrage, sélectionnez la zone d’intérêt, effectuez un zoom avant sur la partie initiale de la première file d’attente de l’UC du contexte (il s’agit de celle qui affiche l’activité) à l’aide de Ctrl + Z. Vous trouverez plus d’informations sur les contrôles **GPUView** dans la section « Résumé des contrôles **GPUView** » du fichier d’aide **GPUView** . La figure ci-dessous affiche uniquement le processus de GeometryRealization.exe zoomé dans la première partie de la file d’attente du contexte de l’UC. La couleur de la file d’attente du contexte de l’UC est indiquée par le rectangle juste en dessous de la file d’attente et les paquets de données de couleur de la file d’attente affichent le travail GPU mis en file d’attente sur le matériel. Le paquet de hachures dans la file d’attente de contexte indique le paquet présent, ce qui signifie que l’application souhaite que le matériel présente le contenu à l’écran.

    ![Capture d’écran illustrant des exemples de « context C P U queue ».](images/profile2.png)

3.  L’heure de démarrage est l’heure à laquelle l’application démarre pour la première fois (dans ce cas, le module point d’entrée de thread d’interface utilisateur SHCORE.dll) jusqu’à ce que le contexte apparaisse pour la première fois (marqué par un paquet hachuré). La figure ci-dessous met en évidence le domaine d’intérêt.

    > [!Note]  
    > Les informations réelles réelles sont représentées dans la file d’attente de retournement, et le temps nécessaire est donc prolongé jusqu’à ce que le paquet présent soit réellement terminé dans la file d’attente de basculement.

     

    La barre d’état complète n’est pas visible dans la figure ci-dessous, qui indique également le temps écoulé entre les parties mises en surbrillance. Il s’agit de l’heure de démarrage de l’application. Dans ce cas pour l’ordinateur mentionné ci-dessus, il s’agit d’un 240ms.

    ![Capture d’écran qui montre les zones d’intérêt relatives au démarrage dans la file d’attente du contexte C P U.](images/profile3.png)

### <a name="cpu-and-gpu-time-per-frame"></a>Temps processeur et GPU par frame

Il existe quelques points à prendre en compte lors de la mesure du temps processeur. Recherchez les zones dans la trace où vous avez fait l’analyse du scénario à analyser. Par exemple, dans l’exemple de réalisation géométrique, l’un des scénarios analysés est la transition entre le rendu des primitives 2048 et 8192, toutes les primitives non réalisées (comme dans, Geometry n’est pas fractionnée sur chaque image). La trace montre clairement la différence dans l’activité du processeur et du GPU avant et après la transition dans le nombre de Primitives.

Deux scénarios sont analysés pour calculer le temps processeur et le temps processeur graphique par frame. Elles sont les suivantes.

-   Transition du rendu des primitives non réalisées 2048 à 8192 primitives non réalisées.
-   Transition du rendu 8192 primitives obtenues à 8192 primitives non réalisées.

Dans les deux cas, il a été observé que la fréquence d’images a été supprimée de façon radicale. La mesure du temps processeur et du GPU, la relation entre les deux, ainsi que quelques autres modèles dans la trace, peut fournir des informations utiles sur les zones problématiques de l’application.

### <a name="calculating-cpu-and-gpu-time-when-2048-primitives-are-being-rendered-unrealized"></a>Calcul du temps processeur et du GPU lorsque 2048 primitives sont rendues non réalisées

1.  Ouvrez le fichier de trace à l’aide de **GPUView.exe**.
2.  Faites défiler jusqu’au processus GeometryRealization.exe.
3.  Sélectionnez une zone pour le calcul du temps processeur et agrandissez-la à l’aide de CTRL + Z.

    ![Capture d’écran montrant une zone sélectionnée pour le calcul du temps C P U dans la file d’attente de l’UC du contexte.](images/profile4.png)

4.  Affichez les informations v-sync en basculant entre F8. En gardant le zoom avant jusqu’à ce qu’il soit facile de voir une seule Vsync de données clairement. Les lignes bleues sont les heures de la synchronisation v. En règle générale, ils se produisent une fois toutes les 16 ms (60 i/s), mais si DWM rencontre un problème de performances, il s’exécute plus lentement, ce qui se produit une fois toutes les 32 ms (30 i/s). Pour obtenir une idée de temps, sélectionnez d’une barre bleue à la suivante, puis examinez le nombre de MS signalé dans le coin inférieur droit de la fenêtre **GPUView** .

    ![Capture d’écran montrant un exemple de temps de synchronisation v.](images/profile5.png)

5.  Pour mesurer le temps processeur par trame, mesurez la durée nécessaire pour tous les threads impliqués dans le rendu. Il peut être utile de limiter le thread supposé être le plus pertinent du point de vue des performances. Par exemple, dans l’exemple réalisation de la géométrie, le contenu est animé et doit être affiché à l’écran chaque frame qui rend le thread d’interface utilisateur le plus important. Une fois que vous avez déterminé le thread à examiner, mesurez la longueur des barres sur ce thread. La moyenne de quelques-unes d’entre elles donne le temps processeur par trame. La figure ci-dessous montre le temps écoulé sur le thread d’interface utilisateur. Cela indique également que cette heure s’adapte bien à deux synchronisations avec v consécutives, ce qui signifie qu’elle est en 60FPS.

    ![Capture d’écran montrant le temps écoulé sur le thread U I.](images/profile6.png)

    Vous pouvez également vérifier en regardant la file d’attente de retournement pour le laps de temps correspondant qui montre que DWM peut présenter chaque frame.

    ![Capture d’écran montrant un exemple de la file d’attente de retournement.](images/profile7.png)

6.  L’heure du GPU peut être mesurée de la même façon que le temps processeur. Effectuez un zoom sur la zone appropriée comme dans le cas de la mesure du temps processeur. Mesurez la longueur des barres de la file d’attente matérielle du GPU avec la même couleur que la couleur de la file d’attente du contexte du processeur. Tant que les barres sont comprises dans les synchronisations en v consécutives, l’application s’exécute sans heurts sur 60FPS.

    ![Capture d’écran montrant un exemple de la file d’attente matérielle GPU affichant les informations qu’une application exécute à 60 F P S.](images/profile8.png)

### <a name="calculating-cpu-and-gpu-time-when-8192-primitives-are-being-rendered-unrealized"></a>Calcul du temps processeur et du GPU lorsque 8192 primitives sont rendues non réalisées

1.  Si vous suivez à nouveau les mêmes étapes, le suivi indique que l’ensemble du travail de l’UC pour une trame ne peut pas être compris entre une synchronisation v et la suivante. Cela signifie que l’application est liée à l’UC. Le thread d’interface utilisateur sature le processeur.

    ![Capture d’écran montrant un exemple de thread d’interface utilisateur saturant le C P U.](images/profile9.png)

    En examinant la file d’attente Flip, il est également clair que DWM n’est pas en mesure de présenter chaque frame.

    ![Capture d’écran montrant un exemple du D W M impossible de présenter toutes les images.](images/profile10.png)

2.  Pour analyser le moment où le temps est passé, ouvrez la trace dans **Xperf**. Pour analyser le temps de démarrage dans **Xperf**, commencez par Rechercher l’intervalle de temps dans **GPUView**. Placez la souris à gauche de l’intervalle et de la droite et notez l’heure absolue affichée en bas de la fenêtre **GPUView** . Ouvrez ensuite le même fichier. etl dans **Xperf** et faites défiler jusqu’au graphique « échantillonnage de l’UC par UC », cliquez avec le bouton droit et sélectionnez « Sélectionner un intervalle... ». Cela permet de taper l’intervalle d’intérêt qui a été découvert en examinant le suivi GPU.

    ![capture d’écran qui montre l’échantillonnage « c p u par c p u » dans « Windows analysis Performance ».](images/profile11.png)

3.  Accédez au menu trace et assurez-vous que l’option « charger les symboles » est cochée. Accédez également à trace-> configurer les chemins d’accès aux symboles et tapez dans le chemin d’accès aux symboles de l’application. Un fichier de symboles contient des informations de débogage sur un exécutable compilé dans une base de données distincte (. pdb). Ce fichier est communément appelé PDB. Vous trouverez plus d’informations sur les fichiers de symboles ici : [fichiers de symboles](/windows/desktop/Debug/symbol-files). Ce fichier peut se trouver dans le dossier « Debug » du répertoire de l’application.

4.  Afin d’obtenir la répartition de l’heure d’exécution de l’application, cliquez avec le bouton droit sur l’intervalle sélectionné à l’étape précédente, puis cliquez sur table de résumé. Pour avoir une vue d’ensemble du temps passé dans chaque dll, décochez « Stack » dans le menu « Columns » (colonnes). Notez que la colonne « Count » affiche ici le nombre d’exemples qui se trouvent dans la dll/fonction donnée. Étant donné qu’environ un échantillon est pris par MS, ce nombre peut être utilisé comme meilleure estimation du temps passé dans chaque dll/fonction. Le contrôle de la « pile » dans le menu colonnes permet d’obtenir le temps inclusif passé dans chaque fonction dans le graphique des appels. Cela vous aidera à décomposer les points à problème.

5.  Les informations de trace de la pile pour les primitives non réalisées 2048 révèlent que 30% du temps processeur est passé dans le processus de réalisation géométrique. Environ 36% du temps est passé dans le pavage et le contour de géométrie.

6.  Les informations de trace de la pile pour les primitives non réalisées 8192 révèlent qu’environ 60% du temps processeur (4 cœurs) est consacré à la réalisation de la géométrie.

    ![Capture d’écran montrant les informations de trace de la pile pour l’heure de C P U.](images/profile12.png)

### <a name="calculating-cpu-time-when-8192-primitives-are-being-rendered-realized"></a>Calcul du temps processeur en cas de rendu des primitives 8192

Il est clair dans les profils que l’application est liée à l’UC. Afin de réduire le temps passé par l’UC, les géométries peuvent être créées une fois et mises en cache. Le contenu mis en cache peut être rendu dans chaque frame sans que le coût de facettisation Geometry soit généré par image. Lorsque vous examinez la trace dans **GPUView** pour la partie réalisée de l’application, il est clair que DWM peut présenter chaque trame et que le temps processeur a été considérablement réduit.

![Capture d’écran montrant un exemple de trace dans GPUView montrant que D W M peut présenter toutes les images.](images/profile13.png)

La première partie du graphique montre les primitives 8192 réalisées. Le temps processeur correspondant par trame peut tenir dans deux synchronisations v consécutives. Dans la partie suivante du graphique, ce n’est pas le cas.

Dans **Xperf**, le processeur est resté inactif pendant la durée la plus longue, avec seulement environ 25% du temps processeur passé sur l’application Geometry réalisation.

![capture d’écran gpuview.](images/profile14.png)

## <a name="summary"></a>Résumé

**GPUView** et **Xperf** et puissants outils permettant d’analyser les performances des applications [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) . Cet article est une introduction à l’utilisation de ces outils et à la compréhension des mesures de performances de base et des caractéristiques de l’application. Outre la compréhension de l’utilisation des outils, il est tout d’abord important de comprendre l’application en cours d’analyse. Commencez par trouver des réponses aux questions telles que l’application qui tente d’atteindre ? Quels sont les threads du système qui sont les plus importants ? Quels sont les compromis que vous voulez faire ? Lorsque vous analysez les traces de performances, commencez par examiner les emplacements évidents des problèmes. L’UC de l’application ou le GPU est-il lié ? L’application peut-elle présenter toutes les images ? Les outils associés à une compréhension de l’application peuvent fournir des informations très utiles pour comprendre, Rechercher et enfin résoudre les problèmes de performances.

 

 