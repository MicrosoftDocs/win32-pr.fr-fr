---
description: si un package Windows Installer installe ou publie des assemblys, le programme d’installation stocke les informations relatives à ces assemblys dans le registre du système local.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: clés de registre de l’assembly écrites par Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fd4a9bf3fa5e1eb557c2a179ec3e9a0853149ff197922a9fbf633a2869f41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746019"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>clés de registre de l’assembly écrites par Windows Installer

si un package Windows Installer installe ou publie des assemblys, le programme d’installation stocke les informations relatives à ces assemblys dans le registre du système local. notez que ces clés de registre sont uniquement destinées à être utilisées en interne par Windows Installer et qu’elles ne doivent pas être exploitées par votre application. Le contenu, l’emplacement et la structure des informations stockées dans ces clés sont susceptibles d’être modifiés. Les applications doivent s’appuyer sur [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) pour gérer les assemblys.

Les assemblys sont inscrits par leurs noms d’assemblys. Les noms des valeurs stockées dans les emplacements suivants sont les noms d’assemblys. Les valeurs réelles sont du type REG \_ multi- \_ SZ et contiennent des données utilisées par [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) pour installer ou réparer des assemblys.

## <a name="information-about-private-assemblies"></a>Informations sur les assemblys privés

Windows le programme d’installation stocke les informations sur les assemblys privés transportés par Windows Installer packages qui ont été installés en tant qu’applications gérées par utilisateur sous la clé de registre suivante :

**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Programme d’installation** \\ **Géré** \\ **Sid *_\\_* de l’utilisateur** \\ Chemin d’accès des **assemblys** \\ **_du programme d’installation vers le fichier de configuration_**

Windows le programme d’installation stocke les informations sur les assemblys privés transportés par Windows Installer packages qui ont été installés par utilisateur sous la clé de registre suivante :

**HKCU** \\ **Logiciel** \\ **Microsoft** \\ **Programme d’installation** \\ **Assemblys** \\ **_chemin d’accès au fichier de configuration_**

Windows le programme d’installation stocke les informations sur les assemblys privés transportés par Windows Installer packages et installés par ordinateur sous la clé de registre suivante :

**HKLM** \\ **Logiciel** \\ **Classes** \\ **Programme d’installation** \\ **Assemblys** \\ **_chemin d’accès au fichier de configuration_**

## <a name="information-about-global-or-shared-assemblies"></a>Informations sur les assemblys globaux ou partagés

Windows le programme d’installation stocke les informations sur les assemblys partagés transportés par Windows Installer packages qui ont été installés en tant qu’applications gérées par utilisateur sous la clé de registre suivante :

**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Programme d’installation** \\ **Géré** \\ **Sid *_\\_* de l’utilisateur Assemblys de programme d’installation** \\  \\ **globaux**

Windows le programme d’installation stocke les informations sur les assemblys partagés transportés par Windows Installer packages qui ont été installés par utilisateur sous la clé de registre suivante :

**HKCU** \\ **Logiciel** \\ **Microsoft** \\ **Programme d’installation** \\ **Assemblys** \\ **Global**

Windows le programme d’installation stocke les informations sur les assemblys partagés transportés par Windows Installer packages et installés par ordinateur sous la clé de registre suivante :

**HKLM** \\ **Logiciel** \\ **Classes** \\ **Programme d’installation** \\ **Assemblys** \\ **Global**

 

 



