---
title: Tests du Kit de certification des applications Windows
description: Vous trouverez ci-dessous des informations de test pour la certification des applications dekstop.
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a353eef0cd73fecac275b750345b3dd97d05dc87
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509458"
---
# <a name="windows-app-certification-kit-tests"></a>Tests du Kit de certification des applications Windows

Vous trouverez ci-dessous des informations de test pour la certification des applications dekstop. Pour plus d’informations, consultez [utilisation du kit de certification des applications Windows](using-the-windows-app-certification-kit.md).

-   [Installation réversible](#clean-reversible-install)
-   [Installer dans le test des dossiers corrects](#install-to-the-correct-folders-test)
-   [Test de fichier signé numériquement](#digitally-signed-file-test)
-   [Test Windows de prise en charge x64](#support-x64-windows-test)
-   [Test de vérification de la version du système d’exploitation](#os-version-checking-test)
-   [Test de contrôle de compte d’utilisateur (UAC)](#user-account-control-uac-test)
-   [Adhérer aux messages du gestionnaire de redémarrage du système](#adhere-to-system-restart-manager-messages)
-   [Test en mode sans échec](#safe-mode-test)
-   [Test de session multi-utilisateur](#multiuser-session-test)
-   [Incidents et blocages de test](#crashes-and-hangs-test)
-   [Test de compatibilité et de résilience](#compatibility-and-resiliency-test)
-   [Test des meilleures pratiques de sécurité Windows](#windows-security-best-practices-test)
-   [Test des fonctionnalités de sécurité Windows](#windows-security-features-test)
-   [Test haute résolution](#high-dpi-test)

## <a name="clean-reversible-install"></a>Installation réversible

Installe et désinstalle l’application et vérifie les fichiers résiduels et les entrées de registre.

-   Arrière-plan
    -   Une installation propre et réversible permet aux utilisateurs de déployer et de supprimer des applications. Pour réussir ce test, l’application doit effectuer les opérations suivantes :
        -   L’application ne force pas le redémarrage du système immédiatement après l’installation ou la désinstallation de l’application. *Le processus d’installation ou de désinstallation d’une application ne doit jamais nécessiter un redémarrage du système une fois l’opération terminée. Si le système doit être redémarré, les utilisateurs doivent pouvoir redémarrer le système à leur convenance.*
        -   L’application n’est pas dépendante des noms de fichiers courts 8,3 (SFN). *Les processus d’installation et de désinstallation de l’application doivent être en mesure d’utiliser des noms de fichiers et des chemins d’accès de dossier longs.*
        -   L’application ne bloque pas l’installation ou la désinstallation silencieuse
        -   L’application effectue les entrées requises dans le registre système. *Les outils d’inventaire Windows et les outils de télémétrie requièrent des informations complètes sur les applications installées. Les programmes d’installation d’application doivent créer les entrées de Registre correctes pour permettre une détection et une désinstallation réussies.*
    -   Si vous utilisez un programme d’installation MSI, MSI crée automatiquement les entrées de Registre ci-dessous. Si vous n’utilisez pas un programme d’installation MSI, le module d’installation doit créer les entrées de Registre suivantes au cours de l’installation :
        -   DisplayName
        -   Emplacement de l’installation
        -   Publisher
        -   UninstallString
        -   VersionMajor ou MajorVersion
        -   VersionMinor ou MinorVersion
    -   L’application doit supprimer toutes ses entrées dans Ajout/suppression de programmes.
-   Détails du test
    -   Ce test vérifie les processus d’installation et de désinstallation de l’application pour le comportement requis.
-   Action corrective
    -   Passez en revue la conception et le comportement de l’application par rapport aux conditions décrites ci-dessus.

## <a name="install-to-the-correct-folders-test"></a>Installer dans le test des dossiers corrects

Vérifie que l’application écrit ses fichiers de programme et de données dans les dossiers appropriés.

-   Arrière-plan
    -   Les applications doivent avoir un système utilisateur et des dossiers par utilisateur correctement, afin de pouvoir accéder aux données et aux paramètres dont elle a besoin tout en protégeant les données et les paramètres de l’utilisateur contre tout accès non autorisé.
-   Dossiers Program Files
    -   L’application doit être installée dans le dossier Program Files par défaut (% ProgramFiles% pour les applications natives 32 bits et 64 bits, et% ProgramFiles (x86)% pour les applications 32 bits s’exécutant sur x64).
    -   **Remarque :** L’application ne doit pas stocker les données utilisateur ou les données d’application dans un dossier Program Files en raison des autorisations de sécurité configurées pour ce dossier.
    -   Les listes de contrôle d’accès des dossiers système Windows autorisent uniquement la lecture et l’écriture des comptes administrateur. Par conséquent, les comptes d’utilisateurs standard n’ont pas accès à ces dossiers. La virtualisation de fichiers permet cependant aux applications de stocker un fichier, tel qu’un fichier de configuration, dans un emplacement système qui est généralement accessible en écriture uniquement par les administrateurs. L’exécution de programmes en tant qu’utilisateur standard dans cette situation peut entraîner un échec s’ils ne peuvent pas accéder à un fichier requis.
    -   Les applications doivent utiliser des [dossiers connus](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) pour s’assurer qu’ils seront en mesure d’accéder à leurs données.
    -   **Remarque :** Windows fournit la virtualisation de fichiers pour améliorer la compatibilité des applications et éliminer les problèmes lorsque les applications s’exécutent en tant qu’utilisateur standard sur Windows. Votre application ne doit pas s’appuyer sur la virtualisation présente dans les futures versions de Windows.
-   Dossiers de données d’application spécifiques à l’utilisateur
    -   Dans les installations « par ordinateur », l’application ne doit pas écrire de données spécifiques à l’utilisateur pendant l’installation. Les données d’installation spécifiques à l’utilisateur doivent être écrites uniquement lorsqu’un utilisateur démarre l’application pour la première fois. Cela est dû au fait qu’il n’y a pas d’emplacement utilisateur correct pour stocker des données au moment de l’installation. Les tentatives effectuées par une application pour modifier les comportements d’association par défaut au niveau de l’ordinateur après l’installation échouent. Au lieu de cela, les valeurs par défaut doivent être revendiquées sur un niveau par utilisateur, ce qui empêche plusieurs utilisateurs de remplacer les valeurs par défaut des autres.
    -   Toutes les données d’application exclusives à un utilisateur spécifique et ne devant pas être partagées avec d’autres utilisateurs de l’ordinateur doivent être stockées dans les utilisateurs \\ <username> \\ AppData.
    -   Toutes les données d’application qui doivent être partagées entre les utilisateurs de l’ordinateur doivent être stockées dans ProgramData.
-   Autres dossiers système et clés de Registre
    -   L’application ne doit jamais écrire directement dans le répertoire et les sous-répertoires Windows. Utilisez les méthodes appropriées pour installer des fichiers, tels que des polices ou des pilotes, dans ces répertoires.
    -   Les applications ne doivent pas démarrer automatiquement au démarrage, par exemple en ajoutant une entrée à un ou plusieurs de ces emplacements :
        -   Clés d’exécution de Registre HKLM et, ou HKCU sous Software \\ Microsoft \\ Windows \\ CurrentVersion
        -   Clés d’exécution de Registre HKLM et/ou HKCU sous Software \\ Wow6432Node \\ Microsoft \\ Windows \\ CurrentVersion
        -   Menu Démarrer AllPrograms > démarrage
-   Détails du test
    -   Ce test vérifie que l’application utilise les emplacements spécifiques du système de fichiers que Windows fournit pour stocker des programmes et des composants logiciels, des données d’application partagées et des données d’application spécifiques à un utilisateur.
-   Actions correctives
    -   Passez en revue la façon dont l’application utilise les dossiers du système et assurez-vous qu’elle les utilise correctement.
-   Exceptions et dérogations
    -   Une dérogation est requise pour les applications de bureau écrivant dans le Global Assembly Cache (GAC) (les applications .NET doivent conserver les dépendances d’assembly privées et les stocker dans le répertoire de l’application, sauf si le partage d’un assembly est explicitement requis).
    -   L’installation dans le dossier Program Files n’est pas obligatoire pour les packages de logiciels de bureau pour obtenir un logo logiciel, uniquement sous la catégorie notions de base sur les logiciels.

## <a name="digitally-signed-file-test"></a>Test de fichier signé numériquement

Teste les fichiers exécutables et les pilotes de périphérique pour vérifier qu’ils disposent d’une signature numérique valide.

-   Arrière-plan
    -   Les fichiers signés numériquement permettent de vérifier que le fichier est authentique et de détecter si le fichier a été falsifié.
    -   L’application de la signature de code en mode noyau est une fonctionnalité Windows également appelée intégrité du code (CI). CI améliore la sécurité de Windows en vérifiant l’intégrité d’un fichier chaque fois qu’il est chargé en mémoire. L’élément de configuration détecte si du code malveillant a modifié un fichier binaire système et génère un événement de diagnostic et de journal d’audit système lorsque la signature d’un module de noyau ne parvient pas à vérifier correctement.
    -   Si l’application nécessite des autorisations élevées, l’invite d’élévation affiche des informations contextuelles sur le fichier exécutable qui demande un accès avec élévation de privilèges. Selon que l’application est signée Authenticode ou non, l’utilisateur peut voir l’invite de consentement ou l’invite d’informations d’identification.
    -   Les noms forts empêchent les tiers d’usurper votre code, tant que vous conservez la sécurité de la clé privée. Le .NET Framework vérifie la signature numérique lors du chargement de l’assembly ou l’installe dans le GAC. Sans accès à la clé privée, un utilisateur malveillant ne peut pas modifier votre code et le signer à nouveau.
-   Détails du test
    -   Tous les fichiers exécutables, tels que ceux avec des extensions de fichier. exe,. dll,. ocx,. sys,. cpl,. drv et. scr, doivent être signés avec un certificat Authenticode.
    -   Tous les pilotes en mode noyau installés par l’application doivent avoir une signature Microsoft obtenue par le biais du programme WHQL ou DRS. Tous les pilotes de filtre de système de fichiers doivent être signés WHQL.
-   Action corrective
    -   Signez les fichiers exécutables de l’application.
    -   Utilisez makecert.exe pour générer un certificat ou obtenir une clé de signature de code à partir de l’une des autorités de certification commerciales (ca), telles que VeriSign, Thawte ou une autorité de certification Microsoft.
-   Exceptions et dérogations
    -   Les dérogations seront considérées uniquement pour les redistribuables tiers non signés. Une preuve de communication demandant une version signée du ou des redistribuables est nécessaire pour que cette renonciation soit accordée.
    -   Les packages logiciels à valeur ajoutée de l’appareil sont exemptés de la certification du pilote en mode noyau, car les pilotes doivent être certifiés par la certification matérielle Windows.

## <a name="support-x64-windows-test"></a>Test Windows de prise en charge x64

Testez l’application pour vous assurer que le fichier. exe est conçu pour l’architecture de la plateforme sur laquelle il sera installé.

-   Arrière-plan
    -   Le fichier exécutable doit être généré pour l’architecture de processeur sur laquelle il est installé. Certains fichiers exécutables peuvent s’exécuter sur une architecture de processeur différente, mais cela n’est pas fiable.
    -   La compatibilité de l’architecture est importante, car les processus 32 bits ne peuvent pas charger les dll 64 bits et les processus 64 bits ne peuvent pas charger de dll 32 bits. De même, les versions 64 bits de Windows ne prennent pas en charge l’exécution d’applications Windows 16 bits, car les handles comportent 32 bits significatifs sur Windows 64 bits et ne peuvent donc pas être passés à des applications 16 bits. Par conséquent, toute tentative de lancement d’une application 16 bits échouera sur les versions 64 bits de Windows.
    -   les pilotes de périphérique 32 bits ne peuvent pas s’exécuter sur les versions 64 bits de Windows et, par conséquent, ils doivent être portés vers l’architecture 64 bits.
    -   Pour les applications en mode utilisateur, Windows 64 bits comprend WOW64, ce qui permet aux applications Windows 32 bits de s’exécuter sur des systèmes exécutant Windows 64 bits, mais avec une perte de performances. Il n’existe aucune couche de traduction équivalente pour les pilotes de périphérique.
    -   Pour assurer la compatibilité avec les versions 64 bits de Windows, les applications doivent prendre en charge de manière native 64 bits ou, au minimum, les applications Windows 32 bits doivent s’exécuter en toute transparence sur les systèmes 64 bits :
        -   Les applications et leurs programmes d’installation ne doit pas contiennent tout code 16 bits ou ne s’appuient sur aucun composant 16 bits.
        -   Le programme d’installation de l’application doit détecter et installer les pilotes et les composants appropriés sur les versions 64 bits de Windows.
        -   Tous les plug-ins de Shell doivent s’exécuter sur les versions 64 bits de Windows.
        -   Les applications qui s’exécutent sous l’émulateur WoW64 ne doivent pas tenter de contourner les mécanismes de virtualisation WOW64. S’il existe des scénarios spécifiques où les applications doivent détecter si elles s’exécutent dans un émulateur WoW64, elles doivent le faire en appelant [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process).
-   Détails du test
    -   L’application ne doit pas installer de binaires 16 bits. L’application ne doit pas installer un pilote en mode noyau 32 bits s’il est supposé s’exécuter sur un ordinateur 64 bits.
-   Actions correctives
    -   Générez les fichiers exécutables et les pilotes pour l’architecture de processeur pour laquelle vous souhaitez les installer.

## <a name="os-version-checking-test"></a>Test de vérification de la version du système d’exploitation

Teste la manière dont l’application vérifie la version de Windows sur laquelle elle s’exécute.

-   Arrière-plan
    -   Les applications vérifient la version du système d’exploitation en testant une version qui est supérieure ou égale à la version requise pour garantir la compatibilité avec les futures versions de Windows.
-   Détails du test
    -   Simule l’exécution de l’application sur différentes versions de Windows pour voir comment elle réagit.
-   Actions correctives
    -   Testez la version correcte de Windows en testant si la version actuelle est supérieure ou égale à la version requise par votre application, service ou pilote.
    -   Les modules d’installation et de désinstallation de pilotes ne doivent jamais vérifier la version du système d’exploitation.
-   Exceptions et dérogations
    -   Les dérogations seront prises en compte pour les applications qui répondent aux critères suivants : *(s’applique à la certification des applications de bureau uniquement)*
        -   Les applications qui sont remises sous la forme d’un seul package s’exécutant sur Windows XP, Windows Vista et Windows 7 et doivent vérifier la version du système d’exploitation pour déterminer les composants à installer sur un système d’exploitation donné.
        -   Applications qui vérifient uniquement la version minimale du système d’exploitation (uniquement lors de l’installation, pas au moment de l’exécution) en utilisant uniquement les appels d’API approuvés et répertorient la version minimale requise dans le manifeste de l’application, si nécessaire.
        -   Applications de sécurité telles que les applications antivirus et de pare-feu, les utilitaires système tels que les utilitaires de défragmentation et les applications de sauvegarde, ainsi que les outils de diagnostic qui vérifient la version du système d’exploitation en utilisant uniquement les appels d’API approuvés.

## <a name="user-account-control-uac-test"></a>Test de contrôle de compte d’utilisateur (UAC)

Teste l’application pour vérifier qu’elle n’a pas besoin d’autorisations élevées pour s’exécuter.

-   Arrière-plan
    -   Une application qui fonctionne ou s’installe uniquement lorsque l’utilisateur est un administrateur oblige les utilisateurs à exécuter l’application avec des autorisations inutilement élevées, ce qui peut permettre aux logiciels malveillants d’accéder à l’ordinateur de l’utilisateur.
    -   Lorsque les utilisateurs sont toujours obligés d’exécuter des applications avec des jetons d’accès élevés, l’application peut être serveur comme point d’entrée pour du code trompeur ou malveillant. Ce programme malveillant peut facilement modifier le système d’exploitation, ou pire, affecter les autres utilisateurs. Il est presque impossible de contrôler un utilisateur disposant d’un accès administrateur complet, car les administrateurs peuvent installer des applications et exécuter des applications ou des scripts sur l’ordinateur. Les responsables informatiques cherchent toujours des moyens de créer des « bureaux standard » où les utilisateurs se connectent en tant qu’utilisateurs standard. Les postes de travail standard réduisent les coûts du support technique et réduisent la surcharge informatique.
    -   La plupart des applications ne requièrent pas de privilèges d’administrateur au moment de l’exécution. Un compte d’utilisateur standard doit être en mesure de les exécuter. Les applications Windows doivent avoir un manifeste (intégré ou externe) pour définir son niveau d’exécution qui indique au système d’exploitation les privilèges nécessaires pour exécuter l’application. Le manifeste d’application s’applique uniquement aux fichiers. exe, et non aux fichiers. dll. Le contrôle de compte d’utilisateur (UAC) n’examine pas les dll pendant la création du processus. Les règles UAC ne s’appliquent pas aux services Microsoft. Le manifeste de l’application peut être incorporé ou externe.
    -   Pour créer un manifeste, créez un fichier portant le nom <nom de l’application \_ # C1.exe. manifest et stockez-le dans le même répertoire que l’exécutable. Notez que tout manifeste externe est ignoré si l’application a un manifeste interne.
        -   Par exemple, <requestedExecutionLevel Level = "" asInvoker \| highestAvailable \| requireAdministrator "" UIAccess = "" true \| false ""/>
        -   Le processus principal de l’application doit être exécuté en tant qu’utilisateur standard (**asInvoker**). Toutes les fonctionnalités d’administration doivent être déplacées dans un processus distinct qui s’exécute avec des privilèges d’administrateur.
        -   Les applications accessibles à l’utilisateur qui requièrent des privilèges élevés doivent être signées avec Authenticode.
-   Détails du test
    -   Tous les fichiers exe de l’utilisateur doivent être marqués avec l’attribut asInvoker. S’ils sont marqués comme highestAvailable ou requireAdministrator, ils doivent être signés correctement avec Authenticode. Tous les exe d’application ne doivent pas avoir l’attribut uiAccess défini sur true. Tout exe qui s’exécute en tant que service est exclu de cette vérification particulière.
-   Actions correctives
    -   Passez en revue le fichier manifeste de l’application pour connaître les entrées et les niveaux d’autorisation corrects.
-   Exceptions et dérogations
    -   Une dérogation est requise pour les applications qui exécutent leur processus principal avec des privilèges élevés (**requireAdministrator** ou **highestAvailable**). Le processus principal est le processus qui fournit le point d’entrée de l’utilisateur à l’application.
    -   Les dérogations seront prises en compte pour les scénarios suivants :
        -   Outils d’administration ou système dont le niveau d’exécution est défini sur **highestAvailable**, **requireAdministrator**, ou les deux.
        -   Seule l’application d’accessibilité ou d’UI Automation Framework affecte la valeur TRUE à l’indicateur uiAccess pour ignorer l’isolation des privilèges de l’interface utilisateur (UIPI). Pour démarrer correctement l’utilisation de l’application, cet indicateur doit être signé avec Authenticode et doit résider dans un emplacement protégé dans le système de fichiers, tel que Program Files.

## <a name="adhere-to-system-restart-manager-messages"></a>Adhérer aux messages du gestionnaire de redémarrage du système

Teste la manière dont l’application répond aux messages d’arrêt et de redémarrage du système.

-   Arrière-plan
    -   Les applications doivent se fermer le plus rapidement possible quand elles sont averties que le système est en cours d’arrêt pour fournir une expérience d’arrêt ou de mise hors tension réactive pour l’utilisateur.
    -   Dans un arrêt critique, les applications qui renvoient la valeur FALSe à [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) reçoivent **WM \_ ENDSESSION** et Closed, tandis que ceux qui expirent en réponse à WM \_ QUERYENDSESSION seront arrêtés de force.
-   Détails du test
    -   Examine la manière dont l’application répond aux messages d’arrêt et de sortie.
-   Actions correctives
    -   Si votre application échoue à ce test, passez en revue la façon dont elle gère ces messages Windows :
        -   [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) avec *lParam*  =  **ENDSESSION \_ CLOSEAPP**(0x1) : les applications de bureau doivent répondre (true) immédiatement en vue d’un redémarrage. Les applications console peuvent appeler [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) pour recevoir une notification d’arrêt. Les services peuvent appeler [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) pour recevoir des notifications d’arrêt dans une routine de gestionnaire.
        -   [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) avec *lParam*  =  **ENDSESSION \_ CLOSEAPP**(0x1) : les applications doivent retourner une valeur 0 dans les 30 secondes et s’arrêter. Au minimum, les applications doivent se préparer en enregistrant les données utilisateur et indiquer les informations nécessaires après un redémarrage.
    -   Les applications console qui reçoivent la notification d' **\_ \_ événement Ctrl C** doivent s’arrêter immédiatement. Les pilotes ne doivent pas refuser un événement d’arrêt système.
    -   **Remarque :** Les applications qui doivent bloquer l’arrêt en raison d’une opération qui ne peut pas être interrompue doivent utiliser [**ShutdownBlockReasonCreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) pour inscrire une chaîne expliquant la raison de l’utilisateur. Une fois l’opération terminée, l’application doit appeler [**ShutdownBlockReasonDestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) pour indiquer que le système peut être arrêté.

## <a name="safe-mode-test"></a>Test en mode sans échec

Teste si le pilote ou le service est configuré pour démarrer en mode sans échec.

-   Arrière-plan
    -   Le mode sans échec permet aux utilisateurs de diagnostiquer et de résoudre les problèmes liés à Windows. Seuls les pilotes et les services nécessaires au fonctionnement de base du système d’exploitation ou fournissent des services de diagnostic et de récupération doivent être chargés en mode sans échec. Le chargement d’autres fichiers en mode sans échec complique la résolution des problèmes liés au système d’exploitation.
    -   Par défaut, seuls les pilotes et les services qui sont préinstallés avec Windows démarrent en mode sans échec. Tous les autres pilotes et services doivent être désactivés, sauf si le système en a besoin pour des opérations de base ou à des fins de diagnostic et de récupération.
-   Détails du test
    -   Les pilotes installés par l’application ne doivent pas être marqués pour le chargement en mode sans échec.
-   Actions correctives
    -   Si le pilote ou le service ne doit pas démarrer en mode sans échec, supprimez les entrées de l’application des clés de registre.
-   Exceptions et dérogations
    -   Les pilotes et les services qui doivent démarrer en mode sans échec nécessitent une dérogation pour être certifiés. La demande de renonciation doit inclure chaque pilote et service à ajouter aux clés de Registre SafeBoot et décrire les raisons techniques pour lesquelles le pilote ou le service doit s’exécuter en mode sans échec. Le programme d’installation de l’application doit inscrire tous les pilotes et services de ce type dans les clés de Registre suivantes :
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network
-   **Remarque :** Vous devez tester les pilotes et les services que vous souhaitez démarrer en mode sans échec pour vous assurer qu’ils fonctionnent en mode sans échec sans erreurs.

## <a name="multiuser-session-test"></a>Test de session multi-utilisateur

Testez le comportement de l’application lorsqu’elle est exécutée dans plusieurs sessions en même temps.

-   Arrière-plan
    -   Les utilisateurs Windows doivent être en mesure d’exécuter des sessions simultanées. Les applications doivent s’assurer que lorsqu’elles s’exécutent dans plusieurs sessions, soit localement, soit à distance, les fonctionnalités normales de l’application ne sont pas affectées. Les paramètres de l’application et les fichiers de données doivent être spécifiques à l’utilisateur, et la confidentialité et les préférences de l’utilisateur doivent être limitées à la session de l’utilisateur.
-   Détails du test
    -   Exécute plusieurs instances simultanées de l’application pour tester les éléments suivants :
        -   Plusieurs instances d’une application s’exécutant en même temps sont isolées les unes des autres.
    -   Cela signifie que les données utilisateur d’une instance ne sont pas visibles par une autre instance. Le son dans une session utilisateur inactive ne doit pas être entendu dans une session utilisateur active. Dans les cas où plusieurs instances d’application utilisent des ressources partagées, l’application doit s’assurer qu’il n’y a pas de conflit.
        -   Si l’application a été installée pour plusieurs utilisateurs, elle stocke les données dans le ou les dossiers appropriés et dans les emplacements du Registre.
        -   L’application peut s’exécuter dans plusieurs sessions utilisateur (changement rapide d’utilisateur) pour l’accès local et à distance.
    -   Pour ce faire, l’application doit vérifier d’autres sessions Terminal Services (TS) pour les instances existantes de l’application. Si l’application ne prend pas en charge plusieurs sessions utilisateur ou accès à distance, elle doit clairement l’indiquer à l’utilisateur lorsqu’elle est lancée à partir d’une session de ce type.
-   Action corrective
    -   Assurez-vous que l’application ne stocke pas les fichiers de données ou les paramètres du système dans des magasins de données spécifiques à l’utilisateur, tels que profil utilisateur ou HKCU. Si c’est le cas, ces informations ne seront pas disponibles pour les autres utilisateurs.
    -   Votre application doit installer les fichiers de configuration et de données au niveau du système au cours de l’installation et créer les fichiers et les paramètres spécifiques à l’utilisateur après l’installation lorsqu’un utilisateur l’exécute.
    -   Assurez-vous que l’application ne bloque pas plusieurs sessions simultanées, localement ou à distance. L’application ne doit pas dépendre de mutex globaux ou d’autres objets nommés pour rechercher ou bloquer plusieurs sessions simultanées.
    -   Si l’application ne peut pas autoriser plusieurs sessions simultanées par utilisateur, utilisez des espaces de noms par utilisateur ou par session pour les mutex et d’autres objets nommés.

## <a name="crashes-and-hangs-test"></a>Incidents et blocages de test

Surveille l’application au cours des tests de certification afin d’enregistrer quand elle cesse de répondre ou se bloque.

-   Arrière-plan
    -   Les échecs d’application tels que les blocages et les blocages représentent une interruption importante pour les utilisateurs et entraînent des frustrations. L’élimination de ces défaillances améliore la stabilité et la fiabilité des applications, et globale, offre aux utilisateurs une meilleure expérience d’application. Les applications qui cessent de répondre ou qui se bloquent peuvent conduire à la perte de données ou une expérience médiocre du point de vue de l’utilisateur.
-   Détails du test
    -   Nous testons la résilience et la stabilité de l’application tout au long des tests de certification.
    -   Le kit de certification des applications Windows appelle [**IApplicationActivationManager :: ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) pour lancer les applications du Windows Store. Pour que la méthode **ActivateApplication** lance une application, il faut que le contrôle de compte d’utilisateur (UAC) soit activé et que la résolution de l’écran soit d’au moins 1 024 × 768 ou 768 × 1 024. Si l’une de ces conditions n’est pas respectée, votre application échouera à ce test.
-   Actions correctives
    -   Assurez-vous que le contrôle UAC est activé sur l’ordinateur de test.
    -   Veillez à exécuter le test sur un ordinateur dont l’écran est suffisamment grand.
    -   Si le lancement de votre application échoue et que votre plateforme de test satisfait aux exigences liées à la méthode [**ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication), vous pouvez résoudre le problème en examinant le journal des événements d’activation. Pour rechercher ces entrées dans le journal des événements :
        1.  Ouvrez eventvwr.exe et accédez au nœud de l' \\ application journaux Windows \\ .
        2.  Filtrez la vue de manière à afficher les ID d’événement 5900 à 6000.
        3.  Dans les entrées du journal, recherchez les informations susceptibles d’expliquer l’échec du lancement de l’application.
    -   Identifiez le fichier posant problème et corrigez-le. Générez et testez de nouveau l’application.
-   Ressources supplémentaires
    -   [Utilisation de Application Verifier dans le cycle de vie de développement de votre logiciel](https://blogs.msdn.com/b/ntdebugging/archive/2014/01/13/debugging-a-windows-8-1-store-app-crash-dump.aspx)
    -   [Application Verifier]( https://go.microsoft.com/fwlink/p/?LinkId=708300)
    -   [Utilisation de Application Verifier](https://www.microsoft.com/?ref=go)
    -   [DLL AppInit](https://www.microsoft.com/?ref=go)
    -   [Réduire le temps de démarrage (applications du Windows Store en C#/VB/C++ et XAML)](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="compatibility-and-resiliency-test"></a>Test de compatibilité et de résilience

-   Arrière-plan
    -   Cette vérification valide deux aspects d’une application, le fichier exécutable principal de l’application, par exemple, le point d’entrée de l’application utilisateur doit être manifeste pour la compatibilité, ainsi que la déclaration du bon GUID. Pour prendre en charge ce nouveau test, le rapport aura un sous-nœud sous « Compatibility & Resiliency ». L’application échoue si une ou les deux conditions sont manquantes.
-   Détails du test
    -   **Compatibilité :** Les applications doivent être entièrement opérationnelles sans utiliser les modes de compatibilité Windows, les messages AppHelp ou d’autres correctifs de compatibilité. Un manifeste de compatibilité permet à Windows de fournir à votre application le comportement de compatibilité approprié dans les différentes versions du système d’exploitation.
    -   **AppInit :** Les applications ne doivent pas répertorier les dll à charger dans la \_ clé de Registre HKEY local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows \\ AppInit \_ dll.
    -   **Switchback :** L’application doit fournir le manifeste Switchback. Si le manifeste est manquant, le kit de certification des applications Windows affiche un message d’avertissement. Le kit de certification des applications Windows vérifie également que le manifeste contient un GUID de système d’exploitation valide.
-   Actions correctives
    -   Corrigez le composant de l’application qui utilise le correctif de compatibilité.
    -   Assurez-vous que l’application ne repose pas sur les correctifs de compatibilité pour ses fonctionnalités.
    -   Vérifiez que votre application est manifeste et que la section compatibilité inclut les valeurs appropriées.
-   Informations supplémentaires
    -   Pour plus d’informations, consultez [DLL AppInit](/previous-versions/windows/apps/hh994639(v=win.10)) .

## <a name="windows-security-best-practices-test"></a>Test des meilleures pratiques de sécurité Windows

-   Arrière-plan
    -   Une application ne doit pas modifier les paramètres de sécurité Windows par défaut
-   Détails du test
    -   Teste la sécurité de l’application en exécutant l’analyseur de surface d’attaque. L’approche consiste à ajouter des catégories de défaillances à chaque test. Par exemple, certaines catégories de test de sécurité peuvent inclure :
        -   Échec de l’initialisation
        -   Échec de l’architecture de sécurité
        -   Échec possible de dépassement de mémoire tampon
        -   Échec de panne
    -   Pour plus d’informations, reportez-vous [ici](/previous-versions/windows/hh920280(v=win.10)).
-   Actions correctives
    -   Dépannez et corrigez le problème identifié par les tests. Générez et testez de nouveau l’application.

## <a name="windows-security-features-test"></a>Test des fonctionnalités de sécurité Windows

-   Arrière-plan
    -   Les applications doivent s’abonner aux fonctionnalités de sécurité Windows. La modification des protections de sécurité Windows par défaut peut exposer les clients à des risques accrus.
-   Détails du test
    -   Teste la sécurité de l’application en exécutant BinScope Binary Analyzer. Pour plus d’informations, reportez-vous [ici](/previous-versions/windows/hh920280(v=win.10)).
-   Actions correctives
    -   Dépannez et corrigez le problème identifié par les tests. Générez et testez de nouveau l’application.

## <a name="high-dpi-test"></a>Test haute résolution

Il est fortement recommandé que les applications Win32 prennent en charge la résolution. C’est la clé qui permet de donner à l’interface utilisateur de l’application un aspect cohérent sur un large éventail de paramètres d’affichage haute résolution. Une application qui ne prend pas en charge la DPI et qui s’exécute sur un paramètre d’affichage haute résolution peut rencontrer des problèmes tels qu’une mise à l’échelle incorrecte des éléments d’interface utilisateur, du texte tronqué et des images floues. Il existe deux façons de déclarer une application prenant en charge DPI. La première consiste à déclarer DPI.

-   Arrière-plan
    -   Cette vérification valide deux aspects d’une application, le ou les exécutables principaux, par exemple, les points d’entrée de l’application utilisateur doivent se manifester pour une reconnaissance haute résolution et les API appropriées sont appelées pour prendre en charge la haute résolution. L’application échoue si une ou les deux conditions sont manquantes. Cette vérification introduira une nouvelle section dans le rapport sur le bureau, consultez l’exemple ci-dessous.
-   Détails du test
    -   Le test génère un avertissement quand nous détectons l’un des éléments suivants :
        -   Le fichier EXE principal ne déclare pas la reconnaissance DPI dans son manifeste et n’appelle pas l’API SetProcessDPIAware. (Avertissez le développeur s’il oublie d’ajouter le manifeste de reconnaissance DPI).
        -   Le fichier EXE principal ne déclare pas la reconnaissance DPI dans son manifeste, mais il appelle l’API SetProcessDPIAware (avertir le développeur qu’il doit utiliser manifest pour déclarer la prise en forme PPP au lieu d’appeler l’API).
        -   Le mainEXE déclare la reconnaissance DPI dans son manifeste, mais il appelle également l’API SetProcessDPIAware (avertissant le développeur que l’appel de cette API n’est pas nécessaire).
        -   Pour les fichiers binaires qui ne sont pas des fichiers exe principaux, s’ils appellent l’API, donnez un avertissement (l’appel de l’API n’est pas recommandé).
-   Actions correctives
    -   L’utilisation de la fonction SetProcessDPIAware () est déconseillée. Si une DLL met en cache les paramètres ppp pendant son initialisation, l’appel de SetProcessDPIAware () dans l’application peut générer une condition de concurrence. L’appel de la fonction SetProcessDPIAware () dans une DLL n’est pas non plus une bonne pratique.
-   Informations supplémentaires
    -   [Écriture d’applications haute résolution](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 