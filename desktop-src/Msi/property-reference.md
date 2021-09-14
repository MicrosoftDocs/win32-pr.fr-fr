---
description: 'cette section répertorie les propriétés définies par Windows Installer :'
ms.assetid: c91119b9-59d5-4a33-91cd-d3ba63659d12
title: Référence de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e38f952632609090c69b85786c6aef64243d420b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009744"
---
# <a name="property-reference"></a>Référence de propriété

cette section répertorie les propriétés définies par Windows Installer :

-   [Propriétés de l’emplacement du composant](#component-location-properties)
-   [Propriétés de configuration](#configuration-properties)
-   [Date, Time, propriétés](#date-time-properties)
-   [Propriétés options d’installation de la fonctionnalité](#feature-installation-options-properties)
-   [Propriétés matérielles](#hardware-properties)
-   [Propriétés de l’état de l’installation](#installation-status-properties)
-   [Propriétés du système d’exploitation](#operating-system-properties)
-   [Propriétés des informations sur le produit](#product-information-properties)
-   [Propriétés de la mise à jour des informations récapitulatives](#summary-information-update-properties)
-   [Propriétés du dossier système](#system-folder-properties)
-   [Propriétés des informations utilisateur](#user-information-properties)

Des propriétés supplémentaires peuvent être spécifiées par des actions personnalisées ou des données créées. Les propriétés dont le nom ne contient pas de lettres minuscules sont des propriétés publiques et peuvent être spécifiées sur la ligne de commande.

Pour plus d’informations sur les valeurs de la clé de Registre **Uninstall** qui sont fournies par les propriétés du programme d’installation, consultez [Uninstall Registry Key](uninstall-registry-key.md).

## <a name="component-location-properties"></a>Propriétés de l’emplacement du composant

La liste suivante fournit des liens vers des informations supplémentaires sur les propriétés de l’emplacement du composant.



| Propriété                                                            | Description                                                                                                                                                                                                        |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OriginalDatabase**](originaldatabase.md)<br/>             | Le programme d’installation définit cette propriété sur la base de données lancée à partir de, la base de données sur la source ou la base de données mise en cache.<br/>                                                                                     |
| [**ParentOriginalDatabase**](parentoriginaldatabase.md)<br/> | Le programme d’installation définit cette propriété pour les installations exécutées par une action d' [installation simultanée](concurrent-installations.md) .<br/>                                                                             |
| [**SourceDir**](sourcedir.md)<br/>                           | Répertoire racine qui contient les fichiers sources.<br/>                                                                                                                                                          |
| [**TARGETDIR**](targetdir.md)<br/>                           | Spécifie le répertoire de destination racine pour l’installation. Pendant une [installation administrative](administrative-installation.md) , cette propriété est l’emplacement où copier le package d’installation.<br/> |



 

## <a name="configuration-properties"></a>Configuration Properties

La liste suivante fournit des liens vers des informations supplémentaires sur d’autres propriétés configurables.



| Propriété                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TRANSACTIONNEL**](action.md)<br/>                                                     | Action initiale appelée après l’initialisation du programme d’installation.<br/>                                                                                                                                                                                                                                                                                                                          |
| [**ALLUSERS**](allusers.md)<br/>                                                 | Détermine l’emplacement de stockage des informations de configuration.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)<br/>                     | URL du canal de mise à jour pour une application.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**ARPCOMMENTS**](arpcomments.md)<br/>                                           | Fournit des commentaires pour l' **Ajout ou la suppression de programmes** dans le panneau de **configuration**.<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPCONTACT**](arpcontact.md)<br/>                                             | Fournit un contact pour l' **Ajout ou la suppression de programmes** dans le panneau de **configuration**.<br/>                                                                                                                                                                                                                                                                                                          |
| [**ARPINSTALLLOCATION**](arpinstalllocation.md)<br/>                             | Chemin d’accès complet au dossier principal d’une application.<br/>                                                                                                                                                                                                                                                                                                                      |
| [**ARPNOMODIFY**](arpnomodify.md)<br/>                                           | Désactive les fonctionnalités qui modifient un produit.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**ARPNOREMOVE**](arpnoremove.md)<br/>                                           | Désactive la fonctionnalité qui supprime un produit.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPNOREPAIR**](arpnorepair.md)<br/>                                           | Désactive le bouton **réparer** de l’Assistant programmes.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**ARPPRODUCTICON**](arpproducticon.md)<br/>                                     | Spécifie l’icône principale du package d’installation.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ARPREADME**](arpreadme.md)<br/>                                               | Fournit un **fichier Lisez-moi** pour l' **Ajout ou la suppression de programmes** dans le panneau de **configuration**.<br/>                                                                                                                                                                                                                                                                                                     |
| [**ARPSIZE**](arpsize.md)<br/>                                                   | Estimation de la taille d’une application, en kilo-octets.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md)<br/>                             | Empêche l’affichage d’une application dans la liste **Ajout/suppression de programmes** .<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPURLINFOABOUT**](arpurlinfoabout.md)<br/>                                   | URL de la page d’hébergement d’une application.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)<br/>                                 | URL pour les informations de mise à jour d’application.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**AVAILABLEFREEREG**](availablefreereg.md)<br/>                                 | Espace du Registre (en kilo-octets) requis par une application. Utilisé par l' [action AllocateRegistrySpace](allocateregistryspace-action.md).<br/>                                                                                                                                                                                                                                              |
| [**\_lecteur CCP**](ccp-drive.md)<br/>                                              | Chemin d’accès racine pour les produits éligibles pour CCP.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**DefaultUIFont**](defaultuifont.md)<br/>                                       | Style de police par défaut utilisé pour les contrôles.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md)<br/>                         | Défini pour désactiver la génération des raccourcis spécifiques qui prennent en charge l' [installation à la demande](installation-on-demand.md).<br/>                                                                                                                                                                                                                                                            |
| [**DISABLEMEDIA**](-disablemedia.md)<br/>                                        | Empêche le programme d’installation d’inscrire des sources multimédias, tels qu’un CD-ROM, en tant que sources valides pour le produit.<br/>                                                                                                                                                                                                                                                                        |
| [**DISABLEROLLBACK**](-disablerollback.md)<br/>                                  | Désactive la restauration de la configuration actuelle.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EXECUTEACTION**](executeaction.md)<br/>                                       | Action de niveau supérieur qui est lancée par ExecuteAction.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**EXECUTEMODE**](executemode.md)<br/>                                           | Mode d’exécution effectué par le programme d’installation.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**FASTOEM**](fastoem.md)<br/>                                                   | Améliore les performances d’installation dans des scénarios OEM spécifiques.<br/>                                                                                                                                                                                                                                                                                                                    |
| [**INSTALLLEVEL**](installlevel.md)<br/>                                         | Niveau initial dans lequel les fonctionnalités sont installées.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**LIMITUI**](limitui.md)<br/>                                                   | Niveau d’interface utilisateur limité en tant que base.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**LOGACTION**](logaction.md)<br/>                                               | Liste des noms d’actions à consigner.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MEDIAPACKAGEPATH**](mediapackagepath.md)<br/>                                 | Cette propriété doit être définie sur le chemin d’accès relatif si le package d’installation ne se trouve pas à la racine du CD-ROM.<br/>                                                                                                                                                                                                                                                               |
| [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)<br/>                 | Cette propriété facultative contient une liste délimitée par des points-virgules des emplacements du registre où l’application stocke les paramètres et les préférences d’un utilisateur. disponible avec Windows Installer 4,0.<br/>                                                                                                                                                                                        |
| [**MSIDISABLEEEUI**](msidisableeeui.md)<br/>                                     | Désactivez l’interface utilisateur incorporée pour l’installation.<br/> **[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge.<br/>                                                                                                                                                                                                           |
| [**MSIFASTINSTALL**](msifastinstall.md)<br/>                                     | réduisez le temps nécessaire à l’installation d’un package de Windows Installer volumineux.<br/> **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/>                                                                                                                                                                                              |
| [**MSIINSTALLPERUSER**](msiinstallperuser.md)<br/>                               | demande que le Windows Installer installer le package uniquement pour l’utilisateur actuel.<br/> **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/>                                                                                                                                                                                  |
| [**MSINODISABLEMEDIA**](msinodisablemedia.md)<br/>                               | Définissez cette propriété pour empêcher le programme d’installation de définir la propriété [**DISABLEMEDIA**](-disablemedia.md) .<br/>                                                                                                                                                                                                                                                                        |
| [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)<br/>   | Définissez cette propriété sur 1 (un) sur la ligne de commande ou dans la [table de propriétés](property-table.md) pour appliquer les règles du composant de mise à niveau pendant les [petites mises à jour](small-updates.md) et les [mises à niveau mineures](minor-upgrades.md) d’un produit spécifique. disponible à partir de Windows Installer 3,0.<br/>                                                                                     |
| [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)<br/> | Lorsque cette propriété a la valeur 1, le programme d’installation peut annuler l’inscription et désinstaller les composants redondants pour empêcher la conservation des composants orphelins sur l’ordinateur.<br/> **[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge.<br/>                                                                                                  |
| [**PRIMARYFOLDER**](primaryfolder.md)<br/>                                       | Permet à l’auteur de désigner un dossier principal pour une installation. Utilisé pour déterminer les valeurs des propriétés [**PrimaryVolumePath**](primaryvolumepath.md), [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md), [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)et [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) .<br/> |
| [**Privilégié**](privileged.md)<br/>                                             | Exécute une installation avec des privilèges élevés.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md)<br/>                             | Action si l’espace disque est insuffisant pour l’installation.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**INITIAL**](reboot.md)<br/>                                                     | Force ou supprime un redémarrage.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**REBOOTPROMPT**](rebootprompt.md)<br/>                                         | Supprime l’affichage des invites pour les redémarrages de l’utilisateur. Tous les redémarrages nécessaires se produisent automatiquement.<br/>                                                                                                                                                                                                                                                                     |
| [**ROOTDRIVE**](rootdrive.md)<br/>                                               | Lecteur par défaut pour une installation.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SÉQUENCE**](sequence.md)<br/>                                                 | Table qui a le schéma de la table de séquences.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**SHORTFILENAMES**](shortfilenames.md)<br/>                                     | Permet d’utiliser des noms de fichiers courts.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**TRANSFORMATIONS**](transforms.md)<br/>                                             | Liste des transformations à appliquer à une base de données.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**TRANSFORMSATSOURCE**](transformsatsource.md)<br/>                             | Informe le programme d’installation que les transformations d’un produit résident à la source.<br/>                                                                                                                                                                                                                                                                                                      |
| [**TRANSFORMSSECURE**](transformssecure.md)<br/>                                 | La définition de la propriété [**TRANSFORMSECURE**](transformssecure.md) sur 1 (un) informe le programme d’installation que les transformations doivent être mises en cache localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur ne dispose pas d’un accès en écriture.<br/>                                                                                                                                                           |
| [**MsiLogFileLocation**](msilogfilelocation.md)<br/>                             | Le programme d’installation définit la valeur de cette propriété sur le chemin d’accès complet du fichier journal, lorsque la journalisation a été activée. cette propriété est disponible à partir de Windows Installer 4,0.<br/>                                                                                                                                                                                                     |
| [**MsiLogging**](msilogging.md)<br/>                                             | définit le mode de journalisation par défaut pour le package Windows Installer. cette propriété est disponible à partir de Windows Installer 4,0.<br/>                                                                                                                                                                                                                                                   |
| [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)<br/>                 | Définissez cette propriété sur 1 pour demander que le programme d’installation utilise les informations utilisateur réelles lors de la définition de la propriété [**adminuser**](adminuser.md) . cette propriété est disponible à partir de Windows Installer 4,0.<br/>                                                                                                                                                                         |



 

## <a name="date-time-properties"></a>Date, Time, propriétés

Les propriétés de [**Date**](date.md) et d' [**heure**](time.md) sont des propriétés dynamiques que le programme d’installation définit lors de l’extraction des données.



| Propriété                        | Description                  |
|---------------------------------|------------------------------|
| [**Date**](date.md)<br/> | Date actuelle.<br/> |
| [**Simultanément**](time.md)<br/> | L’heure actuelle.<br/> |



 

## <a name="feature-installation-options-properties"></a>Propriétés options d’installation de la fonctionnalité

La liste suivante fournit des liens vers des informations supplémentaires sur les propriétés des options d’installation de fonctionnalités.



| Propriété                                                                | Description                                                                                                                                                                       |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADDDEFAULT**](adddefault.md)<br/>                             | Liste des fonctionnalités à installer dans la configuration par défaut.<br/>                                                                                                         |
| [**ADDLOCAL**](addlocal.md)<br/>                                 | Liste des fonctionnalités à installer localement.<br/>                                                                                                                              |
| [**ADDSOURCE**](addsource.md)<br/>                               | Liste des fonctionnalités à exécuter à partir de la source.<br/>                                                                                                                                |
| [**PUBLIÉS**](advertise.md)<br/>                               | Liste des fonctionnalités à publier.<br/>                                                                                                                                     |
| [**COMPADDDEFAULT**](compadddefault.md)<br/>                     | Liste des composants à installer dans la configuration par défaut.<br/>                                                                                                       |
| [**COMPADDLOCAL**](compaddlocal.md)<br/>                         | Liste des ID de composant à installer localement.<br/>                                                                                                                         |
| [**COMPADDSOURCE**](compaddsource.md)<br/>                       | Liste des ID de composant à exécuter à partir du média source.<br/>                                                                                                                        |
| [**FILEADDDEFAULT**](fileadddefault.md)<br/>                     | Liste des clés de fichier pour les fichiers à installer dans la configuration par défaut.<br/>                                                                                              |
| [**FILEADDLOCAL**](fileaddlocal.md)<br/>                         | Liste des clés de fichier pour les fichiers à exécuter localement.<br/>                                                                                                                         |
| [**FILEADDSOURCE**](fileaddsource.md)<br/>                       | Liste des clés de fichier à exécuter à partir du média source.<br/>                                                                                                                     |
| [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)<br/>       | La définition de cette propriété empêche la mise à jour corrective des utilisateurs avec un minimum de privilèges (LUA) d’une application.<br/>                                                                                 |
| [**MsiPatchRemovalList**](msipatchremovallist.md)<br/>           | Liste des correctifs à supprimer pendant l’installation.<br/>                                                                                                                 |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)<br/> | Spécifie si le package utilise la fonctionnalité [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) ou [FilesInUse](filesinuse-dialog.md) .<br/>                                          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)<br/>           | Spécifie la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés et redémarrés pour permettre l’installation de la mise à jour.<br/> |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)<br/>                       | Spécifie la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés pour permettre l’installation de la mise à jour.<br/>               |
| [**MSIPATCHREMOVE**](msipatchremove.md)<br/>                     | La définition de cette propriété supprime les correctifs.<br/>                                                                                                                                 |
| [**PATCH**](patch.md)<br/>                                       | La définition de cette propriété applique un correctif.<br/>                                                                                                                                 |
| [**INSTALLÉ**](reinstall.md)<br/>                               | Liste des fonctionnalités à réinstaller.<br/>                                                                                                                                    |
| [**REINSTALLMODE**](reinstallmode.md)<br/>                       | Chaîne qui contient des lettres qui spécifient le type de réinstallation à effectuer.<br/>                                                                                          |
| [**Installez**](remove.md)<br/>                                     | Liste des fonctionnalités à supprimer.<br/>                                                                                                                                        |



 

## <a name="hardware-properties"></a>Propriétés matérielles

la liste suivante identifie les propriétés matérielles que le Windows Installer définit au démarrage.




| Propriété | Description | 
|----------|-------------|
| <a href="alpha.md"><strong>Alpha</strong></a><br /> | Niveau de processeur numérique lors de l’exécution sur un processeur Alpha.<br /><blockquote>[!Note]<br />cette propriété est obsolète, la plateforme Alpha n’est pas prise en charge par Windows Installer.</blockquote><br /> | 
| <a href="borderside.md"><strong>BorderSide</strong></a><br /> | Largeur des bordures de la fenêtre, en pixels.<br /> | 
| <a href="bordertop.md"><strong>BorderTop</strong></a><br /> | Hauteur des bordures de la fenêtre, en pixels.<br /> | 
| <a href="captionheight.md"><strong>CaptionHeight</strong></a><br /> | Hauteur de la zone de légende normale, en pixels.<br /> | 
| <a href="colorbits.md"><strong>ColorBits</strong></a><br /> | Nombre de bits de couleur adjacents pour chaque pixel.<br /> | 
| <a href="intel.md"><strong>Intel</strong></a><br /> | Niveau de processeur numérique lors de l’exécution sur un processeur Intel.<br /> | 
| <a href="intel64.md"><strong>Intel64</strong></a><br /> | Niveau de processeur numérique lors de l’exécution sur un processeur Itanium.<br /> | 
| <a href="msix64.md"><strong>Msix64</strong></a><br /> | Niveau de processeur numérique lors de l’exécution sur un processeur x64.<br /> | 
| <a href="physicalmemory.md"><strong>PhysicalMemory</strong></a><br /> | Taille de la mémoire RAM installée, en mégaoctets.<br /> | 
| <a href="screenx.md"><strong>ScreenX</strong></a><br /> | Largeur de l’écran, en pixels.<br /> | 
| <a href="screeny.md"><strong>Écran</strong></a><br /> | Hauteur de l’écran, en pixels.<br /> | 
| <a href="textheight.md"><strong>TextHeight</strong></a><br /> | Hauteur des caractères, en unités logiques.<br /> | 
| <a href="virtualmemory.md"><strong>VirtualMemory</strong></a><br /> | Quantité d’espace du fichier d’échange disponible, en mégaoctets.<br /> | 




 

## <a name="installation-status-properties"></a>Propriétés de l’état de l’installation

La liste suivante fournit des liens vers des informations supplémentaires sur les propriétés d’État mises à jour par le programme d’installation lors de l’installation.



| Propriété                                                                      | Description                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AFTERREBOOT**](afterreboot.md)<br/>                                 | Indique que l’installation actuelle suit un redémarrage que l' [action ForceReboot](forcereboot-action.md) appelle.<br/>                                                                                                                                                |
| [**CostingComplete**](costingcomplete.md)<br/>                         | Indique si l’évaluation de l’espace disque est terminée.<br/>                                                                                                                                                                                                             |
| [**Installé**](installed.md)<br/>                                     | Indique qu’un produit est déjà installé.<br/>                                                                                                                                                                                                                |
| [**MSICHECKCRCS**](msicheckcrcs.md)<br/>                               | Le programme d’installation effectue un CRC sur les fichiers uniquement si la propriété [**MSICHECKCRCS**](msicheckcrcs.md) est définie.<br/>                                                                                                                                                           |
| [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)<br/> | Le programme d’installation définit cette propriété sur la clé de session pour la session du [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) .<br/>                                                                                                                                                         |
| [**MsiRunningElevated**](msirunningelevated-.md)<br/>                  | Le programme d’installation définit la valeur de cette propriété sur 1 quand le programme d’installation s’exécute avec des privilèges [*élevés*](e-gly.md) .<br/>                                                                                                                   |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)<br/>           | Le programme d’installation affecte à cette propriété la valeur 1 si un redémarrage du système d’exploitation est actuellement en attente.<br/>                                                                                                                                                              |
| [**MsiUIHideCancel**](msiuihidecancel.md)<br/>                         | Le programme d’installation définit [**MsiUIHideCancel**](msiuihidecancel.md) sur 1 lorsque le niveau d’installation interne comprend **INSTALLUILEVEL \_ HIDECANCEL**.<br/>                                                                                                                   |
| [**MsiUIProgressOnly**](msiuiprogressonly.md)<br/>                     | Le programme d’installation définit [**MsiUIProgressOnly**](msiuiprogressonly.md) sur 1 lorsque le niveau d’installation interne comprend **INSTALLUILEVEL \_ PROGRESSONLY**.<br/>                                                                                                             |
| [**MsiUISourceResOnly**](msiuisourceresonly.md)<br/>                   | [**MsiUISourceResOnly**](msiuisourceresonly.md) sur 1 (un) lorsque le niveau d’installation interne comprend **INSTALLUILEVEL \_ SOURCERESONLY**.<br/>                                                                                                                       |
| [**NOCOMPANYNAME**](nocompanyname.md)<br/>                             | Supprime le paramètre automatique de la propriété [**CompanyName**](companyname.md) .<br/>                                                                                                                                                                          |
| [**NOM de l’utilisateur**](nousername.md)<br/>                                   | Supprime le paramètre automatique de la propriété [**username**](username.md) .<br/>                                                                                                                                                                                |
| [**OutOfDiskSpace**](outofdiskspace.md)<br/>                           | Espace disque insuffisant pour la prise en charge de l’installation.<br/>                                                                                                                                                                                                      |
| [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)<br/>                   | Espace disque insuffisant avec l’option ROLLBACK désactivée.<br/>                                                                                                                                                                                                             |
| [**Présélectionnées**](preselected.md)<br/>                                 | Les fonctionnalités sont déjà sélectionnées.<br/>                                                                                                                                                                                                                                |
| [**PrimaryVolumePath**](primaryvolumepath.md)<br/>                     | Le programme d’installation définit la valeur de cette propriété sur le chemin d’accès du volume désigné par la propriété [**PRIMARYFOLDER**](primaryfolder.md) .<br/>                                                                                                                  |
| [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md)<br/> | Le programme d’installation définit la valeur de cette propriété sur une chaîne qui représente le nombre total d’octets disponibles sur le volume référencé par la propriété [**PrimaryVolumePath**](primaryvolumepath.md) .<br/>                                                      |
| [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md)<br/> | Le programme d’installation définit la valeur de cette propriété sur une chaîne qui représente le nombre total d’octets restants sur le volume que la propriété [**PrimaryVolumePath**](primaryvolumepath.md) fait référence si toutes les fonctionnalités actuellement sélectionnées sont installées.<br/> |
| [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)<br/>   | Le programme d’installation définit la valeur de cette propriété sur une chaîne qui représente le nombre total d’octets requis par toutes les fonctionnalités actuellement sélectionnées sur le volume référencé par la propriété [**PrimaryVolumePath**](primaryvolumepath.md) .<br/>                    |
| [**ProductLanguage**](productlanguage.md)<br/>                         | Identificateur de langue numérique (LANGID) de la base de données. SOUHAITÉE<br/>                                                                                                                                                                                             |
| [**ReplacedInUseFiles**](replacedinusefiles.md)<br/>                   | Défini si le programme d’installation s’installe sur un fichier en cours d’utilisation.<br/>                                                                                                                                                                                          |
| [**RESUME**](resume.md)<br/>                                           | L’installation a repris.<br/>                                                                                                                                                                                                                                         |
| [**RollbackDisabled**](rollbackdisabled.md)<br/>                       | Le programme d’installation définit cette propriété lorsque la restauration est désactivée.<br/>                                                                                                                                                                                                   |
| [**UILevel**](uilevel.md)<br/>                                         | Indique le niveau de l’interface utilisateur.<br/>                                                                                                                                                                                                                           |
| [**UpdateStarted**](updatestarted.md)<br/>                             | Définir le moment où les modifications apportées au système ont commencé pour cette installation.<br/>                                                                                                                                                                                              |
| [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)<br/>               | Défini par le programme d’installation lorsqu’une mise à niveau supprime une application.<br/>                                                                                                                                                                                                  |
| [**VersionMsi**](versionmsi.md)<br/>                                   | le programme d’installation définit cette propriété sur la version de Windows Installer qui est exécutée pendant l’installation.<br/>                                                                                                                                                     |



 

## <a name="operating-system-properties"></a>Propriétés du système d’exploitation

La liste suivante fournit des liens vers des informations supplémentaires sur les propriétés du système d’exploitation que le programme d’installation définit au démarrage.



| Nom de la propriété                                                                             | Brève description                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdminUser**](adminuser.md)<br/>                                                 | défini sur Windows 2000 si l’utilisateur dispose de privilèges d’administrateur.<br/>                                                                                                                                                                                                                        |
| [**ComputerName**](computername.md)<br/>                                           | Nom de l’ordinateur du système actuel.<br/>                                                                                                                                                                                                                                                 |
| [**MsiNetAssemblySupport**](msinetassemblysupport.md)<br/>                         | Sur les systèmes qui prennent en charge les assemblys common language runtime, le programme d’installation définit la valeur de cette propriété sur la version de fichier de fusion.dll. Le programme d’installation ne définit pas cette propriété si le système d’exploitation ne prend pas en charge les assemblys common language runtime.<br/>                   |
| [**MsiNTProductType**](msintproducttype.md)<br/>                                   | indique le type de produit Windows.<br/>                                                                                                                                                                                                                                                  |
| [**MsiNTSuiteBackOffice**](msintsuitebackoffice.md)<br/>                           | sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit cette propriété sur 1 (un) uniquement si les composants Microsoft backoffice sont installés.<br/>                                                                                                                                      |
| [**MsiNTSuiteDataCenter**](msintsuitedatacenter.md)<br/>                           | sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit cette propriété sur 1 (un) uniquement si Windows 2000 Datacenter Server est installé.<br/>                                                                                                                                        |
| [**MsiNTSuiteEnterprise**](msintsuiteenterprise.md)<br/>                           | sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit cette propriété sur 1 (un) uniquement si Windows 2000 Advanced Server est installé.<br/>                                                                                                                                          |
| [**MsiNTSuitePersonal**](msintsuitepersonal.md)<br/>                               | sur Windows XP et les systèmes d’exploitation ultérieurs, le programme d’installation définit cette propriété sur 1 (un) uniquement si le système d’exploitation est local (non Professional).<br/>                                                                                                                                      |
| [**MsiNTSuiteSmallBusiness**](msintsuitesmallbusiness.md)<br/>                     | sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit cette propriété sur 1 (un) uniquement si Microsoft Small Business Server est installé.<br/>                                                                                                                                       |
| [**MsiNTSuiteSmallBusinessRestricted**](msintsuitesmallbusinessrestricted.md)<br/> | sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit cette propriété sur 1 (un) uniquement si Microsoft Small Business Server est installé avec la licence client restrictive.<br/>                                                                                                   |
| [**MsiNTSuiteWebServer**](msintsuitewebserver.md)<br/>                             | sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété [**MsiNTSuiteWebServer**](msintsuitewebserver.md) sur 1 (un) si l’édition web du Windows Server 2003 est installée. disponible uniquement avec la version de Windows Server 2003 du Windows Installer.<br/> |
| [**MsiTabletPC**](msitabletpc.md)<br/>                                             | le programme d’installation définit cette propriété sur une valeur différente de zéro si le système d’exploitation actuel est Windows XP édition Tablet PC.<br/>                                                                                                                                                                 |
| [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md)<br/>                     | Sur les systèmes qui prennent en charge les assemblys Win32, le programme d’installation définit la valeur de cette propriété sur la version de fichier de sxs.dll. Le programme d’installation ne définit pas cette propriété si le système d’exploitation ne prend pas en charge les assemblys Win32.<br/>                                                          |
| [**OLEAdvtSupport**](oleadvtsupport.md)<br/>                                       | définit si OLE prend en charge l’Windows Installer.<br/>                                                                                                                                                                                                                                           |
| [**RedirectedDllSupport**](redirecteddllsupport.md)<br/>                           | Le programme d’installation définit la propriété [**RedirectedDllSupport**](redirecteddllsupport.md) si le système effectuant l’installation prend en charge les [composants isolés](isolated-components.md).<br/>                                                                                              |
| [**RemoteAdminTS**](remoteadmints.md)<br/>                                         | Le programme d’installation définit la propriété [**RemoteAdminTS**](remoteadmints.md) lorsque le système est un serveur d’administration à distance exécutant le service de rôle Terminal Server.<br/>                                                                                                                   |
| [**ServicePackLevel**](servicepacklevel.md)<br/>                                   | Numéro de version du système d’exploitation Service Pack.<br/>                                                                                                                                                                                                                             |
| [**ServicePackLevelMinor**](servicepacklevelminor.md)<br/>                         | Numéro de la version mineure du Service Pack du système d’exploitation.<br/>                                                                                                                                                                                                                       |
| [**SharedWindows**](sharedwindows.md)<br/>                                         | Défini lorsque le système fonctionne en tant que Windows partagé.<br/>                                                                                                                                                                                                                                  |
| [**ShellAdvtSupport**](shelladvtsupport.md)<br/>                                   | Défini si l’interpréteur de commandes prend en charge la publicité des fonctionnalités.<br/>                                                                                                                                                                                                                                       |
| [**SystemLanguageID**](systemlanguageid.md)<br/>                                   | Identificateur de langue par défaut pour le système.<br/>                                                                                                                                                                                                                                          |
| [**TerminalServer**](terminalserver.md)<br/>                                       | Défini lorsque le système est un serveur exécutant le service de rôle Terminal Server.<br/>                                                                                                                                                                                                            |
| [**TTCSupport**](ttcsupport.md)<br/>                                               | Indique si le système d’exploitation prend en charge l’utilisation de fichiers. TTC (collections de polices de type true).<br/>                                                                                                                                                                                            |
| [**Version9X**](version9x.md)<br/>                                                 | numéro de Version du système d’exploitation Windows.<br/>                                                                                                                                                                                                                                     |
| [**VersionDatabase**](versiondatabase.md)<br/>                                     | Version de base de données numérique de l’installation actuelle.<br/>                                                                                                                                                                                                                                |
| [**VersionNT**](versionnt.md)<br/>                                                 | Numéro de version du système d’exploitation.<br/>                                                                                                                                                                                                                                             |
| [**VersionNT64**](versionnt64.md)<br/>                                             | Numéro de version du système d’exploitation si le système s’exécute sur un ordinateur 64 bits.<br/>                                                                                                                                                                                               |
| [**build Windows**](windowsbuild.md)<br/>                                          | Numéro de build du système d’exploitation.<br/>                                                                                                                                                                                                                                                |



 

## <a name="product-information-properties"></a>Propriétés des informations sur le produit

La liste suivante fournit des liens vers des informations supplémentaires sur les propriétés spécifiques au produit spécifiées dans la [table des propriétés](property-table.md).



| Nom de la propriété                                                  | Brève description                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)<br/>                  | Adresse Internet ou URL du support technique.<br/>                                                                                 |
| [**ARPHELPTELEPHONE**](arphelptelephone.md)<br/>        | Numéros de téléphone du support technique.<br/>                                                                                               |
| [**DiskPrompt**](diskprompt.md)<br/>                    | Chaîne affichée par une boîte de message qui vous invite à entrer un disque.<br/>                                                                     |
| [**IsAdminPackage**](isadminpackage.md)<br/>            | Défini sur 1 (un) si l’installation actuelle est exécutée à partir d’un package créé par le biais d’une installation d’administration.<br/>           |
| [**LeftUnit**](leftunit.md)<br/>                        | Place les unités à gauche du nombre.<br/>                                                                                        |
| [**Fabricant**](manufacturer.md)<br/>                | Nom du fabricant de l’application. (Obligatoire)<br/>                                                                               |
| [**MediaSourceDir**](mediasourcedir.md)<br/>            | Le programme d’installation définit cette propriété sur 1 (un) lorsque l’installation utilise une source de média, telle qu’un CD-ROM.<br/>                       |
| [**MSIINSTANCEGUID**](msiinstanceguid.md)<br/>          | La présence de cette propriété indique qu’une transformation de modification du code de produit est inscrite auprès du produit.<br/>                   |
| [**MSINEWINSTANCE**](msinewinstance.md)<br/>            | Cette propriété indique l’installation d’une nouvelle instance d’un produit avec des transformations d’instance.<br/>                              |
| [**ParentProductCode**](parentoriginaldatabase.md)<br/> | Le programme d’installation définit cette propriété pour les installations qu’une action d' [installation simultanée](concurrent-installations.md) exécute.<br/> |
| [**PIDTemplate**](pidtemplate.md)<br/>                  | Chaîne utilisée comme modèle pour la propriété [**PIDKEY**](pidkey.md) .<br/>                                                           |
| [**ProductCode**](productcode.md)<br/>                  | Identificateur unique pour une version de produit spécifique. (Obligatoire)<br/>                                                                 |
| [**ProductName**](productname.md)<br/>                  | Nom lisible par l’utilisateur d’une application. (Obligatoire)<br/>                                                                              |
| [**ProductState**](productstate.md)<br/>                | Définir sur l’état d’installation d’un produit.<br/>                                                                                       |
| [**ProductVersion**](productversion.md)<br/>            | Format de chaîne de la version du produit sous forme de valeur numérique. (Obligatoire)<br/>                                                            |
| [**UpgradeCode**](upgradecode.md)<br/>                  | GUID qui représente un ensemble connexe de produits.<br/>                                                                              |



 

## <a name="summary-information-update-properties"></a>Propriétés de la mise à jour des informations récapitulatives

Les propriétés suivantes sont définies uniquement par des transformations dans les fichiers. msp utilisés pour mettre à jour le flux d’informations de synthèse d’une image administrative.



| Propriété                                                              | Description                                                                                                                  |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)<br/>         | La valeur de cette propriété est écrite dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) .<br/> |
| [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)<br/> | La valeur de cette propriété est écrite dans la propriété [**Résumé des commentaires**](comments-summary.md) .<br/>               |
| [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)<br/>   | La valeur de cette propriété est écrite dans la propriété Résumé de l' [**objet**](subject-summary.md) .<br/>                 |



 

## <a name="system-folder-properties"></a>Propriétés du dossier système

La liste suivante fournit des liens vers des informations supplémentaires sur les dossiers système définis par le programme d’installation au moment de l’installation.



| Propriété                                                        | Description                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**AdminToolsFolder**](admintoolsfolder.md)<br/>         | Chemin d’accès complet au répertoire qui contient les outils d’administration.<br/>         |
| [**AppDataFolder**](appdatafolder.md)<br/>               | Chemin d’accès complet au dossier d' **itinérance** de l’utilisateur actuel.<br/>              |
| [**CommonAppDataFolder**](commonappdatafolder.md)<br/>   | Chemin d’accès complet aux données d’application pour tous les utilisateurs.<br/>                           |
| [**CommonFiles64Folder**](commonfiles64folder.md)<br/>   | Chemin d’accès complet au dossier de **fichiers communs 64 bits** prédéfini.<br/>            |
| [**CommonFilesFolder**](commonfilesfolder.md)<br/>       | Chemin d’accès complet au dossier **fichiers communs** de l’utilisateur actuel.<br/>         |
| [**DesktopFolder**](desktopfolder.md)<br/>               | Chemin d’accès complet au dossier **Desktop** .<br/>                                   |
| [**FavoritesFolder**](favoritesfolder.md)<br/>           | Chemin d’accès complet au dossier **favoris** de l’utilisateur actuel.<br/>            |
| [**FontsFolder**](fontsfolder.md)<br/>                   | Chemin d’accès complet au dossier de **polices** .<br/>                                     |
| [**LocalAppDataFolder**](localappdatafolder.md)<br/>     | Chemin d’accès complet au dossier qui contient des applications locales (non itinérantes).<br/> |
| [**MyPicturesFolder**](mypicturesfolder.md)<br/>         | Chemin d’accès complet au dossier **images** .<br/>                                  |
| [**NetHoodFolder**](nethoodfolder.md)<br/>               | Chemin d’accès complet au dossier **netpare-soleil** .<br/>                                   |
| [**PersonalFolder**](personalfolder.md)<br/>             | Chemin d’accès complet au dossier **documents** de l’utilisateur actuel.<br/>            |
| [**PrintHoodFolder**](printhoodfolder.md)<br/>           | Chemin d’accès complet au dossier **PrintHood** .<br/>                                 |
| [**ProgramFiles64Folder**](programfiles64folder.md)<br/> | Chemin d’accès complet au dossier **des fichiers programmes 64 bits** prédéfini.<br/>           |
| [**ProgramFilesFolder**](programfilesfolder.md)<br/>     | Chemin d’accès complet au dossier **des fichiers programmes 32 bits** prédéfini.<br/>           |
| [**ProgramMenuFolder**](programmenufolder.md)<br/>       | Chemin d’accès complet au dossier de **menu du programme** .<br/>                              |
| [**RecentFolder**](recentfolder.md)<br/>                 | Chemin d’accès complet au dossier **récent** .<br/>                                    |
| [**SendToFolder**](sendtofolder.md)<br/>                 | Chemin d’accès complet au dossier **sendto** de l’utilisateur actuel.<br/>               |
| [**StartMenuFolder**](startmenufolder.md)<br/>           | chemin d’accès complet au dossier **menu Démarrer** .<br/>                                |
| [**StartupFolder**](startupfolder.md)<br/>               | Chemin d’accès complet au dossier de **démarrage** .<br/>                                   |
| [**System16Folder**](system16folder.md)<br/>             | Chemin d’accès complet au dossier des DLL système 16 bits.<br/>                            |
| [**System64Folder**](system64folder.md)<br/>             | Chemin d’accès complet au dossier **System64** prédéfini.<br/>                       |
| [**SystemFolder**](systemfolder.md)<br/>                 | Chemin d’accès complet au dossier **système** de l’utilisateur actuel.<br/>               |
| [**TempFolder**](tempfolder.md)<br/>                     | Chemin d’accès complet au dossier **temp** .<br/>                                      |
| [**TemplateFolder**](templatefolder.md)<br/>             | Chemin d’accès complet au dossier de **modèle** pour l’utilisateur actuel.<br/>             |
| [**WindowsFolder**](windowsfolder.md)<br/>               | chemin d’accès complet au dossier **Windows** .<br/>                                   |
| [**WindowsVolume**](windowsvolume.md)<br/>               | volume du dossier **Windows** .<br/>                                      |



 

## <a name="user-information-properties"></a>Propriétés des informations utilisateur

La liste suivante fournit des liens vers des informations supplémentaires sur les informations fournies par l’utilisateur.



| Propriété                                                      | Description                                                                             |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AdminProperties**](adminproperties.md)<br/>         | Liste des propriétés qui sont définies lors de l’installation d’une administration.<br/>       |
| [**PRENNENT**](companyname.md)<br/>                 | Nom d’organisation de l’utilisateur qui effectue l’installation.<br/>            |
| [**LogonUser**](logonuser.md)<br/>                     | Nom d’utilisateur de l’utilisateur actuellement connecté.<br/>                           |
| [**MsiHiddenProperties**](msihiddenproperties.md)<br/> | Liste des propriétés qui ne peuvent pas être écrites dans le journal.<br/>       |
| [**PIDKEY**](pidkey.md)<br/>                           | Partie de l’ID de produit que l’utilisateur entre.<br/>                                 |
| [**Réf**](productid.md)<br/>                     | ID de produit complet après une validation réussie.<br/>                               |
| [**UserLanguageID**](userlanguageid.md)<br/>           | Identificateur de langue par défaut de l’utilisateur actuel.<br/>                             |
| [**NOM d’utilisateur**](username.md)<br/>                       | Utilisateur qui effectue l’installation.<br/>                                     |
| [**UserSID, propriété**](usersid.md)<br/>                | Défini par le programme d’installation en fonction de l’identificateur de sécurité (SID) de l’utilisateur.<br/> |



 

 

 
