---
description: Décrit comment les points d’analyse activent le comportement du système de fichiers qui fait partie du comportement de la plupart des développeurs Windows.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Points d’analyse et opérations sur les fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209722"
---
# <a name="reparse-points-and-file-operations"></a>Points d’analyse et opérations sur les fichiers

Les *points d’analyse* activent le comportement du système de fichiers qui fait partie du comportement auquel la plupart des développeurs Windows peuvent être habitués. par conséquent, la connaissance de ces comportements lors de l’écriture d’applications qui manipulent des fichiers est vitale pour les applications fiables et fiables destinées à accéder aux systèmes de fichiers qui prennent en charge les points d’analyse. L’étendue de ces considérations dépend de l’implémentation spécifique et du comportement de filtre du système de fichiers associé d’un point d’analyse particulier, qui peut être défini par l’utilisateur. Pour plus d’informations, consultez [points d’analyse](reparse-points.md).

Tenez compte des exemples suivants concernant les implémentations du point d’analyse NTFS, notamment les dossiers montés, les fichiers liés et le serveur de stockage distant Microsoft :

-   Les applications de sauvegarde qui utilisent des [flux de fichier](file-streams.md) doivent spécifier des **\_ \_ données d’analyse de sauvegarde** dans la structure d' [**\_ \_ ID de flux Win32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) lors de la sauvegarde de fichiers avec des points d’analyse.
-   Les applications qui utilisent la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) doivent spécifier l’indicateur de fichier ouvrir l’indicateur de **\_ \_ \_ \_ point d’analyse** lors de l’ouverture du fichier s’il s’agit d’un point d’analyse. Pour plus d’informations, consultez [création et ouverture de fichiers](creating-and-opening-files.md).
-   Le processus de [défragmentation des fichiers](defragmenting-files.md) nécessite une gestion spéciale des points d’analyse.
-   Les applications de détection de virus doivent rechercher les points d’analyse qui indiquent des fichiers liés.
-   La plupart des applications doivent prendre des mesures spéciales pour les fichiers qui ont été déplacés vers un stockage à long terme, si uniquement pour informer l’utilisateur qu’il peut prendre un certain temps pour récupérer le fichier.
-   La fonction [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) ouvre le fichier ou le point d’analyse, en fonction de l’utilisation de l’indicateur de **fichier ouvrir l’indicateur de \_ \_ \_ \_ point d’analyse** .
-   Les liens symboliques, en tant que points d’analyse, ont certaines [considérations de programmation](symbolic-link-programming-considerations.md) spécifiques.
-   Les activités de gestion des volumes pour la lecture des enregistrements du journal des modifications du numéro de séquence de mise à jour nécessitent un traitement spécial des points d’analyse lors de l’utilisation de l' [**\_ enregistrement USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) et de la lecture des structures de [**\_ \_ \_ données du journal USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déterminer si un répertoire est un dossier monté](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[Création de dossiers montés](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[Effets de liens symboliques sur les fonctions des systèmes de fichiers](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
