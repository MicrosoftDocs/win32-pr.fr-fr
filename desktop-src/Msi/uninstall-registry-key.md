---
description: Liste des propriétés de Windows Installer donnant des valeurs écrites sous la clé de Registre Uninstall.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Installer les propriétés de la clé de Registre Uninstall
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: 90174cabed7a1d9ff0ca21b532c459a1026787a6
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "106526915"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Installer les propriétés de la clé de Registre Uninstall

Les propriétés du programme d’installation suivantes donnent les valeurs écrites sous la clé de Registre :

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall**

Les valeurs sont stockées dans une sous-clé identifiée par le GUID du code du produit de l’application.



| Valeur               | Windows Installer, propriété                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | Propriété [**ProductName**](productname.md)                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Dérivée de la propriété [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Publisher           | Propriété [**Manufacturer**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Dérivée de la propriété [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Dérivée de la propriété [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Version             | Dérivée de la propriété [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| HelpLink            | Propriété [**ARPHELPLINK**](arphelplink.md)                                                                                                                                                                                                                                                                                                                          |
| HelpTelephone       | Propriété [**ARPHELPTELEPHONE**](arphelptelephone.md)                                                                                                                                                                                                                                                                                                                |
| InstallDate         | Heure de la dernière réception du service par ce produit. La valeur de cette propriété est remplacée chaque fois qu’un correctif est appliqué ou supprimé du produit ou lorsque l' [option de ligne de commande](command-line-options.md) /v est utilisée pour réparer le produit. Si le produit n’a pas reçu de réparation ou de correctifs, cette propriété contient l’heure à laquelle le produit a été installé sur cet ordinateur. |
| Emplacement de l’installation     | Propriété [**ARPINSTALLLOCATION**](arpinstalllocation.md)                                                                                                                                                                                                                                                                                                            |
| InstallSource       | [**SourceDir**](sourcedir.md) , propriété                                                                                                                                                                                                                                                                                                                              |
| URLInfoAbout        | Propriété [**ARPURLINFOABOUT**](arpurlinfoabout.md)                                                                                                                                                                                                                                                                                                                  |
| URLUpdateInfo       | Propriété [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | Propriété [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)                                                                                                                                                                                                                                                                                                    |
| Commentaires            | Propriété [**ARPCOMMENTS**](arpcomments.md) <br/> Commentaires fournis au panneau de configuration **Ajout/suppression de programmes** .<br/>                                                                                                                                                                                                                                |
| Contact             | Propriété [**ARPCONTACT**](arpcontact.md) <br/> Contactez le panneau de configuration **Ajout/suppression de programmes** .<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | Déterminé et défini par le Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| Language            | Propriété [**ProductLanguage**](productlanguage.md)                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | Déterminé et défini par le Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| Fichier Lisezmoi              | Propriété [**ARPREADME**](arpreadme.md) <br/> Fichier Lisez-moi fourni dans le panneau de configuration **Ajout/suppression de programmes** .<br/>                                                                                                                                                                                                                                      |
| UninstallString     | Déterminé et défini par Windows Installer.                                                                                                                                                                                                                                                                                                                             |
| SettingsIdentifier  | Propriété [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des propriétés](about-properties.md)
</dt> <dt>

[Configuration de l’ajout/suppression de programmes avec Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Référence de propriété](property-reference.md)
</dt> <dt>

[Utilisation de propriétés](using-properties.md)
</dt> </dl>

 

 




