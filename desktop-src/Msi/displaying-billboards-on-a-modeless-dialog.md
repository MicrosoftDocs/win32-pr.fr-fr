---
description: Les panneaux peuvent afficher une séquence d’images et de texte dans une boîte de dialogue au cours d’une installation. En règle générale, les panneaux sont utilisés pour créer l’effet visuel d’un diaporama ou d’une animation qui informe l’utilisateur de la progression d’une installation.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Affichage des panneaux dans une boîte de dialogue non modale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fd0ca40e47a8d52c16db7adde304177d4dc849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114574"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Affichage des panneaux dans une boîte de dialogue non modale

Les panneaux peuvent afficher une séquence d’images et de texte dans une boîte de dialogue au cours d’une installation. En règle générale, les panneaux sont utilisés pour créer l’effet visuel d’un diaporama ou d’une animation qui informe l’utilisateur de la progression d’une installation.

**Pour afficher des panneaux sur une boîte de dialogue non modale**

1.  Incluez un enregistrement dans la [table de boîtes de dialogue](dialog-table.md) pour la boîte de dialogue non modale qui contient le panneau. Après l’affichage d’un panneau, une boîte de dialogue non modale retourne le contrôle au programme d’installation. Cela permet au programme d’installation de traiter les messages et de mettre à jour la boîte de dialogue et le panneau. Pour créer une boîte de dialogue non modale, ne définissez pas le bit de style de boîte de dialogue modale dans le champ attributs de la [table de boîtes de dialogue](dialog-table.md). L’enregistrement de [table de boîte de dialogue](dialog-table.md) suivant spécifie la boîte de dialogue ActionDialog.

    [Table de boîtes de dialogue](dialog-table.md) (partielle)

    | Dialogue\_     | HCentering | VCentering | Largeur | Hauteur | Attributs | Intitulé  | \_Premier contrôle | \_Valeur par défaut du contrôle | Annuler le contrôle \_ |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | ActionDialog | 50         | 50         | 480   | 240    | 5          | Action | Annuler         | Annuler           | Annuler          |

    

     

2.  Ajoutez un enregistrement à la [table de contrôle](control-table.md) pour spécifier que la boîte de dialogue affiche un panneau. L’enregistrement définit la taille et la position de la zone dans la boîte de dialogue dans laquelle les contrôles de tableau blanc répertoriés dans la [table BBControl](bbcontrol-table.md) doivent être affichés. L’enregistrement de [table de contrôle](control-table.md) suivant définit la position et la taille du panneau dans la boîte de dialogue ActionDialog.

    [Table de contrôle](control-table.md) (partielle)

    | Dialogue\_     | Contrôler   | Type      | X   | O   | Largeur | Hauteur | Attributs |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | ActionDialog | Blanc | Blanc | 0   | 110 | 480   | 130    | 1          |

    

     

3.  Le [tableau des panneaux](billboard-table.md) affiche la liste des contrôles du panneau d’affichage et spécifie quand un contrôle de panneau d’affichage spécifique est affiché. Ajoutez un enregistrement à la [table de tableau blanc](billboard-table.md) pour chaque contrôle de tableau blanc. Le [tableau d’panneaux](billboard-table.md) surveille les messages de progression envoyés pendant une installation. Un panneau s’affiche uniquement lorsqu’un message de progression est envoyé par les actions répertoriées dans la colonne action de la [table de tableau blanc](billboard-table.md), et uniquement si la fonctionnalité dans le \_ champ fonctionnalité est sélectionnée pour l’installation. Une fois le panneau affiché, il reste visible jusqu’à ce qu’il soit couvert par un autre panneau, ou jusqu’à la fermeture de la boîte de dialogue. Si plusieurs panneaux sont spécifiés pour une action, ils sont affichés l’un après l’autre dans l’ordre spécifié par le champ de tri. Par exemple, les entrées de [table de tableau blanc](billboard-table.md) suivantes affichent d’abord les BB1, puis les contrôles de tableau [blanc](billboard-control.md) BB2 lorsque l’action [InstallFiles](installfiles-action.md) est exécutée et que la fonctionnalité QuickTest a été sélectionnée pour être installée.

    [Table de tableau blanc](billboard-table.md) (partielle)

    | Blanc | Fonctionnalité   | Action       | Classement |
    |-----------|-----------|--------------|----------|
    | BB1       | QuickTest | InstallFiles | 1        |
    | BB2       | QuickTest | InstallFiles | 2        |

    

     

4.  La [table BBControl](bbcontrol-table.md) spécifie les contrôles qui appartiennent aux [contrôles](billboard-control.md) de tableau blanc répertoriés dans le [tableau](billboard-table.md)d’affiche. Le contrôle de [texte](text-control.md), le [contrôle bitmap](bitmap-control.md)et le [contrôle Icon](icon-control.md) sont les seuls types de contrôles qui peuvent être placés sur un panneau. Vous pouvez placer plusieurs contrôles sur chaque panneau. Entrez le nom du panneau dans le \_ champ de tableau blanc de la [table BBControl](bbcontrol-table.md) exactement tel qu’il apparaît dans la [table du tableau blanc](billboard-table.md).

    Chaque position de contrôle est spécifiée en tant que coordonnées du coin supérieur gauche du contrôle. L’origine du système de coordonnées se trouve dans le coin supérieur gauche du contrôle de tableau blanc plutôt que dans un coin de la boîte de dialogue. Les coordonnées se trouvent dans les unités d’installation, et non dans les unités de boîte de dialogue. Une unité d’installation est égale à 1 douzième la hauteur de la taille de police MS sans serif à 10 points. La [table BBControl](bbcontrol-table.md) suivante enregistre les contrôles de liens vers des panneaux.

    [Table BBControl](bbcontrol-table.md) (partielle)

    | Blanc | BBControl | Type   | X   | O   | Largeur | Hauteur | Attributs | Texte             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Texte      | Texte   | 100 | 30  | 280   | 280    | 3          | Premier tableau blanc  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Logiciel         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Musique            |
    | BB2       | Texte      | Texte   | 100 | 30  | 280   | 20     | 3          | Deuxième panneau |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Musique            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Logiciel         |

    

     

5.  Pour afficher un panneau d’affichage dans la boîte de dialogue ActionDialog, vous devez abonner le contrôle du panneau d’affichage à [SetProgress ControlEvent,](setprogress-controlevent.md) en ajoutant un enregistrement à la [table EventMapping](eventmapping-table.md). Quand le programme d’installation publie le ControlEvent, SetProgress spécifié dans la colonne d’événement, le programme d’installation définit l’attribut de contrôle qui est spécifié dans le champ d’attribut. Le champ d’événement contient l’identificateur de chaîne (sans guillemets) du ControlEvent, SetProgress. Le champ d’attribut contient l’identificateur de chaîne (sans guillemets) de l’attribut à définir. Les champs de boîte de dialogue \_ et de contrôle \_ identifient le contrôle de tableau blanc et doivent correspondre à ces champs dans la [table de contrôle](control-table.md). Par exemple, la [table EventMapping](eventmapping-table.md) suivante abonne un contrôle à un événement.

    [Table EventMapping](eventmapping-table.md) (partielle)

    | Dialogue\_     | contrôle\_ | Événement       | Attribut |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | Blanc | SetProgress | Progress  |

    

     

 

 



