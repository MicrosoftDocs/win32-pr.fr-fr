---
description: Les tables qui répertorient les fonctionnalités et les fonctionnalités prennent en charge les comparaisons pour les quatre principaux systèmes de fichiers Windows, NTFS, exFAT, UDF et FAT32.
ms.assetid: 28cf2805-f1ce-46b4-bf08-a329f67f4d99
title: Comparaison des fonctionnalités du système de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7547e48ff68a8fdab195087904a47a535aa3464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753565"
---
# <a name="file-system-functionality-comparison"></a>Comparaison des fonctionnalités du système de fichiers

Les tableaux suivants répertorient les fonctionnalités et la prise en charge des fonctionnalités pour les quatre principaux systèmes de fichiers Windows, NTFS, exFAT, UDF et FAT32 :

-   [Fonctionnalité](#file-system-functionality-comparison)
-   [Limites](#limits)
-   [Journalisation et journal des modifications](#journaling-and-change-log)
-   [Fonctionnalités d’allocation de bloc](#block-allocation-features)
-   [Sécurité](#security)
-   [Compression](#compression)
-   [Quotas](#quotas)
-   [Magasin d’instances uniques](#single-instance-store)
-   [Rubriques connexes](#related-topics)

## <a name="functionality"></a>Fonctionnalités



| Fonctionnalité                             | NTFS                           | exFAT          | Fonctions définies par l'utilisateur                           | FAT32                      |
|-------------------------------------|--------------------------------|----------------|-------------------------------|----------------------------|
| Horodatages de création<br/>     | Oui<br/>                 | Oui<br/> | Oui<br/>                | Oui<br/>             |
| Horodatages du dernier accès<br/>  | Non (voir remarque ci-dessous)<br/> | Oui<br/> | Oui<br/>                | Oui (date uniquement)<br/> |
| Horodatages de la dernière modification<br/>  | Oui<br/>                 | Oui<br/> | Oui<br/>                | Oui<br/>             |
| Horodatages du dernier archivage<br/> | Non<br/>                  | Non<br/>  | Non<br/>                 | Non<br/>              |
| Respect de la casse<br/>           | Oui (option)<br/>        | Non<br/>  | Oui<br/>                | Non<br/>              |
| Conservation de la casse<br/>          | Oui<br/>                 | Oui<br/> | Oui<br/>                | Oui<br/>             |
| Liens directs<br/>               | Oui<br/>                 | Non<br/>  | Oui<br/>                | Non<br/>              |
| Liens virtuels<br/>               | Oui<br/>                 | Non<br/>  | Non<br/>                 | Non<br/>              |
| Fichiers partiellement alloués<br/>             | Oui<br/>                 | Non<br/>  | Oui<br/>                | Non<br/>              |
| Flux avec nom<br/>            | Oui<br/>                 | Non<br/>  | Oui<br/>                | Non<br/>              |
| Oplocks<br/>                  | Oui<br/>                 | Oui<br/> | Oui<br/>                | Oui<br/>             |
| Attributs étendus<br/>      | Oui<br/>                 | Non<br/>  | Oui (sur disque uniquement)<br/> | Non<br/>              |
| Autres flux de données<br/>   | Oui<br/>                 | Non<br/>  | Oui<br/>                | Non<br/>              |
| Points de montage<br/>             | Oui<br/>                 | Non<br/>  | Non<br/>                 | Non<br/>              |



 

**Windows Server 2003 et Windows XP :** Le champ horodatage du dernier accès NTFS est mis à jour.

## <a name="limits"></a>limites



| Fonctionnalité                             | NTFS                                                                                      | exFAT                                                                                     | Fonctions définies par l'utilisateur                                                                                       | FAT32                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Longueur maximale des noms de fichier<br/> | 255 caractères Unicode<br/>                                                         | 255 caractères Unicode<br/>                                                         | 127 Unicode ou 254 caractères ASCII<br/>                                            | 255 caractères Unicode<br/>                                                         |
| Longueur maximale des chemins<br/> | 32 760 caractères Unicode avec chaque composant de chemin d’accès ne dépassant pas 255 caractères<br/> | 32 760 caractères Unicode avec chaque composant de chemin d’accès ne dépassant pas 255 caractères<br/> | 32 760 caractères Unicode avec chaque composant de chemin d’accès ne dépassant pas 255 caractères<br/> | 32 760 caractères Unicode avec chaque composant de chemin d’accès ne dépassant pas 255 caractères<br/> |
| Taille maximale du fichier<br/>        | 2 ^ 64 1 octets<br/>                                                                   | 2 ^ 64 1 octets<br/>                                                                   | 2 ^ 64 1 octets<br/>                                                                   | 4 Gio<br/>                                                                          |
| Taille de volume maximale<br/>      | 16 to (taille de cluster de 4 Ko) ou 256TB (taille de cluster de 64 Ko)<br/>                        | 2 ^ 32 1 clusters (taille de cluster maximale = 2 ^ 25 1)<br/>                               | 2 ^ 32 blocs<br/>                                                                    | 2 ^ 32 blocs<br/>                                                                    |



 

## <a name="journaling-and-change-log"></a>Journalisation et journal des modifications



| Fonctionnalité                             | NTFS           | exFAT         | Fonctions définies par l'utilisateur           | FAT32         |
|-------------------------------------|----------------|---------------|---------------|---------------|
| Journalisation des métadonnées uniquement<br/> | Oui<br/> | Non<br/> | Non<br/> | Non<br/> |
| Journal des modifications de fichier<br/>          | Oui<br/> | Non<br/> | Non<br/> | Non<br/> |



 

## <a name="block-allocation-features"></a>Fonctionnalités d’allocation de bloc



| Fonctionnalité                        | NTFS                                                                        | exFAT         | Fonctions définies par l'utilisateur            | FAT32         |
|--------------------------------|-----------------------------------------------------------------------------|---------------|----------------|---------------|
| Compression fin<br/>        | Oui (les petits fichiers sont mis en résident dans le descripteur de flux MFT)<br/> | Non<br/> | Non<br/>  | Non<br/> |
| Étendues<br/>             | Oui<br/>                                                              | Non<br/> | Oui<br/> | Non<br/> |
| Taille de bloc variable<br/> | Non (défini par le volume)<br/>                                           | Non<br/> | Non<br/>  | Non<br/> |



 

## <a name="security"></a>Sécurité



| Fonctionnalité                                  | NTFS                                                 | exFAT               | Fonctions définies par l'utilisateur                 | FAT32         |
|------------------------------------------|------------------------------------------------------|---------------------|---------------------|---------------|
| Suivre le propriétaire du fichier<br/>              | Oui<br/>                                       | Non<br/>       | Non<br/>       | Non<br/> |
| Autorisations de fichiers POSIX<br/>        | Non (disponible dans la fonctionnalité du sous-système POSIX)<br/> | Non<br/>       | Oui<br/>      | Non<br/> |
| Listes de contrôle d'accès<br/>          | Oui<br/>                                       | Non<br/>       | Non<br/>       | Non<br/> |
| Chiffrement au niveau du système de fichiers<br/> | Oui<br/>                                       | Non<br/>       | Non<br/>       | Non<br/> |
| Somme de contrôle/ECC<br/>                  | Non<br/>                                        | Métadonnées<br/> | Métadonnées<br/> | Non<br/> |



 

## <a name="compression"></a>Compression



| Fonctionnalité                         | NTFS           | exFAT         | Fonctions définies par l'utilisateur           | FAT32         |
|---------------------------------|----------------|---------------|---------------|---------------|
| Compression intégrée<br/> | Oui<br/> | Non<br/> | Non<br/> | Non<br/> |



 

## <a name="quotas"></a>Quotas



| Fonctionnalité                               | NTFS                           | exFAT         | Fonctions définies par l'utilisateur           | FAT32         |
|---------------------------------------|--------------------------------|---------------|---------------|---------------|
| Espace disque au niveau de l’utilisateur<br/>      | Oui<br/>                 | Non<br/> | Non<br/> | Non<br/> |
| Espace disque au niveau du répertoire<br/> | Non (voir remarque ci-dessous)<br/> | Non<br/> | Non<br/> | Non<br/> |



 

**Remarque**  La fonctionnalité de quotas d’espace disque au niveau du répertoire sur NTFS est disponible via le serveur de fichiers Gestionnaire des ressources.

## <a name="single-instance-store"></a>Magasin de Single-Instance



| Fonctionnalité               | NTFS                           | exFAT         | Fonctions définies par l'utilisateur           | FAT32         |
|-----------------------|--------------------------------|---------------|---------------|---------------|
| Niveau de fichier<br/> | Non (voir remarque ci-dessous)<br/> | Non<br/> | Non<br/> | Non<br/> |



 

**Remarque**  Le magasin d’instances uniques pour NTFS est disponible dans le cadre de la fonctionnalité de stockage d’instance simple de Windows Server.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de fichiers](about-file-management.md)
</dt> <dt>

[Stockage à instance unique et sauvegarde SIS](/windows/desktop/Backup/single-instance-store-and-sis-backup)
</dt> </dl>

 

