---
description: dans Windows Vista et Windows Server 2008 et versions ultérieures, le développeur d’un enregistreur ou d’une application VSS peut choisir d’exclure certains fichiers des clichés instantanés.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Exclusion de fichiers des clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c39acf8c92d44bcf8786a880b6ae5eb6a88786809f5af1609dee1b342cd2fb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122105"
---
# <a name="excluding-files-from-shadow-copies"></a>Exclusion de fichiers des clichés instantanés

dans Windows Vista et Windows Server 2008 et versions ultérieures, le développeur d’un enregistreur ou d’une application VSS peut choisir d’exclure certains fichiers des clichés instantanés.

L’impact sur les performances et la zone de stockage des clichés instantanés (également appelée « zone diff ») de l’utilisation d’un fichier dans un cliché instantané sont directement liés à la quantité de modification dans le contenu du fichier après la création du cliché instantané. En outre, l’exclusion de fichiers des clichés instantanés peut ralentir la création de clichés instantanés.

Pour ces raisons, un fichier doit être exclu des clichés instantanés uniquement s’il est volumineux, subit une modification importante entre un cliché instantané et le suivant, et n’a pas besoin d’être sauvegardé.

Vous ne devez exclure que les fichiers appartenant à votre application.

Si le contexte de cliché instantané n’a \_ \_ pas été \_ \_ défini dans le contexte de cliché instantané, cela signifie que la récupération automatique est désactivée et qu’aucun fichier ne peut être exclu du cliché instantané. Pour plus d’informations, consultez l’énumération des [**\_ \_ attributs d' \_ instantané \_ de volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) .

## <a name="using-the-addexcludefilesfromsnapshot-method"></a>Utilisation de la méthode AddExcludeFilesFromSnapshot

Un enregistreur VSS peut exclure des fichiers d’un cliché instantané comme suit :

1.  Appelez la méthode [**IVssCreateWriterMetadataEx :: AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) pour signaler les fichiers à exclure.
2.  Dans la méthode [**CVssWriter :: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) du writer, supprimez les fichiers du cliché instantané.

## <a name="using-the-filesnottosnapshot-registry-key"></a>Utilisation de la clé de Registre FilesNotToSnapshot

> [!Note]  
> La clé de Registre **FilesNotToSnapshot** est destinée à être utilisée uniquement par les applications. Les utilisateurs qui essaient de l’utiliser rencontrent les limitations suivantes :
>
> -   Elle ne permet pas de supprimer des fichiers d’un cliché instantané créé sur un serveur Windows Server à l’aide de la fonctionnalité Versions précédentes.
> -   Elle ne permet pas de supprimer des fichiers des clichés instantanés pour dossiers partagés.
> -   Il peut supprimer des fichiers d’un cliché instantané qui a été créé à l’aide de l’utilitaire [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) , mais il ne peut pas supprimer les fichiers d’un cliché instantané qui a été créé à l’aide de l’utilitaire [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .
> -   Les fichiers sont supprimés d’un cliché instantané autant que faire se peut. Cela signifie que leur suppression n’est pas garantie.

 

Une application VSS peut supprimer des fichiers d’un cliché instantané lors de la création de clichés instantanés à l’aide de la clé de Registre suivante :

**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ FilesNotToSnapshot**

Cette clé de registre a \_ \_ des valeurs REG multisz pour chaque application dont les fichiers peuvent être exclus. Les fichiers sont spécifiés par des chemins d’accès complets, qui peuvent contenir le \* caractère générique.

Dans tous les cas, l’entrée est ignorée si aucun fichier ne correspond à la chaîne de chemin d’accès.

Une fois qu’un fichier a été ajouté à la valeur de clé de registre appropriée, il est supprimé du cliché instantané lors de la création par le writer d’optimisation du cliché instantané.

Si un chemin d’accès qualifié complet ne peut pas être spécifié, un chemin d’accès peut également être implicite à l’aide de la variable $UserProfile $ ou $AllVolumes $. Par exemple :

-   \\ \\ Nom du sous-répertoire $USERPROFILE $ Directory \\ .\*
-   $AllVolumes $ \\ TemporaryFiles \\ \* .\*

Pour rendre le chemin d’accès récursif, ajoutez « /s » à la fin. Par exemple :

-   \\ \\ Nom du sous-répertoire $USERPROFILE $ Directory \\ . \* /s
-   $AllVolumes $ \\ TemporaryFiles \\ \* . \* /s

La variable $UserProfile $ provoque l’application de la chaîne de chemin d’accès à tous les profils utilisateur sur l’ordinateur. Les profils utilisateur sont énumérés en examinant la clé de Registre suivante :

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ProfileList**

La variable $AllVolumes $ provoque l’application de la chaîne de chemin d’accès à tous les clichés instantanés sur l’ordinateur. Supposons, par exemple, que le chemin d’accès est «$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s», et l’ordinateur a trois volumes : C :, D : et E :. Si C : et E : contiennent le chemin d’accès « \\ TemporaryFiles \\ » et que le volume d : contient uniquement le chemin d : \\ Data \\ , l’arborescence de répertoires c : \\ TemporaryFiles \\ est supprimée des clichés instantanés de C :, et l’arborescence de répertoires E : \\ TemporaryFiles \\ est supprimée des clichés instantanés de E :.

Les administrateurs peuvent désactiver l’extension de la variable $UserProfile $ à l’aide de la clé de Registre suivante :

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Services \\ Vss \\ Paramètres**

Sous cette clé de Registre, spécifiez DisableUserProfileExpansion pour le nom de la valeur, REG \_ DWORD pour le type de valeur et une valeur différente de zéro pour les données de la valeur.

## <a name="about-the-filesnottobackup-registry-key"></a>À propos de la clé de Registre FilesNotToBackup

La clé de Registre **FilesNotToBackup** peut être utilisée pour spécifier les noms des fichiers et répertoires que les applications de sauvegarde ne doivent pas sauvegarder ou restaurer. Toutefois, il n’exclut pas ces fichiers des clichés instantanés. Pour plus d’informations sur cette clé de Registre, consultez [clés et valeurs de Registre pour la sauvegarde et la restauration](../backup/registry-keys-for-backup-and-restore.md).

 

 
