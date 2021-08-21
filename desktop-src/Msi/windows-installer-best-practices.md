---
description: 'cette section énumère une liste de conseils, liés à la documentation principale du kit de développement logiciel (SDK) Windows Installer, pour aider les développeurs d’applications, les auteurs de la configuration, les professionnels de l’informatique et les développeurs d’Infrastructure à découvrir les meilleures pratiques en matière d’utilisation de la Windows Installer :'
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Windows Meilleures pratiques pour le programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e430cf8871279e18107b3ab1deb1f347e9d4779b619ab6cf8133d30cdfa4ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808959"
---
# <a name="windows-installer-best-practices"></a>Windows Meilleures pratiques pour le programme d’installation

cette section énumère une liste de conseils, liés à la documentation principale du kit de développement logiciel (SDK) Windows Installer, pour aider les développeurs d’applications, les auteurs de la configuration, les professionnels de l’informatique et les développeurs d’Infrastructure à découvrir les meilleures pratiques en matière d’utilisation de la Windows Installer :

-   [mettez à jour la version de Windows Installer.](#update-the-windows-installer-version)
-   [répondez aux exigences de certification du Logo de Windows.](#meet-the-windows-logo-certification-requirements)
-   [Préparez le package pour la localisation.](#prepare-the-package-for-localization)
-   [mettez à jour vos outils de développement Windows Installer et votre documentation.](#update-your-windows-installer-development-tools-and-documentation)
-   [Si vous décidez de reconditionner une application d’installation héritée, suivez les bonnes pratiques en matière de réintégration.](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [N’essayez pas de remplacer des ressources protégées.](#do-not-try-to-replace-protected-resources)
-   [Ne dépendez pas de ressources non critiques.](#do-not-depend-upon-non-critical-resources)
-   [utilisez l’API pour récupérer les informations de configuration de Windows Installer.](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [Organisez l’installation de votre application autour des composants.](#organize-the-installation-of-your-application-around-components)
-   [réduisez la taille des packages de Windows Installer volumineux.](#reduce-the-size-of-large-windows-installer-packages)
-   [Si vous utilisez des actions personnalisées, suivez les bonnes pratiques d’action personnalisées.](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [Si vous utilisez des assemblys, suivez les bonnes pratiques d’assembly](#if-you-use-assemblies-follow-good-assembly-practices)
-   [N’expédiez pas d’installations simultanées.](#do-not-ship-concurrent-installations)
-   [Assurez la cohérence des noms de packages et des codes de package.](#keep-package-names-and-package-codes-consistent)
-   [N’utilisez pas les tables SelfReg et TypeLib.](#do-not-use-the-selfreg-and-typelib-tables)
-   [Fournissez l’option d’installation sans interface utilisateur.](#provide-the-option-to-install-without-a-user-interface)
-   [Évitez d’utiliser la stratégie AlwaysInstallElevated a.](#avoid-using-the-alwaysinstallelevated-policy)
-   [Activez la stratégie DisableMedia pour limiter l’installation non autorisée.](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [Conservez les fichiers sources du package d’origine sécurisés et disponibles pour les utilisateurs.](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [Activez la journalisation documentée sur l’ordinateur de l’utilisateur lors du dépannage du déploiement.](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [La désinstallation laisse l’ordinateur de l’utilisateur dans un état propre.](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [Testez les packages pour un déploiement d’installation par utilisateur et par ordinateur.](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [Planifiez et testez une stratégie de maintenance avant d’expédier l’application.](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [Réduisez la dépendance des mises à jour sur les sources d’origine.](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [Ne distribuez pas les modules de fusion non desservis.](#do-not-distribute-unserviceable-merge-modules)
-   [Évitez d’appliquer des correctifs aux installations administratives.](#avoid-patching-administrative-installations)
-   [Enregistrez les mises à jour à exécuter avec des privilèges élevés.](#register-updates-to-run-with-elevated-privilege)
-   [Utilisez la table MsiPatchSequence pour séquencer les correctifs.](#use-the-msipatchsequence-table-to-sequence-patches)
-   [Testez soigneusement le package d’installation.](#test-the-installation-package-thoroughly)
-   [Corrigez toutes les erreurs de validation avant de déployer un package d’installation nouveau ou révisé.](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [Créer une installation sécurisée.](#author-a-secure-installation)
-   [Utiliser PMSIHANDLE au lieu de HANDLE](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>mettez à jour la version de Windows Installer.

-   utilisez Windows Installer 5,0 sur Windows Server 2008 R2 et Windows 7. il s’agit de la version Windows Installer fournie avec le système d’exploitation.
-   utilisez Windows Installer 4,5 sur Windows server 2008, Windows server 2003 avec service pack 1 (sp1), Windows Vista avec service pack 1 (sp1) ou Windows XP avec service pack 2 (SP2). pour plus d’informations sur l’obtention de la dernière version de Windows Installer, consultez [Windows Installer redistribuables](windows-installer-redistributables.md).
-   utilisez Windows Installer 3,1 sur Windows 2000 avec Service Pack 3 (SP3). Windows Le programme d’installation 3,1 possède des fonctionnalités qui facilitent la maintenance et la mise à [jour corrective](patching.md)des applications.
-   de nombreuses fonctionnalités importantes ont été introduites avec la version 3,0 et sont répertoriées dans la section [non prise en charge dans Windows Installer version 2,0](not-supported-in-windows-installer-version-2-0.md). les packages d’Installation et les mises à jour qui ont été créés pour Windows Installer 2,0 peuvent être installés à l’aide de Windows Installer 3,0 et versions ultérieures. les packages de correctifs qui contiennent les nouvelles tables utilisées par Windows Installer 3,0 peuvent toujours être appliqués à l’aide de versions antérieures de Windows Installer mais sans la fonctionnalité de mise à jour corrective Windows Installer 3,0. il est également possible de créer des correctifs qui requièrent explicitement le Windows Installer 3,0 qui ne peuvent pas être appliqués par des versions antérieures de Windows Installer. si un utilisateur ne parvient pas à mettre à jour la version du programme d’installation, assurez-vous que votre application ou mise à jour sera compatible avec une prochaine mise à jour du Windows Installer.
-   pour obtenir la liste des fonctionnalités Windows Installer non prises en charge par les versions antérieures du programme d’installation de Windows [, consultez nouveautés de Windows Installer](what-s-new-in-windows-installer.md).

## <a name="meet-the-windows-logo-certification-requirements"></a>répondez aux exigences de certification du Logo de Windows.

-   même si vous n’envisagez pas de soumettre votre application au programme de logo, le respect des instructions de certification du logo peut contribuer à améliorer votre Windows Installer package. pour obtenir une vue d’ensemble des conditions requises pour le logo et des liens vers des programmes de certification de logo spécifiques, consultez [Windows Installer et logo requirements](windows-installer-and-logo-requirements.md).

## <a name="prepare-the-package-for-localization"></a>Préparez le package pour la localisation.

-   Il est recommandé de préparer la localisation future lors de la création du package d’installation d’origine. vous pouvez suivre la procédure de localisation de packages suggérée pour [localiser un package de Windows Installer](localizing-a-windows-installer-package.md).

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>mettez à jour vos outils de développement Windows Installer et votre documentation.

-   les [outils de développement Windows Installer](windows-installer-development-tools.md) ne sont pas redistribuables et vous devez uniquement utiliser les versions de ces outils disponibles auprès de Microsoft. celles-ci sont disponibles dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md) dans le kit de développement logiciel (SDK) Microsoft Windows.
-   plusieurs éditeurs de logiciels indépendants proposent des outils permettant de créer ou de modifier des packages de Windows Installer. ces outils peuvent fournir un environnement de création de packages qui peut être plus facile à utiliser que les outils fournis dans le kit de développement logiciel (SDK) Windows Installer. vous pouvez en savoir plus sur ces outils à partir des ressources d’informations abordées dans [autres Sources d’informations](other-sources-of-windows-installer-information.md)sur les Windows Installer.
-   La capacité de créer un package à partir de fichiers texte peut être plus intuitive pour certains développeurs. l’ensemble d’outils Windows Installer XML (WiX) disponible sur [Sourceforge.net](https://sourceforge.net/projects/wix) génère des packages d’installation Windows à partir du code source XML.
-   la documentation du [kit de développement logiciel (SDK) Windows Installer](./windows-installer-portal.md) publiée dans la bibliothèque en ligne MSDN est mise à jour le plus fréquemment.
-   utilisez la version récente de [Msizap.exe](msizap-exe.md) (version 3.1.4000.2726 ou ultérieure) qui est disponible dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md) pour Windows Vista ou version ultérieure. Les versions plus petites de Msizap.exe peuvent supprimer des informations sur toutes les mises à jour qui ont été appliquées à d’autres applications sur l’ordinateur de l’utilisateur. Si ces informations sont supprimées, ces autres applications devront peut-être être supprimées et réinstallées pour recevoir des mises à jour supplémentaires.
-   l’éditeur de table de base de données [Orca.exe](orca-exe.md) est un éditeur de table de base de données pour la création et la modification des packages Windows Installer et des modules de fusion. il dispose d’une interface graphique utilisateur de base, mais prend en charge l’édition avancée des bases de données Windows Installer. Même si vous utilisez une autre application comme outil de développement principal, vous pouvez utiliser Orca.exe est pratique pour le dépannage et le test d’un package.
-   consultez [les autres Sources d’informations de Windows Installer](other-sources-of-windows-installer-information.md) pour obtenir des informations sur les Windows Installer actuelles disponibles dans les blogs, les conversations techniques, les groupes de discussion, les articles techniques et les sites web.

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>Si vous décidez de reconditionner une application d’installation héritée, suivez les bonnes pratiques en matière de réintégration.

de nombreux fournisseurs d’applications fournissent des packages de Windows Installer natifs pour l’installation ou leurs produits. un logiciel qui convertit une application d’installation existante existante en package Windows Installer est désigné sous le terme de « outil de réintégration ». le Guide pas à pas du livre blanc [sur la création de Packages Windows Installer et le logiciel de reconditionnement pour le Windows Installer](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx) décrit un outil de réemballage disponible dans le commerce. Le reconditionnement d’une application d’installation existante n’est pas la meilleure pratique de développement. les Applications qui ont été conçues à partir du début pour tirer parti des fonctionnalités de Windows Installer peuvent être plus faciles à installer et à traiter. si vous décidez d’utiliser un logiciel de empaquetage, les pratiques suivantes peuvent vous aider à créer un package plus Windows Installer.

-   les outils de empaquetage convertissent les installations héritées en un package Windows Installer en utilisant une image d’un système intermédiaire avant et après l’installation. Toute modification du Registre, modification de fichier ou paramètre système qui se produit pendant le processus de capture est inclus dans l’installation. Configurez le matériel et le logiciel de l’ordinateur utilisé pour reconditionner l’installation aussi près que possible du système de l’utilisateur prévu. Créez un package distinct pour chaque configuration matérielle différente. Repackage à l’aide d’un ordinateur intermédiaire propre. Supprimez toutes les applications inutiles. Arrêtez tous les processus inutiles. Fermez tous les services système non essentiels.
-   Effectuez toujours une copie de l’installation d’origine avant de commencer à travailler dessus. Travaillez toujours sur la copie. N’arrêtez jamais un reconditionneur avant de terminer la génération du package. Si le reconditionneur endommage le package, vous disposez toujours de l’original.
-   ne reconditionnez pas les mises à jour logicielles Microsoft dans un package Windows Installer. Microsoft publie les mises à jour logicielles, telles que les service packs, sous la forme de fichiers à extraction automatique qui exécutent automatiquement l’installation. ces mises à jour utilisent des programmes d’installation différents de ceux de la Windows Installer pour remplacer les ressources Windows protégées et ne peuvent pas être converties en package Windows Installer. pour plus d’informations sur le déploiement de Windows service packs, consultez le guide de déploiement de Service Pack sur [Microsoft TechNet](https://technet.microsoft.com/).
-   n’utilisez pas un outil de empaquetage pour convertir un package Windows Installer en nouveau package. le Windows Installer ajoute des informations de configuration au système ainsi qu’aux ressources de l’application. Quand un outil de empaquetage compare le système avant et après l’installation, le reconditionneur interprète les informations de configuration dans le cadre de l’application. Cela endommage généralement l’application reconditionnée. utilisez plutôt des [transformations de personnalisation](a-customization-transform-example.md) pour modifier un package de Windows Installer existant ou pour créer un nouveau package. Vous pouvez créer des transformations de personnalisation à l’aide de l’outil [Msitran.exe](msitran-exe.md) .
-   n’utilisez pas un outil de réintégration pour consolider plusieurs packages de Windows Installer dans un même package. Au lieu de cela, vous pouvez utiliser l’outil [Msistuff.exe](msistuff-exe.md) pour configurer le Setup.exe exécutable de démarrage pour installer les packages l’un après l’autre.
-   créez votre Windows Installer package afin qu’il puisse être facilement personnalisé par le client. les variables globales utilisées par l’Windows Installer pendant une installation peuvent être définies à l’aide de [propriétés](properties.md) publiques ou de [transformations de personnalisation](a-customization-transform-example.md). Fournissez une documentation pour l’utilisation de ces propriétés et des valeurs par défaut pratiques pour toutes les valeurs personnalisables. Pour plus d’informations sur l’obtention et la définition des propriétés, consultez [utilisation des propriétés](using-properties.md). Pour obtenir un exemple de transformation de personnalisation, consultez [un exemple de transformation de personnalisation](a-customization-transform-example.md).

## <a name="do-not-try-to-replace-protected-resources"></a>N’essayez pas de remplacer des ressources protégées.

Windows Les packages d’installation ne doivent pas tenter de remplacer les ressources protégées lors de l’installation ou de la mise à jour. le Windows Installer ne supprime pas ou ne remplace pas ces ressources, car Windows empêche le remplacement des fichiers système, des dossiers et des clés de registre essentiels. La protection de ces ressources empêche les défaillances de l’application et du système d’exploitation.

-   lors de l’exécution sur Windows Server 2008 ou Windows Vista, le Windows Installer ignore l’installation des fichiers ou des clés de registre protégés par [Protection des ressources Windows](../wfp/windows-resource-protection-portal.md) (WRP), le programme d’installation entre un avertissement dans le fichier journal et poursuit le reste de l’installation sans erreur. pour plus d’informations, consultez [utilisation de Windows Installer et Protection des ressources Windows](windows-resource-protection-on-windows-vista.md).
-   WRP est le nouveau nom de la protection de fichier Windows (WFP). WRP protège les clés de Registre et les dossiers, ainsi que les fichiers système essentiels. dans Windows Server 2003, Windows XP et Windows 2000, lorsque le Windows Installer a rencontré un fichier protégé par wfp, le programme d’installation demande que WFP installe le fichier. pour plus d’informations, consultez [utilisation de Windows Installer et Protection des ressources Windows](windows-resource-protection-on-windows-vista.md).

## <a name="do-not-depend-upon-non-critical-resources"></a>Ne dépendez pas de ressources non critiques.

Votre installation ou mise à jour ne doit pas dépendre de l’installation de ressources non critiques pour les raisons suivantes.

-   Les actions personnalisées peuvent échouer si elles dépendent d’un composant appartenant à une fonctionnalité que l’utilisateur publie au lieu d’installer.
-   Les actions personnalisées séquencées avant l’action [InstallFinalize](installfinalize-action.md) peuvent échouer si elles dépendent d’un composant contenant un assembly en cours d’installation. le Windows Installer ne valide pas les assemblys dans le global assembly Cache (GAC) tant que l’action InstallFinalize n’est pas terminée.

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>utilisez l’API pour récupérer les informations de configuration de Windows Installer.

l’installation de votre application ou mise à jour ne doit pas dépendre d’un accès direct aux informations de configuration Windows Installer enregistrées sur votre ordinateur. au lieu de cela, utilisez l’interface de programmation d’applications Windows Installer pour récupérer les informations de configuration. l’emplacement et le format des informations de configuration sont gérés par le service Windows Installer et peuvent être modifiés.

-   les fonctions d’installation et de Configuration de l’API Windows Installer sont décrites dans la [référence des fonctions du programme d’installation](installer-function-reference.md).
-   Les [Propriétés de configuration](property-reference.md) sont décrites dans la référence de propriété.
-   Les méthodes et propriétés Automation sont décrites dans la [référence de l’interface Automation](automation-interface-reference.md). L’exemple de script WiLstPrd.vbs se connecte à un objet installer et énumère les produits inscrits et les informations produit. Pour plus d’informations, consultez [répertorier les produits, les propriétés, les fonctionnalités et les composants](list-products-properties-features-and-components.md).

## <a name="organize-the-installation-of-your-application-around-components"></a>Organisez l’installation de votre application autour des composants.

le service Windows Installer installe ou supprime les collections de ressources appelées [composants](windows-installer-components.md). Étant donné que les composants sont généralement partagés, l’auteur d’un package d’installation doit suivre les règles lors de la spécification des composants d’une fonctionnalité ou d’une application.

-   Respectez les règles des composants lors de l' [Organisation des applications en composants](organizing-applications-into-components.md) pour vous assurer que les nouveaux composants ou les nouvelles versions des composants puissent être installés et supprimés sans endommager d’autres applications. Vous pouvez suivre la procédure décrite dans [définition des composants du programme d’installation](defining-installer-components.md).
-   Le programme d’installation effectue le suivi de chaque composant par le GUID d’ID de composant respectif spécifié dans la [table des composants](component-table.md). il est essentiel pour le fonctionnement du mécanisme de décompte de références Windows Installer que le GUID de l’ID du composant est correct. Suivez les instructions dans [modification du code du composant](changing-the-component-code.md).
-   Si votre package doit rompre les règles du composant, tenez compte des conséquences possibles et assurez-vous que votre installation n’installe jamais ces composants lorsqu’ils peuvent endommager les composants sur le système de l’utilisateur. Pour plus d’informations, consultez [que se passe-t-il si les règles des composants sont rompues ?](what-happens-if-the-component-rules-are-broken.md).
-   n’oubliez pas que la Windows Installer applique les règles de contrôle de [version](file-versioning-rules.md) des fichiers lors du [remplacement de fichiers existants](replacing-existing-files.md). le Windows Installer détermine d’abord si le fichier de clé du composant est déjà installé avant de tenter d’installer les fichiers du composant. Si le programme d’installation trouve un fichier portant le même nom que le fichier de clé du composant installé à l’emplacement cible, il compare la version, la date et la langue des deux fichiers de clé et utilise des règles de contrôle de version de fichier pour déterminer s’il faut installer le composant fourni par le package. Si le programme d’installation détermine qu’il doit remplacer la base de composants sur le fichier de clé, il utilise les règles de contrôle de version de fichier sur chaque fichier installé pour déterminer s’il faut remplacer le fichier.

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>réduisez la taille des packages de Windows Installer volumineux.

les Packages de Windows volumineux prennent des ressources système et peuvent être difficiles à installer par les utilisateurs. il est conseillé de réduire la taille des Packages de Windows Installer très volumineux à l’aide des méthodes suivantes.

-   Compressez les fichiers dans l’installation et stockez-les dans un fichier CAB (.cab). Le programme d’installation autorise le stockage du fichier .cab en tant que fichier externe distinct, ou en tant que flux de données dans le package MSI lui-même. Pour plus d’informations [, consultez Utilisation d’armoires et de sources compressées](using-cabinets-and-compressed-sources.md).
-   Supprimez l’espace de stockage gaspillé dans le fichier .msi à l’aide de l’une des options décrites dans [réduction de la taille d’un fichier .msi](reducing-the-size-of-an--msi-file.md).
-   si votre package Windows Installer contient plus de 32767 fichiers, vous devez modifier le schéma de la base de données. Pour plus d’informations, consultez [création d’un package volumineux](authoring-a-large-package.md).

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>Si vous utilisez des actions personnalisées, suivez les bonnes pratiques d’action personnalisées.

le Windows Installer possède de nombreuses [actions standard](standard-actions-reference.md) intégrées pour l’installation et la maintenance des applications. Les développeurs doivent tenter de s’appuyer sur les actions standard aussi bien que possible, au lieu de créer leurs propres [actions personnalisées](custom-actions.md). Toutefois, il existe des situations où le développeur d’un package d’installation trouve qu’il est nécessaire d’écrire une action personnalisée.

-   Suivez les instructions relatives [à l’utilisation des actions personnalisées](using-custom-actions.md).
-   Suivez les [instructions relatives à la sécurisation des actions personnalisées](guidelines-for-securing-custom-actions.md). Les actions personnalisées qui utilisent des informations sensibles ne doivent pas écrire ces informations dans le journal. Pour plus d’informations, consultez [sécurité des actions personnalisées](custom-action-security.md).
-   Les actions personnalisées ne doivent pas tenter de définir un point d’entrée de restauration du système à partir d’une action personnalisée. Pour plus d’informations, consultez [définition d’un point de restauration à partir d’une action personnalisée](setting-a-restore-point-from-a-custom-action.md).
-   Retourner des messages d’erreur à partir d’actions personnalisées et les écrire dans le journal pour faciliter le dépannage des actions personnalisées. Pour plus d’informations, consultez [messages d’erreur-actions personnalisées](error-message-custom-actions.md) et [retour de messages d’erreur à partir d’actions personnalisées](returning-error-messages-from-custom-actions.md).
-   Ne modifiez pas l’état du système à partir d’une action personnalisée immédiate. Les actions personnalisées qui modifient directement le système ou appellent un autre service système doivent être différées à l’heure d’exécution du script d’installation. Chaque [action personnalisée d’exécution différée](deferred-execution-custom-actions.md) qui modifie l’état du système doit être précédée d’une [action de restauration personnalisée](rollback-custom-actions.md) pour annuler la modification de l’état du système lors d’une restauration de l’installation. Pour plus d’informations, consultez [modification de l’état du système à l’aide d’une action personnalisée](changing-the-system-state-using-a-custom-action.md).
-   Les actions personnalisées qui effectuent des opérations d’installation complexes doivent être un [fichier exécutable](executable-files.md) ou une [bibliothèque de liens dynamiques](dynamic-link-libraries.md). Limitez l’utilisation d’actions personnalisées basées sur des [scripts](scripts.md) pour des opérations d’installation simples.
-   Rendez les détails de votre action personnalisée au système facilement détectable par les administrateurs système. Placez dans une table personnalisée les détails des entrées de Registre et des fichiers utilisés par votre action personnalisée et faites en sorte que l’action personnalisée soit lue à partir de cette table. Cela est illustré par l’exemple de [l’utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md). pour plus d’informations sur l’ajout de tables personnalisées à une base de données, consultez [utilisation de requêtes](working-with-queries.md) et [d’exemples de requêtes de base de données à l’aide d’SQL et de scripts](examples-of-database-queries-using-sql-and-script.md).
-   Les actions personnalisées ne doivent pas afficher une boîte de dialogue. Les actions personnalisées nécessitant une interface utilisateur peuvent utiliser la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) à la place. consultez [envoi de Messages à Windows Installer à l’aide de MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).
-   Les actions personnalisées ne doivent pas utiliser les fonctions listées sur la page : les [fonctions ne sont pas utilisables dans les actions personnalisées](functions-not-for-use-in-custom-actions.md).
-   Si l’installation est destinée à s’exécuter sur un serveur Terminal Server, vérifiez que toutes vos actions personnalisées sont susceptibles d’être exécutées sur un serveur Terminal Server. Pour plus d’informations, consultez propriété [**TerminalServer**](terminalserver.md) .
-   Pour qu’une action personnalisée s’exécute lors de la désinstallation d’un correctif particulier, l’action personnalisée doit être présente dans l’application d’origine ou être dans un correctif pour le produit qui est toujours appliqué. Pour plus d’informations, consultez [désinstallation des actions personnalisées](patch-uninstall-custom-actions.md).
-   Les actions personnalisées ne doivent pas utiliser le niveau d’interface utilisateur comme condition pour envoyer des messages d’erreur au programme d’installation, car cela peut interférer avec la journalisation et les messages externes. Pour plus d’informations, consultez [détermination du niveau d’interface utilisateur à partir d’une action personnalisée](determining-ui-level-from-a-custom-action.md).
-   Utilisez des instructions conditionnelles et une [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md) pour vous assurer que votre package exécute correctement des actions personnalisées, qu’il n’exécute pas d’actions personnalisées ou qu’il exécute une autre action personnalisée lors de la désinstallation du package. Vérifiez que le package fonctionne comme prévu lors de la [désinstallation des actions personnalisées](uninstalling-custom-actions.md). Pour plus d’informations, consultez [conditionnement des actions à exécuter pendant la suppression](conditioning-actions-to-run-during-removal.md)
-   Si l’installation doit pouvoir être exécutée par des utilisateurs qui ne disposent pas de privilèges d’administrateur, effectuez un test pour vérifier que toutes les actions personnalisées peuvent être exécutées avec des privilèges non-administrateurs. Les actions personnalisées requièrent des privilèges élevés pour modifier les parties du système qui ne sont pas spécifiques à l’utilisateur. Le programme d’installation peut exécuter des actions personnalisées avec des privilèges élevés si une application managée est en cours d’installation ou si la stratégie système a été spécifiée pour des privilèges élevés. Toutes les actions personnalisées nécessitant des privilèges élevés doivent inclure l' [action personnalisée](custom-action-in-script-execution-options.md) MsidbCustomActionTypeInScript et msidbCustomActionTypeNoImpersonate In-Script les options d’exécution dans le type d’action personnalisé. Cela est illustré par l’exemple de [l’utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md).

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>Si vous utilisez des assemblys, suivez les bonnes pratiques d’assembly

Si votre package utilise des [assemblys](assemblies.md)logiciels, suivez les instructions relatives à l' [Ajout d’assemblys à un package](adding-assemblies-to-a-package.md), à la [mise à jour des assemblys](updating-assemblies.md)et à [l’installation et](installing-and-removing-assemblies.md)à la suppression d’assemblys.

## <a name="do-not-ship-concurrent-installations"></a>N’expédiez pas d’installations simultanées.

les [installations simultanées](concurrent-installations.md), également appelées installations imbriquées, installent un autre Windows Installer package lors d’une installation en cours d’exécution. L’utilisation d’installations simultanées n’est pas une bonne pratique, car elles sont difficiles à traiter par les clients. L’application de correctifs et la mise à niveau peuvent ne pas fonctionner avec des installations simultanées. l’alternative recommandée à l’utilisation des installations simultanées consiste à utiliser à la place une application d’installation et un gestionnaire d’interface utilisateur externe pour installer plusieurs packages de Windows Installer de manière séquentielle.

Pour plus d’informations sur l’utilisation d’un gestionnaire d’interface utilisateur externe, consultez [surveillance d’une installation à l’aide de MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md). Pour plus d’informations sur l’utilisation d’un gestionnaire externe basé sur les enregistrements, consultez [surveillance d’une installation à l’aide de MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).

Les installations simultanées sont parfois utilisées dans des environnements d’entreprise contrôlés pour installer des applications qui ne sont pas destinées au public. Suivez ces instructions si vous décidez d’utiliser des installations simultanées.

-   N’utilisez pas d’installations simultanées pour installer ou mettre à jour un produit d’expédition.
-   Les installations simultanées ne doivent pas partager de composants.
-   Une installation d’administration ne doit pas contenir d’installation simultanée.
-   Le ProgressBars intégré ne doit pas être utilisé avec des installations simultanées.
-   Les ressources qui doivent être publiées ne doivent pas être installées par une installation simultanée.
-   Un package qui effectue une installation simultanée d’une application doit également désinstaller l’application simultanée lorsque le produit parent est désinstallé. Une installation imbriquée existe dans le contexte du produit parent dans Ajout/suppression de programmes dans le panneau de configuration.

## <a name="keep-package-names-and-package-codes-consistent"></a>Assurez la cohérence des noms de packages et des codes de package.

Le fichier .msi peut recevoir n’importe quel nom qui aide les utilisateurs à identifier le package, mais le nom ne doit pas être modifié sans modifier également le code du produit.

-   donnez à votre .msi fichier un nom convivial qui permet à l’utilisateur d’identifier le contenu du package Windows Installer.
-   Le [Code du produit](product-codes.md) est l’identification principale d’une application et doit changer chaque fois qu’il existe une mise à jour complète de l’application. Pour plus d’informations, consultez [**ProductCode**](productcode.md) et [modification du code du produit](changing-the-product-code.md). La modification du nom du fichier .msi de l’application est considérée comme une modification complète et requiert toujours une modification correspondante du code du produit pour maintenir la cohérence.
-   Le [Code du package](package-codes.md) est l’identificateur principal utilisé par le programme d’installation pour rechercher et valider le package approprié pour une installation donnée. Deux fichiers de .msi non identiques ne doivent jamais avoir le même code de package. Si un package est modifié sans modifier le code du package, le programme d’installation peut ne pas utiliser le package le plus récent si les deux sont toujours accessibles au programme d’installation. Le code du package est stocké dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) du flux d’informations de [synthèse](summary-information-stream.md).
-   Notez que les lettres du code du produit et des [GUID](guid.md) du code du package doivent toutes être en majuscules.

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>N’utilisez pas les tables SelfReg et TypeLib.

-   Les auteurs de packages d’installation sont fortement recommandés pour utiliser l’inscription automatique et la table [Selfreg](selfreg-table.md) . Au lieu de cela, ils doivent inscrire des modules en créant une ou plusieurs tables dans le [groupe tables du Registre](registry-tables-group.md). la plupart des avantages de la Windows Installer sont perdus avec l’inscription automatique, car les routines d’auto-inscription ont tendance à masquer les informations de configuration critiques. Pour obtenir la liste des raisons pour lesquelles éviter l’auto-enregistrement, consultez la [table Selfreg](selfreg-table.md).
-   Les auteurs de packages d’installation sont fortement recommandés par rapport à l’utilisation de la table [TypeLib](typelib-table.md) . Au lieu d’utiliser la table TypeLib, inscrivez les bibliothèques de types à l’aide de la table [Registry](registry-table.md) . Si une installation qui utilise la table TypeLib échoue et doit être restaurée, la restauration peut ne pas restaurer l’état de l’ordinateur qui existait avant la restauration.

## <a name="provide-the-option-to-install-without-a-user-interface"></a>Fournissez l’option d’installation sans interface utilisateur.

Les administrateurs préfèrent souvent déployer des applications au sein d’une entreprise sans intervention de l’utilisateur. Il est recommandé de permettre à votre application de fournir la possibilité d’être installée avec le [niveau d’interface utilisateur](user-interface-levels.md) aucun.

-   Utilisez les [propriétés publiques](public-properties.md) pour les informations de configuration. Les administrateurs peuvent fournir ces informations sur la ligne de commande.
-   Ne pas exiger que l’installation dépende des informations collectées à partir de l’interaction de l’utilisateur avec les boîtes de dialogue. Ces informations ne sont pas disponibles au cours d’une installation sans assistance.
-   Ne redémarrez pas automatiquement l’ordinateur de l’utilisateur au cours d’une installation sans assistance.
-   Les administrateurs peuvent définir le niveau de l' [interface utilisateur](user-interface-levels.md) lors de l’installation à l’aide de l' [option de ligne de commande](command-line-options.md) « /q ». Le niveau de l’interface utilisateur peut également être défini par programme avec un appel à [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>Évitez d’utiliser la stratégie AlwaysInstallElevated a.

Si la stratégie [AlwaysInstallElevated a](alwaysinstallelevated.md) n’est pas définie, les applications non distribuées par l’administrateur sont installées à l’aide des privilèges de l’utilisateur et seules les applications gérées obtiennent des privilèges élevés. la définition de cette stratégie indique à Windows Installer d’utiliser des autorisations système lors de l’installation de l’application sur le système. Cette méthode peut ouvrir un ordinateur à un risque de sécurité, car lorsque cette stratégie est définie, un utilisateur non-administrateur peut exécuter des installations avec des privilèges [*élevés*](e-gly.md) et accéder à des emplacements sécurisés sur l’ordinateur. Il est recommandé d’utiliser une autre méthode que la stratégie AlwaysInstallElevated a lors de l' [installation d’un package avec des privilèges élevés pour une application non-administrateur ou une](installing-a-package-with-elevated-privileges-for-a-non-admin.md) mise à [jour corrective d’Applications gérées Per-User](patching-per-user-managed-applications.md).

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>Activez la stratégie DisableMedia pour limiter l’installation non autorisée.

La stratégie [DisableMedia](disablemedia.md) peut empêcher l’installation non autorisée d’applications. Lorsque cette stratégie est activée, les utilisateurs et les administrateurs qui exécutent une installation de maintenance d’un produit ne peuvent pas utiliser la boîte de dialogue Parcourir pour parcourir les sources de média, telles que les CD-ROM, pour les sources d’autres produits installables. La recherche d’autres produits est empêchée, que l’installation soit effectuée avec des privilèges élevés. Il est toujours possible pour l’utilisateur de réinstaller le produit à partir d’un support si celui-ci possède une source de média correctement libellée.

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>Conservez les fichiers sources du package d’origine sécurisés et disponibles pour les utilisateurs.

dans certains cas, la source d’origine du package de Windows Installer peut être nécessaire pour installer à la demande, réparer ou mettre à jour une application. Si le programme d’installation ne parvient pas à localiser une source disponible, il est invité à fournir un média ou à accéder à un emplacement réseau contenant les sources nécessaires. Il est recommandé de s’assurer que le programme d’installation a les sources dont il a besoin sans avoir à demander à l’utilisateur.

-   Utilisez des [signatures numériques et des fichiers CAB externes](digital-signatures-and-external-cabinet-files.md) pour vous assurer que les sources d’origine utilisées par le programme d’installation sont sécurisées. Une image source non compressée stockée dans un emplacement public n’est pas sécurisée.
-   Incluez une liste complète de chemins d’accès source réseau ou URL au package d’installation de l’application dans la propriété [**SourceList**](sourcelist.md) .
-   Utilisez un partage système de fichiers DFS (DFS) pour le chemin d’accès source.
-   utilisez l’API Windows Installer pour récupérer et modifier les informations de liste source pour les applications et les correctifs Windows Installer. Pour plus d’informations, consultez [gestion des sources d’installation](managing-installation-sources.md).
-   utilisez les méthodes et les propriétés de l’objet du [**programme d’installation**](installer-object.md), l’objet [**Product**](product-object.md)et l' [**objet Patch**](patch-object.md) pour récupérer et modifier les informations de la liste source pour Windows Installer applications et les correctifs.
-   Adhérez aux points listés dans [empêcher un correctif d’exiger l’accès aux points de source d’installation d’origine](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) pour réduire la possibilité que votre correctif nécessite l’accès aux sources d’origine.
-   Stockez les fichiers sources du package dans un emplacement qui n’est pas le dossier temporaire du système. Windows Les fichiers sources du programme d’installation stockés dans le dossier temporaire peuvent devenir indisponibles pour les utilisateurs.

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>Activez la journalisation documentée sur l’ordinateur de l’utilisateur lors du dépannage du déploiement.

[Windows Installer journalisation](windows-installer-logging.md) comprend une option de journalisation détaillée qui peut être activée sur l’ordinateur d’un utilisateur. les informations contenues dans un journal détaillé peuvent être utiles lorsque vous tentez de résoudre les problèmes de déploiement Windows Installer package.

-   Vous pouvez activer la journalisation documentée sur l’ordinateur de l’utilisateur à l’aide des [options de ligne de commande](command-line-options.md), de la propriété [**MsiLogging**](msilogging.md) , de la [stratégie de journalisation](logging.md), de [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)et de la méthode [**EnableLog**](installer-enablelog.md) .
-   une ressource très utile pour interpréter les fichiers journaux de Windows Installer est [Wilogutl.exe](wilogutl-exe.md). Cet outil aide à analyser les fichiers journaux et affiche les solutions suggérées aux erreurs qui se trouvent dans un fichier journal.
-   pour plus d’informations sur l’interprétation des fichiers journaux de Windows Installer, consultez le livre blanc disponible sur le site TechNet : [Windows Installer : avantages et implémentation pour les administrateurs système](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx).
-   L’option de journalisation détaillée doit être utilisée uniquement à des fins de dépannage et ne doit pas être conservée, car elle peut avoir des effets néfastes sur les performances du système et sur l’espace disque. Chaque fois que vous utilisez l’outil Ajout/suppression de programmes dans le panneau de configuration, un nouveau fichier est créé.

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>La désinstallation laisse l’ordinateur de l’utilisateur dans un état propre.

La suppression de l’application est aussi importante que l’installation. lors de la désinstallation d’un package Windows Installer, il ne doit pas faire partie des éléments inutiles sur l’ordinateur de l’utilisateur.

-   Si un fichier qui aurait dû être supprimé de l’ordinateur de l’utilisateur reste installé après l’exécution d’une désinstallation, il se peut que le programme d’installation ne supprime pas le composant contenant le fichier pour une ou plusieurs des raisons décrites dans [suppression des fichiers bloqués](removing-stranded-files.md).
-   Si une application doit être inscrite, créez le package pour supprimer les informations de registre lorsque l’application est désinstallée. Pour plus d’informations, consultez [Ajout ou suppression de clés de registre lors de l’installation ou de la suppression de composants](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). si une application n’est pas inscrite, l’application n’est pas répertoriée dans la fonctionnalité ajout/suppression de programmes du panneau de configuration et ne peut pas être gérée à l’aide de l’Windows Installer.
-   pour masquer une application à partir de la fonctionnalité ajout/suppression de programmes du panneau de configuration tout en étant en mesure d’utiliser la Windows Installer pour gérer l’application, suivez les instructions décrites dans [ajout et suppression d’une application et ne laissant aucune Trace dans le registre](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).
-   Les actions personnalisées doivent être conditionnées pour être exécutées si nécessaire lors de la désinstallation. Il peut s’avérer nécessaire d’exécuter différentes actions personnalisées lors de l’installation et de la désinstallation.
-   Les informations de personnalisation spécifiques à l’utilisateur peuvent être stockées dans un fichier texte sur l’ordinateur. Cela présente l’avantage que le fichier peut être supprimé lors de la désinstallation de l’application, même si l’utilisateur de cette personnalisation n’est pas actuellement connecté.

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>Testez les packages pour un déploiement d’installation par utilisateur et par ordinateur.

Il est conseillé d’autoriser les clients à décider s’il faut déployer un package pour l’installation dans le [contexte d’installation](installation-context.md)par ordinateur ou par utilisateur.

-   Déterminez si l’application doit être disponible uniquement pour des utilisateurs particuliers ou pour tous les utilisateurs de l’ordinateur pendant le processus de développement.
-   Vérifiez que le package fonctionne correctement pour les contextes d’installation par utilisateur et par ordinateur.
-   Rendre le package facilement personnalisable et permettre aux clients de décider s’il faut le déployer par utilisateur ou par ordinateur.

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>Planifiez et testez une stratégie de maintenance avant d’expédier l’application.

Vous devez décider de la façon dont vous envisagez de traiter l’application avant de déployer l’application pour la première fois.

-   Tenez compte des types de mises à jour que vous prévoyez d’utiliser pour traiter votre application à l’avenir. le Windows Installer fournit trois types de mises à jour : [mises à jour de petite taille](small-updates.md), [mise à niveau mineure](minor-upgrades.md)et [mises à niveau majeures](major-upgrades.md). Les différences entre ces deux sujets sont décrites dans la rubrique [correctif et mises à niveau](patching-and-upgrades.md) .
-   Avant d’expédier votre application, testez qu’elle fonctionne comme prévu après la maintenance de chaque type de mise à jour.

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>Réduisez la dépendance des mises à jour sur les sources d’origine.

Si les fichiers sources d’origine sont requis pour mettre à jour votre application, cela peut compliquer la maintenance de l’application. Les méthodes suivantes peuvent aider à réduire la dépendance des mises à jour sur les sources d’origine.

-   Utilisez un [*correctif Delta*](d-gly.md) pour mettre à jour les versions de référence de votre application, telles que la version RTM et les versions de Service Pack. Suivez les instructions relatives à l’utilisation des correctifs Delta décrits dans la rubrique : réduction de la [taille des correctifs](reducing-patch-size.md).
-   Suivez les recommandations indiquées dans la rubrique : [empêcher un correctif de demander l’accès à la source d’installation d’origine](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

## <a name="do-not-distribute-unserviceable-merge-modules"></a>Ne distribuez pas les modules de fusion non desservis.

Les applications ne doivent pas dépendre des [modules de fusion](merge-modules.md) pour l’installation du composant si le propriétaire du module de fusion et le propriétaire de l’application sont différents. Cela peut compliquer la maintenance de l’application, car les deux propriétaires doivent coordonner la mise à jour de l’application ou du module. Sans connaître toutes les applications qui ont utilisé le module de fusion, le propriétaire de l’application n’est pas en mesure de mettre à jour le module de fusion sans risque que la mise à jour puisse être incompatible avec une autre application. le propriétaire du module de fusion n’a pas de méthode directe pour mettre à jour les packages Windows Installer qui ont déjà installé le module de fusion.

-   envisagez de fournir les composants nécessaires aux utilisateurs comme une autre installation de Windows Installer.

## <a name="avoid-patching-administrative-installations"></a>Évitez d’appliquer des correctifs aux installations administratives.

fournissez sur un réseau une [installation administrative](administrative-installation.md) du package de Windows Installer d’origine de votre application pour permettre aux membres d’un groupe de travail d’installer l’application. Les utilisateurs de cette image administrative doivent ensuite appliquer des mises à jour à l’instance locale de l’application située sur leur ordinateur. Cela permet aux utilisateurs de synchroniser avec l’image administrative. L’application de mises à jour à l’installation administrative n’est pas recommandée pour les raisons suivantes.

-   La taille et la latence du téléchargement requises par les utilisateurs pour obtenir une mise à jour sont accrues par rapport au téléchargement d’un correctif. la totalité du package Windows Installer mis à jour et des fichiers sources doivent être téléchargés, replacés en cache et réinstallés.
-   Les utilisateurs ne sont pas en mesure d' [installer à la demande](installation-on-demand.md) et de réparer des applications à partir d’une installation administrative mise à jour jusqu’à ce qu’ils replacent et réinstallent l’application.
-   L’application d’un correctif à une installation d’administration supprime la signature numérique du package. Un administrateur doit abandonner le package. pour plus d’informations sur l’utilisation des signatures numériques, consultez [signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md).
-   De nombreux correctifs binaires ciblent l’image RTM de l’application et nécessitent une version de fichier antérieure. L’instance locale d’une application installée à partir d’une installation d’administration mise à jour peut ne pas fonctionner avec d’autres mises à jour. De nombreuses applications de correctifs binaires peuvent échouer.
-   L’application d’un correctif à une installation administrative met à jour les fichiers sources et le fichier .msi, mais ne marque pas l’image réseau avec des informations sur la mise à jour. Les utilisateurs ne peuvent pas déterminer quelles mises à jour ont été reçues de l’installation d’administration. Cela rend impossible la séquence des mises à jour appliquées côté utilisateur avec celles déjà appliquées côté image administrative.
-   Les correctifs appliqués à une installation administrative ne sont pas des [correctifs](uninstallable-patches.md)qui ne peuvent pas être installés. Cela peut empêcher le code du package mis en cache sur l’ordinateur de l’utilisateur de devenir différent du code du package sur l’installation d’administration. Si le code de package mis en cache sur l’ordinateur de l’utilisateur est différent de celui utilisé lors de l’installation administrative, réinstallez l’application à partir de l’installation administrative, puis corrigez l’ordinateur client.
-   Si vous décidez d’appliquer de petites mises à jour en appliquant des correctifs à une image administrative, suivez les instructions décrites dans la rubrique : [application de petites mises à jour en corrigeant une image administrative](applying-small-updates-by-patching-an-administrative-image.md).

## <a name="register-updates-to-run-with-elevated-privilege"></a>Enregistrez les mises à jour à exécuter avec des privilèges élevés.

à partir de Windows Installer 3,0, il est possible d’appliquer des correctifs à une application qui a été installée dans un contexte géré par l’utilisateur, une fois que le correctif a été inscrit comme ayant des privilèges élevés. vous ne pouvez pas appliquer de correctifs aux applications installées dans un contexte géré par utilisateur à l’aide des versions de Windows Installer antérieures à la version 3,0.

-   Utilisez la méthode [**SourceListAddSource**](patch-sourcelistaddsource.md) ou la fonction [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) pour inscrire un package de correctifs comme ayant des privilèges élevés. Suivez les instructions et les exemples fournis dans [application des correctifs Per-User applications gérées](patching-per-user-managed-applications.md).
-   lors de l’exécution de Windows Installer version 4,0 sur Windows Vista, vous pouvez également utiliser la mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md) pour permettre aux auteurs d’installations Windows Installer d’identifier les correctifs signés numériquement qui peuvent être appliqués ultérieurement par des utilisateurs non-administrateurs. Cette fonction est disponible uniquement avec l’installation des packages dans le contexte d' [installation](installation-context.md) par ordinateur (ALLUSERS = 1).
-   Vérifiez que la mise à jour corrective des privilèges minimaux n’a pas été désactivée en définissant la propriété [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) ou la stratégie [DisableLUAPatching](disableluapatching.md) .

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>Utilisez la table MsiPatchSequence pour séquencer les correctifs.

Incluez une [table MsiPatchSequence](msipatchsequence-table.md) dans votre package et ajoutez des informations sur le séquencement des correctifs. à partir de Windows Installer version 3,0, le programme d’installation peut utiliser la Table MsiPatchSequence lors de l' [installation de plusieurs correctifs](installing-multiple-patches.md) pour déterminer la meilleure séquence d’application corrective. utilisez les instructions décrites dans le livre blanc [sur le séquencement des correctifs dans Windows Installer version 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) pour la définition des familles de correctifs.

-   Si possible, spécifiez tous les correctifs comme appartenant à une seule famille de correctifs. Dans de nombreux cas, une seule famille de correctifs offre suffisamment de souplesse pour séquencer les correctifs. La complexité de la création augmente lorsque plusieurs familles de correctifs sont utilisées. Attribuez un nom explicite à la famille de correctifs et affectez des valeurs de séquence dans cette famille de correctifs qui augmentent au fil du temps. Suivez l' [exemple de correctifs multiples](multiple-patching-example.md) pour appliquer des correctifs dans l’ordre dans lequel ils ont été émis.
-   Utilisez la [table PatchSequence](patchsequence-table--patchwiz-dll-.md) dans [Patchwiz.dll](patchwiz-dll.md) pour générer les informations dans la [table MsiPatchSequence](msipatchsequence-table.md). la version de PATCHWIZ.DLL qui a été publiée avec Windows Installer 3,0 peut générer automatiquement des informations sur le séquencement des correctifs. Pour plus d’informations sur l’ajout d’un nouveau correctif, consultez génération d’informations sur les [séquences de correctifs](generating-patch-sequence-information---patchwiz-dll-.md). pour plus d’informations sur les scénarios de séquencement des correctifs, consultez le livre blanc : mise [en séquence des correctifs dans Windows Installer version 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3).

## <a name="test-the-installation-package-thoroughly"></a>Testez soigneusement le package d’installation.

testez l’installation, la réparation et la suppression correctes de votre package Windows Installer. Vous pouvez diviser votre processus de test en éléments suivants.

-   Test d’installation : Testez l’installation avec toutes les combinaisons possibles de fonctionnalités d’application. Testez tous les types d’installation, y compris [l’installation administrative](administrative-installation.md), la [restauration](rollback-installation.md)et l’installation à [la demande](installation-on-demand.md). Essayez toutes les méthodes d’installation possibles, notamment en cliquant sur le fichier .msi, sur les [options de ligne de commande](command-line-options.md)et en installant à partir du panneau de configuration. Teste que le package peut être installé par les utilisateurs dans tous les contextes de privilège possibles. Essayez d’installer le package une fois qu’il a été déployé par toutes les méthodes possibles. activez la [journalisation des Windows Installer](windows-installer-logging.md) pour chaque test et corrigez toutes les erreurs trouvées dans le journal du programme d’installation et le journal des événements.
-   Test de l’interface utilisateur : testez le package lorsqu’il est installé avec tous les [niveaux d’interface utilisateur](user-interface-levels.md)possibles. Testez le package installé sans interface utilisateur et toutes les informations fournies par le biais de l’interface utilisateur. Assurez-vous que l’interface utilisateur est [accessible](accessibility.md) et que l’interface utilisateur fonctionne comme prévu pour différentes résolutions d’écran et tailles de police.
-   Test de maintenance et de réparation-test que le package peut gérer les [correctifs et les mises à niveau](patching-and-upgrades.md) fournis par une [petite mise à jour](small-updates.md), une [mise à niveau mineure](minor-upgrades.md)et des mises à niveau [majeures](major-upgrades.md). Avant de déployer le package, écrivez une mise à jour d’évaluation de chaque type et essayez de l’appliquer au package d’origine.
-   Désinstaller le test : Vérifiez que lorsque le package est supprimé, il ne laisse pas de parties inutiles sur l’ordinateur de l’utilisateur et que seules les informations appartenant au package ont été supprimées. Redémarrez l’ordinateur de test après la désinstallation du package et vérifiez l’intégrité des outils système communs et d’autres applications standard. Teste que le package peut être supprimé par les utilisateurs dans tous les contextes de privilège possibles. Testez toutes les méthodes pour supprimer le package, cliquez sur le fichier .msi, essayez les [options de ligne de commande](command-line-options.md), puis essayez de supprimer le package à partir du panneau de configuration. activez la [journalisation des Windows Installer](windows-installer-logging.md) pour chaque test et corrigez toutes les erreurs trouvées dans le journal du programme d’installation et le journal des événements.
-   Test des fonctionnalités du produit : Assurez-vous que l’application fonctionne comme prévu après l’installation, la réparation ou la suppression du package.

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>Corrigez toutes les erreurs de validation avant de déployer un package d’installation nouveau ou révisé.

exécutez la [validation du package](package-validation.md) sur un package de Windows Installer nouveau ou révisé avant de tenter de l’installer pour la première fois. la Validation vérifie les erreurs de création dans la base de données Windows Installer. Toute tentative d’installation d’un package qui n’est pas validé peut endommager le système de l’utilisateur.

-   Vous pouvez valider votre package à l’aide de [Orca.exe](orca-exe.md) ou [Msival2.exe](msival2-exe.md). les deux outils sont fournis avec le SDK Windows. Les fournisseurs tiers peuvent également intégrer le système de validation des GLACEs dans leur environnement de création.
-   Vous pouvez utiliser l’ensemble standard d' [évaluateurs de cohérence internes-ICEs](internal-consistency-evaluators-ices.md) inclus dans les fichiers. CUB fournis avec le kit de développement logiciel (SDK), ou personnaliser la validation en [générant une glace](building-an-ice.md) et en l’ajoutant au fichier. CUB.
-   Vous pouvez utiliser la Evalcom2.dll pour implémenter l’automatisation de la [validation](validation-automation.md) des packages d’installation et des modules de fusion.

## <a name="author-a-secure-installation"></a>Créer une installation sécurisée.

Suivez ces instructions lors du développement de votre package pour aider à maintenir un environnement sécurisé lors de l’installation.

-   [Instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md)
-   [Instructions pour la sécurisation des packages sur les ordinateurs verrouillés](guidelines-for-securing-packages-on-locked-down-computers.md)
-   [Instructions pour la sécurisation des actions personnalisées](guidelines-for-securing-custom-actions.md)

## <a name="use-pmsihandle-instead-of-handle"></a>Utiliser PMSIHANDLE au lieu de HANDLE

Les variables de type **PMSIHANDLE** sont définies dans msi. h. Il est recommandé que votre application utilise le type **PMSIHANDLE** , car le programme d’installation ferme les objets **PMSIHANDLE** à mesure qu’ils sont hors de portée, tandis que votre application doit fermer **MSIHANDLE** objets en appelant [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).

Par exemple, si vous utilisez du code comme celui-ci :

``` syntax
MSIHANDLE hRec = MsiCreateRecord(3);
```

Remplacez-le par :

``` syntax
PMSIHANDLE hRec = MsiCreateRecord(3);
```

 

 
