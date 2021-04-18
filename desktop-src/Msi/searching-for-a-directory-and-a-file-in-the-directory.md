---
description: Pendant une installation Windows Installer, le programme d’installation peut rechercher un répertoire et un fichier dans ce répertoire.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Recherche d’un répertoire et d’un fichier dans le répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519951"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a>Recherche d’un répertoire et d’un fichier dans le répertoire

**Pour rechercher un répertoire, puis un fichier dans ce répertoire**

1.  Commencez par Rechercher le répertoire.

    AppDir doit être défini comme signature valide du répertoire. Si AppDir n’est pas défini comme une signature valide, AppSearch n’a pas d’emplacement pour rechercher le fichier, par exemple, si la recherche est pour c : \\ MyDir \\MyApp.exe, appdir doit être défini comme c : \\ mydir. AppDir peut être défini en incluant un enregistrement dans la [table DrLocator](drlocator-table.md), ou par une autre méthode. Aucun enregistrement n’est inclus dans la [table de signatures](signature-table.md) pour la recherche dans l’annuaire. Pour la recherche de fichiers, répertoriez la signature et le nom de fichier dans la table de signatures. Les champs restants de cet enregistrement peuvent avoir la valeur null pour rechercher n’importe quelle version de MyApp.exe.

    [Table de signature](signature-table.md) (partielle)

    

    | Signature          | Nom de fichier            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Utilisez la [table AppSearch](appsearch-table.md).

    Entrez la propriété que le programme d’installation doit définir si le répertoire avec la signature AppDir est installé. Si le programme d’installation détecte que ce répertoire est installé, il définit MYDIR sur le chemin d’accès au répertoire. Entrez la propriété que le programme d’installation doit définir si MyApp.exe est installé.

    [Table AppSearch](appsearch-table.md) (partielle)

    

    | Propriété         | Signature          |
    |------------------|--------------------|
    | MYDIR<br/> | AppDir<br/>  |
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  Utilisez la [table DrLocator](drlocator-table.md).

    Entrez dans la colonne parent la signature, AppDir, qui est définie en tant que chemin d’accès du répertoire. Spécifiez dans la colonne profondeur le nombre de niveaux de sous-répertoires à rechercher dans ce répertoire. AppDir doit être défini comme signature de répertoire. AppDir peut être défini en incluant un enregistrement comme indiqué ici ou par une autre méthode.

    [Table DrLocator](drlocator-table.md)

    

    | Signature | Parent | Chemin d’accès      | Profondeur |
    |-----------|--------|-----------|-------|
    | AppDir    |        | C : \\ mydir | 0     |
    | AppFile   | AppDir |           | 0     |

    

     

4.  Inclure l’action AppSearch dans la séquence d’action.

    Si MyApp.exe est trouvé pour être installé dans AppDir, le programme d’installation définit la propriété MYAPP sur l’emplacement du fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




