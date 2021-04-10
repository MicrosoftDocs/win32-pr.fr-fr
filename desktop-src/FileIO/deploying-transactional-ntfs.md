---
description: Contrôle de la mise en cache dans le NTFS transactionnel.
ms.assetid: 0fd272ee-cf5f-4ba9-b8aa-ff0016f51d4b
title: Déploiement de NTFS transactionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7c44e0ad3b83854e56d18171072a7cb4615d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951603"
---
# <a name="deploying-transactional-ntfs"></a>Déploiement de NTFS transactionnel

Le NTFS transactionnel (TxF), comme la plupart des mécanismes de transaction, dépend du classement correct des écritures de données. Garantir un classement approprié en écriture nécessite un contrôle explicite de la mise en cache des données. Pour répondre à cette exigence, TxF exige que les lecteurs de disque implémentent les mécanismes de contrôle de mise en cache qui font partie d’interfaces de lecteur standardisées telles que SCSI, SATA et ATA.

Le mécanisme de contrôle de mise en cache utilisé par TxF est un indicateur connu sous le nom de fonction Forced Unit Access (FUA). Cet indicateur spécifie que le lecteur doit écrire les données sur un support de stockage stable avant la fin du signalement. À certains points critiques au sein d’une transaction, TxF doit émettre un FUA pour s’assurer que certaines données de contrôle nécessaires à la restauration d’une transaction ne sont pas perdues en cas de panne de courant.

Les lecteurs de disque de classe serveur (SCSI et Fiber Channel) prennent généralement en charge l’indicateur FUA. À partir de Vista, Windows prend en charge l’indicateur FUA uniquement pour les disques SCSI et Fiber Channel.

Sur les lecteurs de produit (ATA/SATA/USB), TxF présente des périodes de vulnérabilité pendant lesquelles une panne de courant peut entraîner l’incapacité de TxF à restaurer correctement la transaction, laissant ainsi les données dans un état incohérent, sauf si le cache d’écriture du lecteur est désactivé.

Certains adaptateurs de bus hôte (HBA) et contrôleurs de stockage (par exemple, les systèmes RAID) disposent de caches intégrés sur batterie. Étant donné que ces appareils conservent les données mises en cache en cas de panne de courant, tous les disques qui y sont connectés ne sont pas tenus d’honorer l’indicateur FUA. En outre, un disque dont l’alimentation est protégée par une alimentation sans interruption (UPS) n’a pas besoin d’honorer l’indicateur FUA. Cela est dû au fait que l’onduleur conserve suffisamment de temps pour que le disque vide son cache sur le support.

La désactivation du cache d’écriture d’un lecteur élimine la nécessité pour le lecteur d’honorer l’indicateur FUA. Vous pouvez désactiver la mise en cache d’écriture d’un disque en émettant le code de contrôle d' [**informations du cache du \_ jeu de disques \_ \_ \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_set_cache_information) sur le disque. L’état du cache d’écriture (activé/désactivé) est conservé entre les redémarrages du système. L’émission de ce code de contrôle aura des conséquences significatives sur les performances de toutes les e/s émises sur ce disque, ce qui sera probablement une dégradation notable des performances. L’utilisation de ce code de contrôle doit être soigneusement envisagée avant le déploiement.

> [!Note]  
> Pour que TxF puisse protéger de manière cohérente l’intégrité de vos données par le biais de pannes de courant, le système doit satisfaire au moins l’un des critères suivants :
>
> -   Utilisez des disques de classe serveur (SCSI, Fiber Channel).
> -   Assurez-vous que les disques sont connectés à un adaptateur de bus hôte avec mise en cache avec batterie de secours.
> -   Utilisez un contrôleur de stockage (par exemple, système RAID) comme unité de stockage.
> -   Assurez-vous que l’alimentation du disque est protégée par un onduleur.
> -   Vérifiez que la fonctionnalité de mise en cache d’écriture du disque est désactivée.

 

 

 



