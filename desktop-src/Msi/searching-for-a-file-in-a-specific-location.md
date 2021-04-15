---
description: Pendant une installation Windows Installer, le programme d’installation peut rechercher un fichier dans un emplacement spécifique sur le système de l’utilisateur.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Recherche d’un fichier dans un emplacement spécifique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529499"
---
# <a name="searching-for-a-file-in-a-specific-location"></a>Recherche d’un fichier dans un emplacement spécifique

**Pour rechercher un fichier dans un emplacement spécifique sur un système utilisateur**

1.  Répertorie la signature et le nom de fichier dans la [table de signatures](signature-table.md). Les champs restants de cet enregistrement peuvent avoir la valeur null pour rechercher n’importe quelle version de MyApp.exe.

    [Table de signature](signature-table.md)

    

    | Signature          | Nom de fichier            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Entrez la propriété que le programme d’installation doit définir si MyApp.exe est installé.

    [Table AppSearch](appsearch-table.md) (partielle)

    

    | Propriété         | Signature          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Utilisez la [table DrLocator](drlocator-table.md). Entrez le chemin d’accès complet au fichier sur le système de l’utilisateur dans le champ chemin d’accès. Entrez la valeur 0 dans la colonne profondeur pour rechercher dans le dossier bin.

    [Table DrLocator](drlocator-table.md)

    

    | Signature          | Parent | Chemin d’accès                                                    | Profondeur        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C : \\ Program Files \\ MyProducts \\ bin de projets \\<br/> | 0<br/> |

    

     

4.  Inclure l’action AppSearch dans la séquence d’action. Si MyApp.exe est installé dans le dossier C : \\ Program Files \\ MyProducts \\ projects \\ , le programme d’installation définit la propriété MyApp sur l’emplacement du fichier.

 

 




