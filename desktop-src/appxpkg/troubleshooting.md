---
title: Résolution des problèmes d’empaquetage, de déploiement et d’interrogation des applications Windows
description: Utilisez ces suggestions pour résoudre les problèmes que vous rencontrez lors de l’empaquetage, du déploiement ou de l’interrogation d’un package d’application.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 09/10/2021
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: 4bea9a6ce0504822c65ae9016bd3e37b1806eac2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126792616"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Résolution des problèmes d’empaquetage, de déploiement et d’interrogation des applications Windows

utilisez ces suggestions pour résoudre les problèmes que vous rencontrez lors de l’empaquetage, du déploiement ou de l’interrogation d’un package d’application Windows (. msix/. appx) en tant que développeur.

> [!NOTE]
> Cet article s’adresse aux développeurs. si vous n’êtes pas un développeur et que vous recherchez de l’aide sur une erreur d’installation de Windows application, consultez [prise en charge](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10)de l’Windows.

## <a name="get-diagnostic-information"></a>Recevoir des informations de diagnostic

Lorsqu’une API échoue, elle retourne un code d’erreur qui décrit le problème. Si le code d’erreur ne fournit pas suffisamment d’informations, vous trouverez plus d’informations de diagnostic dans les journaux des événements détaillés.

Pour accéder aux journaux des événements de Packaging et de déploiement à l’aide de **Observateur d’événements**, procédez comme suit :

1. Effectuez l’une des opérations suivantes :

    * dans le menu Windows, cliquez sur **démarrer** , tapez **observateur d’événements** et **appuyez sur entrée**.
    * Exécutez **eventvwr. msc**.

2. dans la page de gauche, développez  >  **journaux des Applications et des Services** observateur d’événements (Local)  >  **Microsoft**  >  **Windows**.
3. Recherchez les journaux disponibles dans les catégories suivantes :

    * **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/opérationnel**
    * **AppXDeployment-serveur**  >  **Microsoft-Windows-AppXDeploymentServer/opérationnel**

Commencez par examiner les journaux sous **AppXDeployment-Server**. Si l’erreur a été provoquée par **0x80073CF0** ou **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, des détails supplémentaires peuvent être présents dans les journaux **AppxpackagingOM** .

Vous pouvez également utiliser la commande [AppxLog](/powershell/module/appx/get-appxlog) dans PowerShell pour récupérer les premiers événements journalisés. L’exemple suivant affiche les journaux associés à l’opération de déploiement la plus récente.

```PowerShell
Get-Appxlog
```

L’exemple suivant affiche les journaux associés à l’opération de déploiement la plus récente dans une table interactive dans une fenêtre distincte.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Common error codes (Codes d’erreur courants)

Ce tableau répertorie certains des codes d’erreur les plus courants. Si vous avez besoin d’aide pour l’une de ces erreurs ou si vous rencontrez un code d’erreur qui ne figure pas dans cette liste, consultez [options d’aide supplémentaires](#get-additional-help).


| Code d'erreur | Valeur | Description et causes possibles | 
|------------|-------|---------------------------------|
| <strong>E_FILENOTFOUND</strong> | 0x80070002 | Fichier ou chemin d'accès introuvable. Cela peut se produire pendant une validation de TypeLib COM exige que le chemin d’accès au répertoire existe réellement dans votre package MSIX.<br /> | 
| <strong>ERROR_BAD_FORMAT</strong> | 0x8007000B | Le package n’est pas formaté correctement et doit être recréé ou resigné.<br /> Vous pouvez obtenir cette erreur en cas de discordance entre le nom d’objet du certificat de signature et le nom de l’éditeur de AppxManifest.xml.<br /> Consultez <a href="how-to-sign-a-package-using-signtool.md">Comment signer un package d’application à l’aide de SignTool</a>.<br /> | 
| <strong>E_INVALIDARG</strong> | 0x80070057 | Un ou plusieurs arguments ne sont pas valides. Si vous consultez le journal des événements AppXDeployment-Server et que vous voyez l’événement suivant : « lors de l’installation du package, le système n’a pas pu inscrire l’extension Windows. repositoryExtension en raison de l’erreur suivante : le paramètre est incorrect. » <br /> vous pouvez obtenir cette erreur si les éléments de manifeste DisplayName ou Description contiennent des caractères interdits par Windows pare-feu, par exemple `|` , en raison du fait que Windows ne peut pas créer le profil AppContainer pour le package. Supprimez ces caractères du manifeste et essayez d’installer le package. <br /> | 
| <strong>ERROR_INSTALL_OPEN_</strong><br /><strong>PACKAGE_FAILED</strong><br /> | 0x80073CF0 | Impossible d’ouvrir le package.<br /> Causes possibles :<br /><ul><li>Le package n'est pas signé.</li><li>Le nom de l’éditeur ne correspond pas à l’objet du certificat de signature.</li><li>Le préfixe file://est manquant ou le package est introuvable à l’emplacement spécifié.</li></ul>Pour plus d’informations, consultez le journal des événements <strong>AppxPackagingOM</strong> .<br /> | 
| <strong>ERROR_INSTALL_PACKAGE_</strong><br /><strong>NOT_FOUND</strong><br /> | 0x80073CF1 | Le package est introuvable.<br /> Vous pouvez obtenir cette erreur lors de la suppression d’un package qui n’est pas installé pour l’utilisateur actuel.<br /> | 
| <strong>ERROR_INSTALL_INVALID_</strong><br /><strong>Packages</strong><br /> | 0x80073CF2 | Les données du package ne sont pas valides.<br /> | 
| <strong>ERROR_INSTALL_RESOLVE_</strong><br /><strong>DEPENDENCY_FAILED</strong><br /> | 0x80073CF3 | Échec de la mise à jour du package, d'une dépendance ou validation de conflit.<br /> Causes possibles :<br /><ul><li>Le package entrant est en conflit avec un package installé.</li><li>Une dépendance de package spécifiée est introuvable.</li><li>Le package ne prend pas en charge l’architecture de processeur correcte.</li></ul>Pour plus d’informtion, consultez le journal des événements <strong>AppXDeployment-Server</strong> .<br /> | 
| <strong>ERROR_INSTALL_OUT_</strong><br /><strong>OF_DISK_SPACE</strong><br /> | 0x80073CF4 | L’espace disque est insuffisant sur votre ordinateur. Libérez de l’espace et réessayez.<br /> | 
| <strong>ERROR_INSTALL_NETWORK_</strong><br /><strong>TOUTE</strong><br /> | 0x80073CF5 | Le package ne peut pas être téléchargé.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>REGISTRATION_FAILURE</strong><br /> | 0x80073CF6 | Le package ne peut pas être inscrit.<br /> Pour plus d’informations, consultez le journal des événements <strong>AppXDeployment-Server</strong> .<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>DEREGISTRATION_EFAILURE</strong><br /> | 0x80073CF7 | Impossible d’annuler l’inscription du package.<br /> Vous pouvez obtenir cette erreur lors de la suppression d’un package.<br /> Pour plus d’informations, consultez le journal des événements <strong>AppXDeployment-Server</strong> .<br /> | 
| <strong>ERROR_INSTALL_CANCEL</strong> | 0x80073CF8 | L’utilisateur a annulé la demande d’installation.<br /> | 
| <strong>ERROR_INSTALL_FAILED</strong> | 0x80073CF9 | Échec de l’installation du package. Contactez le fournisseur du logiciel.<br /> Pour plus d’informations, consultez le journal des événements <strong>AppXDeployment-Server</strong> .<br /> | 
| <strong>ERROR_REMOVE_FAILED</strong> | 0x80073CFA | Échec de la suppression du package.<br /> Vous pouvez obtenir cette erreur pour les échecs qui se produisent pendant la désinstallation du package.<br /> Pour plus d’informations, consultez <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.<br /> | 
| <strong>ERROR_PACKAGE_</strong><br /><strong>ALREADY_EXISTS</strong><br /> | 0x80073CFB | Le package fourni est déjà installé, et la réinstallation du package est bloquée. <br /> Vous pouvez obtenir cette erreur si vous installez un package qui n’est pas identique au niveau du bit au package déjà installé. Notez que la signature numérique fait également partie du package. Par conséquent, si un package est reconstruit ou resigné, il n’est plus identique au niveau du bit au package précédemment installé. Deux options possibles pour corriger cette erreur sont les suivantes : (1) incrémenter le numéro de version de l’application, puis reconstruire et abandonner le package (2) Supprimez l’ancien package pour chaque utilisateur sur le système avant d’installer le nouveau package. <br /> | 
| <strong>ERROR_NEEDS_REMEDIATION</strong> | 0x80073CFC | L’application ne peut pas être démarrée. Essayez de réinstaller l’application.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>PREREQUISITE_FAILED</strong><br /> | 0x80073CFD | Impossible de satisfaire un prérequis d’installation spécifié.<br /> | 
| <strong>ERROR_PACKAGE_</strong><br /><strong>REPOSITORY_CORRUPTED</strong><br /> | 0x80073CFE | Le référentiel du package est endommagé.<br /> Vous pouvez recevoir cette erreur si le dossier référencé par cette clé de Registre n’existe pas ou est endommagé : <br /><strong>HKLM\Software\Microsoft\ Windows\</strong><br /><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong><br /> Pour récupérer à partir de cet État, actualisez votre PC.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>POLICY_FAILURE</strong><br /> | 0x80073CFF | Pour installer cette application, vous avez besoin d’une licence de développeur ou d’un système compatible chargement. <br /> Vous pouvez recevoir cette erreur si le package ne remplit pas l’une des conditions suivantes :<br /><ul><li>l’application est déployée à l’aide de la touche F5 dans Visual Studio sur un ordinateur disposant d’une licence de développeur Windows.</li><li>le package est signé avec une signature Microsoft et déployé dans le cadre de Windows ou à partir du Microsoft Store.</li><li>le package est signé avec une signature approuvée et installé sur un ordinateur disposant d’une licence de développeur, d’un ordinateur joint à un domaine avec la stratégie AllowAllTrustedApps activée, ou d’un ordinateur avec une licence Windows chargement avec la stratégie AllowAllTrustedApps activée.</li></ul> | 
| <strong>ERROR_PACKAGE_UPDATING</strong> | 0x80073D00 | L’application ne peut pas être démarrée car elle est en cours de mise à jour.<br /> | 
| <strong>ERROR_DEPLOYMENT_</strong><br /><strong>BLOCKED_BY_POLICY</strong><br /> | 0x80073D01 | L’opération de déploiement de package est bloquée par la stratégie. Contactez votre administrateur système.<br /> Causes possibles :<br /><ul><li>Le déploiement de package est bloqué par les stratégies de contrôle d’application.</li><li>Le déploiement du package est bloqué par la stratégie « autoriser les opérations de déploiement dans les profils spéciaux ».</li></ul>L’une des raisons possibles est la nécessité d’un profil itinérant. Pour plus d’informations sur la configuration des profils utilisateur itinérants sur des comptes d’utilisateur, consultez <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">déployer des profils utilisateur itinérants</a>. Si aucune stratégie n’est configurée sur votre système et que vous voyez toujours cette erreur, vous êtes peut-être connecté avec un profil temporaire. Déconnectez-vous et reconnectez-vous, puis recommencez l’opération.<br /> | 
| <strong>ERROR_PACKAGES_IN_USE</strong> | 0x80073D02 | Le package n’a pas pu être installé car les ressources qu’il modifie sont actuellement utilisées.<br /> | 
| <strong>ERROR_RECOVERY_</strong><br /><strong>FILE_CORRUPT</strong><br /> | 0x80073D03 | Le package n’a pas pu être récupéré car les données nécessaires à la récupération sont endommagées.<br /> | 
| <strong>ERROR_INVALID_</strong><br /><strong>STAGED_SIGNATURE</strong><br /> | 0x80073D04 | La signature n’est pas valide. Pour s’inscrire en mode développeur, AppxSignature. p7x et AppxBlockMap.xml doivent être valides ou ne doivent pas être présents.<br /> si vous êtes développeur à l’aide de la touche F5 avec Visual Studio, assurez-vous que votre répertoire de projet créé ne contient pas de signature ou de fichiers de mappage de bloc à partir des versions précédentes du package.<br /> | 
| <strong>ERROR_DELETING_EXISTING_</strong><br /><strong>APPLICATIONDATA_STORE_FAILED</strong><br /> | 0x80073D05 | Une erreur s’est produite lors de la suppression des données d’application précédemment existantes du package.<br /> Vous pouvez recevoir cette erreur si le <a href="/previous-versions/hh441475(v=vs.110)">simulateur</a> est en cours d’exécution. Fermez le simulateur. Vous pouvez également obtenir cette erreur si des fichiers sont ouverts dans les données de l’application (par exemple, si un fichier journal est ouvert dans un éditeur de texte).<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>PACKAGE_DOWNGRADE</strong><br /> | 0x80073D06 | Le package n’a pas pu être installé car une version plus récente de ce package est déjà installée.<br /> | 
| <strong>ERROR_SYSTEM_</strong><br /><strong>NEEDS_REMEDIATION</strong><br /> | 0x80073D07 | Une erreur a été détectée dans un fichier binaire système. Pour résoudre le problème, essayez d’actualiser le PC. <br /> | 
| <strong>ERROR_APPX_INTEGRITY_</strong><br /><strong>FAILURE_EXTERNAL</strong><br /> | 0x80073D08 | un fichier binaire non Windows endommagé a été détecté sur le système. <br /> | 
| <strong>ERROR_RESILIENCY_</strong><br /><strong>FILE_CORRUPT</strong><br /> | 0x80073D09 | Impossible de reprendre l’opération, car les données nécessaires à la récupération sont endommagées. <br /> | 
| <strong>ERROR_INSTALL_FIREWALL_</strong><br /><strong>SERVICE_NOT_RUNNING</strong><br /> | 0x80073D0A | impossible d’installer le package, car le service de pare-feu Windows n’est pas en cours d’exécution. activez le service de pare-feu Windows, puis réessayez.<br /> | 
| <strong>ERROR_PACKAGE_MOVE_FAILED</strong> | 0x80073D0B | Échec de l’opération de déplacement du package.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>NOT_EMPTY</strong><br /> | 0x80073D0C | L’opération de déploiement a échoué, car le volume n’est pas vide.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>OFFLINE</strong><br /> | 0x80073D0D | L’opération de déploiement a échoué car le volume est hors connexion. Pour une mise à jour de package, le volume fait référence au volume installé de toutes les versions de package.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>ENDOMMAGÉ</strong><br /> | 0x80073D0E | L’opération de déploiement a échoué, car le volume spécifié est endommagé.<br /> | 
| <strong>ERROR_NEEDS_REGISTRATION</strong><br /><strong></strong><br /> | 0x80073D0F | L’opération de déploiement a échoué car l’application spécifiée doit être inscrite en premier.<br /> | 
| <strong>ERROR_INSTALL_WRONG_</strong><br /><strong>PROCESSOR_ARCHITECTURE</strong><br /> | 0x80073D10 | L’opération de déploiement a échoué, car le package cible une architecture de processeur incorrecte.<br /> | 
| <strong>ERROR_DEV_SIDELOAD_</strong><br /><strong>LIMIT_EXCEEDED</strong><br /> | 0x80073D11 | Vous avez atteint le nombre maximal de packages faisant développeur autorisés sur cet appareil. Désinstallez un package faisant, puis réessayez.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_</strong><br /><strong>MAIN_PACKAGE</strong><br /> | 0x80073D12 | Un package d’application principal est requis pour installer ce package facultatif. Installez d’abord le package principal, puis réessayez.<br /> | 
| <strong>ERROR_PACKAGE_NOT_</strong><br /><strong>SUPPORTED_ON_FILESYSTEM</strong><br /> | 0x80073D13 | Ce type de package d’application n’est pas pris en charge sur ce système de fichiers.<br /> | 
| <strong>ERROR_PACKAGE_MOVE_</strong><br /><strong>BLOCKED_BY_STREAMING</strong><br /> | 0x80073D14 | L’opération de déplacement du package est bloquée jusqu’à la fin de la diffusion de l’application.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_APPLICATIONID_</strong><br /><strong>NOT_UNIQUE</strong><br /> | 0x80073D15 | Un package d’application principal ou un autre package d’application facultatif possède le même ID d’application que ce package facultatif. Modifiez l’ID de l’application pour le package facultatif afin d’éviter les conflits.<br /> | 
| <strong>ERROR_PACKAGE_STAGING_</strong><br /><strong>ONHOLD</strong><br /> | 0x80073D16 | Cette session intermédiaire a été conservée pour permettre la hiérarchisation d’une autre opération intermédiaire.<br /> | 
| <strong>ERROR_INSTALL_INVALID_</strong><br /><strong>RELATED_SET_UPDATE</strong><br /> | 0x80073D17 | Impossible de mettre à jour un jeu associé, car le jeu mis à jour n’est pas valide. Tous les packages de l’ensemble associé doivent être mis à jour en même temps.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br /> | 0x80073D18 | Pour un package facultatif avec un point d’entrée FullTrust, le package principal doit disposer de la fonctionnalité <strong>runFullTrust</strong> .<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_USER_LOG_OFF</strong><br /> | 0x80073D19 | Une erreur s’est produite en raison de la fermeture de la session d’un utilisateur.<br /> | 
| <strong>ERROR_PROVISION_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_PROVISIONED</strong><br /> | 0x80073D1A | Une provision facultative de packages nécessite que le package principal de dépendance soit également approvisionné.<br /> | 
| <strong>ERROR_PACKAGES_REPUTATION_</strong><br /><strong>CHECK_FAILED</strong><br /> | 0x80073D1B | Les packages n’ont pas pu <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">Vérifier la réputation SmartScreen</a>.<br /> | 
| <strong>ERROR_PACKAGES_REPUTATION_</strong><br /><strong>CHECK_TIMEDOUT</strong><br /> | 0x80073D1C | L’opération de vérification de la <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">réputation SmartScreen</a> a expiré.<br /> | 
| <strong>ERROR_DEPLOYMENT_OPTION_</strong><br /><strong>NOT_SUPPORTED</strong><br /> | 0x80073D1D | L’option de déploiement actuelle n’est pas prise en charge.<br /> | 
| <strong>ERROR_APPINSTALLER_</strong><br /><strong>ACTIVATION_BLOCKED</strong><br /> | 0x80073D1E | L’activation est bloquée en raison des paramètres de mise à jour. appinstaller pour cette application.<br /> | 
| <strong>ERROR_REGISTRATION_FROM_</strong><br /><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br /> | 0x80073D1F | Les lecteurs distants ne sont pas pris en charge. Utilisez <strong> \\ server\share</strong> pour inscrire un package distant.<br /> | 
| <strong>ERROR_APPX_RAW_</strong><br /><strong>DATA_WRITE_FAILED</strong><br /> | 0x80073D20 | Échec du traitement et de l’écriture des données du package téléchargé sur le disque.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_VOLUME_POLICY_PACKAGE</strong><br /> | 0x80073D21 | L’opération de déploiement a été bloquée en raison d’une stratégie par famille de packages qui limite les déploiements sur un volume non-système. Par stratégie, cette application doit être installée sur le lecteur système, mais elle n’est pas définie par défaut. dans Stockage paramètres, définissez le lecteur système comme emplacement par défaut pour enregistrer le nouveau contenu, puis réessayez l’installation.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_VOLUME_POLICY_MACHINE</strong><br /> | 0x80073D22 | L’opération de déploiement a été bloquée en raison d’une stratégie au niveau de l’ordinateur qui limite les déploiements sur un volume non-système. Par stratégie, cette application doit être installée sur le lecteur système, mais elle n’est pas définie par défaut. dans Stockage paramètres, définissez le lecteur système comme emplacement par défaut pour enregistrer le nouveau contenu, puis réessayez l’installation.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_PROFILE_POLICY</strong><br /> | 0x80073D23 | L’opération de déploiement a été bloquée, car un déploiement de profil spécial n’est pas autorisé (les profils spéciaux sont des profils utilisateur où les modifications sont ignorées une fois que l’utilisateur se déconnecte). Essayez de vous connecter à un compte qui n’est pas un profil spécial. Vous pouvez essayer de vous déconnecter et de vous reconnecter au compte actif, ou essayer de vous connecter à un autre compte.<br /> | 
| <strong>ERROR_DEPLOYMENT_FAILED_</strong><br /><strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br /><strong>DIRECTORY</strong><br /> | 0x80073D24 | L’opération de déploiement a échoué en raison d’un <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">Répertoire de packages mutable</a>en conflit. Pour installer ce package, supprimez le package existant avec le répertoire de packages mutable en conflit.<br /> | 
| <strong>ERROR_SINGLETON_RESOURCE_</strong><br /><strong>INSTALLED_IN_ACTIVE_USER</strong><br /> | 0x80073D25 | L’installation du package a échoué, car une ressource Singleton a été spécifiée et un autre utilisateur sur lequel ce package est installé est connecté. Assurez-vous que tous les utilisateurs actifs sur lesquels le package est installé sont déconnectés et réessayez l’installation.<br /> | 
| ERROR_DIFFERENT_VERSION_<strong></strong><br /><strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br /> | 0x80073D26 | L’installation du package a échoué car une autre version du service est installée. Essayez d’installer une version plus récente du package.<br /> | 
| <strong>ERROR_SERVICE_EXISTS_</strong><br /><strong>AS_NON_PACKAGED_SERVICE</strong><br /> | 0x80073D27 | L’installation du package a échoué, car une version du service existe en dehors d’un package. msix/. Appx. Contactez votre fournisseur de logiciels.<br /> | 
| <strong>ERROR_PACKAGED_SERVICE_</strong><br /><strong>REQUIRES_ADMIN_PRIVILEGES</strong><br /> | 0x80073D28 | L’installation du package a échoué car des privilèges d’administrateur sont requis. Contactez un administrateur pour installer ce package.<br /> | 
| <strong>ERROR_REDIRECTION_TO_</strong><br /><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br /> | 0x80073D29 | Le déploiement du package a échoué, car l’opération aurait été redirigée vers le compte par défaut, lorsque l’appelant ne l’a pas fait.<br /> | 
| <strong>ERROR_PACKAGE_LACKS_</strong><br /><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br /> | 0x80073D2A | Le déploiement du package a échoué, car le package nécessite une capacité à cibler en mode natif cet hôte.<br /> | 
| <strong>ERROR_UNSIGNED_PACKAGE_</strong><br /><strong>INVALID_CONTENT</strong><br /> | 0x80073D2B | Le déploiement du package a échoué, car son contenu n’est pas valide pour un package non signé.<br /> | 
| <strong>ERROR_UNSIGNED_PACKAGE_</strong><br /><strong>INVALID_PUBLISHER_NAMESPACE</strong><br /> | 0x80073D2C | Le déploiement du package a échoué, car son serveur de publication n’est pas dans l’espace de noms non signé.<br /> | 
| <strong>ERROR_SIGNED_PACKAGE_</strong><br /><strong>INVALID_PUBLISHER_NAMESPACE</strong><br /> | 0x80073D2D | Le déploiement du package a échoué, car son serveur de publication n’est pas dans l’espace de noms signé.<br /> | 
| <strong>ERROR_PACKAGE_EXTERNAL_</strong><br /><strong>LOCATION_NOT_ALLOWED</strong><br /> | 0x80073D2E | Le déploiement du package a échoué, car son serveur de publication n’est pas dans l’espace de noms signé.<br /> | 
| <strong>ERROR_INSTALL_FULLTRUST_</strong><br /><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br /> | 0x80073D2F | Une dépendance de l’exécution de l’hôte qui est résolue en un package avec un contenu de confiance totale requiert que le package principal dispose de la fonctionnalité <strong>runFullTrust</strong> .<br /> | 
| <strong>APPX_E_PACKAGING_INTERNAL</strong> | 0x80080200 | L’API de Packaging a rencontré une erreur interne.<br /> | 
| <strong>APPX_E_INTERLEAVING_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080201 | Le package n’est pas valide car son contenu est entrelacé.<br /> | 
| <strong>APPX_E_RELATIONSHIPS_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080202 | Le package n’est pas valide, car il contient des relations OPC.<br /> | 
| <strong>APPX_E_MISSING_</strong><br /><strong>REQUIRED_FILE</strong><br /> | 0x80080203 | Le package n’est pas valide, car un manifeste ou un mappage de bloc est manquant, ou un fichier d’intégrité du code est présent, mais un fichier de signature est manquant.<br /> Assurez-vous que le package ne contient pas un ou plusieurs des fichiers requis suivants :<br /><ul><li>\AppxManifest.xml</li><li>\AppxBlockMap.xml</li></ul>Si le package contient \AppxMetadata\CodeIntegrity.cat, il doit également contenir \AppxSignature.p7x.<br /> | 
| <strong>APPX_E_INVALID_MANIFEST</strong> | 0x80080204 | Le fichier AppxManifest.xml du package n’est pas valide.<br /> | 
| <strong>APPX_E_INVALID_BLOCKMAP</strong> | 0x80080205 | Le fichier AppxBlockMap.xml du package n’est pas valide.<br /> | 
| <strong>APPX_E_CORRUPT_CONTENT</strong> | 0x80080206 | Le contenu du package ne peut pas être lu, car il est endommagé.<br /> | 
| <strong>APPX_E_BLOCK_</strong><br /><strong>HASH_INVALID</strong><br /> | 0x80080207 | La valeur de hachage calculée du bloc ne correspond pas à la valeur de est stockée dans le mappage de bloc.<br /> | 
| <strong>APPX_E_REQUESTED_</strong><br /><strong>RANGE_TOO_LARGE</strong><br /> | 0x80080208 | La plage d’octets demandée est supérieure à 4 Go lorsqu’elle est traduite en plage d’octets de blocs.<br /> | 
| <strong>TRUST_E_NOSIGNATURE</strong> | 0x800B0100 | Aucune signature n’est présente dans l’objet.<br /> Vous pouvez recevoir cette erreur si le package n’est pas signé ou si la signature n’est pas valide. Le package doit être signé pour être déployé.<br /> | 
| <strong>CERT_E_UNTRUSTEDROOT</strong> | 0x800B0109 | Une chaîne de certificats A été traitée, mais se termine par un certificat racine qui n’est pas approuvé par le fournisseur d’approbation.<br /> Consultez <a href="/previous-versions/br230260(v=vs.110)">signature d’un package</a>.<br /> | 
| <strong>CERT_E_CHAINING</strong> | 0x800B010A | Impossible de créer une chaîne de certificats pour une autorité de certification racine de confiance.<br /> Consultez <a href="/previous-versions/br230260(v=vs.110)">signature d’un package</a>.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>SIP_CLIENT_DATA</strong><br /> | 0x80080209 | La structure <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>utilisée pour signer le package ne contenait pas les données requises<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>KEY_INFO</strong><br /> | 0x8008020A | La structure <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> utilisée pour chiffrer ou déchiffrer le package contient des données non valides.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>CONTENTGROUPMAP</strong><br /> | 0x8008020B | Le mappage de groupe de contenu du package. msix/. AppX n’est pas valide.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>APPINSTALLER</strong><br /> | 0x8008020C | Le <a href="/windows/msix/app-installer/app-installer-root">fichier. appinstaller</a> du package n’est pas valide.<br /> | 
| <strong>APPX_E_DELTA_BASELINE_</strong><br /><strong>VERSION_MISMATCH</strong><br /> | 0x8008020D | La version du package de base de référence dans le package delta ne correspond pas à la version du package de base à mettre à jour.<br /> | 
| <strong>APPX_E_DELTA_PACKAGE_</strong><br /><strong>MISSING_FILE</strong><br /> | 0x8008020E | Le package delta ne contient pas de fichier du package mis à jour.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>DELTA_PACKAGE</strong><br /> | 0x8008020F | Le package Delta n’est pas valide.<br /> | 
| <strong>APPX_E_DELTA_APPENDED_</strong><br /><strong>PACKAGE_NOT_ALLOWED</strong><br /> | 0x80080210 | Le package ajouté Delta n’est pas autorisé pour l’opération en cours.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PACKAGING_LAYOUT</strong><br /> | 0x80080211 | Le fichier de disposition d’empaquetage n’est pas valide.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PACKAGESIGNCONFIG</strong><br /> | 0x80080212 | Le fichier packageSignConfig n’est pas valide.<br /> | 
| <strong>APPX_E_RESOURCESPRI_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080213 | Le fichier Resources. pri n’est pas autorisé lorsqu’il n’existe aucun élément de ressource dans le manifeste du package.<br /> | 
| <strong>APPX_E_FILE_</strong><br /><strong>COMPRESSION_MISMATCH</strong><br /> | 0x80080214 | L’état de compression du fichier dans la ligne de base et le package mis à jour ne correspond pas.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PAYLOAD_PACKAGE_EXTENSION</strong><br /> | 0x80080215 | Les extensions non. AppX ne sont pas autorisées pour les packages de charge utile ciblant des plateformes plus anciennes.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br /> | 0x80080216 | Le fichier encryptionExclusionFileList n’est pas valide.<br /> | 


## <a name="applications-dont-start-and-their-names-are-dimmed"></a>Les applications ne démarrent pas et leurs noms sont estompés

sur un ordinateur exécutant Windows 10 ou version ultérieure, vous ne pouvez pas démarrer certaines applications et les noms d’application apparaissent grisés.

![certains noms d’application apparaissent grisés dans le menu Démarrer](./images/app-names-dimmed.png)

Lorsque vous essayez d’ouvrir une application en sélectionnant le nom grisé, vous pouvez recevoir l’un des messages d’erreur suivants :

> Il y a un problème avec \<*application name*> . Contactez votre administrateur système pour le réparer ou le réinstaller  
> Erreur : cette application ne peut pas s’ouvrir

en outre, les entrées d’événements suivantes sont consignées dans le journal « Microsoft-Windows-TWinUI/operational » sous **Applications et Services\Microsoft\ Windows \Apps**:

> nom du journal : Microsoft-Windows-TWinUI/operational  
> Source : Microsoft-Windows-immersif-Shell  
> Date : *Date* de <>  
> ID d’événement : 5960  
> Catégorie de tâche : (5960)  
> Niveau : erreur  
> Mots clés :  
> Description :  
> Activation de l’application Microsoft.BingNews_8wekyb3d8bbwe ! AppexNews pour le Windows. Le lancement du contrat a été bloqué avec l’erreur 0x80073CFC, car son package est dans l’État : modifié.  

### <a name="cause"></a>Cause

Ce problème se produit parce que l’entrée de Registre correspondant à la valeur d’État du package correspondant à l’application a été modifiée.

### <a name="resolution"></a>Résolution

> [!WARNING]
> Des problèmes graves peuvent survenir si vous modifiez le Registre de façon incorrecte à l’aide de l’Éditeur du Registre ou d’une autre méthode. Ces problèmes peuvent nécessiter la réinstallation du système d'exploitation. Microsoft ne peut pas garantir que ces problèmes puissent être résolus. Toute modification du registre relève de votre propre responsabilité.

Pour résoudre ce problème :

1. Démarrez l’éditeur du Registre, puis recherchez la sous-clé **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** .
2. Pour sauvegarder les données de sous-clé, cliquez avec le bouton droit sur **PackageList**, sélectionnez **Exporter**, puis enregistrez les données en tant que fichier de registre.
3. Pour chacune des applications répertoriées dans les entrées de journal de l’ID d’événement 5960, procédez comme suit :  
   1. Recherchez l’entrée **PackageStatus** .
   2. Affectez à **PackageStatus** la valeur zéro (**0**).
   > [!NOTE]  
   > S’il n’existe aucune entrée pour l’application sous **PackageList**, le problème est dû à une autre cause. Dans le cas de l’exemple d’événement de cet article, la sous-clé complète est **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. Redémarrez l'ordinateur.

## <a name="get-additional-help"></a>Obtenir une aide supplémentaire

si vous avez besoin d’aide pour résoudre un problème que vous rencontrez lors de l’empaquetage, du déploiement ou de l’interrogation d’un package d’application Windows (. msix/. appx) en tant que développeur, reportez-vous à ces ressources de support pour développeurs supplémentaires.

- [Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offre des réponses pertinentes et opportunes à vos problèmes techniques à partir d’une communauté d’experts et d’ingénieurs Microsoft.
- Pour obtenir de l’aide auprès de la communauté sur les questions de développement, nous avons nos [Forums](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)et [StackOverflow](https://stackoverflow.com/questions).
- le site de [support technique](https://developer.microsoft.com/windows/support) pour les développeurs de Windows présente d’autres options de support.

## <a name="related-topics"></a>Rubriques connexes

- [Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md)
- [Comment résoudre les erreurs de signature de package d’application](how-to-troubleshoot-app-package-signature-errors.md)
