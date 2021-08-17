---
title: Scénarios de l’Assistant Compatibilité des programmes pour Windows 8
description: Scénarios de l’Assistant Compatibilité des programmes pour Windows 8
ms.assetid: C61BF746-63EE-4F4E-81D3-52947FD4954D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63fbd912e14ac682ffe820ad140b2cad6a487dfbac833aa419c53389a9339ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852597"
---
# <a name="program-compatibility-assistant-scenarios-for-windows-8"></a>Scénarios de l’Assistant Compatibilité des programmes pour Windows 8

## <a name="platforms"></a>Plateformes

**Clients** -Windows XP \| Windows Vista \| Windows 7 \| Windows 8  

## <a name="description"></a>Description

l’Assistant compatibilité des programmes (PCA) est une fonctionnalité de Windows 8 qui permet aux utilisateurs finaux d’exécuter des applications de bureau conçues pour des versions Windows antérieures. Windows 8 dispose d’une grande compatibilité d’application intégrée qui permet aux applications conçues pour Windows 7 ou versions antérieures de Windows de fonctionner de manière efficace sur Windows 8 automatiquement. Toutefois, il existe un petit nombre d’applications qui peuvent avoir des problèmes d’exécution sans intervention.

Lorsqu’un utilisateur exécute une application, PCA effectue le suivi de l’application et identifie les symptômes de certains problèmes de compatibilité connus dans Windows 8. Lorsqu’il détecte des symptômes de problème, il offre à l’utilisateur la possibilité d’appliquer un correctif recommandé qui permettra de mieux exécuter l’application sur Windows 8.

## <a name="scenarios"></a>Scénarios

PCA effectue le suivi des applications pour un ensemble de problèmes de compatibilité connus dans Windows 8. PCA effectue le suivi des problèmes, identifie les correctifs et fournit une boîte de dialogue à l’utilisateur avec des instructions pour appliquer un correctif recommandé. L’utilisateur peut décider d’appliquer les correctifs recommandés, ou choisir de ne rien faire et annuler la recommandation. Si l’utilisateur annule l’opération, PCA ne suit plus cette application.

PCA applique généralement l’un des trois modes de compatibilité de Windows : Windows XP SP3, Windows Vista SP2 ou Windows 7, selon la date à laquelle le programme (ou son programme d’installation) a été créé. PCA utilise les \_ attributs DATE de la liaison et VERSION du sous-système du programme, ainsi que les sections TRUSTINFO et compatibilité du manifeste du fichier exécutable pour déterminer quel mode est pertinent et s’applique Windows XP SP3 (y compris les privilèges d’administrateur), Windows Vista SP2 ou Windows 7, respectivement. Un glossaire à la fin du document répertorie chacun des modes de compatibilité auxquels PCA s’applique, ainsi que sa description.

Pour tous les scénarios listés ci-dessous, PCA effectue le suivi des applications une deuxième fois après l’application d’un correctif. Si l’application continue à échouer de la même manière même après l’application d’un correctif de compatibilité, PCA annule le correctif. PCA arrête alors définitivement le suivi de l’application spécifique qui a échoué.

Alors que PCA effectue le suivi de nombreux problèmes potentiels, tous les problèmes peuvent entraîner des échecs d’application. PCA recommande uniquement les correctifs dans les cas où il existe une forte probabilité que l’échec de l’application soit dû à Windows raisons de compatibilité. Les sections ci-dessous s’étendent sur chacun des scénarios PCA développés dans Windows 8. Chaque section décrit le scénario à problème et les recommandations fournies par l’APC pour permettre à l’application de continuer à fonctionner correctement sur Windows 8.

pour en savoir plus sur les modifications de compatibilité dans Windows 8, reportez-vous aux autres rubriques du guide de *compatibilité Windows 8*.

Les scénarios suivis et recommandés par PCA sont les suivants :

-   L’installation ou la désinstallation de l’application échoue
-   l’application ne parvient pas à s’exécuter avec un message de vérification de version Windows
-   L’application ne parvient pas à se lancer en raison de privilèges d’administrateur
-   Blocage de l’application en raison de problèmes de mémoire spécifiques
-   L’application échoue en raison de fichiers système incompatibles
-   L’application échoue en raison d’erreurs non gérées sur l’Windows 64 bits
-   l’application échoue lors de la tentative de suppression des fichiers protégés non Windows
-   l’application échoue lors de la tentative de modification des fichiers Windows
-   L’application échoue en raison d’un mode de couleur de 8 ou 16 bits
-   L’application échoue en raison de problèmes graphiques et d’affichage
-   L’application ne peut pas déclarer la reconnaissance DPI
-   l’application échoue en raison de fonctionnalités de Windows manquantes
-   L’application échoue en raison de pilotes non signés sur le Windows 8 64 bits
-   Applications de suivi installées par le biais des paramètres de compatibilité
-   L’application ne parvient pas à lancer des programmes d’installation ou des mises à jour
-   Programmes d’installation d’applications qui doivent s’exécuter avec des privilèges d’administration
-   Applets du panneau de configuration héritées qui doivent s’exécuter avec des privilèges d’administration

Chacun de ces scénarios est développé ci-dessous :

**L’installation ou la désinstallation de l’application échoue**

L’un des types d’échecs d’application les plus courants se produit pendant l’installation de l’application. Les programmes d’installation plus anciens échouent le plus souvent de deux manières :

-   le programme d’installation n’a pas connaissance des fonctionnalités de contrôle de compte d’utilisateur (UAC, User Account Control) dans Windows 8, il peut donc ne pas s’exécuter avec les privilèges complets nécessaires pour apporter des modifications au système aux zones protégées de Windows 8
-   le programme d’installation vérifie la version de Windows et se bloque de s’exécuter si la version est supérieure à ce qu’elle attend.

Ces conditions d’échec sont deux des types les plus courants d’échecs de compatibilité dans le programme d’installation. PCA, à l’aide d’autres composants Windows tels que le contrôle de compte d’utilisateur, détecte les programmes d’installation au lancement et les suit jusqu’à la fin de l’installation. si le programme d’installation ne parvient pas à ajouter des fichiers ou à ajouter une entrée valide dans la partie « ajout/suppression de programmes » du panneau de configuration Windows, PCA considère que l’installation a échoué.

Dans ce cas, PCA recommande un mode de compatibilité adapté à l’application. le mode de compatibilité permet au programme d’installation de s’exécuter en mode Windows et s’assure également que l’application s’exécute avec des privilèges d’administrateur. PCA applique le mode de compatibilité RUNASADMIN, ainsi que le mode de compatibilité Windows XP, Windows Vista ou Windows 7 approprié. À la fin de l’installation qui a échoué, l’utilisateur verra une boîte de dialogue avec la recommandation de l’APC :

![boîte de dialogue échec de l’installation ou de la désinstallation de l’application](images/pcafigure1.png)

L’utilisateur peut alors choisir d’effectuer les opérations suivantes :

-   Exécutez le programme en utilisant les paramètres de compatibilité (option recommandée), après quoi PCA appliquera le paramètre recommandé (mode de compatibilité), redémarrez le programme d’installation et suivez-le jusqu’à ce que l’installation se termine correctement.
-   Indique que le programme a été correctement installé, auquel cas PCA n’ajoutera aucun paramètre et arrêtera le suivi de l’installation
-   Cliquez sur Fermer. dans ce cas, PCA n’ajoutera aucun paramètre et arrêtera le suivi de cette configuration

le même mécanisme est utilisé pour aider la désinstallation de l’application lorsqu’un utilisateur tente de désinstaller l’application à partir de la section « ajout de suppression de programmes » dans Windows, ou à partir du raccourci de désinstallation de l’application.

**l’application ne parvient pas à s’exécuter avec un message de vérification de version Windows**

l’un des échecs de compatibilité les plus courants dans l’exécution de l’application est dû à la vérification de la version de Windows. de nombreuses applications, lors du lancement, vérifient la version de Windows ; s’ils ne reconnaissent pas la version, ils se bloquent même si l’application peut être exécutée sans problème.

En règle générale, ces vérifications sont associées à deux conditions suivies par l’APC :

L’application affiche une boîte de message qui avertit l’utilisateur. Voici un exemple :

![l’application ne parvient pas à s’exécuter avec une boîte de dialogue de message de vérification de version Windows](images/pcafigure2.png)

-   L’application se termine immédiatement ou se bloque

Si PCA identifie ces deux conditions pour une application, il fournit une recommandation à l’utilisateur. PCA permettra à l’utilisateur de réexécuter l’application avec les paramètres de compatibilité. PCA appliquera le mode de compatibilité Windows XP, Windows Vista ou Windows 7 approprié en fonction de l’application. Comme dans tous les scénarios, l’utilisateur peut indiquer à PCA que l’application s’est exécutée correctement ou refuser les paramètres recommandés en cliquant sur le bouton Fermer. Un exemple de boîte de dialogue est fourni comme indiqué ci-dessous :

![l’application ne peut pas s’exécuter avec une boîte de dialogue d’option de message de vérification de version Windows](images/pcafigure3.png)

**L’application ne parvient pas à démarrer ou à s’exécuter en raison de privilèges d’administrateur**

Certaines applications ont besoin de privilèges d’administrateur pour exécuter et exécuter leurs fonctionnalités. toutefois, dans Windows 8, comme Windows 7 et Windows Vista, les applications s’exécutent dans des niveaux de privilège inférieurs par défaut en raison du contrôle de compte d’utilisateur. les applications plus récentes conçues pour Windows Vista et versions ultérieures déclarent généralement le niveau de privilège qu’elles doivent exécuter à l’aide de la section TRUSTINFO du manifeste EXE. Toutefois, les applications plus anciennes échouent généralement de deux manières :

-   Application affiche un message à l’utilisateur pour lequel il requiert des privilèges d’administration, comme dans l’exemple ci-dessous :

![l’application ne parvient pas à démarrer ou à s’exécuter en raison de la boîte de dialogue des privilèges administratifs](images/pcafigure4a.png)

-   L’application se termine immédiatement ou se bloque

Si PCA identifie ces deux conditions pour une application, il fournit une recommandation à l’utilisateur. PCA permettra à l’utilisateur de réexécuter l’application avec des privilèges d’administration (PCA applique le mode de compatibilité RUNASHIGHEST). L’utilisateur recevra une invite de contrôle de compte d’utilisateur lors de la réexécution de l’application. Comme dans tous les scénarios, l’utilisateur peut choisir de réexécuter avec le paramètre recommandé, ou de désactiver les paramètres recommandés en cliquant sur Fermer. Un exemple de boîte de dialogue est fourni comme indiqué ci-dessous :

![l’application ne parvient pas à démarrer ou à s’exécuter en raison de la boîte de dialogue d’options des privilèges](images/pcafigure5.png)

**Blocage de l’application en raison de problèmes de mémoire spécifiques**

Certaines applications se bloquent en raison d’un problème de mémoire bien connu. L’application déréférence une DLL de la mémoire, puis appelle une fonction pour exécuter du code dans la même DLL. Cela provoque un blocage immédiat de l’application. si ce problème n’est pas dû à des modifications de compatibilité Windows 8, il s’agit d’un problème relativement courant dans un large éventail d’applications. PCA effectue le suivi de ce problème pour permettre aux utilisateurs d’exécuter leur application de manière plus fiable.

Pour ces applications, PCA applique automatiquement le mode de compatibilité PINDLL en mode silencieux. Le mode de compatibilité appelé par PCA empêche l’application de libérer la DLL de la mémoire. Par conséquent, l’appel de fonction dans la DLL par l’application fonctionne, ce qui empêche l’application de se bloquer et de continuer à fonctionner correctement.

**L’application échoue en raison de fichiers système incompatibles**

certaines applications conçues pour Windows XP et les versions antérieures incluent des copies de Windows dll système avec leurs programmes d’installation. lorsque de telles applications sont installées, l’application dispose d’une copie plus ancienne de la dll dans son propre dossier, ainsi que de la dernière version de la dll qui se trouve dans les dossiers système Windows.

sur Windows Vista et versions ultérieures, cette condition peut provoquer l’échec de l’application lorsqu’elle tente de charger la dll locale, car cette dll ne fonctionnera pas correctement avec le reste des dll système Windows actuelles. Étant donné que l’application n’est généralement pas informée des versions plus récentes de cette DLL, elle ne fonctionne pas correctement.

lorsque PCA détecte que la dll n’a pas pu se charger correctement, il applique un paramètre de compatibilité qui permet à Windows de charger la version la plus récente de la dll à partir du dossier système Windows afin que l’application puisse s’exécuter correctement.

À la fin de la première exécution non réussie de l’application, les utilisateurs verront la boîte de dialogue PCA qui les avertit du paramètre appliqué comme indiqué ci-dessous :

![l’application échoue en raison d’une boîte de dialogue de fichiers système incompatibles](images/pcafigure6.png)

**L’application échoue en raison d’erreurs non gérées sur l’Windows 64 bits**

sur la version 64 bits de Windows 8, une nouvelle exception a été activée pour le mécanisme de rappel de boucle de message. cette exception a été introduite pour la première fois dans Windows 7, mais elle n’était pas obligatoire pour gérer cette erreur. dans Windows 8, les applications qui utilisent des boucles de messages doivent gérer cette nouvelle exception. Si ce n’est pas le cas, ils se bloquent. les applications conçues pour des versions antérieures de Windows ne sont peut-être pas conscientes de cette exception et peuvent donc ne pas traiter cette erreur (exception) correctement.

PCA détecte les applications qui échouent en raison de cette erreur non gérée et applique automatiquement le mode de compatibilité DISABLEUSERCALLBACKEXCEPTION pour l’application. Une fois que le paramètre est appliqué à la fin de l’exécution, l’utilisateur est notifié comme indiqué ci-dessous. L’application obtiendra le mode lors de la prochaine exécution et sera en mesure d’éviter cette erreur.

![l’application échoue en raison d’erreurs non gérées dans la boîte de dialogue Windows 64 bits](images/pcafigure7.png)

**l’application échoue lors de la tentative de suppression des fichiers protégés non Windows**

certaines applications conçues pour Windows XP et antérieures supposent qu’elles s’exécutent généralement avec des privilèges d’administrateur complets. dans le cadre du comportement normal de l’application, ils peuvent tenter de supprimer les fichiers protégés non Windows (dans program files ou Windows dossiers). Lorsque l’opération de suppression échoue, de nombreuses applications peuvent se bloquer.

PCA détecte ces applications qui ne parviennent pas à supprimer les fichiers protégés et se bloque, et fournit une recommandation à l’utilisateur. PCA permettra à l’utilisateur de réexécuter l’application avec les paramètres de compatibilité. Comme dans tous les scénarios, l’utilisateur peut indiquer à PCA que l’application s’est exécutée correctement ou refuser les paramètres recommandés en cliquant sur le bouton Fermer. Dans ce cas, PCA applique le mode de compatibilité VIRTUALIZEDELETE. Un exemple de boîte de dialogue est fourni comme indiqué ci-dessous :

![l’application échoue lors de la tentative de suppression de la boîte de dialogue fichiers non Windows protégés](images/pcafigure8.png)

**l’application échoue lors de la tentative de modification des fichiers Windows ou des clés de registre**

certaines applications conçues pour Windows XP et antérieures supposent qu’elles s’exécutent généralement avec des privilèges d’administrateur complets. dans le cadre du comportement normal de l’application, ils peuvent tenter de modifier, supprimer ou écrire des fichiers Windows protégés (dans des fichiers programme ou des dossiers Windows) ou des clés de registre appartenant à Windows. Lorsque l’une des opérations d’écriture, de suppression ou de modification d’un fichier ou d’une clé de Registre échoue, de nombreuses applications peuvent se bloquer ou échouer de manière incorrecte.

PCA détecte ces applications qui ne parviennent pas à écrire dans des fichiers Windows protégés ou des clés de registre, et fournit une recommandation à l’utilisateur lorsque l’application se ferme. PCA permettra à l’utilisateur de réexécuter l’application avec les paramètres de compatibilité. Comme dans tous les scénarios, l’utilisateur peut indiquer à PCA que l’application s’est exécutée correctement ou refuser les paramètres recommandés en cliquant sur le bouton Fermer. Dans ce cas, PCA applique le mode de compatibilité WRPMITIGATION. Un exemple de boîte de dialogue est fourni comme indiqué ci-dessous :

![l’application échoue lors de la tentative de modification des fichiers Windows ou des clés de Registre](images/pcafigure9.png)

**L’application échoue en raison d’un mode de couleur de 8 ou 16 bits**

dans le cadre de la repartement de Windows 8 pour les applications Windows du windows Store, l’une des principales modifications est que le Gestionnaire de fenêtrage (DWM) prend désormais en charge uniquement les couleurs 32 bits dans Windows 8. Les modes de couleur inférieurs sont maintenant simulés.

beaucoup d’applications et de jeux plus anciens conçus pour Windows XP ou avant utilisent des modes de couleurs 8 bits ou 16 bits. Sans aucune atténuation, ces applications risquent de ne pas s’exécuter sur Windows 8. Toutefois, lorsque ces applications énumèrent ou essaient d’utiliser l’un des modes de couleurs 8 bits ou 16 bits pour l’affichage, PCA identifie immédiatement le problème et, à l’aide de DWM, s’assure que l’application fonctionne correctement avec le mode de couleurs simulé.

Notez que cela se produit dès que l’application demande les modes de couleur basse et est transparente pour l’utilisateur. L’utilisateur n’a pas besoin de redémarrer l’application pour obtenir cette atténuation, car ce correctif est toujours nécessaire pour garantir le bon fonctionnement de l’application.

**L’application échoue en raison de problèmes graphiques et d’affichage**

étant donné que Gestionnaire de fenêtrage (DWM) est toujours activé dans Windows 8, certaines anciennes applications Windows XP era peuvent échouer si l’application utilise des api graphiques en mode mixte, comme dans l’utilisation des api GDI et DirectX pour dessiner à l’écran (principalement des jeux plus anciens) et tente d’utiliser le mode plein écran :

-   DWM empêchera la peinture directe sur le bureau et le jeu ou l’application échouera, ou dessinerez un écran noir sur le bureau, et aucun graphique ne sera visible.
-   dans ce cas, quand l’application se ferme, Windows détecte que l’application ou le jeu présente un problème en mode plein écran et applique le mode de compatibilité DXMAXIMIZEDWINDOWEDMODE qui permet à l’application ou au jeu de s’exécuter en mode fenêtre agrandi au lieu d’un mode plein écran.
-   Une fois que le paramètre est appliqué à la fin de l’exécution, l’utilisateur est averti par l’APC comme indiqué ci-dessous. l’application obtiendra le mode de compatibilité lors de la prochaine exécution et pourra s’exécuter correctement

![l’application échoue en raison de la boîte de dialogue des problèmes graphiques et d’affichage](images/pcafigure10.png)

**L’application ne peut pas déclarer la reconnaissance DPI**

un autre problème d’affichage typique avec de nombreuses applications plus anciennes se produit lorsque Windows et l’application s’exécutent en mode haute résolution, mais l’application ne déclare pas sa connaissance de la haute résolution par le biais de son manifeste EXE. Parmi les problèmes courants qui peuvent se produire en raison de cette incompatibilité dans les paramètres, citons les éléments d’interface utilisateur découpés ou le texte et la taille de police incorrecte. Pour plus d’informations sur les problèmes, consultez ce lien [ici](/previous-versions//dd464660(v=vs.85)).

dans ce cas, Windows détecte que l’application prend en charge les résolutions élevées et applique le mode de compatibilité HIGHDPIAWARE à l’application à la fin de la première exécution. PCA informe ensuite l’utilisateur de cette opération comme indiqué ci-dessous :

![l’application ne parvient pas à déclarer la détection PPP](images/pcafigure11.png)

**l’Application échoue en raison de fonctionnalités de Windows manquantes**

certaines applications dépendent de Windows fonctionnalités qui ont été supprimées depuis Windows Vista. Lorsque ces applications essaient de charger les dll ou les composants COM manquants, elles ne fonctionnent pas.

PCA détecte les applications lorsqu’ils essaient de charger les fonctionnalités de Windows manquantes, et fournit une recommandation pour télécharger ces composants et les installer une fois l’application terminée. L’utilisateur peut cliquer sur « obtenir de l’aide en ligne » pour trouver une alternative ou pour télécharger la fonctionnalité et l’installer. Si nécessaire, l’utilisateur peut choisir de ne rien faire en cliquant sur Fermer.

![l’application échoue en raison de la boîte de dialogue des fonctionnalités Windows manquantes](images/pcafigure12.png)

**L’application échoue en raison de pilotes non signés sur le Windows 8 64 bits**

64 bits Windows a requis des pilotes signés numériquement (fichiers SYS) depuis Windows Vista. toutefois, les applications plus anciennes conçues avant la sortie de Windows Vista fournissaient des pilotes qui n’étaient pas signés numériquement. si un tel pilote non signé est installé, Windows ne les charge pas. dans de rares cas, il est possible que Windows ne démarre pas si ces pilotes sont marqués comme des pilotes au moment du démarrage.

Certaines applications plus anciennes installent des pilotes qui ne sont pas signés sur le Windows 64 bits. Tout appareil ou application qui tente d’utiliser ce pilote peut échouer ou provoquer un incident système. Pour éviter ce type de scénario, PCA détecte les applications lorsqu’ils installent des pilotes non signés et désactive le pilote qu’il est marqué comme pilote au moment du démarrage.

Il indique également à l’utilisateur d’acquérir un pilote signé numériquement pour que l’application fonctionne correctement. Le message s’affiche à la suite de l’installation du pilote et du résultat de l’installation de l’application. Si une autre application installe le même pilote, cette application obtiendra également le même message.

![l’application échoue en raison de pilotes non signés sur la boîte de dialogue Windows 8 64 bits](images/pcafigure13.png)

**Applications de suivi installées par le biais des paramètres de compatibilité**

Lorsqu’un programme d’installation échoue, PCA permet au programme d’installation d’utiliser différents modes de compatibilité en fonction du type d’échec. Une fois que le programme d’installation a été exécuté avec les paramètres de compatibilité, PCA effectue le suivi des raccourcis ajoutés par le programme d’installation. Cela permet de savoir si les applications qui ont été installées peuvent également avoir besoin des paramètres de compatibilité appliqués à leur programme d’installation.

Lorsqu’un utilisateur lance une telle application, PCA invite l’utilisateur à demander si l’application fonctionnait correctement. Si l’utilisateur répond, « oui », l’APC arrête le suivi de l’application. Si l’utilisateur répond « non », il applique le même mode de compatibilité qui a été appliqué au programme d’installation de l’application et Réexécute l’application avec le mode de compatibilité appliqué.

**L’application ne parvient pas à lancer des programmes d’installation ou des mises à jour**

Les applications lancent parfois des programmes enfants qui doivent s’exécuter en tant qu’administrateurs. C’est généralement le cas lorsqu’une application tente de lancer son logiciel de mise à jour pour vérifier et installer les nouvelles mises à jour de l’application. Lorsque les applications exécutent directement ces programmes enfants, le programme enfant peut ne pas démarrer, car l’application elle-même n’a pas de privilèges d’administrateur, ou parce que le programme enfant n’a pas été correctement marqué pour l’élévation avec le manifeste du contrôle de compte d’utilisateur.

PCA effectue le suivi de ces erreurs et, lorsque l’application principale se ferme, applique automatiquement le mode de compatibilité ELEVATECREATEPROCESS qui permet aux programmes enfants de s’exécuter correctement. Lorsque l’application lance l’application enfant lors des exécutions suivantes, l’utilisateur verra s’afficher une boîte de dialogue UAC pour le programme enfant.

Voici un exemple de la boîte de dialogue PCA :

![l’application ne parvient pas à lancer la boîte de dialogue programmes d’installation ou de mise à jour](images/pcafigure14.png)

**Programmes d’installation d’applications qui doivent s’exécuter avec des privilèges d’administration**

les programmes d’installation de Windows applications de bureau requièrent des privilèges d’administrateur, car ils écrivent des fichiers, des dossiers et des entrées de registre dans des zones système protégées. Windows (UAC) dispose d’une logique de détection pour identifier à quel moment un programme d’installation est exécuté et invite immédiatement l’utilisateur à fournir des privilèges d’administrateur par le biais de la boîte de dialogue UAC. Toutefois, dans certains cas, cette logique ne sera pas en mesure de déterminer qu’une application était effectivement un programme d’installation et risque de ne pas obtenir de privilèges d’administrateur. il s’agit en général de programmes d’installation personnalisés qui n’utilisent pas de technologies d’installation bien connues telles que Windows Installer ou installer la protection.

Dans ce cas, PCA détecte que le programme d’installation n’a pas pu écrire ses fichiers. À la fin de l’installation qui a échoué, PCA fournira une recommandation pour appliquer les paramètres de compatibilité. Si l’utilisateur choisit de cliquer sur « exécuter le programme », PCA appliquera le mode de compatibilité RUNASADMIN et réexécutera le programme d’installation. Si l’utilisateur choisit de fermer, aucun paramètre n’est appliqué. Voici un exemple de boîte de dialogue PCA :

![Capture d’écran montrant un exemple de boîte de dialogue pour un programme d’installation d’application qui doit s’exécuter avec des privilèges d’administrateur.](images/pcafigure15.png)

Les applets du panneau de configuration existants qui doivent s’exécuter avec des applets de commande du panneau de configuration modifient généralement les paramètres système et doivent pouvoir exécuter l’administrateur Active Directory. toutefois, ceux qui sont écrits avant Windows Vista n’ont pas de manifeste EXE ou ne disposent pas de la section TRUSTINFO qui déclare le niveau de privilège requis. Lors de l’exécution de ces applets, PCA les détecte et, à la fin de la première exécution, fournit une recommandation pour s’exécuter avec les paramètres d’administration. Si l’utilisateur choisit de cliquer sur « exécuter le programme », PCA applique le mode de compatibilité RUNASADMIN, puis réexécute le programme d’installation. Si l’utilisateur choisit de fermer, aucun paramètre ne sera appliqué. Voici un exemple de boîte de dialogue PCA :

![boîte de dialogue programmes d’installation d’application qui doivent s’exécuter avec des privilèges d’administration](images/pcafigure16.png)

**Vérification des paramètres recommandés par le biais des commentaires des utilisateurs**

À la fin de chacun des scénarios (une fois que l’application est exécutée avec les paramètres de compatibilité recommandés), PCA demande à l’utilisateur une question simple :

![vérification des paramètres recommandés par le biais de la boîte de dialogue commentaires de l’utilisateur](images/pcafigure17.png)

L’utilisateur peut fournir des commentaires si l’application fonctionnait ou a échoué avec le paramètre de compatibilité. Ces données seront envoyées anonymement à Microsoft. cela permet de s’assurer que ces correctifs peuvent être intégrés à Windows 8 par le biais du processus de mise à jour Windows, afin que les futurs utilisateurs de Windows 8 ne rencontreront plus l’échec de l’application, et que PCA n’aura plus besoin d’effectuer le suivi de l’application en cas d’échec.

**Suivi des problèmes qui n’ont pas de recommandations**

Les applications peuvent échouer de différentes façons pour des raisons de compatibilité. PCA effectue le suivi de nombreux problèmes de compatibilité supplémentaires par rapport à ce qui est indiqué dans les scénarios ci-dessus. Dans ce cas, la plupart du temps, le problème de manifeste dépend de l’application. Cela signifie que certaines applications gèrent correctement ces problèmes et la récupèrent, tandis que d’autres ne le peuvent pas. Ainsi, pour ces problèmes, alors que PCA effectue toujours le suivi de l’application, il ne fournit pas de recommandation directe pour un correctif.

Les problèmes suivis par PCA qui n’ont pas de paramètre recommandé ou de boîte de dialogue incluent des applications qui :

-   Avoir un Runtime très bref : les applications s’exécutent pendant plus de trois secondes
-   Créer des objets mémoire globaux sans privilèges administratifs
-   Avoir une erreur (exception Win32) au lancement
-   Vérifier les privilèges d’administration (mais peut échouer)
-   utiliser des codecs indeo (déconseillés à partir de Windows Vista)
-   Essayez d’écrire ou de supprimer des clés à partir d’emplacements de Registre protégés tels que HKLM
-   Blocage au lancement

**Application de correctifs via l’onglet compatibilité et l’outil de résolution des problèmes de compatibilité**

Comme indiqué ci-dessus, les applications peuvent échouer pour diverses raisons de compatibilité. Certains d’entre eux n’ont pas de recommandation PCA claire puisque les paramètres dépendent de l’application. Toutefois, les utilisateurs peuvent accéder à l’outil de résolution des problèmes de compatibilité ou à l’onglet compatibilité pour appliquer certains correctifs courants afin d’essayer de faire en sorte que leur application défaillante fonctionne correctement sur Windows 8. Dans ce cas, PCA continuera de suivre l’application pour les problèmes de compatibilité, avant et après l’application du correctif. Une fois l’application exécutée avec le correctif appliqué, PCA demande à l’utilisateur si le correctif a fonctionné. Une fois que l’utilisateur répond à la question, les données sont envoyées de manière anonyme par télémétrie à Microsoft. ces données sont collectées à partir de nombreux utilisateurs et analysées, et les correctifs éligibles sont ensuite distribués de manière globale à tous les utilisateurs Windows 8 via la mise à jour Windows.

**Utilisation de l’utilitaire de résolution des problèmes de compatibilité**

l’utilitaire de résolution des problèmes de compatibilité est un mécanisme de Windows qui vous permet de diagnostiquer les problèmes liés aux applications et d’appliquer les correctifs recommandés pour qu’ils fonctionnent correctement. Cela est nécessaire uniquement lorsque PCA ne fournit aucune recommandation pour l’application.

L’utilitaire de résolution des problèmes permet aux utilisateurs de parcourir et de répondre à un ensemble de questions et, en fonction des réponses, il appliquera un ensemble de correctifs et autorisera les utilisateurs à tester leurs applications et à vérifier les correctifs. Une fois la vérification effectuée, les correctifs sont appliqués de façon permanente aux applications pour améliorer leur fonctionnement sur Windows 8.

L’interface utilisateur de l’utilitaire de résolution des problèmes est indiquée ci-dessous pour référence :

![utilisation de la boîte de dialogue résolution des problèmes de compatibilité](images/pcafigure18.png)

Vous pouvez démarrer l’utilitaire de résolution des problèmes de compatibilité de deux manières :

**À partir de l’écran d’accueil :**

1.  Type : utilitaire de résolution des problèmes de compatibilité
2.  dans la section paramètres, cliquez sur la vignette « exécuter les programmes effectués pour une version précédente de Windows »

  
**À partir de la vignette de l’application :**

1.  Dans l’écran d’accueil, cliquez avec le bouton droit sur la vignette de l’application.
2.  Cliquez sur Ouvrir l’emplacement du fichier (applications de bureau uniquement)
3.  Dans le ruban de l’Explorateur, cliquez sur l’onglet « application ».
4.  Choisir « résoudre les problèmes de compatibilité »

  


**Utilisation de l’onglet Compatibilité**

Notez qu’il est recommandé uniquement aux utilisateurs qui sont des experts d’essayer différents paramètres de compatibilité. Cette méthode ne fournit aucune recommandation sur le type de correctif à appliquer aux applications. Ici, l’utilisateur doit savoir quels correctifs peuvent être appliqués pour faire fonctionner l’application. Si vous n’êtes pas sûr des correctifs, veuillez utiliser l’utilitaire de résolution des problèmes de compatibilité pour trouver un correctif pour l’application.

Pour accéder à l’onglet Compatibilité :

 **À partir de l’écran d’accueil :**

1.  Cliquez avec le bouton droit sur la vignette de l’application
2.  Ouvrir l’emplacement du fichier (applications de bureau uniquement)

  
**À partir du ruban Explorateur :**

1.  Cliquez sur Propriétés
2.  Accédez à l’onglet compatibilité.
3.  Sélectionner les correctifs de compatibilité
4.  Réexécuter l’application
    > [!Note]  
    > Vous pouvez revenir au même emplacement pour modifier ou supprimer également les correctifs. Vous pouvez également appliquer les correctifs à tous les utilisateurs sur l’ordinateur à l’aide du bouton fourni dans l’onglet.

     

  


![utilisation de l’onglet Compatibilité](images/pcafigure19.png)

**Applications avec des problèmes de compatibilité connus**

Outre les scénarios de détection des problèmes d’exécution répertoriés ci-dessus, PCA informe également les utilisateurs au démarrage de l’application si l’application rencontre des problèmes de compatibilité connus. La liste est stockée dans la base de données de compatibilité des applications système. Il existe deux types de messages :

-   **Messages de blocage matériel**: si l’application est incompatible et si l’autorisation de l’exécution de l’application se traduira par un impact grave sur le système (par exemple, un blocage Windows ou l’incapacité à démarrer après l’installation), un message de blocage comme indiqué ci-dessous s’affiche.

![applications avec problèmes de compatibilité connus-boîte de dialogue des messages de blocage matériel](images/pcafigure20.png)

-   **Messages de blocage logiciel**: si l’application présente un problème de compatibilité connu et risque de ne pas fonctionner correctement, le message suivant s’affiche :

![applications avec problèmes de compatibilité connus-boîte de dialogue messages de blocage souple](images/pcafigure21.png)

dans les deux cas, l’option « obtenir de l’aide en ligne » envoie un rapport d’erreurs Windows pour obtenir une réponse en ligne de Microsoft et l’afficher à l’utilisateur. En général, les réponses pointent l’utilisateur sur l’un des trois types de ressources suivants :

-   Une mise à jour du fournisseur de l’application
-   Site Web d’un fournisseur d’applications pour plus d’informations
-   Un article de la base de connaissances Microsoft pour plus d’informations

**Télémétrie pour PCA**

une fois que l’assistant compatibilité des applications a traité tous les problèmes d’application sur un ordinateur Windows 8 et qu’il obtient toutes les commentaires des utilisateurs, il recueille des données anonymes sur l’application, le programme d’installation, les problèmes détectés et les paramètres de compatibilité appliqués à l’application, et les renvoie à Microsoft. Ces données sont collectées à partir de tout utilisateur qui souhaite fournir des données anonymes (par le biais du programme d’amélioration du produit Programme d’amélioration des services). une fois ces données collectées, les défaillances et les correctifs de l’application sont analysés, et les correctifs sont ensuite distribués à l’intégralité de l’écosystème Windows par le biais du mécanisme de Windows Update afin que tout utilisateur de l’application dans les futurs avantages du correctif automatiquement.

**Contrôles d’administration et gestion des paramètres PCA**

Les administrateurs informatiques peuvent contrôler le comportement de l’APC de deux manières :

-   **Désactiver PCA** : ce paramètre permet aux administrateurs informatiques de désactiver les boîtes de dialogue que l’APC affiche aux utilisateurs. PCA continuera de suivre et de détecter les problèmes et de renvoyer les données de télémétrie
-   **Désactiver la télémétrie** de l’application : ce paramètre désactive toute collection et envoi de données de télémétrie par PCA
    > [!Note]  
    > Si le programme d’amélioration du produit est désactivé, ce paramètre n’a aucun impact.

     

**Conception d’applications à utiliser avec PCA**

Les développeurs doivent s’assurer que leurs applications fonctionnent correctement dans tous les scénarios de compatibilité décrits ci-dessus. Les développeurs doivent tester et valider leurs applications pour chacun des scénarios ci-dessus et s’assurer qu’il n’existe aucun problème de compatibilité. Si des problèmes de compatibilité sont identifiés, les développeurs doivent apporter les correctifs nécessaires à leurs applications pour s’assurer que le problème de compatibilité est résolu. Voici quelques-uns des correctifs courants que les développeurs doivent prendre en compte :

-   éliminer les vérifications de version du système d’exploitation Windows lors de l’installation et du runtime
-   Supprimer la vérification des privilèges (vérification de l’accès administrateur); utiliser le manifeste EXE pour déclarer le niveau de privilège requis
-   s’assurer que les fichiers binaires de Windows ne sont pas fournis dans le programme d’installation de l’application
-   Éliminer l’écriture dans des zones protégées (Registre, dossiers) ou l’écriture de fichiers protégés
-   Signer numériquement tous les fichiers binaires (EXE, DLL, fichiers SYS)
-   Pour les programmes d’installation, assurez-vous que l’entrée’ajout/suppression de programmes’est correctement ajoutée. au minimum, cette entrée de métadonnées d’application doit inclure le nom de l’application, le serveur de publication, la chaîne de version et la langue prise en charge. Cela indique à PCA que le programme d’installation s’est terminé correctement et fournit également un moyen pratique pour les utilisateurs de désinstaller l’application.

en veillant à ce que la section TRUSTINFO et compatibilité du manifeste de l’application (exécutable) soit mise à jour comme indiqué dans le guide de compatibilité Windows 8 permettra à PCA de savoir que l’application a été conçue pour la Windows 8 et que l’application s’exécute toujours en mode natif sans aucun mode de compatibilité appliqué.

Pour vous assurer que l’application PCA considère que l’application est conçue pour Windows 8 :

-   Les exe tous (programme d’installation ou Runtime) doivent être manifestés pour TRUSTINFO et les sections de compatibilité pour Windows 8
-   Le programme d’installation doit ajouter une entrée’ajout/suppression de programmes'

**Glossaire**

Les modes de compatibilité utilisés par PCA sont répertoriés ci-dessous avec une brève description de ce que le mode active.



| Mode                         | Description                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows7RTM                  | ce mode émule le comportement commun de Windows 7, y compris le numéro de version du système d’exploitation 6,1                                                                   |
| WindowsVistaSP2              | ce mode émule le comportement commun de Windows 7, y compris le numéro de version du système d’exploitation 6,1                                                                   |
| WindowsXPSp3                 | ce mode émule le comportement common Windows XP SP3, y compris le numéro de version 5,1 du système d’exploitation. Cela comprend également le mode RUNASHIGHEST                    |
| RUNASHIGHEST                 | Ce mode invite l’utilisateur à exécuter l’application avec le privilège le plus élevé disponible. Les utilisateurs disposant de privilèges d’administration verront une invite d’élévation du contrôle de compte d’utilisateur pour l’application |
| RUNASADMIN                   | Ce mode invite toujours l’utilisateur à exécuter l’application avec des privilèges d’administrateur. les applications avec ce mode obtiendront toujours l’invite d’élévation UAC                    |
| ELEVATECREATEPROCESS         | Ce mode permet aux processus enfants de l’application principale d’être exécutés avec des privilèges d’administrateur. les processus enfants obtiennent une boîte de dialogue d’élévation du contrôle de compte d’utilisateur                          |
| PINDLL                       | Ce mode force une DLL à être en mémoire pour une application même si l’application décharge la DLL                                                                                |
| DISABLEUSERCALLBACKEXCEPTION | Ce mode intercepte les exceptions de rappel de l’utilisateur et permet à l’application de continuer sans avoir à gérer l’exception                                          |
| VIRTUALIZEDELETE             | Ce mode intercepte les opérations de suppression sur les fichiers protégés et empêche les applications d’échouer en raison d’exceptions non gérées de l’opération de suppression                   |
| WRPMITIGATION                | ce mode retourne une réussite lorsqu’une application tente d’écrire, de modifier ou de supprimer des fichiers ou des entrées de registre protégés Windows (sans réellement terminer l’opération)  |
| DXMAXIMIZEDWINDOWEDMODE      | Ce mode identifie les applications qui passent en mode plein écran et les redirige en mode fenêtre agrandi.                                                          |
| HIGHDPIAWARE                 | ce mode permet au reste de Windows de savoir que l’application prend en charge la haute résolution et aide le rendu approprié des éléments d’interface utilisateur, du texte, de la police, etc.                              |



 

 

 