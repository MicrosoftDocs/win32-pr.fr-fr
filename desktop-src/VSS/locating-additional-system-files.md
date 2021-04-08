---
description: Lorsque vous effectuez une sauvegarde ou une restauration VSS, l’état du système Windows est défini comme étant une collection de plusieurs éléments clés du système d’exploitation et de leurs fichiers. Ces éléments doivent toujours être traités comme une unité par les opérations de sauvegarde et de restauration.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Sauvegarde et restauration de l’état du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755541"
---
# <a name="backing-up-and-restoring-system-state"></a>Sauvegarde et restauration de l’état du système

> [!Note]  
> Cette rubrique s’applique à Windows Vista, Windows Server 2008 et versions ultérieures. Pour plus d’informations sur Windows Server 2003, voir [sauvegarde et restauration de l’état du système dans Windows server 2003 R2 et Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)

 

Lorsque vous effectuez une sauvegarde ou une restauration VSS, l’état du système Windows est défini comme étant une collection de plusieurs éléments clés du système d’exploitation et de leurs fichiers. Ces éléments doivent toujours être traités comme une unité par les opérations de sauvegarde et de restauration.

> [!Note]  
> Microsoft ne fournit pas de support technique pour les développeurs ou les professionnels de l’informatique pour l’implémentation de restaurations en ligne sur l’état du système sur Windows (toutes les versions).

 

Lors de la sauvegarde et de la récupération de l’état du système, la stratégie recommandée consiste à sauvegarder et à récupérer les volumes système et de démarrage en plus des fichiers énumérés par les Writers d’État du système. Les Writers d’État du système sont des enregistreurs dont l’attribut de [**\_ \_ type d’utilisation VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) est défini sur VSS \_ ut \_ BOOTABLESYSTEMSTATE ou VSS \_ ut \_ SYSTEMSERVICE.

> [!IMPORTANT]
> Si un enregistreur VSS est identifié par son [**\_ \_ type d’utilisation de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) comme un enregistreur de l’état du système, il doit être inclus dans une sauvegarde de l’état du système, même s’il peut être sélectionné.

 

Outre les fichiers binaires du système d’exploitation et du pilote énumérés par les Writers d’État du système, certains autres fichiers doivent être sauvegardés dans le cadre de l’état du système.

Tous les composants signalés par un enregistreur VSS du système font partie de l’état du système, à l’exception de ceux pour lesquels l' \_ indicateur VSS CF \_ not \_ System \_ State est défini.

Les programmes de sauvegarde doivent également définir la clé de Registre **LastRestoreId** . Pour plus d’informations, consultez [clés et valeurs de Registre pour la sauvegarde et la restauration](../backup/registry-keys-for-backup-and-restore.md).

> [!Note]  
> Dans Windows Vista, Windows Server 2008 et versions ultérieures, les noms et les emplacements de certains fichiers système ont été modifiés comme suit.

 

## <a name="system-state"></a>État du système

Pour Windows Server 2012 et versions ultérieures, en plus des fichiers signalés par les différents enregistreurs d’état système VSS, seuls les fichiers de licence suivants doivent être inclus explicitement et les fichiers DRM suivants doivent être exclus explicitement.

## <a name="windows-media-digital-rights-management-files"></a>Fichiers Rights Management numériques Windows Media

Dans Windows Server 2008 et versions ultérieures, les fichiers suivants, y compris tous les sous-répertoires sous le chemin d’accès suivant, sont exclus de l’état du système et ne doivent pas être sauvegardés :

-   % ProgramData% \\ Microsoft \\ Windows \\ DRM\\

Cela remplace les informations de la section Windows Media Digital Rights Management de l' [utilisation des fonctionnalités de sécurité et de système de fichiers](working-with-file-system-and-security-features.md).

## <a name="performance-counter-configuration-files"></a>Fichiers de configuration du compteur de performances

Les fichiers de configuration des compteurs de performances se trouvent dans le répertoire% SystemRoot% \\ system32 \\ et portent les noms suivants :

<dl> Perf ? 00 ?. anciens  
Perfc0 ??. anciens  
Perfd0 ??. anciens  
Perfh0 ??. anciens  
Perfi0 ??. anciens  
Prfc0 ???. anciens  
Prfd0 ???. anciens  
Prfh0 ???. anciens  
Prfi0 ???. anciens  
</dl>

Ces fichiers sont modifiés uniquement lors de l’installation de l’application et doivent être sauvegardés et restaurés au cours des sauvegardes et restaurations de l’état du système.

## <a name="iis-configuration-files"></a>Fichiers de configuration IIS

> [!Note]  
> Dans Windows Vista avec Service Pack 1 (SP1) et versions ultérieures, vous ne devez pas sauvegarder ces fichiers. Au lieu de cela, utilisez l’enregistreur de configuration IIS dans la zone. Pour plus d’informations sur ce writer, consultez [la page enregistreurs VSS intégrés](in-box-vss-writers.md).

 

Les fichiers de configuration IIS appropriés et leurs emplacements sont répertoriés ci-dessous :

-   Le fichier de machine.config .NET FX se trouve dans le répertoire de la version du Framework.
-   Le fichier web.config racine ASP.NET se trouve dans le répertoire de la version du Framework.
    > [!Note]  
    > Les fichiers de configuration pour .NET FX et ASP.NET se trouvent dans le répertoire de la version du Framework. Si plusieurs versions du Framework sont installées sur l’ordinateur, ce répertoire contiendra un fichier de configuration pour chaque version installée.

     

-   Le fichier de configuration central IIS applicationHost.config se trouve dans le répertoire% windir% \\ system32 \\ inetsrv \\ config. Pour que le serveur comprenne ce fichier de configuration, il existe des fichiers de schéma qui déterminent sa grammaire et sa structure. Ces fichiers se trouvent dans le répertoire du schéma de configuration% windir% \\ system32 \\ inetsrv \\ \\ .

Le chemin d’accès au répertoire de la version du Framework est stocké dans la clé de Registre suivante :

**HKEY \_ logiciel de l' \_ ordinateur local \\ \\ Microsoft \\ . NETFramework \\ InstallRoot**

En outre, les clés de chiffrement suivantes doivent être sauvegardées :<dl> % ProgramData% \\ Microsoft \\ crypto \\ RSA \\ MachineKeys\\\*  
% SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*  
</dl>

## <a name="framework-files"></a>Fichiers du Framework

Toutes les versions du .NET Framework doivent être sauvegardées. Les fichiers se trouvent dans l’un des répertoires suivants (ou les deux) :

<dl> % windir% \\ Microsoft.NET \\ Framework  
% windir% \\ Microsoft.NET \\ Framework64  
</dl>

En outre, les fichiers d’assembly doivent être sauvegardés. Ces fichiers se trouvent dans le répertoire suivant :<dl> assembly% windir% \\  
</dl>

## <a name="task-scheduler-task-files"></a>Fichiers de tâches Planificateur de tâches

Les fichiers de tâches du planificateur de tâches doivent être sauvegardés. Les fichiers se trouvent dans l’un ou l’autre des emplacements suivants :

<dl> % windir% \\ system32 \\ tâches et tous les sous-répertoires (de manière récursive)  
% windir% \\ tâches (aucun sous-répertoire)  
</dl>

 

 
