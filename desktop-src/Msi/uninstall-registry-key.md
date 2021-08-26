---
description: liste des propriétés de Windows Installer donnant des valeurs écrites sous la clé de registre Uninstall.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Propriétés du programme d’installation pour la clé de Registre Uninstall
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: b898cd2a83a05783141ddf1fb4a7cbebb783bbcd7640526c5b653afa434d2175
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810318"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Propriétés du programme d’installation pour la clé de Registre Uninstall

Les propriétés du programme d’installation suivantes donnent les valeurs écrites sous la clé de Registre :

**HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall**

Les valeurs sont stockées dans une sous-clé identifiée par le GUID du code du produit de l’application.



| Valeur               | Windows Installer (propriété)                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | Propriété [**ProductName**](productname.md)                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Dérivée de la propriété [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Éditeur           | Propriété [**Manufacturer**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
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
| EstimatedSize       | déterminé et défini par le Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| Langage            | Propriété [**ProductLanguage**](productlanguage.md)                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | déterminé et défini par le Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| Fichier Lisezmoi              | Propriété [**ARPREADME**](arpreadme.md) <br/> Fichier Lisez-moi fourni dans le panneau de configuration **Ajout/suppression de programmes** .<br/>                                                                                                                                                                                                                                      |
| UninstallString     | déterminé et défini par Windows Installer.                                                                                                                                                                                                                                                                                                                             |
| SettingsIdentifier  | Propriété [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des propriétés](about-properties.md)
</dt> <dt>

[configuration de l’ajout/suppression de programmes avec Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Référence de propriété](property-reference.md)
</dt> <dt>

[Utilisation de propriétés](using-properties.md)
</dt> </dl>

 

 




