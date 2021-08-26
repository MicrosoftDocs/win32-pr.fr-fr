---
description: pendant une installation Windows Installer, le programme d’installation peut rechercher un fichier dans un emplacement spécifique sur le système de l’utilisateur.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Recherche d’un fichier dans un emplacement spécifique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b131708e5f9ff37474864aa5d6ef13abcab8f0d162563ca810c7e31fe2c41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041149"
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

    

    | Signature          | Parent | Chemin                                                    | Profondeur        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C : \\ Program Files \\ MyProducts \\ bin de projets \\<br/> | 0<br/> |

    

     

4.  Inclure l’action AppSearch dans la séquence d’action. Si MyApp.exe est installé dans le dossier C : \\ Program Files \\ MyProducts \\ projects \\ , le programme d’installation définit la propriété MyApp sur l’emplacement du fichier.

 

 




