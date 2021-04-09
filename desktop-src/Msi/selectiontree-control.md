---
description: Ce contrôle permet à un utilisateur de modifier l’état de sélection des fonctionnalités listées dans le tableau des fonctionnalités.
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: Contrôle SelectionTree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5287736c3293c736d6d392ce8532b76ee7b62ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868837"
---
# <a name="selectiontree-control"></a>Contrôle SelectionTree

Ce contrôle permet à un utilisateur de modifier l’état de sélection des fonctionnalités listées dans le [tableau des fonctionnalités](feature-table.md). Le contrôle est associé à une propriété de valeur de chaîne que l’utilisateur peut définir par une [boîte de dialogue de navigation](browse-dialog.md). Vous pouvez associer le contrôle à une propriété en entrant le nom de la propriété dans la colonne propriété de la [table de contrôle](control-table.md).

Le contrôle SelectionTree publie automatiquement les événements de [contrôle](control-events.md) suivants sur Windows XP ou les systèmes d’exploitation antérieurs. Le contrôle SelectionTree publie ces événements lorsque l’élément sélectionné est modifié d’un nœud à un autre. Si l’arborescence de sélection n’a pas de nœud, le contrôle publie ces événements et efface le contenu des contrôles qui s’abonnent à l’événement. Il n’est pas nécessaire que ces ControlEvents soient répertoriés dans la [table ControlEvent,](controlevent-table.md).



| Événement de contrôle                                                 | Description                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [SelectionAction](selectionaction-controlevent.md)           | Publie une chaîne à partir de la [table UIText](uitext-table.md) décrivant l’élément mis en surbrillance.      |
| [SelectionBrowse](selectionbrowse-controlevent.md)           | Génère une boîte de dialogue Parcourir utilisée pour modifier le chemin d’accès de l’élément mis en surbrillance.                     |
| [SelectionDescription](selectiondescription-controlevent.md) | Publie une chaîne à partir de la [table de fonctionnalités](feature-table.md) décrivant l’élément mis en surbrillance.    |
| [SelectionNoItems](selectionnoitems-controlevent.md)         | Supprime le texte descriptif ou désactive les boutons d’un élément obsolète.                          |
| [SelectionPath](selectionpath-controlevent.md)               | Publie le chemin d’accès de l’élément mis en surbrillance.                                                       |
| [SelectionPathOn](selectionpathon-controlevent.md)           | Publie une valeur indiquant si un chemin de sélection est associé à la fonctionnalité actuellement sélectionnée. |
| [Options de sélection](selectionsize-controlevent.md)               | Publie la taille de l’élément mis en surbrillance.                                                        |



 

À compter des systèmes Windows Server 2003, les contrôles SelectionTree publient tous les événements du tableau ci-dessus, et publient en outre un [ControlEvent, de script](doaction-controlevent.md) ou un [ControlEvent, SetProperty](setproperty-controlevent.md). Les enregistrements doivent être ajoutés à la [table ControlEvent,](controlevent-table.md) pour publier les actions de script ou SetProperty ControlEvents.



| Événement de contrôle                               | Description                                        |
|---------------------------------------------|----------------------------------------------------|
| [Action](doaction-controlevent.md)       | Notifie le programme d’installation d’exécuter une action personnalisée. |
| [setProperty](setproperty-controlevent.md) | Affecte une nouvelle valeur à une propriété.                    |



 

À partir de Windows Installer version 3,0, les contrôles SelectionTree publient un événement qui exécute des [actions personnalisées](custom-actions.md) énumérées dans la [table ControlEvent,](controlevent-table.md). Le contrôle SelectionTree publie cet événement chaque fois que la sélection de fonctionnalités change dans le contrôle ou chaque fois qu’un état de sélection différent est choisi pour la fonctionnalité actuelle. Les actions personnalisées s’exécutent chaque fois que l’événement est publié. Le contrôle SelectionTree envoie des informations à l’action personnalisée en définissant les valeurs des propriétés suivantes. Toutes ces propriétés sont effacées lorsque le contrôle SelectionTree est fermé.

**Windows Installer 2,0 :** Non pris en charge. Le contrôle SelectionTree ne publie pas l’événement et ne définit pas les propriétés suivantes.



| Propriété                                | Description                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsiSelectionTreeSelectedFeature         | Nom de la fonctionnalité sélectionnée dans le champ fonctionnalité du [tableau des fonctionnalités](feature-table.md).                                                                      |
| MsiSelectionTreeSelectedAction          | État de l’action d’installation de la fonctionnalité sélectionnée. La valeur peut être INSTALLSTATE \_ absente, InstallState \_ local, InstallState \_ source ou InstallState \_ publié. |
| MsiSelectonTreeChildrenCount            | Nombre de nœuds enfants directs.                                                                                                                                    |
| MsiSelectionTreeInstallingChildrenCount | Nombre de nœuds enfants directs qui sont des nœuds enfants INSTALLSTATE \_ local, InstallState \_ source ou InstallState \_ publiés.                                                    |
| MsiSelectionTreeSelectedCost            | Coût de l’installation de la fonctionnalité sélectionnée en unités de 512 octets.                                                                                                   |
| MsiSelectionTreeChildrenCost            | Coût de l’installation de toutes les fonctionnalités enfants en unités de 512 octets.                                                                                              |
| MsiSelectionTreeSelectedPath            | Chemin d’installation de la fonctionnalité sélectionnée. Défini uniquement si la fonctionnalité est installée en tant que INSTALLSTATE \_ local.                                       |



 

> [!Note]
>
> Le contenu du champ de texte de la [table de contrôle](control-table.md) n’est jamais affiché par le contrôle SelectionTree. Au lieu de cela, ce champ spécifie le style de texte à afficher par le contrôle et contient une description du contrôle utilisé par les utilitaires de révision d’écran. Pour définir la police et le style de police d’une chaîne de texte, ajoutez le préfixe { \\ style} ou {&*style*} à la chaîne de caractères affichés. Où style est un identificateur figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md). Si aucun de ces deux n’est présent, mais que la propriété [**DefaultUIFont**](defaultuifont.md) est définie en tant que style de texte valide, cette police est utilisée. Les informations suivantes sont lues par les utilitaires de révision d’écran comme description du contrôle. Consultez [accessibilité](accessibility.md).

 

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec ce contrôle. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                                               | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Nom d’une propriété indirecte associée au contrôle. Si le bit d’attribut indirect est défini, le contrôle affiche ou modifie la valeur de la propriété portant ce nom. Si le bit d’attribut indirect est défini, ce nom est également la valeur de la propriété figurant dans la colonne propriété de la [table de contrôle](control-table.md).                                    |
| [Position](position-control-attribute.md)                         |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la [table de contrôle](control-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nom de la propriété associée à ce contrôle. Si le bit d’attribut indirect n’est pas défini, le contrôle affiche ou modifie la valeur de la propriété portant ce nom. Cet attribut est spécifié dans la colonne propriété de la [table de contrôle](control-table.md).                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valeur actuelle de la propriété affichée ou modifiée par ce contrôle. Si le bit d’attribut indirect n’est pas défini, il s’agit de la valeur de PropertyName. Si le bit d’attribut indirect est défini, il s’agit de la valeur de IndirectPropertyName. Si l’attribut change, le contrôle reflète la nouvelle valeur.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Affiche le texte dans lecteurs en fonction du texte entré dans la colonne de texte de la [table de contrôle](control-table.md). Consultez [accessibilité](accessibility.md).                                                                                                                                                                                                          |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs dans la [table de contrôle](control-table.md) pour rendre le contrôle visible ou masqué lors de sa création.<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Contrôle dans un état désactivé. Contrôle dans un état activé.<br/> Incluez ce bit dans le mot de bits dans la colonne attributs du [contrôle](control-table.md) pour activer le contrôle lors de la création.<br/> Vous pouvez également activer ou désactiver un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Affiche le style visuel par défaut. Affiche le contrôle avec l’enfoncée, la 3D et l’apparence.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                             |
| [Indirect](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Le contrôle affiche ou modifie la valeur de la propriété dans la colonne propriété de la [table de contrôle](control-table.md). Le contrôle affiche ou modifie la valeur de la propriété qui a l’identificateur figurant dans la colonne propriété de la table de contrôle.<br/> Détermine si la propriété associée à ce contrôle est référencée indirectement.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Le texte du contrôle est affiché dans l’ordre de lecture de gauche à droite. Le texte du contrôle est affiché dans l’ordre de lecture de droite à gauche.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Le texte du contrôle est aligné à gauche. Le texte du contrôle est aligné à droite.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | La barre de défilement se trouve sur le côté droit du contrôle. La barre de défilement se trouve sur le côté gauche du contrôle.<br/>                                                                                                                                                                                                                                         |
| [BiDi](bidi-control-attribute.md)                                 | 0x000000E0                       | Définissez cette valeur pour une combinaison des attributs [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)et [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                          |



 

## <a name="remarks"></a>Notes

Ce contrôle peut être créé à partir de la \_ classe WC TreeView à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Il possède les styles de **\_ bordure WS**, **TV \_ HASLINES**, TV **\_ HASBUTTONS**, **TV \_ LINESATROOT**, **TV \_ DISABLEDRAGDROP**, **TV \_ SHOWSELALWAYS**, **WS \_ Child**, **WS \_ TABSTOP** et **WS \_ Group** .

L’arborescence de sélection n’est remplie que si l’action [CostInitialize](costinitialize-action.md) et l' [action CostFinalize](costfinalize-action.md) ont été appelées.

La chaîne suivante dans la [table UIText](uitext-table.md) est liée à ce contrôle.



| Terme                                                                                                         | Description                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>AbsentPath<br/> | Chemin d’accès affiché pour un élément dans l’État absent.<br/> |



 

Les six chaînes suivantes sont utilisées pour afficher le nombre d’enfants sélectionnés et la taille associée à l’élément mis en surbrillance :

-   SelChildCostPos
-   SelChildCostNeg
-   SelParentCostPosPos
-   SelParentCostPosNeg
-   SelParentCostNegPos
-   SelParentCostNegNeg

Les chaînes suivantes sont utilisées pour afficher les options de sélection disponibles pour un élément dans un menu contextuel :

-   MenuAbsent
-   MenuLocal
-   MenuCD
-   MenuNetwork
-   MenuAllLocal
-   MenuAllCD
-   MenuAllNetwork

Les chaînes suivantes sont utilisées pour expliquer la sélection actuelle dans le ControlEvent, [SelectionDescription](selectiondescription-controlevent.md) .

-   SelAbsentAbsent
-   SelAbsentLocal
-   SelAbsentCD
-   SelAbsentNetwork
-   SelLocalAbsent
-   SelLocalLocal
-   SelLocalCD
-   SelLocalNetwork
-   SelCDAbsent
-   SelNetworkAbsent
-   SelCDLocal
-   SelNetworkLocal
-   SelCDCD
-   SelNetworkNetwork

Les quatre chaînes localisées suivantes sont utilisées pour la mise en forme de la taille d’un fichier :

-   Octets
-   Ko
-   Mo
-   Go

 

 
