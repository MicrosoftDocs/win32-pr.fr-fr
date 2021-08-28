---
description: la propriété FASTOEM est conçue pour permettre aux oem de réduire le temps nécessaire à l’installation de Windows Installer applications pour un scénario spécifique.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: FASTOEM, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c882ee78645a7f3a0fd8cd2677ca7ddfabade9b4395202cbbf0ab547b12a19eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129579"
---
# <a name="fastoem-property"></a>FASTOEM, propriété

la propriété **FASTOEM** est conçue pour permettre aux oem de réduire le temps nécessaire à l’installation de Windows Installer applications pour un scénario spécifique. Ne créez pas la propriété **FASTOEM** dans la [table de propriétés](property-table.md).

La propriété **FASTOEM** n’est applicable que si toutes les conditions suivantes sont remplies :

-   L’application est en cours d’installation sur le même volume que le dossier contenant les fichiers sources.
-   Les fichiers sources sont supprimés après l’installation.
-   Aucune interface utilisateur n’est affichée au cours de l’installation. Le [niveau de l’interface utilisateur](user-interface-levels.md) est aucun.
-   L’installation est effectuée dans le [contexte d’installation](installation-context.md)par ordinateur.
-   Il y a suffisamment d’espace sur l’ordinateur pour une installation réussie.
-   Il s’agit de la première installation. L’installation n’a pas pour effet de publier, de réinstaller, de supprimer ou d’exécuter une installation administrative.
-   Aucune fonctionnalité n’est installée pour être exécutée à partir de la source.
-   Le package d’installation ne contient aucun [composant isolé](isolated-components.md). Étant donné que les composants isolés requièrent que les fichiers sources restent situés à la source, la propriété **FASTOEM** ne peut pas être utilisée actuellement avec des composants isolés.

si toutes les conditions précédentes sont remplies, la définition de la propriété **FASTOEM** permet à Windows Installer d’améliorer les performances en procédant comme suit :

-   Déplacer au lieu de copier les fichiers sur le même volume. Cela ne garantit pas que tous les fichiers sont déplacés au lieu d’être copiés. Notez que si l’ordinateur comporte plusieurs disques durs, vous devez initialiser la propriété [**ROOTDRIVE**](rootdrive.md) sur la ligne de commande sur le même lecteur contenant la source d’installation.
-   Omettez cette source dans la liste source de l’application afin que les installations de réinstallation ou de maintenance suivantes retrouvent par défaut les sources de CD-ROM spécifiées dans la [table des médias](media-table.md).
-   Rationalisez les [coûts des fichiers](file-costing.md).
-   supprime les messages de progression envoyés de Windows Installer au client.

## <a name="remarks"></a>Remarques

Étant donné qu’aucun message de progression n’est envoyé lorsque **FASTOEM** est défini, il est recommandé que les auteurs écrivent manuellement la valeur 1800 pour le délai d’expiration dans la clé

**HKLM** \\ **Logiciel** \\ **Stratégies** \\ **Microsoft** \\ **Windows** \\ **Programme d’installation** \\ **Délai d’expiration**

Timeout est un type de **valeur de Registre \_ DWORD** .

pour afficher la taille de l’application dans ajout/suppression de programmes dans le panneau de configuration Windows 2000, vous devez écrire manuellement la valeur de EstimatedSize dans la clé

**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Désinstaller** \\ **<  Code > du produit**

Il s’agit d’un type de **valeur de Registre \_ DWORD** qui est égal à la taille de l’application, en kilo-octets. Le programme d’installation n’écrit pas automatiquement cette valeur.

Utilisez l’exemple de ligne de commande suivant si le CD-ROM fourni aux utilisateurs finaux stocke le package d’installation de l’application à la racine du CD-ROM. Notez que le nom du volume dans la [table des médias](media-table.md) du fichier .msi doit correspondre à l’étiquette de volume du CD-ROM.

**Msiexec/I C : \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 disablerollback = 1 ROOTDRIVE = C :\\**

Utilisez l’exemple de ligne de commande suivant si le package d’installation ne se trouve pas à la racine du CD-ROM fourni aux utilisateurs finaux. Vous devez définir la propriété [**MEDIAPACKAGEPATH**](mediapackagepath.md) dans ce cas sur le chemin d’accès au package d’installation. Le nom de volume dans la [table des médias](media-table.md) du fichier .msi doit correspondre à l’étiquette de volume du CD-ROM. Dans ce cas, suivez cet exemple.

**Msiexec/I C : \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 disablerollback = 1 MEDIAPACKAGEPATH = c : \\ TempImage \\package.msi ROOTDRIVE = c :\\**

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




