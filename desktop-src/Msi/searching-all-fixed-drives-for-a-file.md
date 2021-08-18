---
description: pendant une installation Windows Installer, le programme d’installation peut rechercher un fichier sur tous les lecteurs fixes.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Recherche d’un fichier sur tous les lecteurs fixes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d460cd55fe54a98c6a02e23e49af9ea9838c7651262fa03f868bdb76acc2d506
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041249"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>Recherche d’un fichier sur tous les lecteurs fixes

**Pour rechercher un fichier sur tous les lecteurs fixes**

1.  Entrez la signature et le nom du fichier dans la [table de signatures](signature-table.md). Les champs restants de cet enregistrement peuvent avoir la valeur null pour rechercher n’importe quelle version de MyApp.exe.

    [Table de signature](signature-table.md) (partielle)

    

    | Signature          | Nom de fichier            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Entrez la propriété que le programme d’installation doit définir si MyApp.exe est installé.

    [Table AppSearch](appsearch-table.md)

    

    | Propriété         | Signature          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Utilisez la [table DrLocator](drlocator-table.md). Laissez les champs parent et chemin vides pour rechercher tous les lecteurs fixes du système utilisateur. Spécifiez dans la colonne profondeur le nombre de niveaux de sous-répertoires à rechercher. Par exemple, l’affectation de la valeur 0 à Depth détecte c : \\MyApp.exe, mais ne détecte pas le fichier à une profondeur de 2, par exemple : c : \\ Program Files \\ myapps \\MyApp.exe.

    [Table DrLocator](drlocator-table.md)

    

    | Signature          | Parent | Chemin | Profondeur        |
    |--------------------|--------|------|--------------|
    | AppFile<br/> |        |      | 3<br/> |

    

     

4.  Inclure l’action AppSearch dans la séquence d’action. Si MyApp.exe est installé, le programme d’installation définit la propriété MYAPP à l’emplacement du fichier. Si le fichier est installé, MYAPP prend la valeur true dans une expression conditionnelle.

 

 




