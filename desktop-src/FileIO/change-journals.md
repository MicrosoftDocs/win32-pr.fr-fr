---
description: Quand une modification est apportée à un fichier ou à un répertoire dans un volume, le journal des modifications USN pour ce volume est mis à jour avec une description de la modification et le nom du fichier ou du répertoire.
ms.assetid: 9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d
title: Journaux des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7556a080e0e85a428a502bb77afcbffc3975b5255d2efed5158c008f30d928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534099"
---
# <a name="change-journals"></a>Journaux des modifications

Une application de sauvegarde automatique est un exemple de programme qui doit vérifier les modifications apportées à l’état d’un volume pour effectuer sa tâche. La méthode d’analyse en force brute de la vérification des modifications dans les répertoires ou les fichiers consiste à analyser l’ensemble du volume. Toutefois, il ne s’agit pas d’une approche acceptable en raison de la baisse des performances du système. Une autre méthode consiste à ce que l’application enregistre une notification de répertoire (en appelant les fonctions [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) ou [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) ) pour les répertoires à sauvegarder. Cette méthode est plus efficace que la première méthode. Toutefois, elle nécessite qu’une application s’exécute en permanence. En outre, si un grand nombre de répertoires et de fichiers doivent être sauvegardés, la quantité de traitement et la surcharge de mémoire pour une telle application peuvent également entraîner une diminution des performances du système d’exploitation.

Pour éviter ces inconvénients, le système de fichiers NTFS gère un journal des modifications du numéro de séquence de mise à jour (USN). Quand une modification est apportée à un fichier ou à un répertoire dans un volume, le journal des modifications USN pour ce volume est mis à jour avec une description de la modification et le nom du fichier ou du répertoire.

Les journaux des modifications sont également nécessaires pour récupérer l’indexation du système de fichiers, par exemple après une défaillance de volume ou d’ordinateur. La possibilité de récupérer l’indexation signifie que le système de fichiers peut éviter le processus fastidieux de réindexation de l’ensemble du volume dans de tels cas.

Les rubriques suivantes traitent des journaux des modifications.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                             | Description                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modifier les enregistrements de journal](change-journal-records.md)<br/>                                                                   | À mesure que des fichiers, des répertoires et d’autres objets de système de fichiers NTFS sont ajoutés, supprimés et modifiés, le système de fichiers NTFS entre les enregistrements de journal de modification dans les flux, un pour chaque volume de l’ordinateur.<br/>                                           |
| [Utilisation de l’identificateur du journal des modifications](using-the-change-journal-identifier.md)<br/>                                         | Le système de fichiers NTFS associe un identificateur non signé 64 bits à chaque journal des modifications.<br/>                                                                                                                                                   |
| [Création, modification et suppression d’un journal des modifications](creating-modifying-and-deleting-a-change-journal.md)<br/>             | Les administrateurs peuvent créer, supprimer et recréer des journaux de modifications.<br/>                                                                                                                                                                         |
| [Obtention d’un handle de volume pour les opérations de journal des modifications](obtaining-a-volume-handle-for-change-journal-operations.md)<br/> | Pour obtenir un handle vers un volume en vue d’une utilisation avec des opérations de journal des modifications du numéro de séquence de mise à jour (USN), appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec le paramètre *lpFileName* défini sur une chaîne au format suivant : \\ \\ . \\ *X*.<br/> |
| [Opérations de journal des modifications](change-journal-operations.md)<br/>                                                             | Codes et structures de contrôle à utiliser avec le journal des modifications du numéro de séquence de mise à jour (USN) du système de fichiers NTFS.<br/>                                                                                                                                |



 

 

 




