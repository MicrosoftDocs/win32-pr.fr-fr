---
description: cette section décrit comment ajouter des chaînes de ressources à la Windows Installer tableau de raccourcis pour une utilisation avec des Interfaces utilisateur multilingues (MUI).
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: Exemple de raccourci MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b38f674a63e854fbcd4439229c5aded5b0efe6cfc17d3e475f8a52f30db949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640286"
---
# <a name="a-mui-shortcut-example"></a>Exemple de raccourci MUI

cette section décrit comment ajouter des chaînes de ressources à la Windows Installer tableau de [raccourcis](shortcut-table.md) pour une utilisation avec des Interfaces utilisateur multilingues (MUI).

**Windows Installer 2,0 et Windows Installer 3,0 :** Non pris en charge. cet exemple requiert Windows Installer 4,0.

reportez-vous à la documentation du [interface utilisateur multilingue (mui)](/windows/desktop/Intl/multilingual-user-interface) pour plus d’informations sur le développement d’applications compatibles mui.

pour ajouter les chaînes de ressources utilisées par Windows les Interfaces utilisateur multilingues Vista à un package Windows Installer :

1.  Ajoutez les informations de tous les fichiers de langue et de langue neutres à la [table de fichiers](file-table.md). Par exemple, les fichiers peuvent se composer d’un fichier indépendant de la langue (msimsg.dll) et de fichiers de langue pour l’anglais (msimsgen.dll. MUI), le japonais (msimsgja.dll. MUI) et le chinois (msimsgcs.dll. MUI). Chaque fichier peut appartenir à un autre composant. Chaque fichier peut avoir un nom de fichier long et un nom de fichier courts. Dans le cas de cet exemple, les informations suivantes peuvent être ajoutées à la [table file](file-table.md).

    [Table de fichiers](file-table.md) (partielle)

    

    | Fichier        | Composant\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmuija | MSIMSG \_ MUI \_ ja | msimsgja.dll\|msimsg.dll. mui |
    | msimsgmuics | \_CS MSIMSG MUI \_ | msimsgcs.dll\|msimsg.dll. mui |
    | msimsgmuien | MSIMSG \_ MUI \_ en | msimsgen.dll\|msimsg.dll. mui |
    | msimsgdll   | MSIMSG          | msimsg.dll                   |

    

     

2.  Ajoutez des informations à la [table des composants](component-table.md) pour ces composants. Chaque composant a un identificateur GUID unique qui doit être entré dans le champ ComponentId de la table des composants. Le fichier appartenant au composant peut servir de chemin d’accès au keyPath pour ce composant. Le répertoire qui contient chaque composant peut être spécifié dans le \_ champ Répertoire. Les informations suivantes peuvent être ajoutées à la table des composants.

    [Table des composants](component-table.md) (partielle)

    

    | Composant       | Répertoire\_   | KeyPath     |
    |-----------------|---------------|-------------|
    | MSIMSG \_ MUI \_ ja | MUIFolder \_ ja | msimsgmuija |
    | \_CS MSIMSG MUI \_ | MUIFolder \_ CS | msimsgmuics |
    | MSIMSG \_ MUI \_ en | MUIFolder \_ en | msimsgmuien |
    | MSIMSG          | MUIFolder     | msimsgdll   |

    

     

3.  Modifiez la table des [répertoires](directory-table.md) afin que les composants soient installés dans les répertoires appropriés. Veillez à inclure des informations sur le répertoire dans lequel le raccourci sera installé. Par exemple, les informations suivantes peuvent être ajoutées à la table des répertoires d’un package qui installe les composants et un raccourci situé dans le répertoire DesktopFolder

    [Table de répertoires](directory-table.md) (partielle)

    

    | Répertoire     | Répertoire \_ parent | DefaultDir |
    |---------------|-------------------|------------|
    | TARGETDIR     |                   | SourceDir  |
    | MsiTest       | TARGETDIR         | MsiTest:.  |
    | MUIFolder     | MsiTest           | MUI        |
    | MUIFolder \_ CS | MUIFolder         | cs-CZ      |
    | MUIFolder \_ en | MUIFolder         | fr-FR      |
    | MUIFolder \_ ja | MUIFolder         | ja-JP      |
    | DesktopFolder | TARGETDIR         | .          |

    

     

4.  Ajoutez une ligne à la table de [raccourcis](shortcut-table.md) pour chaque raccourci. Par exemple, la table de [raccourcis](shortcut-table.md) peut contenir les informations suivantes pour deux raccourcis, Quick1 et Quick2, installés dans le répertoire DirectoryFolder. Chaque raccourci appartient à la fonctionnalité spécifiée dans le champ cible. L’icône associée au raccourci peut être spécifiée dans le champ icône \_ et la table [icône](icon-table.md) .

    [Table de raccourcis](shortcut-table.md) (partielle)

    

    | Raccourci | Répertoire\_   | Composant\_ | Cible               | Icône             |
    |----------|---------------|-------------|----------------------|------------------|
    | Quick1   | DesktopFolder | MSIMSG      | FeatureChild1 \_ local | HelpFileIcon.exe |
    | Quick2   | DesktopFolder | MSIMSG      | FeatureChild1 \_ local | HelpFileIcon.exe |

    

     

5.  Ajoutez des informations à la table des [fonctionnalités](feature-table.md) de la fonctionnalité propriétaire du raccourci. Lorsque le raccourci est activé, le programme d’installation vérifie que tous les composants appartenant à cette fonctionnalité sont installés avant de lancer le fichier de clé du composant spécifié dans la \_ colonne composant du tableau de [raccourcis](shortcut-table.md) . Dans le cas de cet exemple, les informations suivantes peuvent être ajoutées à la table de la table des fonctionnalités pour la \_ fonctionnalité locale FeatureParent1.

    [Table des fonctionnalités](feature-table.md) (partielle)

    

    | Fonctionnalité               | Parent de la fonctionnalité \_       | Titre                 | Attributs |
    |-----------------------|-----------------------|-----------------------|------------|
    | FeatureParent1 \_ local |                       | FeatureParent1 \_ local | 16         |
    | FeatureChild1 \_ local  | FeatureParent1 \_ local | FeatureParent1 \_ local | 0          |

    

     

6.  Pour chaque nouveau raccourci, ajoutez les informations de la chaîne de ressource aux champs DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL et DescriptionResourceId de la [table de raccourcis](shortcut-table.md). Les champs DisplayResourceDLL et DescriptionResourceDLL contiennent la chaîne de ressource au format de chaîne [mis en forme](formatted.md) . La chaîne mise en forme peut utiliser la \[ \# convention *filekey* \] du format [mis en forme](formatted.md) . Ajoutez les index d’affichage et de description pour les chaînes de ressource dans les champs DisplayResourceId et DescriptionResourceId.

    [Table de raccourcis](shortcut-table.md) (partielle)

    

    | Raccourci | DisplayResourceDLL | DisplayResourceId | DescriptionResourceDLL | DescriptionResourceId |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Quick1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Quick2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  après avoir installé le package, effectuez un test pour vérifier que le interface utilisateur multilingue fonctionne comme prévu.

 

 
