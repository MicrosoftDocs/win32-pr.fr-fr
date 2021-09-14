---
description: Un contrôle DirectoryList affiche une partie du chemin d’accès qui est actuellement affiché dans le contrôle PathEdit. Le contrôle DirectoryList affiche les dossiers situés sous le répertoire actuellement affiché par le contrôle DirectoryCombo.
ms.assetid: 05e70381-28c0-4568-808e-ff2dee8ff790
title: Contrôle DirectoryList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6a1e48a25ae057c836c7b815dae18e7dcf5c3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091557"
---
# <a name="directorylist-control"></a>Contrôle DirectoryList

Un contrôle DirectoryList affiche une partie du chemin d’accès qui est actuellement affiché dans le [contrôle PathEdit](pathedit-control.md). Le contrôle DirectoryList affiche les dossiers situés sous le répertoire actuellement affiché par le [contrôle DirectoryCombo](directorycombo-control.md).

Les contrôles PathEdit, DirectoryCombo et DirectoryList sont associés à la même propriété de valeur de chaîne. Cette propriété est le chemin d’accès sélectionné par l’utilisateur. Entrez le nom de la propriété dans la colonne propriété de la [table de contrôle](control-table.md). Cette propriété doit avoir une valeur initiale contenant au moins un volume et un sous-niveau. Spécifiez la valeur initiale de la propriété dans la colonne valeur de la [table de propriétés](property-table.md).

Ce contrôle est destiné à être utilisé dans une [boîte de dialogue de navigation](browse-dialog.md) avec le contrôle [PathEdit](pathedit-control.md) et DirectoryList.

Le contrôle DirectoryList publie le ControlEvents suivant.



| ControlEvent                                            | Description                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| [DirectoryListNew](directorylistnew-controlevent.md)   | Crée un nouveau dossier et sélectionne le champ de nom à modifier.      |
| [IgnoreChange](ignorechange-controlevent.md)           | Met en surbrillance, mais ne s’ouvre pas, un dossier dans le répertoire actif. |
| [DirectoryListUp](directorylistup-controlevent.md)     | Sélectionne le parent du répertoire actuel.                      |
| [DirectoryListOpen](directorylistopen-controlevent.md) | Sélectionne et met en surbrillance un répertoire.                               |



 

Le contenu du champ de texte de la [table de contrôle](control-table.md) n’est jamais affiché par le contrôle DirectoryList. Au lieu de cela, ce champ spécifie le style de texte à afficher par le contrôle et contient une description du contrôle utilisé par les utilitaires de révision d’écran. Pour définir la police et le style de police d’une chaîne de texte, ajoutez le préfixe { \\ style} ou {&*style*} à la chaîne de caractères affichés. Où style est un identificateur figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md). Si aucun de ces deux n’est présent, mais que la propriété [**DefaultUIFont**](defaultuifont.md) est définie comme un style de texte valide, cette police sera utilisée. Les informations suivantes sont lues par les utilitaires de révision d’écran comme description du contrôle. Consultez [accessibilité](accessibility.md).

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec ce contrôle. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                                               | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Il s’agit du nom d’une propriété indirecte associée au contrôle. Si le bit d’attribut indirect est défini, le contrôle affiche ou modifie la valeur de la propriété portant ce nom. Si le bit d’attribut indirect est défini, ce nom est également la valeur de la propriété figurant dans la colonne propriété de la [table de contrôle](control-table.md).                        |
| [Position](position-control-attribute.md)                         |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la [table de contrôle](control-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Il s’agit du nom de la propriété associée à ce contrôle. Si le bit d’attribut indirect n’est pas défini, le contrôle affiche ou modifie la valeur de la propriété portant ce nom. Cet attribut est spécifié dans la colonne propriété de la [table de contrôle](control-table.md).                                                                                        |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valeur actuelle de la propriété affichée ou modifiée par ce contrôle. Si le bit d’attribut indirect n’est pas défini, il s’agit de la valeur de PropertyName. Si le bit d’attribut indirect est défini, il s’agit de la valeur de IndirectPropertyName. Si l’attribut change, le contrôle reflète la nouvelle valeur.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Pour afficher du texte dans les lecteurs d’écran, entrez le texte dans la colonne de texte de la [table de contrôle](control-table.md). Consultez [accessibilité](accessibility.md).                                                                                                                                                                                                                 |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs dans la [table de contrôle](control-table.md). pour rendre le contrôle visible ou masqué lors de sa création.<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                     |
| [Activé](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Contrôle dans un état désactivé. Contrôle dans un état activé.<br/> Incluez ce bit dans le mot de bits dans la colonne attributs du [contrôle](control-table.md) pour activer le contrôle lors de la création.<br/> Vous pouvez également activer ou désactiver un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Affiche le style visuel par défaut. Affiche le contrôle avec l’enfoncée, la 3D et l’apparence.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                             |
| [Indirect](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Le contrôle affiche ou modifie la valeur de la propriété dans la colonne propriété de la [table de contrôle](control-table.md). Le contrôle affiche ou modifie la valeur de la propriété qui a l’identificateur figurant dans la colonne propriété de la table de contrôle.<br/> Détermine si la propriété associée à ce contrôle est référencée indirectement.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Le texte du contrôle est affiché dans l’ordre de lecture de gauche à droite. Le texte du contrôle est affiché dans l’ordre de lecture de droite à gauche.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Le texte du contrôle est aligné à gauche. Le texte du contrôle est aligné à droite.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | La barre de défilement se trouve sur le côté droit du contrôle. La barre de défilement se trouve sur le côté gauche du contrôle.<br/>                                                                                                                                                                                                                                         |
| [Contrôle BiDi](bidi-control-attribute.md)                         | 0x000000E0                       | Définissez cette valeur pour une combinaison des attributs [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)et [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                          |



 

## <a name="remarks"></a>Notes

Ce contrôle peut être créé à partir de la \_ classe WC ListView à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Elle contient les styles **LVS \_ List**, **LVS \_ EDITLABELS**, **WS \_ VSCROLL**, LVS **\_ SHAREIMAGELISTS**, **LVS \_ AutoArrange**, LVS **\_ SINGLESEL**, **WS \_ Border**, **LVS \_ SORTASCENDING**, **WS \_ Child**, **WS \_ Group** et **WS \_ TABSTOP** .

Ce contrôle permet à l’utilisateur de sélectionner un sous-dossier de la sélection actuelle. Avec des boutons supplémentaires, il permet également à l’utilisateur de sélectionner un nouveau dossier dans la sélection actuelle ou de remonter d’un niveau dans le chemin d’accès. Si l’utilisateur choisit le bouton **créer un nouveau dossier** dans un dossier où un nouveau dossier existe déjà, un deuxième dossier n’est pas créé et le nom du nouveau dossier existant est sélectionné pour modification.

 

