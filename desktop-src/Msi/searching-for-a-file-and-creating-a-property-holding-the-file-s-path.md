---
description: pendant une installation Windows Installer, le programme d’installation peut rechercher un fichier et créer une propriété contenant le chemin d’accès du fichier.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Recherche d’un fichier et création d’une propriété contenant le chemin d’accès du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009643"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a>Recherche d’un fichier et création d’une propriété contenant le chemin d’accès du fichier

**Pour rechercher un fichier et créer une propriété contenant le chemin d’accès de ce fichier**

1.  Commencez par Rechercher le fichier en répertoriant la signature et le nom de fichier dans la [table de signatures](signature-table.md).

    Les champs restants de cet enregistrement peuvent être laissés vides pour permettre la recherche d’une version de MyApp.exe.

    [Table de signature](signature-table.md) (partielle)

    

    | Signature          | Nom de fichier            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Ensuite, spécifiez le chemin d’accès du fichier recherché dans la [table DrLocator](drlocator-table.md).

    Comme AppFolder n’est pas listé dans la [table de signatures](signature-table.md), le programme d’installation détermine que AppFolder est un dossier plutôt qu’un fichier.

    [Table DrLocator](drlocator-table.md)

    

    | Signature            | Parent             | Chemin d’accès | Profondeur |
    |----------------------|--------------------|------|-------|
    | AppFile<br/>   |                    |      |       |
    | AppFolder<br/> | AppFile<br/> |      |       |

    

     

3.  Enfin, remplissez la [table AppSearch](appsearch-table.md) afin que l' [action AppSearch](appsearch-action.md) retourne le chemin d’accès de AppFolder.

    Une fois que le programme d’installation a exécuté l’action AppSearch, la valeur de MONDOSSIER est le chemin d’accès complet de AppFolder.

    [Table AppSearch](appsearch-table.md) (partielle)

    

    | Propriété            | Signature            |
    |---------------------|----------------------|
    | MONDOSSIER<br/> | AppFolder<br/> |

    

     

 

 




