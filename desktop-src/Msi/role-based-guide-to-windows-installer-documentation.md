---
description: Windows Le programme d’installation est la solution recommandée pour l’installation et la configuration d’applications sur Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Guide basé sur les rôles pour Windows Installer la Documentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f886050f3bb0256f6f0f993e613be940cee9cd2fe748b2d17b5dc0f0f84a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625861"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>Guide basé sur les rôles pour Windows Installer la Documentation

Windows Le programme d’installation est la solution recommandée pour l’installation et la configuration d’applications sur Windows. Par conséquent, certaines des informations contenues dans ce kit de développement logiciel (SDK) présentent un intérêt pour un large éventail de développeurs de logiciels et de professionnels de l’informatique. Cette section est fournie à titre de guide pour les lecteurs qui préfèrent voir des liens vers des rubriques organisées par rôle professionnel et les scénarios de tâches courantes. Étant donné que les rôles peuvent varier d’une organisation à l’autre, le regroupement suivant doit être considéré comme un guide d’un emplacement pour commencer à rechercher les informations dont vous avez besoin.

-   [Développeurs d’applications](#application-developers)
-   [Auteurs d’installation](#setup-authors)
-   [Professionnels de l’informatique](#it-professionals)
-   [Développeurs d’infrastructure](#infrastructure-developers)

cette documentation est destinée aux développeurs de logiciels qui souhaitent créer des applications qui utilisent Windows Installer. En tant que principale source de documentation de référence pour le programme d’installation, le kit de développement logiciel (SDK) fournit des informations sur les packages d’installation et le service d’installation. Elle contient des descriptions complètes de l’interface de programmation d’applications (API) et des éléments de la base de données du programme d’installation.

pour plus d’informations, consultez [autres Sources d’informations sur les Windows Installer](other-sources-of-windows-installer-information.md).

## <a name="application-developers"></a>Développeurs d’applications

les développeurs d’applications créent des applications qui appellent l’interface de programmation d’applications Windows Installer et installent des packages d’installation Windows au moment de l’exécution. la Windows Installer peut faire fonctionner dans une application telle que la réparation automatique et l’installation à la demande. En règle générale, les développeurs d’applications effectuent les opérations suivantes :

-   Activer l’installation à la demande des applications au moment de l’exécution à partir d’une autre application.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Utilisation des fonctions de programme d’installation](using-installer-functions.md)
    -   [Référence des fonctions du programme d’installation](installer-function-reference.md)
    -   [Installation à la demande](installation-on-demand.md)
    -   [Gestion des composants](component-management.md)
    -   [Modification des raccourcis du programme d’installation](editing-installer-shortcuts.md)
    -   [**Propriété OLEAdvtSupport**](oleadvtsupport.md)
    -   [Prise en charge des plateformes de la publication](platform-support-of-advertisement.md)

-   Activez la réparation automatique des applications en réinstallant les composants en fonction des besoins au moment de l’exécution.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Utilisation des fonctions de programme d’installation](using-installer-functions.md)
    -   [Référence des fonctions du programme d’installation](installer-function-reference.md)
    -   [Résilience](resiliency.md)
    -   [Résilience source](source-resiliency.md)
    -   [Recherche d’une fonctionnalité ou d’un composant endommagé](searching-for-a-broken-feature-or-component.md)
    -   [Remplacement des fichiers existants](replacing-existing-files.md)

-   Affichez une interface utilisateur pour collecter des informations sur l’utilisateur et des préférences de configuration la première fois qu’une application est installée ou exécutée. l’interface utilisateur doit être ajoutée par l’auteur du programme d’installation du Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Utilisation des fonctions de programme d’installation](using-installer-functions.md)
    -   [Initialisation d’une application](initializing-an-application.md)
    -   [Boîte de dialogue FirstRun](firstrun-dialog.md)
    -   [À propos de l’interface utilisateur](about-the-user-interface.md)

-   Créez des applications qui utilisent un modèle d’indirection pour faire référence aux composants avec des fonctionnalités parallèles. les catégories de composants qualifiés doivent être ajoutées par l’auteur du programme d’installation du Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Composants qualifiés](qualified-components.md)
    -   [Utilisation des composants qualifiés](using-qualified-components.md)

-   Utilisez des assemblys privés et côte à côte pour isoler les applications et réduire les conflits de DLL.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Assemblys](assemblies.md)
    -   [clés de registre de l’assembly écrites par Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [installation d’assemblys Win32 pour le partage côte à côte sur Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [installation d’assemblys Win32 pour l’utilisation privée d’une Application sur Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [Table MsiAssembly](msiassembly-table.md)
    -   [Table MsiAssemblyName](msiassemblyname-table.md)
    -   [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [**Propriété MsiWin32AssemblySupport**](msiwin32assemblysupport.md)
    -   [**Propriété MsiNetAssemblySupport**](msinetassemblysupport.md)
    -   [**Composants isolés**](isolated-components.md)

-   Préparez l’application pour installer ses propres mises à niveau majeures complètes.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Correctifs et mises à niveau](patching-and-upgrades.md)
    -   [Mises à niveau majeures](major-upgrades.md)
    -   [**UpgradeCode, propriété**](upgradecode.md)
    -   [**Utilisation d’un UpgradeCode**](using-an-upgradecode.md)
    -   [Empêcher l’installation d’un ancien package sur une version plus récente](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   Préparez l’application pour installer ses propres mises à niveau mineures, petites mises à jour ou correctifs.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Correctifs et mises à niveau](patching-and-upgrades.md)
    -   [Petites mises à jour](small-updates.md)
    -   [Mises à niveau mineures](minor-upgrades.md)

-   organisez les ressources d’application en composants pouvant fonctionner avec l’Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Windows Composants du programme d’installation](windows-installer-components.md)
    -   [Utilisation des fonctionnalités et des composants](working-with-features-and-components.md)
    -   [Utilisation de composants transitifs](using-transitive-components.md)
    -   [Que se passe-t-il si les règles des composants sont rompues ?](what-happens-if-the-component-rules-are-broken.md)
    -   [Organisation des applications en composants](organizing-applications-into-components.md)
    -   [Composants isolés](isolated-components.md)
    -   [Composants qualifiés](qualified-components.md)

## <a name="setup-authors"></a>Auteurs d’installation

les auteurs du programme d’installation créent des packages de Windows Installer (fichiers .msi) qui contiennent la logique d’installation et les informations nécessaires pour installer une application. ils utilisent généralement des outils de création tels que [Orca.exe](orca-exe.md) pour remplir la base de données Windows Installer avec la logique d’installation et des informations. En règle générale, les auteurs d’installation effectuent les opérations suivantes :

-   déterminer les fonctionnalités disponibles avec différentes versions de Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [détermination de la Version de Windows Installer](determining-the-windows-installer-version.md)
    -   [Versions commercialisées de Windows Installer](released-versions-of-windows-installer.md)
    -   [nouveautés de Windows Installer](what-s-new-in-windows-installer.md)

-   organisez les ressources d’application en composants Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Windows Composants du programme d’installation](windows-installer-components.md)
    -   [Organisation des applications en composants](organizing-applications-into-components.md)
    -   [Modification du code du composant](changing-the-component-code.md)
    -   [Que se passe-t-il si les règles des composants sont rompues ?](what-happens-if-the-component-rules-are-broken.md)
    -   [Windows Exemples de programme d’installation](windows-installer-examples.md)

-   utilisez des outils de création de packages tiers Windows Installer ou des outils du kit de développement logiciel (SDK) tels que [Orca.exe](orca-exe.md) pour remplir une base de données d’installation et créer un package de Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Windows Outils de développement du programme d’installation](windows-installer-development-tools.md)
    -   [Package d’installation, à propos de la base de données du programme d’installation](installation-package.md)
    -   [Windows Extensions de fichier du programme d’installation](windows-installer-file-extensions.md)
    -   [Tables de base de données](database-tables.md)
    -   [Codes de package](package-codes.md)
    -   [Création d’un package volumineux](authoring-a-large-package.md)
    -   [Windows Programme d’installation sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md)
    -   [Attribution d’un nom aux tables, propriétés et actions personnalisées](naming-custom-tables-properties-and-actions.md)
    -   [Limitations OLE sur les Flux](ole-limitations-on-streams.md)
    -   [Format de définition de colonne](column-definition-format.md)
    -   [Réduction de la taille d’un fichier .msi](reducing-the-size-of-an--msi-file.md)

-   créez la base de données Windows Installer pour installer des fichiers.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Groupe de tables principales](core-tables-group.md)
    -   [Groupe de tables de fichiers](file-tables-group.md)
    -   [Table de fichier](file-table.md)
    -   [Recherche de fichiers](file-searching.md)
    -   [Coût des fichiers](file-costing.md)
    -   [Installation du fichier](file-installation.md)
    -   [Fichiers auxiliaires](companion-files.md)
    -   [Règles de contrôle de version des fichiers](file-versioning-rules.md)
    -   [Contrôle de version de fichier par défaut](default-file-versioning.md)
    -   [Remplacement des fichiers existants](replacing-existing-files.md)
    -   [Utilisation d’armoires et de sources compressées](using-cabinets-and-compressed-sources.md)
    -   [Suppression des fichiers bloqués](removing-stranded-files.md)
    -   [Installation des composants permanents, des fichiers, des polices, des clés de Registre](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Table FileSFPCatalog](filesfpcatalog-table.md)
    -   [Recherche d’un fichier et création d’une propriété contenant le chemin d’accès du fichier](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [Recherche d’un répertoire et d’un fichier dans le répertoire](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Windows Exemples de programme d’installation](windows-installer-examples.md)

-   créer une base de données Windows Installer qui installe une structure de répertoires et des dossiers.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Groupe de tables principales](core-tables-group.md)
    -   [Groupe de tables de fichiers](file-tables-group.md)
    -   [Table des composants](component-table.md)
    -   [Table de répertoire](directory-table.md)
    -   [Utilisation de la table Directory](using-the-directory-table.md)
    -   [Utilisation d’une propriété de répertoire dans un chemin d’accès](using-a-directory-property-in-a-path.md)
    -   [Propriétés du dossier système](property-reference.md)
    -   [Table CreateFolder](createfolder-table.md)
    -   [Table LockPermissions](lockpermissions-table.md)
    -   [Table MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [Modification de l’emplacement cible d’un répertoire](changing-the-target-location-for-a-directory.md)
    -   [Windows Exemples de programme d’installation](windows-installer-examples.md)

-   créer une base de données Windows Installer qui installe des clés de registre.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Groupe de tables principales](core-tables-group.md)
    -   [Groupe de tables de Registre](registry-tables-group.md)
    -   [Table du Registre](registry-table.md)
    -   [Modification du Registre](modifying-the-registry.md)
    -   [Ajout ou suppression de clés de registre lors de l’installation ou de la suppression de composants](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [Ajout et suppression d’une application et absence de trace dans le registre](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Installation des composants permanents, des fichiers, des polices, des clés de Registre](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier .ini existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [Recherche d’une entrée de Registre et création d’une propriété contenant la valeur du Registre](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [clés de registre de l’assembly écrites par l’Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Désinstaller la clé de Registre](uninstall-registry-key.md)
    -   [Table SelfReg](selfreg-table.md)
    -   [Spécification de l’ordre d’inscription automatique](specifying-the-order-of-self-registration.md)
    -   [Windows Exemples de programme d’installation](windows-installer-examples.md)

-   créer une base de données Windows Installer qui installe les services.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Table ServiceInstall](serviceinstall-table.md)
    -   [Table ServiceControl](servicecontrol-table.md)
    -   [Table des composants](component-table.md)

-   créer une base de données Windows Installer qui installe des composants isolés ou des composants COM.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Groupe de tables de Registre](registry-tables-group.md)
    -   [Table de classe](class-table.md)
    -   [Table ComPlus](complus-table.md)
    -   [Composants isolés](isolated-components.md)
    -   [Utilisation des composants isolés](using-isolated-components.md)
    -   [Installation de composants isolés](installation-of-isolated-components.md)
    -   [Réinstallation de composants isolés](reinstallation-of-isolated-components.md)
    -   [Suppression de composants isolés](removal-of-isolated-components.md)
    -   [Installation d’un composant COM dans un emplacement privé](installing-a-com-component-to-a-private-location.md)
    -   [Rendre un composant COM dans un package existant privé](make-a-com-component-in-an-existing-package-private.md)
    -   [installation d’une Application COM+ avec la Windows Installer](installing-a-com--application-with-the-windows-installer.md)
    -   [Installation d’un composant non-COM dans un emplacement privé](installing-a-non-com-component-to-a-private-location.md)
    -   [Rendre un composant non-COM dans un package existant privé](make-a-non-com-component-in-an-existing-package-private.md)

-   créer une base de données Windows Installer qui installe les assemblys.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Table MsiAssembly](msiassembly-table.md)
    -   [Table MsiAssemblyName](msiassemblyname-table.md)
    -   [Assemblys](assemblies.md)
    -   [clés de registre de l’assembly écrites par l’Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Installation d’assemblys Win32](installation-of-win32-assemblies.md)

-   créer une base de données Windows Installer qui installe les pilotes ODBC et les traducteurs.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Table ODBCAttribute](odbcattribute-table.md)
    -   [Table ODBCDriver](odbcdriver-table.md)
    -   [Table ODBCTranslator](odbctranslator-table.md)
    -   [Table ODBCDataSource](odbcdatasource-table.md)
    -   [Table ODBCSourceAttribute](odbcsourceattribute-table.md)

-   créer une base de données Windows Installer qui installe le protocole MIME.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Table MIME](mime-table.md)
    -   [Table d’extension](extension-table.md)
    -   [Modification du Registre](modifying-the-registry.md)

-   créer une base de données Windows Installer qui installe les variables d’environnement.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Table d’environnement](environment-table.md)

-   créer une base de données Windows Installer qui installe les raccourcis.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Tableau de raccourcis](shortcut-table.md)
    -   [Table MsiShortcutProperty](msishortcutproperty-table.md)
    -   [Modification des raccourcis du programme d’installation](editing-installer-shortcuts.md)
    -   [Windows Exemples de programme d’installation](windows-installer-examples.md)

-   créer une base de données Windows Installer qui installe plusieurs instances d’applications.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Installation de plusieurs instances de produits et correctifs](installing-multiple-instances-of-products-and-patches.md)
    -   [Création de plusieurs instances à l’aide de transformations d’instance](authoring-multiple-instances-with-instance-transforms.md)
    -   [Installation de plusieurs instances à l’aide de transformations d’instance](installing-multiple-instances-with-instance-transforms.md)

-   Spécifiez les options et les États de sélection des fonctionnalités par défaut.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Groupe de tables principales](core-tables-group.md)
    -   [Table des composants](component-table.md)
    -   [Tableau des fonctionnalités](feature-table.md)
    -   [Table FeatureComponents](featurecomponents-table.md)
    -   [Contrôle des États de sélection des fonctionnalités](controlling-feature-selection-states.md)
    -   [Propriétés options d’installation de la fonctionnalité](property-reference.md)

-   Spécifiez les conditions qui doivent être remplies pour installer une application ou des composants sélectionnés.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Table de conditions](condition-table.md)
    -   [Table LaunchCondition](launchcondition-table.md)
    -   [Table des composants](component-table.md)
    -   [Utilisation des propriétés dans les instructions conditionnelles](using-properties-in-conditional-statements.md)
    -   [Syntaxe d’instruction conditionnelle](conditional-statement-syntax.md)
    -   [Mesures de conditionnement à exécuter pendant la suppression](conditioning-actions-to-run-during-removal.md)
    -   [Exemples de syntaxe d’instruction conditionnelle](examples-of-conditional-statement-syntax.md)

-   Créez la séquence d’actions utilisée pour installer l’application.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Utilisation d’une table de séquences](using-a-sequence-table.md)
    -   [Groupe de tables de procédure d’installation](installation-procedure-tables-group.md)
    -   [Exemple de table de séquence détaillé](sequence-table-detailed-example.md)
    -   [Actions avec restrictions de séquencement](actions-with-sequencing-restrictions.md)
    -   [Actions sans restrictions de séquencement](actions-without-sequencing-restrictions.md)
    -   [Utilisation des propriétés dans les instructions conditionnelles](using-properties-in-conditional-statements.md)
    -   [Syntaxe d’instruction conditionnelle](conditional-statement-syntax.md)
    -   [Exemples de syntaxe d’instruction conditionnelle](examples-of-conditional-statement-syntax.md)
    -   [Mesures de conditionnement à exécuter pendant la suppression](conditioning-actions-to-run-during-removal.md)
    -   [Actions standard](standard-actions.md)
    -   [Windows Exemples de programme d’installation](windows-installer-examples.md)

-   préparez le package d’installation de l’application pour les futures mises à niveau de l’application par le service Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Correctifs et mises à niveau](patching-and-upgrades.md)
    -   [Préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md)
    -   [Utilisation d’un UpgradeCode](using-an-upgradecode.md)
    -   [Mettre à niveau la table](upgrade-table.md)
    -   [**UpgradeCode, propriété**](upgradecode.md)
    -   [Empêcher l’installation d’un ancien package sur une version plus récente](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [Modification du code du produit](changing-the-product-code.md)
    -   [Mise à jour des assemblys](updating-assemblies.md)
    -   [Windows Exemples de programme d’installation](windows-installer-examples.md)

-   résolvez les problèmes Windows Installer packages en cours de développement.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Validations de package](package-validation.md)
    -   [Évaluateurs de cohérence internes-CIEM](internal-consistency-evaluators-ices.md)
    -   [Windows Journalisation du programme d’installation](windows-installer-logging.md)
    -   [Vérification de l’installation des fonctionnalités, des composants, des fichiers](checking-the-installation-of-features-components-files.md)
    -   [Création d’un package volumineux](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Windows Outils de développement du programme d’installation](windows-installer-development-tools.md)
    -   [Validation des modules de fusion](validating-merge-modules.md)
    -   [Validation d’une base de données d’installation](validating-an-installation-database.md)
    -   [Validation de la mise à niveau d’une installation](validating-an-installation-upgrade.md)
    -   [Recherche d’une fonctionnalité ou d’un composant endommagé](searching-for-a-broken-feature-or-component.md)
    -   [Windows Messages d’erreur du programme d’installation](windows-installer-error-messages.md)
    -   [Journalisation des demandes de redémarrage](logging-of-reboot-requests.md)

-   Assurez une configuration et une installation sécurisées de l’application.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md)
    -   [Instructions pour la sécurisation des actions personnalisées](guidelines-for-securing-custom-actions.md)
    -   [Sécurité des actions personnalisées](custom-action-security.md)
    -   [Instructions pour la sécurisation des packages sur les ordinateurs verrouillés](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [Création d’une installation signée entièrement vérifiée à l’aide d’Automation](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [Exemple d’installation de Windows Installer basée sur une URL](a-url-based-windows-installer-installation-example.md)
    -   [Création de l’interface utilisateur pour l’entrée de mot de passe](authoring-the-user-interface-for-password-input.md)
    -   [Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md)
    -   [utilisation de Windows Installer avec UAC](using-windows-installer-with-uac.md)
    -   [Mise à jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**Propriété AdminUser**](adminuser.md)
    -   [**Privileged, propriété**](privileged.md)
    -   [**Propriété SecureCustomProperties**](securecustomproperties.md)

-   Créez une interface utilisateur pour présenter les options permettant de configurer l’installation et d’obtenir des informations de l’utilisateur sur le processus d’installation en attente.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [À propos de l’interface utilisateur](about-the-user-interface.md)
    -   [Ajout de contrôles et de texte](adding-controls-and-text.md)
    -   [Création d’un contrôle ProgressBar](authoring-a-progressbar-control.md)
    -   [Messages d’invite de création de disque](authoring-disk-prompt-messages.md)
    -   [Création d’une condition « Veuillez patienter... » Boîte de message](authoring-a-conditional-please-wait-------message-box.md)
    -   [Aperçu de l’interface utilisateur](previewing-the-user-interface.md)
    -   [Ajout de texte stocké dans une propriété](adding-text-stored-in-a-property.md)
    -   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   Créer une interface utilisateur externe pour présenter une interface utilisateur personnalisée afin de configurer l’installation et d’obtenir des informations de l’utilisateur sur le processus d’installation en attente.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [Surveillance d’une installation à l’aide de MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [analyse des Messages de Windows Installer](parsing-windows-installer-messages.md)
    -   [Retour de valeurs à partir d’un gestionnaire d’interface utilisateur externe](returning-values-from-an-external-user-interface-handler.md)
    -   [\_Gestionnaire INSTALLUI](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [Gestion des messages de progression à l’aide de MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md)
    -   [Surveillance d’une installation à l’aide de MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md)

-   Définissez les informations de l’application dans **Ajout/suppression de programmes** (ARP).

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [configuration de l’ajout/suppression de programmes avec Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
    -   [Ajout et suppression d’une application et absence de trace dans le registre](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Désinstaller la clé de Registre](uninstall-registry-key.md)

-   écrivez des actions personnalisées pour gérer la logique d’installation qui n’est pas prise en charge en mode natif par Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Actions personnalisées](custom-actions.md)
    -   [Liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md)
    -   [Instructions pour la sécurisation des actions personnalisées](guidelines-for-securing-custom-actions.md)
    -   [Référence des actions personnalisées](custom-action-reference.md)
    -   [Utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [Utilisation d’une action personnalisée pour lancer un fichier installé à la fin de l’installation](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [Accès à une base de données ou à une session à partir d’une action personnalisée](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [Accès à la session de programme d’installation actuelle à partir d’une action personnalisée](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [Modification de l’état du système à l’aide d’une action personnalisée](changing-the-system-state-using-a-custom-action.md)

-   amorcez le Windows Installer sur l’ordinateur d’un utilisateur.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Amorçage](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [Amorçage du téléchargement Internet](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [Exemple d’installation de Windows Installer basée sur une URL](a-url-based-windows-installer-installation-example.md)
    -   [Configuration des ressources Setup.exe](configuring-the-setup-exe-resources.md)
    -   [Téléchargement d’une installation à partir d’Internet](downloading-an-installation-from-the-internet.md)

-   respectez les instructions de Active Accessibility lors de l’écriture de packages Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Accessibilité](accessibility.md)

-   Préparez l’internationalisation de l’installation d’une application.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [préparation d’un Package de Windows Installer pour la localisation](preparing-a-windows-installer-package-for-localization.md),
    -   [localisation d’un Package Windows Installer](localizing-a-windows-installer-package.md)
    -   [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md)
    -   [Ajout de ressources localisées](adding-localized-resources.md)
    -   [Exemple de localisation](a-localization-example.md)
    -   [Localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md)
    -   [Localiser des colonnes de base de données](localizing-database-columns.md)
    -   [Création d’une base de données avec une page de codes neutre](creating-a-database-with-a-neutral-code-page.md)
    -   [Gestion des pages de codes des tables importées et exportées](code-page-handling-of-imported-and-exported-tables.md)
    -   [Localisation de la langue affichée par les boîtes de dialogue](localizing-the-language-displayed-by-dialogs.md)
    -   [Importation de tables Error et ActionText localisées](importing-localized-error-and-actiontext-tables.md)
    -   [Mise à jour des propriétés ProductLanguage et ProductCode](updating-productlanguage-and-productcode-properties.md)
    -   [Mise à jour d’un flux d’informations de synthèse](updating-a-summary-information-stream.md)
    -   [Composants qualifiés](qualified-components.md)
    -   [Table UIText](uitext-table.md)
    -   [Gérer la langue et la page de codes](manage-language-and-codepage.md)
    -   [Vérification de la page de codes de la base de données d’installation](checking-the-installation-database-code-page.md)

-   créez des packages Windows Installer pour les plateformes 32 bits et 64 bits.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Windows Programme d’installation sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md)
    -   [Actions personnalisées 64 bits](64-bit-custom-actions.md)
    -   [Utilisation d’actions personnalisées 64 bits](using-64-bit-custom-actions.md)
    -   [Utilisation des modules de fusion 64 bits](using-64-bit-merge-modules.md)

-   redistribuer les composants de Windows Installer partagés et la logique d’installation en tant que modules de fusion.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Modules de fusion](merge-modules.md)
    -   [Création d’une transformation de langue pour un module de fusion à plusieurs langues](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [Application d’un module de fusion configurable avec des personnalisations](applying-a-configurable-merge-module-with-customizations.md)

-   planifiez ou supprimez les redémarrages au cours d’une installation Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Redémarrages du système](system-reboots.md)
    -   [Journalisation des demandes de redémarrage](logging-of-reboot-requests.md)

-   Créer des mises à jour ou des correctifs pour une application existante en créant un correctif.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Création d’un correctif de mise à jour de petite taille](creating-a-small-update-patch.md)
    -   [Exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md)

-   Créez un package à double usage qui peut installer une application uniquement pour l’utilisateur actuel ou pour tous les utilisateurs de l’ordinateur.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Contexte d’installation](installation-context.md)
    -   [Création d’un package unique](single-package-authoring.md)
    -   [Exemple de création de package unique](single-package-authoring-example.md)

-   personnalisez les services sur l’ordinateur à l’aide de l’Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Utilisation de la configuration des services](using-services-configuration.md)

-   sécurisez les ressources sur l’ordinateur à l’aide de l’Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md)
    -   [Sécurisation des ressources](securing-resources-.md)

-   Énumérer tous les composants installés sur l’ordinateur et obtenir le chemin d’accès à la clé du composant.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Énumération des composants](enumerating-components-.md)

-   Installer plusieurs packages à l’aide du [*traitement des transactions*](t-gly.md).

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Installations sur plusieurs packages](multiple-package-installations.md)

-   incorporez une interface utilisateur personnalisée dans le package Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Utilisation de l’interface utilisateur](using-the-user-interface.md)
    -   [Utilisation d’une interface utilisateur incorporée](using-an-embedded-ui.md)

## <a name="it-professionals"></a>Professionnels de l’informatique

les professionnels de l’informatique et les administrateurs peuvent personnaliser et déployer des packages de Windows Installer existants. ces utilisateurs reconditionnent les configurations des applications existantes dans Windows Installer des packages d’installation, et installent et gèrent les images administratives des installations Windows Installer sur les réseaux.

-   personnaliser les applications et le programme d’installation en générant et en appliquant des transformations Windows Installer

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Personnalisation](customization.md)
    -   [Transformations de base de données](database-transforms.md)
    -   [Exemple de transformation de personnalisation](a-customization-transform-example.md)
    -   [Fusions et transformations](merges-and-transforms.md)
    -   [Utilisation des transformations pour ajouter des ressources](using-transforms-to-add-resources.md)
    -   [Générer une transformation](generate-a-transform.md)
    -   [Options de ligne de commande](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [Appliquer une transformation](apply-a-transform.md)
    -   [Afficher une transformation](view-a-transform.md)
    -   [Afficher les différences entre deux bases de données](view-differences-between-two-databases.md)
    -   [Mise à jour corrective des applications personnalisées](patching-customized-applications.md)

-   déployez un package d’installation Windows Installer, une mise à jour ou un correctif logiciel.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Installation d’une application](installing-an-application.md)
    -   [Correctifs et mises à niveau](patching-and-upgrades.md)
    -   [Transformations](transforms.md)
    -   [Installation d’un package avec des privilèges élevés pour un non-administrateur](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Application de mises à niveau majeures en appliquant des correctifs à l’installation locale du produit](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [Application de mises à niveau majeures en installant le produit](applying-major-upgrades-by-installing-the-product.md)
    -   [Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Application de petites mises à jour en réinstallant le produit](applying-small-updates-by-reinstalling-the-product.md)
    -   [Application de petites mises à jour en corrigeant une image administrative](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Mise à jour corrective des installations initiales](patching-initial-installations.md)
    -   [Options de ligne de commande](command-line-options.md)

-   résolvez les problèmes Windows Installer packages.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Windows Journalisation du programme d’installation](windows-installer-logging.md)
    -   [Vérification de l’installation des fonctionnalités, des composants, des fichiers](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Recherche d’une fonctionnalité ou d’un composant endommagé](searching-for-a-broken-feature-or-component.md)
    -   [Windows Messages d’erreur du programme d’installation](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   utilisez les scripts pour interroger des packages Windows Installer pour obtenir des informations sur un produit et modifier l’installation.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Interface d’automatisation](automation-interface.md)
    -   [Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
    -   [utilisation de Windows Installer avec WMI](using-windows-installer-with-wmi.md)

-   Créer et gérer des installations administratives.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Installation administrative](administrative-installation.md)
    -   [Options de ligne de commande](command-line-options.md)
    -   [**Propriété AdminProperties**](adminproperties.md)
    -   [Application de petites mises à jour en corrigeant une image administrative](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Application d’un package de correctifs à une installation d’administration](applying-a-patch-package-to-an-administrative-installation.md)
    -   [Ordre d’exécution des actions](action-execution-order.md)
    -   [**Propriété IsAdminPackage**](isadminpackage.md)
    -   [Ordre de priorité des propriétés](order-of-property-precedence.md)
    -   [**Propriété AdminProperties**](adminproperties.md)

-   Rendre une application accessible à tous les utilisateurs d’un ordinateur ou à un utilisateur spécifié uniquement.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Contexte d’installation](installation-context.md)
    -   [**ALLUSERS, propriété**](allusers.md)

-   Interprétez les packages, installez les produits et configurez les options de fonctionnalité à l’aide d’une ligne de commande.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Options de ligne de commande](command-line-options.md)
    -   [Définition des valeurs de propriété publiques sur la ligne de commande](setting-public-property-values-on-the-command-line.md)
    -   [Obtention et définition des propriétés](getting-and-setting-properties.md)
    -   [Réinstallation d’une fonctionnalité ou d’une application](reinstalling-a-feature-or-application.md)
    -   [Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Application de petites mises à jour en réinstallant le produit](applying-small-updates-by-reinstalling-the-product.md)
    -   [Modification de l’emplacement cible d’un répertoire](changing-the-target-location-for-a-directory.md)
    -   [Application de petites mises à jour en corrigeant une image administrative](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Application de mises à niveau majeures en installant le produit](applying-major-upgrades-by-installing-the-product.md)
    -   [Propriétés de configuration](property-reference.md)
    -   [Propriétés options d’installation de la fonctionnalité](property-reference.md)

-   Utilisez la stratégie pour gérer les droits d’accès et les autorisations.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Stratégies d’ordinateur](machine-policies.md),
    -   [Stratégies d’utilisateur](user-policies.md),
    -   [Installation d’un package avec des privilèges élevés pour un non-administrateur](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Publication d’une application Per-User à installer avec des privilèges élevés](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Propriété AdminUser**](adminuser.md)
    -   [**Privileged, propriété**](privileged.md)
    -   [**Propriété EnableUserControl**](enableusercontrol.md)
    -   [**UserSID, propriété**](usersid.md)
    -   [**Propriété SecureCustomProperties**](securecustomproperties.md)

-   Installer plusieurs packages à l’aide du [*traitement des transactions*](t-gly.md).

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Installations sur plusieurs packages](multiple-package-installations.md)

-   incorporez une interface utilisateur personnalisée dans un package Windows Installer.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Utilisation de l’interface utilisateur](using-the-user-interface.md)
    -   [Utilisation d’une interface utilisateur incorporée](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>Développeurs d’infrastructure

les développeurs d’Infrastructure peuvent créer des plateformes unifiées pour le déploiement et la gestion de logiciels qui utilisent le service Windows Installer. ils peuvent utiliser l’interface de programmation Windows Installer pour interroger, gérer et distribuer des applications, des correctifs et des sources sur un système.

-   Localisez, stockez et interrogez l’État, les informations et les clients des composants.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Fonctions spécifiques au composant](installer-function-reference.md)
    -   [Fonctions d’État du système](installer-function-reference.md)
    -   [Objet installer](installer-object.md)
    -   [Product, objet](product-object.md)
    -   [Objet patch](patch-object.md)

-   Inventorier et interroger pour obtenir des informations et l’état des produits et des fonctionnalités.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Inventaire des produits et des correctifs](inventory-products-and-patches-.md)
    -   [Fonctions d’État du système](installer-function-reference.md)
    -   [Fonctions de requête de produit](installer-function-reference.md)
    -   [Objet installer](installer-object.md)
    -   [Product, objet](product-object.md)
    -   [Objet patch](patch-object.md)

-   améliorez la résilience de la source à l’aide de la Windows Installer pour inventorier, interroger et modifier la liste source des applications, des mises à niveau et des correctifs.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [**SOURCELIST, propriété**](sourcelist.md)
    -   [**Résilience source**](source-resiliency.md)
    -   [Fonctions d’installation et de configuration](installer-function-reference.md)
    -   [Objet installer](installer-object.md)
    -   [Product, objet](product-object.md)
    -   [Objet patch](patch-object.md)

-   améliorez la résilience de la source à l’aide de la Windows Installer pour inventorier, interroger et modifier des sources multimédias.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [**SOURCELIST, propriété**](sourcelist.md)
    -   [Résilience source](source-resiliency.md)
    -   [Fonctions d’installation et de configuration](installer-function-reference.md)
    -   [Product, objet](product-object.md)
    -   [Objet patch](patch-object.md)

-   Inventaire et requête pour obtenir des informations et l’état des correctifs.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Inventaire des produits et des correctifs](inventory-products-and-patches-.md)
    -   [Référence des fonctions du programme d’installation](installer-function-reference.md)
    -   [Objet patch](patch-object.md)

-   Utilisez la stratégie pour gérer les droits d’accès et les autorisations.

    Pour plus d’informations, consultez les rubriques suivantes :

    -   [Stratégies d’ordinateur](machine-policies.md)
    -   [Stratégies utilisateur](user-policies.md)
    -   [Installation d’un package avec des privilèges élevés pour un non-administrateur](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Publication d’une application Per-User à installer avec des privilèges élevés](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Propriété AdminUser**](adminuser.md)
    -   [**Privileged, propriété**](privileged.md)
    -   [**Propriété EnableUserControl**](enableusercontrol.md)
    -   [**UserSID, propriété**](usersid.md)
    -   [**Propriété SecureCustomProperties**](securecustomproperties.md)

 

 



