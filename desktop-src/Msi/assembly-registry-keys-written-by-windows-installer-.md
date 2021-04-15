---
description: Si un package Windows Installer installe ou publie des assemblys, le programme d’installation stocke les informations relatives à ces assemblys dans le Registre du système local.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Clés de registre de l’assembly écrites par Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528869"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>Clés de registre de l’assembly écrites par Windows Installer

Si un package Windows Installer installe ou publie des assemblys, le programme d’installation stocke les informations relatives à ces assemblys dans le Registre du système local. Notez que ces clés de Registre sont uniquement destinées à être utilisées en interne par Windows Installer et qu’elles ne doivent pas être exploitées par votre application. Le contenu, l’emplacement et la structure des informations stockées dans ces clés sont susceptibles d’être modifiés. Les applications doivent s’appuyer sur [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) pour gérer les assemblys.

Les assemblys sont inscrits par leurs noms d’assemblys. Les noms des valeurs stockées dans les emplacements suivants sont les noms d’assemblys. Les valeurs réelles sont du type REG \_ multi- \_ SZ et contiennent des données utilisées par [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) pour installer ou réparer des assemblys.

## <a name="information-about-private-assemblies"></a>Informations sur les assemblys privés

Windows Installer stocke les informations sur les assemblys privés transportés par Windows Installer packages qui ont été installés en tant qu’applications gérées par utilisateur sous la clé de Registre suivante :

**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Programme d’installation** \\ **Géré** \\ **Sid *_\\_* de l’utilisateur** \\ Chemin d’accès des **assemblys** \\ * *_du programme d’installation vers le fichier de configuration_* _

Windows Installer stocke les informations sur les assemblys privés transportés par Windows Installer packages qui ont été installés par utilisateur sous la clé de Registre suivante :

_***\\** **\\** **\\** **\\** Chemin d’accès des assemblys du logiciel HKCU Microsoft installer **\\** _vers le fichier de configuration_*_

Windows Installer stocke les informations sur les assemblys privés concédés par des packages Windows Installer et installées par ordinateur sous la clé de Registre suivante :

_*HKLM **\\** Software **\\** classes **\\** programme **\\** **\\** _d’installation chemin d’accès au fichier de configuration_*_

## <a name="information-about-global-or-shared-assemblies"></a>Informations sur les assemblys globaux ou partagés

Windows Installer stocke les informations sur les assemblys partagés transportés par Windows Installer packages qui ont été installés en tant qu’applications gérées par utilisateur sous la clé de Registre suivante :

_*HKLM **\\** Logiciel **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** installer **\\** Managed **\\** _User sid_*_ \\ _ *assemblys de programme d’installation **\\** **\\** Global**

Windows Installer stocke les informations sur les assemblys partagés effectués par Windows Installer packages qui ont été installés par utilisateur sous la clé de Registre suivante :

**HKCU** \\ **Logiciel** \\ **Microsoft** \\ **Programme d’installation** \\ **Assemblys** \\ **Global**

Windows Installer stocke les informations sur les assemblys partagés transportés par les packages Windows Installer et installés par ordinateur dans la clé de Registre suivante :

**HKLM** \\ **Logiciel** \\ **Classes** \\ **Programme d’installation** \\ **Assemblys** \\ **Global**

 

 



