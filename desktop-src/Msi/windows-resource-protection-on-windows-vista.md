---
description: Windows le programme d’installation adhère à Protection des ressources Windows (WRP) lors de l’installation de fichiers système essentiels, de dossiers et d’informations de registre dans Windows Server 2008 et versions ultérieures et Windows Vista et versions ultérieures.
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: utilisation de Windows Installer et Protection des ressources Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72808184ff11b29bfeb02dda576e9393e34189fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007308"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>utilisation de Windows Installer et Protection des ressources Windows

Windows le programme d’installation adhère à Protection des ressources Windows (WRP) lors de l’installation de fichiers système essentiels, de dossiers et d’informations de registre dans Windows Server 2008 et versions ultérieures et Windows Vista et versions ultérieures.

WRP dans Windows server 2008 et Windows Vista remplace Windows Protection de fichiers (WFP) dans Windows Server 2003, Windows XP et Windows 2000. Windows les développeurs du programme d’installation doivent noter les modifications suivantes dans la manière dont le programme d’installation gère les ressources protégées dans Windows Server 2008 et versions ultérieures et Windows Vista et versions ultérieures :

-   lors de l’exécution sur Windows Server 2008 et versions ultérieures ou Windows Vista et versions ultérieures, le Windows Installer ignore l’installation d’un fichier protégé par WRP, le programme d’installation entre un avertissement dans le fichier journal et continue avec le reste de l’installation sans erreur. dans Windows Server 2003, Windows XP et Windows 2000, lorsque le Windows Installer a rencontré un fichier protégé par wfp, le programme d’installation demande que WFP installe le fichier.
-   WRP sur Windows Server 2008 et versions ultérieures ou Windows Vista et versions ultérieures peuvent protéger les clés de registre en plus des fichiers. si le Windows Installer rencontre une clé de registre protégée par WRP, le programme d’installation ignore l’installation de cette clé de registre, le programme d’installation entre un avertissement dans le fichier journal et continue avec le reste de l’installation sans erreur.
-   notez que si un composant Windows Installer contient un fichier ou une clé de registre qui est protégé par WRP, cette ressource doit être utilisée comme chemin d’accès au keypath du composant. dans ce cas, Windows Installer n’installe pas, ne met pas à jour ou ne supprime pas le composant. Vous ne devez pas inclure de ressources protégées dans un package d’installation. au lieu de cela, vous devez utiliser les [mécanismes de remplacement des ressources pris en charge](../wfp/supported-file-replacement-mechanisms.md) pour [Protection des ressources Windows](../wfp/windows-resource-protection-portal.md).

pour plus d’informations sur WRP, consultez [Protection des ressources Windows](../wfp/windows-resource-protection-portal.md) et les informations fournies sur [Microsoft Technet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>WFP pour Windows Server 2003 et Windows XP/2000

Windows le programme d’installation adhère à la Protection de fichiers Windows (WFP) lors de l’installation de fichiers système essentiels sur Windows Server 2003, Windows XP et Windows 2000. Si un fichier système protégé est modifié par une installation sans assistance d’une application, la protection des fichiers Windows restaure le fichier dans la version de fichier vérifiée.

Windows Le programme d’installation ne tente jamais d’installer ou de remplacer un fichier protégé. lorsque l’action [installfiles](installfiles-action.md) ou toute autre action planifiée avant InstallFiles tente d’installer un fichier protégé sur Windows Server 2003, Windows XP ou Windows 2000, le programme d’installation appelle la plateforme WFP avec une demande d’installation ou de remplacement du fichier protégé. Le programme d’installation demande l’installation du fichier à partir de WFP immédiatement après l’exécution de l’action InstallFiles. WFP installe ou remplace le fichier sur le système de l’utilisateur par une version mise en cache du fichier protégé. Notez que cela ne garantit pas que la version du fichier installée à partir du cache correspond à la version requise par l’application. Une fois que WFP a installé le fichier, le programme d’installation détermine si cette version correspond à la version du package. Si la version du fichier du package est supérieure à la version installée, le programme d’installation informe l’utilisateur qu’il ne peut pas mettre à jour le système et qu’une mise à jour du système d’exploitation peut être requise pour l’application.

Si une action séquencé après [InstallFiles](installfiles-action.md) tente d’installer ou de remplacer un fichier protégé qui n’est pas déjà installé sur le système, le programme d’installation ne peut pas appeler WFP pour installer le fichier. Dans ce cas, le programme d’installation informe l’utilisateur qu’il ne peut pas mettre à jour le système et qu’une mise à jour du système d’exploitation peut être requise pour l’application.

Le programme d’installation vérifie également la fonctionnalité WFP lors de la suppression de fichiers et ne tente jamais de supprimer les fichiers système protégés.

## <a name="component-key-files-protected-by-wfp"></a>Fichiers de clé de composant protégés par WFP

notez que si un composant Windows Installer contient un fichier WFP, ce fichier doit être spécifié en tant que chemin d’accès de clé du composant.

quand le programme d’installation tente d’installer le fichier de clé d’un composant sur Windows Server 2003, Windows XP ou Windows 2000, il appelle d’abord WFP pour déterminer si le fichier de clé est protégé. Lorsque le fichier de clé d’un composant est protégé par WFP et que ce fichier de clé est déjà installé, le programme d’installation ne met à jour le composant que si la version du fichier de clé dans le package est supérieure à la version installée. Si le package d’installation spécifie qu’un composant doit être installé et que le fichier de clé du composant n’est pas installé actuellement, même si le fichier de clé est protégé, le programme d’installation installe le composant. Une fois qu’un composant ayant un fichier de clé protégé par WFP est installé, il est installé de façon permanente et le programme d’installation ne supprime pas ou ne remplace jamais le composant.

## <a name="installation-of-assemblies-by-wfp"></a>Installation d’assemblys par WFP

WFP pour les assemblys diffère de WFP pour les fichiers système.

WFP protège les fichiers système Windows Server 2003, Windows XP et Windows 2000 en détectant les tentatives de remplacement des fichiers système protégés. Cette protection est déclenchée lorsque WFP reçoit une notification de modification de répertoire pour un fichier dans un répertoire protégé. Lorsque WFP reçoit cette notification, il détermine quel fichier a changé. Si le fichier est protégé, WFP recherche la signature de fichier dans un fichier catalogue statique pour déterminer si le nouveau fichier est la version correcte. Si la version du fichier n’est pas correcte, le système remplace le fichier par la version appropriée à partir du média de distribution ou du cache.

À l’inverse, la WFP des assemblys est dynamique. WFP est étendu aux fichiers lorsqu’ils sont ajoutés au cache d’assembly côte à côte partagé. Si un assembly est endommagé, WFP demande que le programme d’installation remplace le fichier. Windows Le programme d’installation peut ne pas être en mesure de remplacer le fichier, selon que le package source est accessible ou non. Si le package source est inaccessible, la plateforme WFP affiche une boîte de dialogue indiquant qu’il est impossible de restaurer le fichier.

Notez que les assemblys côte à côte partagés non managés, installés dans% windir% \\ WinSxS, sont protégés par WFP. Les assemblys privés non managés, installés dans le répertoire de l’application, ne sont pas protégés par WFP. Les assemblys globaux managés installés dans le répertoire de l’application ou le GAC de l’assembly% windir% ne \\ \\ sont pas protégés par WFP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Protection des ressources](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 
