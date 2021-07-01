---
title: 'Spécifications techniques des jeux pour Windows : bonnes pratiques pour les jeux sur Windows XP, Windows Vista, Windows 7 et Windows 8'
description: Cet article présente les conditions techniques et les meilleures pratiques pour les jeux qui s’exécutent sur Windows.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c7a0f52685b0b99247ebfd86af3727d834ca63
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120304"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Jeux pour les exigences techniques de Windows : meilleures pratiques pour les jeux sur Windows XP, Windows Vista, Windows 7 et Windows 8

Cet article présente les conditions techniques et les meilleures pratiques pour les jeux qui s’exécutent sur Windows. Nous avons écrit ces exigences techniques et les meilleures pratiques principalement pour couvrir Windows Vista et Windows 7, ainsi que le système d’exploitation Windows XP hérité. Ces meilleures pratiques s’appliquent généralement aux jeux Win32 de bureau sur Windows 8.

Cet article contient les sections suivantes :

-   [Différences pour Windows 8](#differences-for-windows-8)
    -   [Informations supplémentaires](#additional-information)
-   [Jeux pour Windows](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [Intégration de l’Explorateur de jeux 1,1](#11-games-explorer-integration)
    -   [1,2 prise en charge de la protection parentale/contrôle parental](/windows)
    -   [1,3 prendre en charge des jeux enregistrés enrichis](#13-support-rich-saved-games)
    -   [1,4 prendre en charge la configuration conditionnelle du contrôleur commun Xbox 360 pour Windows \[\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1,5 prendre en charge plusieurs proportions et résolutions](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [Lancement de la prise en charge 1,6 à partir de Windows Media Center](#16-support-launch-from-windows-media-center)
    -   [Support Direct3D 1,7](#17-direct3d-support)
    -   [1,8 activer la prise en charge des résolutions élevées](#18-enable-high-dpi-aware)
-   [Sécurité et compatibilité](#security-and-compatibility)
    -   [2,1 suivre les instructions relatives au contrôle de compte d’utilisateur](#21-follow-user-account-control-guidelines)
    -   [2,2 prendre en charge les versions x64 de Windows](#22-support-windows-x64-versions)
    -   [2,3 fichiers de signature](#23-sign-files)
    -   [2,4 signer les pilotes](#24-sign-drivers)
    -   [2,5 effectuer la vérification de version appropriée](#25-perform-proper-version-checking)
    -   [2,6 prendre en charge les sessions utilisateur simultanées](#26-support-concurrent-user-sessions)
    -   [2,7 prendre en charge les noms longs](#27-support-long-names)
-   [Installation](#32-support-user-account-control-for-installation)
    -   [Installation facile du support 3,1](#31-support-easy-installation)
    -   [3,2 prendre en charge le contrôle de compte d’utilisateur pour l’installation](#32-support-user-account-control-for-installation)
    -   [3,3 installer pour corriger les dossiers](#33-install-to-correct-folders)
    -   [3,4 Installation des ressources Windows correctement](#34-install-windows-resources-properly)
    -   [3,5 éviter les redémarrages au cours de l’installation](#35-avoid-reboots-during-installation)
    -   [3,6 utiliser le contrôle de version de fichier correctement](#36-use-file-versioning-correctly)
    -   [3,7 prise en charge de l’exigence conditionnelle d’exécution automatique \[\]](#37-support-autorun-conditional-requirement)
-   [Fiabilité](#reliability)
    -   [4,1 éliminer les redémarrages inutiles](#41-eliminate-unnecessary-reboots)
    -   [4,2 éliminer les échecs de Application Verifier](#42-eliminate-application-verifier-failures)
    -   [4,3 prise en charge des Rapport d’erreurs Windows et des informations de version de fichier](#43-support-windows-error-reporting-and-file-version-information)
-   [Contrôleur commun Xbox 360 pour terminologie Windows](#xbox-360-common-controller-for-windows-terminology)
-   [Instructions pour les produits middleware de jeux](#guidelines-for-game-middleware-products)
    -   [Introduction](#introduction)
    -   [Recommandations supplémentaires](#additional-recommendations)
    -   [Jeux pour les vitrines Windows](#games-for-windows-showcases)
-   [Ressources](#resources)

## <a name="differences-for-windows-8"></a>Différences pour Windows 8

Voici un résumé des principales différences lors de l’application de ces exigences techniques et des meilleures pratiques à Windows 8.

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**L’interface utilisateur de l’Explorateur de jeux n’est pas visible**
</dt> <dd>

Tous les jeux que vous enregistrez avec l' [Explorateur de jeux](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) sont exposés en tant que vignettes dans la nouvelle interface utilisateur Windows, mais une grande partie des métadonnées associées au titre ne sont plus visibles. Vous utilisez toujours l’outil jeux de fichiers de définition de jeux (GDFMAKER.EXE), qui est désormais disponible dans le kit de développement logiciel (SDK) Windows, pour créer les métadonnées. Vous utilisez également les mécanismes existants pour déployer les métadonnées. Continuez à tester votre inscription à l’Explorateur de jeux à l’aide de Windows 7, et vérifiez que la vignette de l’interface utilisateur Windows s’affiche lorsque vous l’installez sur Windows 8 (voir [1,1 jeux Explorateur intégration](#11-games-explorer-integration)).

Pour télécharger le kit de développement logiciel (SDK) Windows 8, consultez [téléchargements pour le développement d’applications de bureau](https://msdn.microsoft.com/windows/desktop/aa904949).

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**L’inscription auprès des API Game Explorer continue d’être le mécanisme d’inscription de votre jeu avec les contrôles parentaux Windows**
</dt> <dd>

Nous vous recommandons d’exécuter la version SDK Windows de GDFMAKER sur la version finale de Windows 8 pour vous assurer qu’elle peut remplir tous les systèmes d’évaluation actuellement pris en charge.

> [!Note]  
> Cette version de GDFMAKER nécessite .NET 4,0.

 

Consultez [1,2 support parental Safety/parental Controls](/windows).

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Il existe désormais trois choix pour l’utilisation de l’API XINPUT en fonction de vos besoins**
</dt> <dd>

XINPUT 1,4 est intégré à Windows 8. Les applications du Windows Store et les applications de bureau Win32 peuvent utiliser XINPUT 1,4. Toutes les versions de Windows peuvent utiliser XINPUT 9.1.0 pour les contrôleurs communs simplifiés, mais il n’existe aucun package de redistribution avec XINPUT 9.1.0. Toutes les versions de Windows peuvent également utiliser la version XINPUT 1,3 du kit de développement logiciel (SDK) DirectX existante, qui nécessite le déploiement de DirectSetup.

Consultez [1,4 prendre en charge le contrôleur commun Xbox 360 pour Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Seul un ensemble limité d’applications de bureau Win32 est pris en charge sur Windows RT**
</dt> <dd>

Les jeux qui s’exécutent sur Windows 7 peuvent et doivent s’exécuter correctement sur les plateformes Windows 8 x86 et x64.

Consultez [2,2 prise en charge des versions x64 de Windows](#22-support-windows-x64-versions).

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Vérifier que les vérifications du système d’exploitation sont effectuées correctement**
</dt> <dd>

La version du système d’exploitation Windows 8 est 6,2. Windows 8 passe les tests de la barre minimale actuellement recommandés pour le déploiement de jeux.

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**Le package de redistribution DirectX End-User s’exécute correctement sur Windows 8, comme il le fait sur Windows 7, pour déployer D3DX9, D3DX10, D3DX11, XINPUT 1,3, XAUDIO 2,7, XACTEngine, etc.**
</dt> <dd>

Toutefois, il existe un problème connu avec DirectSetup sur les systèmes avec uniquement .NET 4,0 installé en raison de la gestion du déploiement des assemblys DirectX 1,1 managés hérités. Ce problème s’applique à la fois à Windows 8, qui est fourni avec .NET 4,5 par défaut, et aux nouveaux ordinateurs Windows XP sur lesquels .NET 4,0 Runtime est installé. Toutefois, ce problème ne s’applique pas aux versions de .NET antérieures à .NET 4,0. Bien que Windows 8 ait un comportement de compatibilité des applications pour résoudre automatiquement ce problème (ce qui nécessite un accès réseau), nous recommandons que les jeux qui continuent de déployer la mise à jour DirectSetup vers le SDK DirectX (juin 2010) soient actualisés. Comme toujours, si vous utilisez DirectSetup pour votre titre, découpez votre titre jusqu’à l’ensemble minimal de CAB requis.

Consultez [3,4 installation correcte des ressources Windows](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Les jeux qui requièrent le runtime compatible .NET 2,0 (2,0, 3,0, 3,5) continuent d’utiliser les mécanismes de déploiement existants**
</dt> <dd>

Ces jeux déclenchent un comportement de compatibilité des applications sur Windows 8 pour activer le Runtime .NET 3,5 automatiquement (ce qui nécessite un accès réseau). Toutefois, nous recommandons aux développeurs .NET de passer au Runtime .NET 4,0.

> [!Note]  
> Les assemblys DirectX 1,1 managés hérités ne sont pas compatibles avec le Runtime .NET 4. x.

 

Consultez [3,4 installation correcte des ressources Windows](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**L’utilisation d’un AutoRunner ou d’une autre technologie de préinstallation qui s’appuie sur .NET n’est pas recommandée**
</dt> <dd>

Vous pouvez supposer que seuls les runtimes compatibles .NET 2,0 (2,0, 3,0, 3,5) sont présents sur Windows Vista et Windows 7. Seul le runtime compatible .NET 4,0 est présent sur Windows 8 par défaut.

Consultez la page exécution de la [prise en charge automatique 3,7](#37-support-autorun-conditional-requirement).

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Il existe une Application Verifier mise à jour pour Windows 8**
</dt> <dd>

Le kit de développement logiciel (SDK) Windows 8 comprend ce Application Verifier mis à jour.

Consultez [4,2 éliminer les échecs de Application Verifier](#42-eliminate-application-verifier-failures).

</dd> </dl>

### <a name="additional-information"></a>Informations supplémentaires

<dl>

[Guide de compatibilité avec Windows 8 et Windows Server 2012](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[Où est le kit SDK DirectX ?](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>Jeux pour Windows

**Résumé des conditions requises pour les jeux**

**Avantages du client**

Les jeux informatiques sont une expérience de divertissement clé sur Windows, mais les préoccupations en matière de facilité d’utilisation ont entraîné une frustration des clients au fil des années. Traditionnellement, les jeux sont installés comme des applications, mais ils sont utilisés plus comme des médias de divertissement (films ou chansons, par exemple). Les innovations, telles que l’Explorateur de jeux, exposent les jeux de manière cohérente et différente des applications standard. Ces innovations donnent également aux Jeux l’état des citoyens de première classe dans Windows, ainsi que la musique et les images. Les exigences suivantes permettent de s’assurer que Windows Vista et Windows 7 offrent une expérience de jeu améliorée, plus accessible et unifiée. En même temps, ils garantissent la compatibilité avec Windows XP.

### <a name="11-games-explorer-integration"></a>Intégration de l’Explorateur de jeux 1,1

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Le jeu doit être visible dans l’Explorateur de jeux (le dossier **Games** ) sur Windows Vista et Windows 7. Lorsque cette option est sélectionnée, le jeu doit également afficher les métadonnées correctes, y compris l’éditeur, le développeur, la date de publication, la version, les scores de l’indice de performance Windows, l’évaluation (le cas échéant) et les liens hypertexte associés.

Si le jeu est distribué numériquement par le biais d’un service de jeu en ligne, le fournisseur de services doit également apparaître dans l’Explorateur de jeux. Pour garantir une gestion correcte du fournisseur et permettre l’utilisation de flux RSS, la version 2 du schéma pour les fichiers de définition de jeu (GDFs) doit être utilisée. (Pour plus d’informations sur GDFs, consultez informations supplémentaires.)

En outre, les programmes d’installation de jeux doivent respecter les règles suivantes lorsqu’ils s’exécutent sur Windows Vista et Windows 7 :

-   L’installation ne doit pas créer de raccourci pour lancer le jeu sur le bureau, dans le menu Démarrer ou dans un autre emplacement.
-   Les tâches et les raccourcis de suppression ne doivent pas être créés.
-   Les utilisateurs doivent pouvoir supprimer le jeu à l’aide de programmes et fonctionnalités dans le panneau de configuration de Windows Vista et Windows 7, ou ajouter ou supprimer des programmes dans le panneau de configuration de Windows XP.

Sur Windows XP et sur les versions antérieures de Windows, le programme d’installation de Game est libre de créer des groupes de programmes, des icônes de bureau ou des raccourcis en fonction des besoins.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

L’Explorateur de jeux Windows est similaire au concept des dossiers Windows XP **Mes documents** ou **Mes images**. L’idée est de centraliser le contenu similaire dans un même emplacement et de faciliter l’organisation et les activités contextuelles. L’Explorateur de jeux étend le concept **Mes documents** ou **Mes images** en permettant une organisation et un contrôle plus riches des jeux. L’Explorateur de jeux permet aux joueurs de visualiser, d’organiser et d’interagir avec tous les jeux installés sur leurs systèmes. Il permet également aux éditeurs de jeux de communiquer plus efficacement des informations de jeu importantes. Le système est piloté par les données, ce qui permet à un éditeur de jeux de mettre facilement à jour les informations de jeu au cours de la durée de vie du produit.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

L’intégration avec l’Explorateur de jeux requiert la création d’un fichier de définition de jeu (GDF), qui est un fichier texte XML incorporé dans un fichier binaire (fichier exécutable ou DLL) en tant que ressource, ainsi qu’une icône Windows. Le jeu doit ensuite être inscrit auprès de l’Explorateur de jeux. Le GDF active également l’exposition d’informations fournies telles que le titre du jeu, le serveur de publication, le développeur, les liens vers les sites Web et les tâches facultatives. Notez que les tâches de support ne peuvent être que des liens vers des sites Web, mais les tâches de lecture peuvent également être utilisées pour des tâches de support facultatives.

L’Explorateur de jeux peut utiliser une image bitmap miniature, mais il est recommandé, à la place, de fournir une ressource icône Windows avec de grandes icônes (256 256). La ressource icône doit inclure des tailles d’image 256 256 48 48, 32 32 et 16 16 dans les profondeurs de couleurs 24 bits (True Color) et 8 bits (256). L’éditeur d’icône fourni dans Visual Studio 2008 et 2010 prend en charge ces formats d’icône de grande taille, comme c’est le cas pour IconWorkshop Lite.

Des informations détaillées sur l’intégration de à **Windows Games Explorer** sont fournies dans le kit de développement logiciel (SDK) DirectX. Le kit de développement logiciel (SDK) DirectX inclut un éditeur de fichier de définition de jeu (GDF), ainsi qu’un exemple de GDF inclus dans GDFExampleBinary, un exemple. Un autre exemple, GameUxInstallHelper, fournit des routines pour intégrer les fonctionnalités requises dans les systèmes d’installation existants. Le validateur du fichier de définition de jeu (gdftrace.exe) fournit une prise en charge du débogage pour l’évaluation d’un GDF. Consultez également « intégration de l’Explorateur Windows Games » dans la documentation du kit de développement logiciel (SDK) DirectX pour C++.

Windows 7 introduit la prise en charge de la deuxième version d’un schéma pour les fichiers GDF. La nouvelle version comprend une méthode simplifiée pour la création de tâches de lecture et la prise en charge des notifications de mise à jour, des fournisseurs de services de jeu, des statistiques de jeux et des flux RSS pour les fournisseurs de services de jeu. La dernière version de GameUxInstallHelper gère l’ensemble de l’inscription et la prise en charge héritée nécessaires à l’utilisation d’un fichier GDF version 2 avec Windows Vista. Utilisez les outils et l’exemple de code du kit de développement logiciel (SDK) DirectX à partir du 2009 août ou d’une version ultérieure. Il est recommandé d’utiliser un fichier GDF version 2 pour activer la prise en charge des flux RSS, des statistiques de jeu et des notifications de mise à jour. Consultez également les exemples ProviderGDFExampleBinary et GameStatisticsExample.

Sur Windows Vista Professionnel, Windows 7 professionnel et édition entreprise de Windows Vista et Windows 7, le lien jeux dans le menu Démarrer est masqué. L’Explorateur de jeux est toujours disponible dans le menu démarrer en cliquant sur **tous les programmes**, puis sur **jeux**.

Pour les applications associées qui sont installées avec votre jeu, mais pas les jeux, vous êtes libre de créer des groupes de programmes, des raccourcis et des icônes de bureau sur toutes les versions de Windows, y compris Windows Vista et Windows 7. Ces applications associées doivent passer les jeux applicables pour les besoins de Windows ; Pour plus d’informations, consultez [instructions pour les produits de middleware de jeux](#guidelines-for-game-middleware-products). Game services est encouragé à s’inscrire auprès de Games Explorer en tant que fournisseur de jeux pour Windows 7. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1,2 prise en charge de la protection parentale/contrôle parental

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les jeux doivent prendre entièrement en charge la sécurité des familles Windows en adhérant aux règles suivantes :

-   Les jeux ne doivent pas exiger que l’utilisateur dispose d’informations d’identification d’administration pour jouer. L’installation, la mise à jour corrective et la suppression peuvent nécessiter des informations d’identification d’administration, conformément aux exigences de la section 3. (En ce qui concerne la condition 2,1, suivez les instructions relatives au contrôle de compte d’utilisateur.)
-   Les jeux évalués par des panneaux d’évaluation pris en charge par Windows, tels que ESRB et PEGI, doivent inclure les informations d’évaluation qui leur sont attribuées dans leur fichier de définition de jeu (GDF). Toutes les données de contrôle d’accès disponibles doivent être incluses dans chaque version localisée de GDF, ainsi que dans la version indépendante de la langue.
-   Les jeux doivent répertorier leurs exécutables dans GDF pour fournir une bonne expérience utilisateur pour les restrictions d’application générales, sauf si le jeu utilise une technologie anti-piratage qui crée des exécutables nommés de manière aléatoire au moment de l’exécution.
-   Les jeux doivent appeler la méthode **VerifyAccess** de l’interface de l’Explorateur de jeux pendant le démarrage, s’ils sont disponibles, et se terminer s’ils renvoient la \* valeur false à pfHasAccess.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Tous les jeux doivent s’exécuter dans le contexte d’un compte d’utilisateur standard pour autoriser les comptes contrôlés par Windows parental Controls à jouer au jeu. Les parents veulent pouvoir surveiller et contrôler l’accès de leurs enfants aux jeux. En outre, de nombreux groupes industriels, gouvernementaux et de défense souhaitent obtenir de meilleures méthodes pour permettre aux parents de surveiller et de contrôler les jeux auxquels leurs enfants sont exposés. Conjointement avec l’architecture offerte par l’Explorateur de jeux, Microsoft fournit aux parents cette possibilité via les contrôles parentaux Windows.

Même pour les jeux qui ne participent pas à un programme de grille de contrôle d’accès, la nécessité de disposer de privilèges élevés crée une expérience de lecture médiocre pour la majorité des comptes d’utilisateur. C’est particulièrement le cas si les contrôles parentaux sont activés, ce qui obligerait le parent à entrer le mot de passe de l’administrateur chaque fois que le jeu est lancé.

Le système de contrôle parental Windows permet aux parents de sélectionner les évaluations qu’ils estiment être appropriées pour leurs enfants. Les contrôles parentaux prennent en charge un grand nombre des systèmes de classement internationaux. Le contrôle parental permet également aux parents de restreindre l’accès aux Jeux en fonction des descripteurs de contenu (si le système d’évaluation applicable les prend en charge) et d’autoriser ou d’interdire l’accès à des jeux individuels.

Le choix par défaut du système d’évaluation pour les contrôles parentaux Windows est basé sur les paramètres régionaux du système, mais il peut être modifié par l’utilisateur dans **Options régionales et linguistiques** dans le **panneau de configuration**. Par conséquent, chaque langue prise en charge doit fournir toutes les données de contrôle d’accès disponibles afin que l’utilisateur soit libre de sélectionner le panneau de classification qu’il souhaite.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Les jeux sans évaluation doivent toujours répondre aux conditions requises pour prendre en charge la lecture en tant qu’utilisateur standard et appeler **VerifyAccess**. Par défaut, ces jeux ont la catégorie non évaluée, affichent le texte « aucune évaluation fournie » dans l’Explorateur de jeux et sont soumis au paramètre **restrictions de jeu** dans **contrôle parental** pour les jeux non classés. Le paramètre des **restrictions** par défaut est autoriser.

Les informations d’évaluation dans GDF seront ignorées si le binaire contenant n’est pas correctement signé avec Authenticode. Voir la condition 2,3.

L’éditeur de fichier de définition de jeu dans le kit de développement logiciel (SDK) DirectX comprend tous les systèmes de classification pris en charge et réplique correctement ces informations dans toutes les versions localisées de GDF, ainsi qu’une version indépendante de la langue. L’outil GDFTrace décodera et vérifiera toutes les informations de contrôle d’accès présentes. Utilisez la version du 2009 août ou une version ultérieure de ces outils.

Le fournisseur GDF pour un fournisseur de jeux ne contient généralement pas d’informations d’évaluation et il est soumis aux paramètres de contenu non évalué.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Système d'exploitation</th>
<th>Systèmes d’évaluation pris en charge</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><ul>
<li>CERO (Japon)</li>
<li>ESRB (ÉTATS-UNIS)</li>
<li>OFLC (Australie)</li>
<li>PEGI (Europe)</li>
<li>PEGI Finlande (déconseillé)</li>
<li>PEGI Portugal</li>
<li>PEGI/BBFC (Royaume-Uni)</li>
<li>USK (Allemagne)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista avec un Service Pack</td>
<td>Les service packs pour Windows Vista ajoutent la prise en charge des éléments suivants :<br/>
<ul>
<li>GRB (Corée du Sud)</li>
<li>&quot;Descripteurs de contenu de variant léger ESRB &quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows 7</td>
<td>Windows 7 prend en charge les systèmes de contrôle d’accès pris en charge par Windows Vista et ajoute la prise en charge des éléments suivants : <br/>
<ul>
<li>CSRR (Taïwan)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 8</td>
<td>Windows 8 prend en charge les systèmes de contrôle d’accès précédents et ajoute la prise en charge des éléments suivants :<br/>
<ul>
<li>Fin-au (Australie)</li>
<li>DJCTQ (Brésil)</li>
<li>PFB (Afrique du Sud)</li>
<li>OFLC-NZ (Nouvelle-Zélande)</li>
</ul>
Windows 8 prend en charge les systèmes suivants, désormais dépréciés :<br/>
<ul>
<li>PEGI-FI (Finlande)</li>
<li>OFLC (Australie)</li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Tout titre incluant de nouveaux descripteurs de contenu ESRB Windows Vista Service Pack 1 (SP1) s’affichera comme étant non évalué sur Windows Vista sans Service Pack.

 

Les données de classification plus récentes sont ignorées sur les versions des systèmes d’exploitation sans prise en charge. La variante PEGI (Finlande) est désormais dépréciée au profit du système d’évaluation standard PEGI (Europe). Le système OFLC est désormais déconseillé en faveur de la fin au-dessus de l’Australie.

Pour plus d’informations sur la mise à disposition d’un jeu avec des privilèges d’utilisateur standard, consultez l’article DirectX [contrôle de compte d’utilisateur pour les développeurs de jeux](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

Consultez la spécification 1,1 pour plus d’informations sur le fichier de définition de jeu (GDF).

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1,3 prendre en charge des jeux enregistrés enrichis

\[Cette exigence a été supprimée\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 prendre en charge la configuration conditionnelle du contrôleur commun Xbox 360 pour Windows \[\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les jeux qui prennent en charge les contrôleurs de manette doivent prendre en charge le contrôleur Xbox 360 pour Windows à l’aide de l’API [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) . Si les périphériques DirectInput sont également pris en charge, DirectInput peut également être utilisé. Toutefois, XInput doit être l’API par défaut si un appareil compatible Xbox 360 est utilisé.

Toutes les références aux déclencheurs et aux boutons du contrôleur commun doivent utiliser les noms Xbox 360. Pour plus d’informations, consultez la liste [terminologique du contrôleur commun Xbox 360 pour Windows](#xbox-360-common-controller-for-windows-terminology) .

Les vibrations du contrôleur doivent être désactivées lorsque le jeu est dans un état suspendu ou suspendu.

Le contrôle de souris/clavier ne peut pas être entièrement désactivé à tout moment. Au minimum, une option permettant de revenir à des menus de jeu doit être disponible.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Cette exigence offre aux joueurs la liberté de choisir d’utiliser le contrôleur Xbox 360 ou le clavier et la souris, en fonction de la méthode d’entrée qui est plus naturelle et intuitive.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Cette exigence ne s’applique pas aux jeux qui utilisent uniquement la souris et/ou le clavier.

Nous vous recommandons d’implémenter la navigation dans les menus pour utiliser les boutons de contrôleur standard largement acceptés :

-   A-accepter
-   B-annuler
-   Démarrer-accepter ou suspendre
-   Back-Cancel, précédent un écran ou un niveau de menu

Pour plus d’informations, consultez [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).

La rubrique [XInput et DirectInput](/windows/desktop/xinput/xinput-and-directinput) aborde les problèmes liés à l’utilisation des deux API en même temps.

Il est recommandé de ne pas utiliser DirectInput pour implémenter des contrôles du clavier ou de la souris. Les contrôles de clavier et de souris doivent uniquement être implémentés à l’aide de messages Windows et d’API Win32. Pour plus d’informations sur l’obtention d’informations de déplacement de souris haute résolution sans utiliser DirectInput, consultez [tirer parti de High-Definition mouvement de la souris](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement).

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1,5 prendre en charge plusieurs proportions et résolutions

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Le jeu doit prendre en charge au moins les proportions et les résolutions d’écran associées suivantes :

-   4:3 normal (800 600 ou 1024 768)
-   écran large 16:9 (1280 720)
-   16:10 grand écran (1152 720 ou 1680 1050 ou 800 480)

Pour la configuration et la détection de la résolution d’écran, le jeu doit respecter les règles suivantes :

-   Le jeu utilise la résolution du Bureau du périphérique d’affichage par défaut s’il s’agit d’une résolution prise en charge. Les proportions du Bureau doivent être utilisées comme critère de recherche si le jeu choisit une autre résolution par défaut.
-   Le jeu doit inviter l’utilisateur à confirmer les nouveaux paramètres d’affichage lorsqu’une modification est apportée. Si l’utilisateur n’accepte pas dans les 15 secondes, l’affichage doit revenir au paramètre précédent.
-   Le jeu ne doit pas étirer les pixels ou centrer une fenêtre de rendu 4:3 pour prendre en charge les proportions panoramiques. Toutefois, cadre est acceptable.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Avec le Bureau de Windows 3D, il est impossible de supposer un proportions ou une résolution en raison des facteurs suivants :

-   Prise en charge des affichages de détails élevés.
-   Augmentation de la part de marché des moniteurs panoramiques.
-   Déploiements HDTV pour Windows Media Center.
-   Exigences d’accessibilité.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Dans l’idéal, le jeu est défini par défaut sur les proportions natives de l’affichage. Toutefois, l’obtention de ces informations peut être un défi, de sorte qu’une solution plus générale peut supposer que le bureau fonctionne aux proportions natives. La résolution du Bureau peut être obtenue en appelant [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) avec les \_ paramètres de Registre enum \_ .

Pour plus d’informations, consultez les sections proportions et grand écran de l’article DirectX [Présentation de l’expérience de 10 mètres pour les développeurs de jeux Windows](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>Lancement de la prise en charge 1,6 à partir de Windows Media Center

\[Cette exigence a été supprimée.\]

### <a name="17-direct3d-support"></a>Support Direct3D 1,7

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Si le jeu utilise Direct3D, la version minimale prise en charge doit être Direct3D 9, et Direct3D doit être le convertisseur par défaut sélectionné.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

L’architecture graphique principale de Windows Vista et Windows 7 est conçue autour de Direct3D. Direct3D 8 et versions antérieures sont pris en charge par le remappage des interfaces héritées.

L’utilisation de versions de Direct3D plus récentes que Direct3D 9 est vivement encouragée. Consultez les jeux pour Windows Showcase S. 1. L’obligation d’exiger Direct3D 10 ou Direct3D 11 est entièrement conforme à la condition 1,7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1,8 activer la prise en charge des résolutions élevées

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les jeux et leurs programmes d’installation doivent s’exécuter correctement sans problèmes visuels lorsque la mise à l’échelle DPI (points par pouce) est activée (testée avec 144 PPP pour une mise à l’échelle de 150% à la résolution d’écran de 1600 1200) sur Windows Vista et Windows 7.

En général, l’exécutable du jeu est requis pour déclarer la prise en charge DPI. Pour ce faire, incorporez un élément de manifeste : <dpiAware> true <dpiAware> .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les moniteurs LCD de haute qualité sont courants en tant qu’écrans d’ordinateur, et ils sont plus performants lorsqu’ils sont dirigés vers leurs résolutions natives (généralement 1280 1024, 1600 1200, etc.). Les clients qui ont des difficultés à lire le texte et à voir les images à cette résolution définissent souvent leurs ordinateurs de bureau à une résolution inférieure et souffrent d’artefacts visuels de la mise à l’échelle de l’écran LCD. Au lieu de cela, les clients peuvent conserver la résolution à la taille native et modifier la résolution de l’affichage des fenêtres, ce qui rend l’apparence des éléments et du texte plus grande sans sacrifier la qualité de l’image.

Bien que cette fonctionnalité soit disponible dans certains formulaires depuis Windows XP, elle est rarement activée par les clients ou par les fabricants d’ordinateurs OEM. Plus de la moitié de tous les affichages d’ordinateurs actuels sont définis sur une résolution inférieure à la résolution native du moniteur, en fonction des commentaires des clients. Windows 7 rend cette fonctionnalité plus visible pour les clients lors de l’installation initiale et lors de la modification des paramètres d’affichage, en les encourageant à utiliser la mise à l’échelle DPI plutôt que de modifier la résolution du bureau.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

La fonction [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) peut être utilisée à la place, si elle est appelée tôt dans le code de démarrage du processus. L’ajout au manifeste est préférable, pour s’assurer qu’il n’existe aucune condition de concurrence critique avec les éléments logiciels (tels que les dll) qui peuvent s’initialiser avant l’appel du point d’entrée principal. Notez que **SetProcessDPIAware** est présent uniquement sur Windows Vista et Windows 7.

L’ajout de l’élément manifeste est facile à faire avec Visual Studio 2005 et 2008. Créez un fichier nommé dpiaware. manifest qui contient le texte suivant :

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

Ensuite, dans Visual Studio, ajoutez dpiware. manifest au projet. Assurez-vous que l' **insertion du manifeste** est définie sur **Oui** dans les propriétés du projet. Notez que les versions antérieures de l’outil Manifest (Mt.exe) génèrent un avertissement parasite avec les éléments de manifeste prenant en charge DPI. Pour résoudre ce point, mettez à jour Mt.exe vers la version la plus récente à partir du SDK Windows.

Visual Studio 2010 comprend un paramètre dans les propriétés du projet, nommé **activer la prise** en compte des PPP, qui élimine la nécessité d’un fichier tel que dpiaware. manifest. Recherchez **activer la reconnaissance dpi** en développant les **Propriétés de configuration** et l' **outil manifeste**, puis en sélectionnant **entrée & sortie**.

Sur Windows, le mode d’affichage traditionnel est par défaut de 96 ppp, ce qui était courant pour les moniteurs CRT.

Tandis que les applications plein écran modifient la résolution d’affichage, elles utilisent souvent des messages de fenêtre et des métriques lors de la configuration des tampons et de l’affichage des rectangles. La virtualisation DPI fait apparaître les modes d’affichage plein écran rognés, et la déclaration de prise en charge DPI empêche ces problèmes. Pour plus d’informations, consultez [écriture d' DPI-Aware applications Win32](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Sécurité et compatibilité

**Résumé des exigences de sécurité et de compatibilité**

**Avantages du client**

Les exigences suivantes améliorent la sécurité globale des jeux et permettent de s’assurer qu’ils fonctionnent avec Windows sur différentes architectures, sous différentes configurations et dans différents modes.

### <a name="21-follow-user-account-control-guidelines"></a>2,1 suivre les instructions relatives au contrôle de compte d’utilisateur

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Chaque fichier exécutable (autrement dit, chaque fichier doté d’une extension .exe) doit contenir un manifeste incorporé qui définit son niveau d’exécution en incluant la balise suivante :

``` syntax
            <requestedExecutionLevel>
```

Par exigence 1,2, le jeu principal et l’exécutable d’exécution automatique doivent avoir le niveau d’exécution asInvoker pour prendre en charge les contextes d’utilisateur standard.

Les fichiers de données utilisateur qui ont des associations de fichiers inscrits avec l' **Explorateur de fichiers** doivent être placés dans un sous-dossier du dossier spécifié par CSIDL \_ Personal (également appelé **documents** ou **Mes documents**). Tous les autres fichiers de données utilisateur doivent être stockés dans un sous-dossier des dossiers spécifiés par CSIDL \_ local \_ AppData ou CSIDL \_ Common \_ AppData. (Ces répertoires sont masqués par défaut pour les utilisateurs individuels et pour tous les utilisateurs.)

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

L’expérience Windows d’un utilisateur est plus sécurisée si les applications s’exécutent uniquement avec les autorisations nécessaires.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Si seules quelques fonctionnalités d’une application requièrent des privilèges d’administrateur (par exemple, une application qui doit configurer un pare-feu), le processus principal de l’application doit toujours être exécuté à l’aide des privilèges d’utilisateur standard. Les fonctionnalités qui requièrent des privilèges d’administrateur doivent être déplacées dans un processus distinct, tel qu’un programme d’installation ou un utilitaire de configuration.

Si les privilèges d’administrateur ne sont pas requis, le fichier XML manifeste incorporé doit inclure les éléments suivants :

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Si des privilèges d’administrateur sont requis, le fichier XML manifeste incorporé doit inclure les éléments suivants :

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Avec Visual Studio 2005, cela est facilement incorporé en ajoutant simplement un fichier manifeste (. manifest) qui contient l’un des blocs précédents au projet, et en veillant à ce que **incorporer le manifeste** soit défini sur **Oui** dans les propriétés du projet pour l’outil manifeste. Pour Visual Studio 2008 et 2010, les propriétés UAC peuvent être définies directement dans les propriétés du projet pour l’éditeur de liens sur la page **fichier manifeste** . Notez que les versions antérieures de l’outil Manifest (Mt.exe) génèrent un avertissement parasite avec les éléments du manifeste UAC. Pour résoudre ce point, mettez à jour Mt.exe vers la version la plus récente à partir du SDK Windows.

Consultez la condition 3,1 pour plus d’informations sur les cas particuliers d’installation, de mise à jour corrective et de suppression.

Les bibliothèques de liens dynamiques (dll) ne nécessitent pas de tels manifestes.

Pour plus d’informations sur le contrôle de compte d’utilisateur, voir [contrôle de compte d’utilisateur pour les développeurs de jeux](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2,2 prendre en charge les versions x64 de Windows

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Pour assurer la compatibilité avec les éditions 64 bits de Windows, les jeux doivent répondre aux exigences suivantes.

-   Les programmes d’installation de titres et de titres ne doivent pas contenir de code 16 bits ou ne s’appuient sur aucun composant 16 bits.
-   Si le jeu dépend des pilotes en mode noyau pour fonctionner, les versions x64 de ces pilotes doivent être disponibles. Le programme d’installation du jeu doit détecter et installer les pilotes et les composants appropriés pour les éditions 64 bits de Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

De nombreux utilisateurs Windows Vista et Windows 7 exécutent des éditions 64 bits du système d’exploitation pendant toute la durée de vie du produit. il est donc essentiel que les applications soient compatibles avec ce système d’exploitation.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Windows sur Windows 64 (WOW64) permet au code 32 bits de s’exécuter sur les éditions 64 bits de Windows. il n’est donc pas nécessaire que l’application soit du code natif 64 sur les éditions 64 bits de Windows. Le code seize bits ne s’exécute pas sur les éditions 64 bits de Windows.

La gestion de la compatibilité avec Windows XP Professionnel Édition x64 n’est pas obligatoire, mais elle est vivement encouragée.

Pour plus d’informations, consultez la page [programmation 64 bits pour les développeurs de jeux](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> </dl>

### <a name="23-sign-files"></a>2,3 fichiers de signature

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Tous les fichiers de code exécutable (en général, les fichiers avec l’extension .exe ou .dll) doivent être signés avec un certificat Authenticode publiquement valide et doivent avoir une URL de serveur d’horodatage valide pour la signature de production.

Si votre jeu utilise Windows Installer, les fichiers du package d’installation (fichiers .msi) doivent être signés.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

La signature d’un fichier aide les utilisateurs à décider s’il faut faire confiance à une application et s’assurer que les fichiers n’ont pas été falsifiés. Il permet également aux applications de s’exécuter correctement dans les environnements verrouillés.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Pour plus d’informations, consultez [signature Authenticode pour les développeurs de jeux](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Si votre jeu utilise Windows Installer, nous vous recommandons d’activer la mise à jour corrective UAC/LUA, en incluant une table MsiPatchCertificate. Pour plus d’informations, consultez Mise à [jour corrective du contrôle de compte d’utilisateur](/windows/desktop/Msi/user-account-control--uac--patching).

Nous ne recommandons pas la signature des fichiers Cabinet (.cab), sauf s’ils sont relativement petits (moins de 100 Mo).

</dd> </dl>

### <a name="24-sign-drivers"></a>2,4 signer les pilotes

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Tout pilote en mode noyau installé par le jeu doit être signé avec un certificat Authenticode publiquement valide.

Tout pilote de périphérique en mode noyau installé par le jeu doit avoir une signature Microsoft, qui peut être obtenue à partir du laboratoire WHQL (Windows Hardware Quality Labs) ou du programme DRS (Driver FIABILITE signature).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les pilotes mal écrits ou malveillants peuvent gravement affecter la stabilité et la sécurité d’un système. Sur les éditions 64 bits de Windows Vista et Windows 7, les pilotes non signés ne sont pas chargés. Cette stratégie peut également être activée pour les éditions 32 bits de Windows Vista et Windows 7.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Les versions natives 32 bits et 64 bits de tous les pilotes en mode noyau sont nécessaires par exigence 2,2.

Vous trouverez plus d’informations sur les programmes de signature de pilotes Microsoft sur le [portail des développeurs de matériel Windows](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2,5 effectuer la vérification de version appropriée

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les jeux ne peuvent pas s’exécuter sur les systèmes d’exploitation ultérieurs, comme indiqué par les modifications apportées au numéro de version de Windows, sauf si le contrat de licence utilisateur final interdit l’utilisation sur les systèmes d’exploitation ultérieurs. Si le jeu est supposé échouer, il doit le faire normalement en affichant un message approprié à l’utilisateur.

Si les contrôles de version de Windows sont effectués, les API de vérification de version ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) ou [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) doivent être utilisées pour vérifier la version du système d’exploitation. Les clés de registre ne doivent pas être lues pour déterminer la version.

Les vérifications de version explicite pour le runtime DirectX ne doivent pas être présentes dans le jeu. Ces contrôles de version ne doivent pas être présents dans l’installation qui lance le programme d’installation de DirectX Runtime (DirectSetup).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Lorsque les utilisateurs Windows mettre à niveau leurs systèmes d’exploitation, ils ne doivent pas être bloqués pour jouer à des jeux actuels simplement parce que le numéro de version de Windows a augmenté. Les contrôleurs de version mal écrits continuent à créer des problèmes pour les logiciels qui, dans le cas contraire, fonctionnent correctement sur les versions plus récentes de Windows ou simplement avec l’ajout d’un Service Pack Windows.

La logique de comparaison de contrôle de version fragile pour le runtime DirectX a créé de nombreuses installations ayant échoué lorsqu’elle est exécutée sur des versions différentes de Windows. Le numéro de version de DirectX s’applique uniquement aux composants centraux du système d’exploitation. Elle ne s’applique pas aux composants du kit de développement logiciel (SDK) DirectX côte à côte qui sont utilisés par de nombreux jeux.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Il est assez courant de voir les programmes d’installation de vérifier une version minimale du système d’exploitation. Cette vérification doit toutefois être effectuée avec soin pour s’assurer qu’elle teste une valeur supérieure ou égale à, plutôt qu’une égalité simple, ce qui permet de verrouiller une version spécifique du système d’exploitation. L’utilisation du test **HighVersionLie** de Application Verifier est un moyen simple et rapide de déterminer la façon dont votre programme d’installation réagira à une modification importante du numéro de version du système d’exploitation.

L’utilisation correcte du package de redistribution du runtime DirectX (programme d’installation de DirectX) implique toujours son lancement lors de l’installation, de préférence en mode silencieux. Cela permet au code fourni par Microsoft d’effectuer toutes les mises à jour de version requises. Il permet également l’installation de tous les composants facultatifs du kit de développement logiciel (SDK) DirectX côte à côte, tels que D3DX, XACT, MDX ou XInput.

Pour connaître les meilleures pratiques de déploiement du runtime DirectX, consultez [installation de DirectX pour les développeurs de jeux](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

Il est recommandé que les jeux qui prennent en charge Windows XP vérifient un niveau de Service Pack supérieur ou égal à 2, car le Service Pack 2 (SP2) et le Service Pack 3 (SP3) apportent des améliorations significatives en matière de sécurité, un impératif de redistribution du runtime DirectX simplifié et un déploiement extrêmement large. La plupart des technologies Microsoft modernes qui prennent en charge Windows XP requièrent SP2 ou SP3 (XAudio2, Games for Windows-LIVE, etc.).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2,6 prendre en charge les sessions utilisateur simultanées

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les jeux qui reposent sur des graphiques 3D ne sont pas requis pour travailler sur une connexion Bureau à distance, mais l’utilisateur doit recevoir une alerte en cas d’échec du jeu.

Les jeux doivent prendre en charge les scénarios multitâches Windows standard en adhérant aux règles suivantes :

-   Les jeux ne doivent pas bloquer l’utilisation simultanée de sessions utilisateur.
-   Un jeu doit s’exécuter dans une nouvelle session utilisateur lorsqu’il est déjà en cours d’exécution dans une autre session.
-   Le son du jeu dans une session utilisateur ne doit pas être entendu lorsqu’un autre utilisateur est actif dans une autre session.
-   Les jeux doivent prendre en charge le changement rapide d’utilisateur.
-   Les jeux ne doivent pas essayer de désactiver le basculement de tâche standard. Les jeux ne doivent pas désactiver le raccourci clavier ALT + TAB. Les jeux sont autorisés à désactiver les raccourcis clavier d’accessibilité, comme décrit dans la rubrique [désactivation des touches de raccourci dans les jeux](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les utilisateurs Windows doivent être en mesure d’exécuter des sessions simultanées sans conflit ou perturbation. Il s’agit d’un scénario courant pour un ordinateur Windows qui est partagé par une famille, Roommates ou d’autres.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Pour tester si le jeu est lancé dans une session à distance, appelez [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ REMOTESESSION). Une valeur différente de zéro indique que la session est distante.

Pour plus d’informations, consultez [changement rapide d’utilisateur](/windows-hardware/drivers/display/fast-user-switching). Notez que le changement rapide d’utilisateur se produit si des restrictions de temps de contrôle parental sont activées lorsque l’heure de l’utilisateur est écoulée. Pour plus d’informations, consultez la spécification 1,2.

</dd> </dl>

### <a name="27-support-long-names"></a>2,7 prendre en charge les noms longs

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Si un jeu prend en charge l’enregistrement de fichiers, il doit être en mesure d’enregistrer des fichiers avec des noms et des chemins d’accès longs. Le jeu doit gérer correctement les caractères spéciaux du système de fichiers, tels que \\ / : \* ? « < >, dans les champs d’entrée utilisateur utilisés pour créer des noms de fichiers ou des chemins d’accès.

Les jeux doivent fonctionner correctement lorsqu’un utilisateur a un nom d’utilisateur long.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les joueurs sont habitués à utiliser des noms longs sur des chemins d’accès profonds qui sont pris en charge par le système d’exploitation sous-jacent.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Les noms longs sont définis comme étant ceux qui contiennent les valeurs maximales définies dans la SDK Windows.

</dd> </dl>

## <a name="installation"></a>Installation

**Résumé des exigences de sécurité et de compatibilité**

**Avantages du client**

Les clients peuvent être assurés que les applications seront installées sur Windows sans dégrader le système d’exploitation ou d’autres applications si les applications utilisent les méthodes de distribution des composants système officiels. Une expérience d’installation rationalisée fournit une expérience out-of-Box plus accessible et sans problème pour les jeux.

### <a name="31-support-easy-installation"></a>Installation facile du support 3,1

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les jeux doivent fournir un chemin simplifié dans l’interface utilisateur du programme d’installation en implémentant les éléments suivants :

-   Affichez au maximum une invite de CLUF.
-   Le chemin d’installation par défaut doit contourner toutes les sélections pour l’installation (telles que les sélections du dossier d’installation ou du composant), prendre les sélections par défaut, puis exécuter le jeu ou le lanceur une fois l’installation réussie, sans invites supplémentaires. Si vous le souhaitez, vous pouvez fournir une option d’installation personnalisée pour les options de configuration avancées.
-   Installez les composants du système d’exploitation requis (tels que les runtimes DirectX et Visual C) à l’aide des packages de redistribution Microsoft appropriés. L’installation doit être effectuée en mode silencieux, sans invite et sans être protégée par des vérifications de version de composant.
-   Fournissez la suppression via **programmes et fonctionnalités** dans le **panneau de configuration** pour l’application de jeu et les fichiers de travail générés. Une option permettant de supprimer tous les fichiers de données créés par l’utilisateur est recommandée. Le processus de suppression doit garantir que tous les fichiers installés sont supprimés et que tous les paramètres (par exemple, entrées de la liste des exceptions du pare-feu et clés de registre) sont effacés. Les composants du système d’exploitation redistribué ne doivent pas être supprimés.
-   Si le jeu requiert l’ajout d’exceptions au pare-feu Windows, le processus d’installation peut inviter à informer les utilisateurs que cette modification est nécessaire. Cette invite doit apparaître avant le début de l’installation.

L’installation et la suppression peuvent nécessiter des droits d’administration. L’application de correctifs peut nécessiter une demande d’informations d’identification administratives, en fonction de la fréquence de mise à jour. La lecture normale du jeu ne doit pas nécessiter de droits d’administration, par exigence 2,1 suivre les instructions relatives au contrôle de compte d’utilisateur.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Facile à installer, il s’agit d’une philosophie de développement de jeux centrée sur Windows, conçue pour simplifier et rationaliser le processus parfois fastidieux et confus d’installation de jeux sur les ordinateurs qui exécutent des systèmes d’exploitation Windows. L’installation facile est activée en utilisant un ensemble de technologies et de meilleures pratiques qui réduisent la complexité inutile et les risques d’installation de jeux sur les ordinateurs Windows.

Les principaux objectifs sont les suivants :

-   Réduisez le temps nécessaire pour participer au jeu et commencez à jouer.
-   Réduisez le nombre de boîtes de dialogue et de choix à très peu, voire aucun, afin de simplifier l’installation du jeu.

Certaines installations traditionnelles ont des invites qui autorisent les installations non fonctionnelles, même si l’application semble être correctement installée. Par exemple, un jeu peut demander à un utilisateur d’accepter un CLUF. Le jeu est ensuite installé, puis le CLUF DirectX s’affiche. Ce CLUF permet aux utilisateurs de refuser et, par conséquent, d’ignorer l’installation du runtime DirectX. Ce scénario peut entraîner l’échec de l’exécution d’un jeu en raison de composants manquants.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Pour plus d’informations sur l’installation de jeux, les techniques d’installation de jeux non traditionnelles, les solutions de mise à jour correctives compatibles avec le contrôle de compte utilisateur et la gestion des correctifs fréquents, consultez les articles suivants sur DirectX :

-   [Simplification de l’installation du jeu](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Installation à la demande pour les jeux](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [Mise à jour corrective des logiciels de jeu dans Windows XP, Windows Vista et Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Meilleures pratiques pour l’installation de jeux en ligne massivement multijoueurs](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> La suppression de fichiers de données générés spécifiques à l’utilisateur ne doit être effectuée que pour l’utilisateur actuel et pour les emplacements d’utilisateurs partagés communs. Il n’existe aucun moyen fiable d’analyser le système pour supprimer des fichiers spécifiques à l’utilisateur pour d’autres utilisateurs, même si la suppression nécessite des informations d’identification d’administration.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3,2 prendre en charge le contrôle de compte d’utilisateur pour l’installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Le programme d’installation du jeu ne doit pas supposer qu’il s’exécute dans le même contexte que l’utilisateur. Les emplacements spécifiques à l’utilisateur sont différents du programme d’installation et du lecteur même pour les systèmes à utilisateur unique en raison de l’élévation des informations d’identification de l’administrateur. Par conséquent, lorsqu’un jeu s’exécute pour la première fois, il doit effectuer des tâches spécifiques à l’utilisateur, indépendamment du processus d’installation.

La boîte de dialogue exception du pare-feu Windows ne doit pas s’afficher lorsqu’un utilisateur héberge ou rejoint un jeu multijoueur. Toutes les configurations requises doivent être effectuées au moment de l’installation. Les instructions d’installation doivent informer l’utilisateur que cette opération aura lieu dans le cadre de l’installation.

Le programme d’installation de jeu doit fournir un manifeste incorporé qui désigne le niveau d’exécution requis, par exigence 2,1 suivre les instructions relatives au contrôle de compte d’utilisateur.

Si le jeu est lancé par le programme d’installation une fois l’installation terminée, il doit être lancé dans le contexte de l’utilisateur d’origine.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

L’une des modifications les plus importantes apportées au système d’exploitation Windows dans Windows Vista est l’ajout du contrôle de compte d’utilisateur (UAC), qui exécute des applications avec des privilèges réduits par défaut. Par conséquent, les programmes d’installation doivent gérer les niveaux de privilège en conséquence. Windows 7 utilise également beaucoup le contrôle de compte d’utilisateur. Bien que Windows 7 améliore l’expérience utilisateur du contrôle de compte d’utilisateur, les programmes d’installation doivent toujours répondre aux mêmes exigences que sur Windows Vista pour fonctionner correctement, sans recourir à un comportement de virtualisation potentiellement confus.

Le contrôle de compte d’utilisateur est actif par défaut sur Windows Vista et Windows 7, et la grande majorité des clients (88% ou plus, en fonction des commentaires) laissent cette fonctionnalité activée.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Pour plus d’informations sur la configuration du pare-feu Windows, consultez l’article DirectX [pare-feu Windows pour les développeurs de jeux](/windows/desktop/DxTechArts/games-and-firewalls) et l’exemple FirewallInstallHelper.

Le lancement standard du jeu à la fin du processus d’installation ne répond pas au dernier aspect de cette exigence si l’installation est lancée par un utilisateur standard et si le processus d’installation requiert des privilèges d’administrateur (autrement dit, vous invite à entrer des informations d’identification d’administrateur). Il hérite également des privilèges d’administrateur, ce qui constitue un risque potentiel pour la sécurité. Au lieu de cela, un chargeur de démarrage de l’installation doit lancer le jeu après avoir retourné un appel du programme d’installation réussi. Pour plus d’informations, consultez l’article de MSDN Magazine [pour apprendre à vos applications à jouer avec le contrôle de compte d’utilisateur Windows Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3,3 installer pour corriger les dossiers

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les jeux installés pour tous les utilisateurs doivent être installés par défaut dans le dossier Program Files. Les données utilisateur doivent être écrites lors de la première exécution du jeu, et non lors de l’installation.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les utilisateurs doivent avoir la possibilité d’installer des applications là où ils en ont besoin. Ils doivent également disposer d’une expérience cohérente et sécurisée avec l’emplacement par défaut des fichiers.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Les jeux peuvent utiliser les différents emplacements de dossiers connus (tels que ceux spécifiés par CSIDL \_ local \_ AppData et CSIDL \_ Common \_ AppData) pour stocker des quantités significatives de données de jeu et prendre en charge les fichiers exécutables pour implémenter des scénarios d’installation avancée à la demande et de mise à jour corrective.

Étant donné que l’installation peut nécessiter une élévation vers un autre compte d’utilisateur pendant le processus d’installation de tous les utilisateurs, il n’existe pas d’emplacement utilisateur correct dans lequel stocker des données au moment de l’installation. En outre, si le chiffrement de fichier est activé, les fichiers chiffrés sont accessibles uniquement par le compte d’utilisateur qui les a créés.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3,4 Installation des ressources Windows correctement

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les applications ne doivent pas tenter d’installer des fichiers ou des clés de Registre protégés par Protection des ressources Windows (WRP). Si l’application requiert des versions plus récentes des composants système, elle doit mettre à jour ces composants à l’aide d’un service pack Microsoft ou d’un package d’installation approuvé par Microsoft qui contient le composant système. Les composants système ne doivent jamais être reconditionnés.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Protection des ressources Windows (WRP) est conçu pour s’assurer que les ressources système protégées ne sont mises à jour qu’à l’aide de mécanismes d’installation ou de mise à jour approuvés par Microsoft. WRP améliore la fiabilité du système en s’assurant que les résultats d’une installation sont prévisibles.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

WRP est le successeur de la protection des fichiers Windows, qui protège la majorité des composants système installés dans le dossier Windows. WRP protège la plupart des clés de Registre qui stockent les paramètres de création d’objets COM. Il réserve également certains dossiers pour une utilisation exclusive par le système d’exploitation. Les tentatives d’accès aux ressources protégées entraînent généralement une erreur de refus d’accès.

Pour plus d’informations sur les meilleures pratiques lorsque le runtime DirectX est déployé avec un jeu, consultez l’article DirectX DirectX [installation for Game Developers](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3,5 éviter les redémarrages au cours de l’installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Le programme d’installation de jeu ne doit pas supposer que l’installation de composants Windows à partir de packages de redistribution nécessite un redémarrage, sauf si le redémarrage est indiqué par un résultat de retour ou par la documentation de Microsoft.

Si le programme d’installation de jeu force toujours un redémarrage, celui-ci doit être approuvé par Microsoft.

Les boîtes de dialogue de fichiers en cours d’utilisation incluses dans Windows Installer packages doivent contenir une option pour fermer automatiquement les applications et tenter de les redémarrer une fois l’installation terminée.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Le redémarrage du système après une installation est une interruption inopportune pour les utilisateurs et n’est généralement pas nécessaire.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Pour plus d’informations, consultez [utilisation de Windows Installer avec le gestionnaire de redémarrage](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3,6 utiliser le contrôle de version de fichier correctement

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Le programme d’installation du jeu doit vérifier correctement si les dernières versions de fichiers sont installées. L’installation d’un jeu ne doit jamais régresser les fichiers que vous ne générez pas ou qui sont partagés par des applications que vous ne générez pas.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les composants partagés et les composants système sont souvent mis à jour pour les correctifs de sécurité et les fonctionnalités étendues. Une installation qui comprend une version antérieure des composants mis à jour ne doit pas entraîner la perte des mises à jour et des correctifs qui ont déjà été appliqués.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3,7 prise en charge de l’exigence conditionnelle d’exécution automatique \[\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Pour les jeux distribués sur CD, DVD ou tout autre support amovible qui prennent en charge l’exécution automatique, lorsque le disque est inséré pour la première fois, l’application doit automatiquement exécuter ou inviter l’utilisateur à installer le jeu, sauf si l’utilisateur a désactivé la fonctionnalité d’exécution automatique.

Une fois l’application installée, une nouvelle insertion du disque dans le lecteur ne doit pas entraîner le redémarrage automatique de l’installation. Il est acceptable de demander aux utilisateurs s’ils souhaitent mettre à jour ou modifier leurs choix d’installation.

L’application d’exécution automatique ne doit pas demander d’élévation (c’est-à-dire qu’elle doit avoir Invoke dans le manifeste, par exigence 2,1, bien qu’elle puisse lancer le programme d’installation ou un autre utilitaire qui requiert des droits d’administration. L’élévation doit se produire uniquement si le jeu n’est pas installé, ou si l’utilisateur le sélectionne spécifiquement.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

L’exécution automatique simplifie l’utilisation d’applications distribuées par le média, telles que les jeux qui nécessitent généralement que le disque soit présent dans le lecteur pour jouer au jeu.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Il n’est pas possible de demander à l’utilisateur de naviguer dans l’Explorateur de fichiers pour lancer l’installation à partir du CD ou du DVD.

Pour les jeux distribués sur plusieurs disques, les disques suivants devraient idéalement utiliser la fonctionnalité d’exécution automatique ou poursuivre l’installation sans inviter l’utilisateur à appuyer sur une touche ou à effectuer une autre action.

Lors de la création d’un programme d’exécution automatique, vérifiez que tous les composants requis sont présents sur les nouvelles installations de Windows. Les applications classiques s’appuient sur les technologies installées par le programme d’installation, mais l’exécution automatique elle-même est exécutée avant toute installation de ce type. Un exemple courant est l’échec des programmes d’exécution automatique, car les dll du runtime Visual C n’ont pas été incluses dans le cadre de l’installation de Windows. Le programme d’exécution automatique doit donc utiliser le déploiement CRT local de l’application ou lier le CRT de manière statique.

Les programmes d’exécution automatique écrits pour une utilisation sur des versions de Windows antérieures à Windows Vista ne doivent pas utiliser le Runtime .NET, car cette technologie n’est pas fournie avec Windows XP ou des versions antérieures de Windows. Windows Server 2003 et Windows Vista sont les premières versions de Windows à inclure le Runtime .NET dans le cadre de leur système d’exploitation.

Pour des raisons similaires, les programmes d’exécution automatique ne peuvent pas exiger la présence de composants côte à côte facultatifs du kit de développement logiciel (SDK) DirectX, tels que D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT et MDX 1,1.

Pour obtenir un exemple d’utilisation de l’exécution automatique, consultez exemple d’exécution automatique.

</dd> </dl>

## <a name="reliability"></a>Fiabilité

**Résumé des exigences de sécurité et de compatibilité**

**Avantages du client**

Ces exigences rendent une application plus fiable en minimisant le nombre de blocages, de blocages et de redémarrages. Les exigences de fiabilité permettent de s’assurer que les logiciels sont plus prévisibles, gérables, résilients et récupérables.

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 éliminer les redémarrages inutiles

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Tous les programmes d’installation de l’application doivent tirer parti des API du gestionnaire de redémarrage pour éviter les redémarrages du système (voir la condition 3,5).

Les jeux ne doivent pas bloquer l’arrêt.

Toutes les applications doivent répondre au gestionnaire de redémarrage en écoutant et en répondant aux messages d’arrêt suivants :

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ QUERYENDSESSION avec LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Les applications GUI doivent répondre (TRUE) immédiatement en vue d’un redémarrage.

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ ENDSESSION avec LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Les applications doivent retourner une valeur 0 dans les 5 secondes, puis fermer.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL + C 
</dt> <dd>

Les applications console qui reçoivent ce message doivent être immédiatement fermées.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les redémarrages du système sont une interruption majeure. Ils conduisent à une expérience utilisateur incorrecte et doivent être réduits. Certaines opérations, telles que les mises à jour système critiques, peuvent nécessiter des redémarrages. En écoutant les messages d’arrêt, le jeu et les autres applications peuvent réagir rapidement aux demandes du gestionnaire de redémarrage. De cette façon, ils peuvent éviter des retards inutilement dans les demandes de redémarrage valides.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Si un programme d’installation de jeu utilise la technologie de Windows Installer (MSI) sans aucune action personnalisée, cette fonctionnalité est fournie automatiquement. Les packages de redistribution Microsoft prennent également en charge le gestionnaire de redémarrage.

Pour plus d’informations sur le gestionnaire de redémarrage, consultez l’article MSDN [sur le gestionnaire de redémarrage](/windows/desktop/RstMgr/about-restart-manager).

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4,2 éliminer les échecs de Application Verifier

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Le jeu ne doit générer aucun échec s’exécutant sous Microsoft Application Verifier (AppVerifier), version 4,0 ou ultérieure, dans les tests suivants :

-   Concepts de base : handles, tas, verrous, mémoire, TLS
-   Divers : DangerousAPIs, DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

AppVerifier teste de nombreux problèmes connus qui provoquent des blocages et des blocages dans les applications Windows, ainsi que des failles de sécurité connues.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Pour plus d’informations sur Application Verifier, consultez [Application Verifier](/previous-versions/ms220948(v=vs.80)) et [utilisation de Application Verifier dans le cycle de vie du développement de logiciels](/previous-versions/aa480483(v=msdn.10)) sur MSDN. Vous pouvez télécharger Application Verifier à partir des [Détails du téléchargement : Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) sur le centre de téléchargement Microsoft.

Cette exigence ne s’applique pas aux applications managées pures sans Interop native.

Ces tests doivent être exécutés sur une version Release. Les builds de débogage peuvent générer des échecs erronés. Certaines technologies anti-piratage et anti-fraude peuvent perturber l’exécution d’AppVerifier. Par conséquent, ces tests doivent être effectués sans que les technologies anti-piratage et anti-fraude soient activées.

Il peut être nécessaire d’affecter la valeur FALSe à la propriété Full du test de base : les segments de mémoire, car le système d’exploitation complet augmente considérablement la sollicitation de la mémoire de l’application en cours d’exécution. Les échecs sont toujours détectés, mais ils peuvent être plus difficiles à repérer si vous utilisez uniquement des PageHeap partiels.

Si vous utilisez les tests UAC/LUA dans Application Verifier pour respecter les exigences de contrôle de compte utilisateur 2,1 et 3,2, vous devez utiliser l' [analyseur d’utilisateurs standard](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) pour passer en revue les résultats. Il existe également de nombreux autres tests utiles fournis par Application Verifier que vous avez fortement encouragés à utiliser dans le développement et les tests pour garantir un niveau élevé de compatibilité avec les versions actuelles et futures de Windows. Le test **HighVersionLie** est utilisé pour vérifier la conformité avec la condition 2,5.

Visual Studio Team System comprend un sous-ensemble de la fonctionnalité AppVerifier intégrée à l’environnement de débogage. Cela peut s’avérer utile pour le suivi et la résolution des problèmes avec les concepts de base : segments de mémoire, Handles et verrous.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4,3 prise en charge des Rapport d’erreurs Windows et des informations de version de fichier

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Pour activer la prise en charge des Rapport d’erreurs Windows, les jeux doivent remplir les conditions suivantes :

-   Les jeux doivent gérer uniquement les exceptions connues et attendues. Rapport d’erreurs Windows ne doit pas être désactivé. Si une erreur telle qu’une violation d’accès apparaît dans un jeu, elle doit autoriser Rapport d’erreurs Windows à signaler l’incident.
-   Tous les fichiers exécutables (par exemple, les fichiers .exe ou les dll) doivent contenir un nom de produit, un nom de société et une version de fichier précis.
-   La sortie normale du jeu ne doit pas aboutir à une erreur d’exception inconnue.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les API Rapport d’erreurs Windows fournissent des commentaires essentiels à Microsoft pour détecter les blocages et les blocages étendus dans les applications. Cela permet à Microsoft et à ses partenaires de détecter et de résoudre rapidement les problèmes liés au système et aux pilotes qui entraînent des défaillances de l’application rapidement.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Les jeux peuvent inclure des gestionnaires d’exceptions personnalisés non gérés pour effectuer une prise en charge personnalisée et des fonctionnalités de création de rapports, mais ils doivent transmettre une erreur aux fonctions **ReportFault** ou **WerReportSubmit** .

Les informations de version de fichier appropriées peuvent être vérifiées en affichant les propriétés du fichier dans l’interface utilisateur du bureau Windows et en vérifiant la page de propriétés version.

Pour plus d’informations sur les API de Rapport d’erreurs Windows et sur l’analyse des vidages sur incident qui sont générés lorsque vous utilisez ce service, consultez l’article DirectX [analyse du vidage sur incident](/windows/desktop/DxTechArts/crash-dump-analysis).

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>Contrôleur commun Xbox 360 pour terminologie Windows



| Nom                                          | Description                                                                                                 |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| Un                                        | Bouton A.                                                                                     |
| B                                        | Bouton B.                                                                                     |
| RETOUR                                     | Bouton Retour.                                                                                  |
| (vers la droite/gauche) du pare-chocs                      | Bouton situé en haut à droite et à gauche du contrôleur. Équivalent à un bouton épaule.    |
| pavé directionnel                          | Pavé directionnel du contrôleur.                                                                   |
| Pavé D                                    | Abréviation acceptée du pavé directionnel.                                                         |
| DP                                       | Abréviation du pavé directionnel et étiquette du contrôleur.                                                |
| RB, LB                                   | Abréviations droite et gauche des abréviations et des étiquettes de contrôleur.                                        |
| RS, LS                                   | Abréviations et étiquettes de contrôleur du stick droit et gauche.                                         |
| RT, LT                                   | Abréviations et étiquettes de contrôleur de déclencheur de droite et de gauche.                                       |
| RSB, LSB                                 | Abréviations et étiquettes de contrôleur du stick droit et gauche.                                         |
| ÉCRAN D’ACCUEIL                                    | Bouton Démarrer.                                                                                 |
| (droite/gauche) Stick                       | Le stick du contrôleur. Ancien joystick.                                                       |
| bouton Stick (droite/gauche)                | Bouton du Stick Controller. Bouton précédent joystick.                                         |
| déclencheur (droit/gauche)                     | Déclencheur du contrôleur.                                                                          |
| Vibration                                | Commentaires de jeu générés par le moteur du contrôleur. N’utilisez pas Rumble.                           |
| X                                        | Bouton X.                                                                                     |
| Y                                        | Bouton Y.                                                                                     |
| Contrôleur Xbox 360 pour Windows          | Le boîtier de commande Xbox 360 vendu en tant que référence de matériel PC, y compris un disque de pilote de périphérique Windows.          |
| Contrôleur sans fil Xbox 360 pour Windows | Le boîtier sans fil Xbox 360 vendu en tant que référence de matériel PC, y compris un disque de pilote de périphérique Windows. |



 

## <a name="guidelines-for-game-middleware-products"></a>Instructions pour les produits middleware de jeux

### <a name="introduction"></a>Introduction

Pour que les jeux soient éligibles au programme Games for Windows, ils doivent remplir une liste de spécifications techniques. Tous les composants tiers livrés avec un titre (fichiers exécutables, dll, pilotes, etc.) doivent également respecter ces exigences pour que le jeu soit éligible. Ce document met en évidence les exigences les plus courantes qui doivent également être respectées par les composants tiers pour que le jeu réussisse les tests de conformité. Les programmes d’installation et les packages de production/moteurs de production doivent consulter le document jeux complets pour les exigences techniques de Windows, car la plupart de ces exigences sont affectées par ces outils.

### <a name="additional-recommendations"></a>Autres recommandations

Au-delà de la garantie que votre composant prend en charge la création de titres conformes à la configuration requise pour les jeux pour Windows, vous devez prendre en compte un certain nombre d’autres éléments à prendre en compte lors de la conception et du déploiement d’une bibliothèque ou d’un utilitaire de prise en charge pour un jeu Windows.

-   Pour prendre en charge les développeurs qui travaillent sur des applications x64 natives 64 bits, fournissez des versions natives 32 bits et 64 bits de vos bibliothèques. La version 32 bits doit être compatible avec 64 bits par 2,2. Les bibliothèques pour les applications 32 bits ne doivent pas supposer que le bit supérieur d’une adresse de 32 bits est inutilisé pour prendre en charge l’utilisation dans les applications LARGEADDRESSAWARE x86.
-   Si vous fournissez des en-têtes de code natif (C/C++), utilisez la syntaxe d’attribut du langage d’annotation standard (SAL) pour décorer vos routines d’API publiques. Cela permettra aux utilisateurs de votre bibliothèque d’acquérir l’avantage maximal de l’utilisation de l’analyse statique du code (/analyze), qui fait partie de Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium et Visual Studio 2010 Ultimate, ainsi que des outils de compilateur SDK Windows disponibles au public.
-   Si votre produit crée des threads dans le processus de l’utilisateur, veillez à nommer chaque thread afin que les outils de débogage puissent annoter correctement les threads en cours d’exécution.
-   Si vous écrivez des routines destinées à être appelées dans la boucle principale d’un jeu, utilisez les routines D3DX D3DPERF \_ BeginEvent/EndEvent et D3DPERF \_ SetMarker pour annoter des opérations de haut niveau afin d’identifier plus facilement les goulots d’étranglement à l’aide de pix pour Windows.
    > [!Note]  
    > Pour la fonctionnalité Graphics Diagnostics de Visual Studio 2012, ces routines D3DX et PIX sont remplacées par l’interface [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) .

     

-   Pour les bibliothèques de mise en réseau, fournissez des implémentations IP neutres et évitez les routines IPv4 uniquement déconseillées pour prendre en charge les technologies IPv6 et Teredo dans Windows XP avec Service Pack 2, Windows Vista et Windows 7.
-   Les fournisseurs de services de jeu doivent s’inscrire auprès de l’Explorateur de jeux à l’aide de la version 2 du schéma GDF et utiliser la fonctionnalité RSS pour fournir des informations relatives aux services.

### <a name="games-for-windows-showcases"></a>Jeux pour les vitrines Windows

### <a name="introduction"></a>Introduction

Les jeux pour les vitrines Windows vont au-delà de la fourniture d’une expérience de jeu solide sur les PC Windows. En implémentant ces fonctionnalités, les jeux peuvent améliorer l’expérience utilisateur sur les plateformes Windows les plus récentes.

Les jeux pour les titres Windows doivent satisfaire à toutes les exigences techniques répertoriées dans cet article, mais les fonctionnalités de présentation sont facultatives. Ces titres sont libres d’implémenter certains, aucun ou l’ensemble de ces démonstrations.

### <a name="s1-exploit-direct3d-11"></a>S. 1 exploiter Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Direct3D 11 est l’API de rendu nouvelle génération pour Windows Vista et Windows 7. Les jeux qui exploitent Direct3D 11 utilisent du contenu optimisé, des techniques de rendu avancées et de nouvelles fonctionnalités matérielles pour créer une expérience attrayante sur le matériel qui prend en charge 10, 10,1 et 11.

Si le jeu implémente également Direct3D 9, une comparaison côte à côte doit démontrer une amélioration perceptible de la qualité du contenu, de la fidélité visuelle, des performances, de la complexité des scènes et d’autres zones de fidélité des graphiques pour Direct3D 11. Cette prise en charge est soumise aux jeux pour la condition technique 1,7 de Windows.

La technologie Direct3D 10level9 peut être utilisée pour prendre en charge le matériel vidéo de classe de nuanceur 2.0/3.0 Direct3D 9-Class sur Windows Vista et Windows 7, au lieu d’utiliser une implémentation Direct3D 9 côte à côte pour une prise en charge matérielle étendue. Toutefois, cela n’est pas suffisant pour illustrer cette démonstration.

Sur les ordinateurs exécutant Windows Vista ou Windows 7 avec Direct3D 11 installé, le jeu doit utiliser Direct3D 11 par défaut.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

L’API Direct3D 11 repose sur l’infrastructure WDDM (Windows Display Driver Model) et Direct3D 10,1 pour prendre en charge de nouvelles fonctionnalités : la polygonalisation matérielle, les nuanceurs de calcul, le rendu multithread et la création de ressources, de nouveaux formats de compression de texture et un langage de nuanceur plus flexible. Direct3D 11 offre une prise en charge matérielle unifiée des cartes vidéo modernes, y compris la dernière version de Direct3D 11, toutes les cartes vidéo Direct3D 10 et 10,1, ainsi que de nombreuses cartes vidéo de nuanceur modèle 2.0/3.0 Direct3D 9, qui est le matériel vidéo minimal requis pour le bureau Aero 3D.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

La migration d’un moteur de rendu Direct3D 9 pour utiliser la nouvelle interface Direct3D 11 est une tâche bien définie :

-   Éliminez toutes les opérations à fonction fixe en faveur des nuanceurs programmables.
-   Mettez à jour tous les nuanceurs existants avec la nouvelle syntaxe de Shader Model 4. x/5.
-   Mettez à jour la gestion des ressources pour prendre en charge le nouveau modèle de vue.
-   Convertissez toutes les ressources pour utiliser une nouvelle liste de formats disponibles.
-   Mettez à jour la gestion de l’état de rendu pour utiliser des blocs d’État immuables et retravaillez les constantes de nuanceur dans des mémoires tampons constantes.

Cette conversion est essentielle pour activer la démonstration Direct3D 11, bien que le résultat ne réponde pas à l’exigence de présentation de l’exploitation de la nouvelle API.

La nouvelle API et le modèle de programmation HLSL associé offrent de nombreuses opportunités pour le contenu amélioré :

-   Tirer parti des fonctionnalités matérielles Direct3D 10 existantes, telles que les nuanceurs de géométrie, les flux sortants, les tableaux de textures et les formats de texture compressés textures BC4/BC5.
-   Tirer parti des fonctionnalités matérielles Direct3D 10,1 existantes, telles que les modes de fusion indépendants par rendu cible, la profondeur MSAA Read, l’accès aux nuanceurs par exemple MSAA, les tableaux de mappage de cube et le rendu aux formats compressés par bloc (BC).
-   Implémentation des algorithmes GPU avancés à l’aide du nuanceur de calcul avec CS4. x sur les cartes vidéo Direct3D 10/10.1 existantes (mises à jour des pilotes vidéo) ou CS 5,0 sur les cartes vidéo Direct3D 11 de nouvelle génération.
-   Rendu sur plusieurs threads à l’aide de la création de ressources à threads libres et de plusieurs contextes de périphérique pour améliorer les performances sur les systèmes multicœurs (avec des pilotes vidéo mis à jour). Pour plus d’informations, consultez les jeux pour Windows Showcase S. 3.
-   Grâce aux nouvelles fonctionnalités du matériel vidéo de classe Direct3D 11, telles que le pavage de matériel avec les nuanceurs de la coque et du domaine, le matériel de nuanceur HLSL 5,0 est doté de formats de texture compressés BC6HBC7 et de la liaison de nuanceur dynamique.

Les techniques qui peuvent être implémentées avec Direct3D 9 (en grande partie via un coût d’UC élevé) peuvent être désactivées de manière efficace sur le GPU, ce qui permet de libérer des ressources processeur pour prendre en charge d’autres demandes de jeux.

Les API Direct3D 11, les outils de prise en charge et les exemples sont disponibles dans le kit de développement logiciel (SDK) DirectX. Consultez également API graphiques dans Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S. 2 exploiter x64 natif

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Le jeu comprend un exécutable natif 64 bits qui offre une nouvelle expérience attrayante activée par les éditions x64 de Windows s’exécutant sur du matériel compatible x64. Une comparaison côte à côte avec la version 32 bits du jeu doit montrer une amélioration perceptible de la complexité du contenu, une réduction des temps de chargement globaux et des performances.

Sur les éditions 64 bits de Windows, l’installation doit toujours configurer la version native 64 bits du jeu comme valeur par défaut pour les raccourcis de l’Explorateur de jeux et Windows XP Professionnel Édition x64. Si vous souhaitez une installation double, une tâche de lecture supplémentaire peut être spécifiée pour l’Explorateur de jeux sur Windows Vista et Windows 7 qui pointe vers la version 32 bits, mais la version native de 64 bits doit rester la valeur par défaut.

Notez que le jeu doit prendre en charge les éditions 64 bits de Windows Vista et Windows 7 pour répondre à cette recommandation de vitrine. La prise en charge de Windows XP Professionnel Édition x64 est encouragée, mais pas obligatoire.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

la technologie x64 offre des fonctionnalités d’adressage 64 bits pour les marchés des clients et des serveurs qui incluent une compatibilité descendante de 32 bits à pleine vitesse pour les applications existantes. x64 est un élément clé de la feuille de route pour AMD (AMD64) et Intel (EMT64), et, à l’exception des processeurs ultra-mobiles, prennent en charge la technologie pour tous les processeurs actuels et futurs.

Windows XP Professionnel Édition x64 était le premier système d’exploitation Windows orienté client pour la prise en charge de la technologie x64, et Windows Vista et Windows 7 étendaient beaucoup la disponibilité de l’activation du système d’exploitation pour l’informatique grand public 64 bits. Avec 2 Go de RAM comme standard sur de nombreux nouveaux ordinateurs, les améliorations apportées à la mise à l’échelle de la mémoire ne sont pas bénéfiques pour les applications 32 bits qui ne peuvent pas gérer plus de 2 Go de RAM physique. De nombreux jeux sont confrontés à des défis de l’ensemble des contenus disponibles dans les contraintes de 2 Go d’espace d’adressage virtuel, en particulier lorsqu’ils sont combinés avec les grandes mémoires vidéo disponibles sur les GPU haut de gamme, et le passage à la technologie x64 augmente considérablement les niveaux de détail pris en charge.

compatibilité x64 pour les jeux 32 bits est un jeu pour Windows Technical Requirement (2,2), mais tirer pleinement parti des nouvelles technologies requiert une implémentation native de 64 bits.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

L’avantage principal de l’adressage 64 bits est la possibilité d’accéder directement à plus de 2 Go de mémoire physique et virtuelle. L’espace d’adressage de mémoire virtuelle de grande taille permet une utilisation intensive des e/s mappées en mémoire sans vous soucier des problèmes d’épuisement de l’espace d’adressage de la machine virtuelle, ce qui est courant dans la programmation 32 bits. Les jeux peuvent tirer parti du nouvel espace pour améliorer de façon considérable les temps de chargement ou, dans certains cas, pour éliminer les pauses de chargement du contenu.

Les applications 32 bits existantes peuvent tirer parti des éditions x64 en ayant la possibilité de traiter des adresses avec des données 32 bits complètes lorsqu’elles sont créées avec l’option d’éditeur de liens d’activation des adresses volumineuses (**/LARGEADDRESSAWARE**). Sur les versions 32 bits de Windows XP, les modes de démarrage spéciaux permettaient à ces applications d’adresser jusqu’à 3 Go de RAM, et les éditions x64 offrent un accès pouvant atteindre 4 Go de RAM pour les applications de prise en charge d’adresses importantes (LAA). Tandis que l’utilisation d’une adresse LAA dans une application 32 bits ne répond pas à cette exigence de vitrine, cette technologie de pont est un moyen extrêmement utile de fournir des avantages supplémentaires de mise à l’échelle sur les versions x64 de Windows pour ceux qui n’implémentent pas pleinement cette exigence de vitrine.

Pour plus d’informations, consultez la page [programmation 64 bits pour les développeurs de jeux](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) et la [RAM, VRAM et davantage de RAM : les jeux 64 bits sont](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) disponibles dans Gamasutra.

> [!Note]  
> L’un des principaux défis de cette démonstration est de vous assurer que les bibliothèques ou les composants tiers sur lesquels repose votre jeu sont disponibles pour le développement natif 64 bits. De nombreuses API Microsoft héritées ont également été éliminées de l’environnement natif 64 bits, ce qui peut prouver un défi pour les bases de code du moteur qui contiennent des implémentations plus anciennes des systèmes clés.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S. 3 exploitation des processeurs Many-Core

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Le jeu implémente des fonctionnalités qui tirent parti de processeurs multicœurs, avec une mise à l’échelle de 3, 4 ou plus de cœurs, le cas échéant.

Si le jeu prend en charge les systèmes à processeur unique ou à double cœur, une comparaison côte à côte avec un système à quatre cœurs doit démontrer de nouvelles fonctionnalités perceptibles, des effets intéressants supplémentaires, une amélioration de la qualité du contenu et/ou des performances améliorées.

Étant donné que la mise à l’échelle à double cœur est déjà largement prise en charge par les jeux, et qu’elle est automatiquement utilisée par diverses améliorations du pilote Direct3D, la mise à l’échelle à double cœur n’est pas suffisante pour démontrer cette démonstration.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

La croissance continue des performances pour les processeurs a basculé de l’amélioration du taux d’horloge à l’ajout de cœurs de calcul. Les feuilles de route AMD et Intel sont basées sur des conceptions multicœurs évolutives. Toutes les plateformes de jeux de nouvelle génération ont des processeurs multicœurs, en raison de ce changement fondamental dans l’évolution des processeurs. Les applications à thread unique ne voient plus les gains significatifs des processeurs de nouvelle génération. La mise à l’échelle du nombre de cœurs de PROCESSEURs en mode d’utilisation commun ne peut pas dépasser au moins trois.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Notez que les nombres de cœurs n’ont pas besoin d’être une puissance de deux. les jeux doivent donc être mis à l’échelle de façon linéaire et gérer les nombres de cœurs de 3, 4, 5, 6, 7, 8, etc.

La mise à l’échelle en augmentant le nombre de threads dans une application fournit un retour uniquement si le coût de la communication et de la synchronisation des threads est conservé. La mise à l’échelle basée sur les fonctionnalités peut s’avérer une solution plus facile à terme, ce qui permet au jeu de fonctionner normalement sans les threads supplémentaires sur les systèmes à cœur unique et de les activer lorsque l’alimentation supplémentaire de l’UC est disponible.

Pour plus d’informations, consultez [codage de plusieurs cœurs sur xbox 360 et Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) et [Considérations sur la programmation avec blocage pour Xbox 360 et Microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) dans les articles DirectX, ainsi que l’utilitaire DXUTLockFreePipe et l’exemple CoreDetection.

L’utilisation de la création de ressources à thread libre de Direct3D 11 et des contextes d’appareil est utile pour obtenir une évolutivité à plusieurs cœurs dans le rendu et le chargement des ressources graphiques. Consultez les jeux pour Windows Showcase S. 1.

Notez que l’utilisation directe de l’instruction de processeur RDTSC, au lieu d’utiliser des API Windows pour calculer la synchronisation sur des systèmes multicœurs, peut entraîner des problèmes sur certaines configurations matérielles et de système d’exploitation. consultez [minutage des jeux et processeurs multicœurs](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) dans les articles DirectX.

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S. 4 jeux de support pour Windows LIVE

Les jeux pour Windows LIVE ne sont plus pris en charge par Microsoft.

### <a name="s5-support-windows-touch"></a>S. 5 prendre en charge Windows Touch

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les jeux avec fonctions tactiles Windows peuvent être lus à l’aide de fonctions tactiles et/ou de gestes sur les ordinateurs exécutant Windows 7 avec un affichage tactile. L’entrée au clavier peut également être utilisée, mais l’interface de lecture principale doit être basée sur les fonctions tactiles.

L’activation de Touch ne doit pas empêcher l’utilisation de la souris ou du contrôleur commun, sous réserve de l’exigence technique 1,4.

Le programme d’installation du jeu n’est pas censé prendre en charge la fonctionnalité tactile Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les affichages compatibles multipoint pour les ordinateurs sont disponibles pour les ordinateurs portables et les ordinateurs de bureau. ils représentent une fonctionnalité matérielle clé qui est promue avec la version de Windows 7. Windows 7 prend en charge l’interaction tactile Windows sur tout le bureau et les interfaces de contrôles communs.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Les applications en code natif peuvent accéder aux messages tactiles à l’aide des \_ messages WM Touch, en combinaison avec la fonction [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) . Voir aussi les manipulations et l’API d’inertie.

Windows Presentation Foundation (WPF) 4,0 fournit une solution gérée pour les interfaces multipoint.

Pour plus d’informations, consultez le kit de développement logiciel (SDK) Windows Touch.

</dd> </dl>

### <a name="s6-support-high-color"></a>S. 6 prend en charge la haute couleur

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Occupation**
</dt> <dd>

Les jeux qui prennent en charge High Color utilisent un format 10:10:10:2 (DXGI \_ format \_ R10G10B10A2, D3DFMT \_ A2B10G10R10) ou 16:16:16:16 (dxgi \_ format R16G16B16A16, D3DFMT \_ \_ A16B16G16R16) pour le rendu de la mémoire tampon en arrière-plan et le mode d’affichage plein écran.

En utilisant une cible de rendu de couleur élevée, le contenu de la plage de High-Dynamic (HDR) peut être rendu avec une gamme étendue ou étendue lors de l’exécution du mappage de tonalités sur une plage de 10 bits ou 16 bits.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Raisonnement**
</dt> <dd>

Les moniteurs peuvent afficher plus de 256 niveaux de couleur par canal depuis de nombreuses années, même lorsque les affichages CRT étaient répandus. Le matériel d’analyse sur les cartes vidéo a été le facteur de limitation. Les GPU modernes, y compris la plupart des matériels de classe Direct3D 9 et tout le matériel Direct3D 10 et de plus en plus, disposent de matériel de numérisation compatible avec au moins 10 bits par canal, et la fonctionnalité matérielle est définie pour s’étendre à 16 bits par canal de couleur à l’avenir. Les systèmes d’interconnexion TV HD (HDMI, DisplayPort) ont été conçus pour gérer plus de 8 bits par canal et le format VGA analogique contiendra déjà ces signaux.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informations supplémentaires**
</dt> <dd>

Notez que la couleur haute, ou haute couleur, fait référence au passage de l’affichage des couleurs 256 (8 bits) aux affichages de couleurs 15 ou 16 bits. La plupart des systèmes d’affichage ont une longueur telle qu’elle a été déplacée sur une couleur de 24 bits, ou 8 bits par canal de couleur pour les couleurs rouge, vert et bleu. Par couleur élevée ici, nous entendons une nouvelle génération de systèmes qui peuvent fonctionner avec plus de 8 bits par canal de couleur individuel. Est également appelé « couleur profonde ».

</dd> </dl>

### <a name="recommended-best-practices"></a>Bonnes pratiques recommandées

### <a name="introduction"></a>Introduction

En plus de répondre aux exigences techniques et d’adopter une ou plusieurs démonstrations dans votre titre, il existe un certain nombre de pratiques recommandées qui doivent être suivies pour tous les jeux Windows. Bien que ces recommandations soient en dehors de l’étendue des exigences techniques de base, il est vivement recommandé de les utiliser pour tous les jeux pour les titres Windows.

### <a name="additional-recommendations"></a>Autres recommandations

-   Utilisez le compilateur et le runtime Visual Studio les plus récents. Les versions plus récentes du compilateur implémentent des améliorations significatives pour la qualité du code généré et pour les problèmes de sécurité, et elles utilisent des stratégies d’optimisation de processeur modernes. La mise à jour du compilateur et de l’utilisation du runtime C le plus récent est un moyen simple de migrer vers des pratiques de codage modernes.
-   Utilisez la version de bibliothèque de liens dynamiques (DLL) du runtime C, plutôt que la liaison statique, et utilisez le CRT sécurisé. (Des exceptions peuvent être faites dans des cas de préinstallation spéciaux, comme pour un programme d’exécution automatique ou pour le programme d’installation proprement dit).
-   Pour le jeu audio, utilisez XAudio2, X3DAudio et/ou XACT, plutôt que DirectSound. Utilisez DirectSound sur Windows XP (uniquement) et WASAPI sur Windows Vista et Windows 7 pour les moteurs audio qui effectuent toutes les conversions et la conversion de la vitesse source et n’ont besoin que d’une solution à faible latence pour la sortie audio.
-   Évitez d’utiliser des API héritées et déconseillées : DirectDraw, DirectSound, DirectPlay, couche de performances de DirectMusic, DirectPlay Voice et le mode de rétention Direct3D. Notez que DirectPlay Voice et le mode de rétention Direct3D ne sont pas disponibles sur Windows Vista ou Windows 7. La couche de performances de DirectPlay et de DirectMusic n’est pas disponible pour les applications x64 natives.
-   Optimisez à l’aide de jeux d’instructions SSE/SSE2 SIMD. Consultez l’API [DirectXMath](/windows/desktop/dxmath/directxmath-portal) dans le SDK Windows en tant que solution multiplateforme pour les opérations mathématiques optimisées pour SIMD.
-   Utilisez les meilleures pratiques modernes pour la sécurité Windows (y compris les options du compilateur et de l’éditeur de liens telles que **/NXCOMPAT**, **/GS**, **/SAFESEH**, **/DynamicBase**, **/SDL**, etc.). Pour plus d’informations, consultez [meilleures pratiques en matière de sécurité dans le développement de jeux](/windows/desktop/DxTechArts/best-security-practices-in-game-development).
-   Utilisez les derniers composants et bibliothèques de SDK Windows. Supprimer les dépendances sur les composants hors bande DirectSetup déployés, tels que D3DX9, D3DX10 et D3DX11. Envisagez d’utiliser [DirectXTex](https://github.com/Microsoft/DirectXTex) ou [DirectXTK](https://github.com/Microsoft/DirectXTK) , ou les deux.
-   Évitez d’utiliser l’ancien compilateur HLSL et utilisez à la place le compilateur HLSL moderne. Si la prise en charge du nuanceur de pixels 1. x est requise par votre application, utilisez l’assembly de nuanceur plutôt que le HLSL, ou limitez l’utilisation de l’ancien compilateur à ces scénarios uniquement.

## <a name="resources"></a>Ressources



| Terme                                                                                                                                                                                                                         | Description                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Jeux pour Windows : cas de test <br/>                              | Meilleures pratiques pour les jeux sur Windows XP, Windows Vista et Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>SDK Windows <br/>                                                                                                      | [Kits de développement logiciel Windows](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Instructions relatives au contrôle de compte d’utilisateur <br/>                      | [Exigences de développement d’applications Windows Vista pour la compatibilité du contrôle de compte d’utilisateur](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portail des développeurs WinQual <br/>                                                  | [Windows Quality Online Services (winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>Portail des développeurs DirectX <br/>                                                  | [Centre de développement DirectX](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog sur les jeux pour Windows et DirectX SDK<br/> | [Jeux pour Windows et kit de développement logiciel (SDK) DirectX](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Autres articles DirectX<br/>                                             | [Articles techniques sur DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

