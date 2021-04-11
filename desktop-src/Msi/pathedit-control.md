---
description: Le contrôle PathEdit affiche un champ d’édition qui permet à un utilisateur de sélectionner la section de fin d’un chemin d’accès.
ms.assetid: 074ef4d5-3ac1-4bdb-90c5-9798d89a749f
title: Contrôle PathEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65d1237199f202e6c674ab4526ccd4747b02c09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202873"
---
# <a name="pathedit-control"></a>Contrôle PathEdit

Le contrôle PathEdit affiche un champ d’édition qui permet à un utilisateur de sélectionner la section de fin d’un chemin d’accès. Ce contrôle prend en charge l’entrée du nom de dossier sélectionné ou du chemin d’accès complet dans le champ d’édition. Un utilisateur peut également entrer un chemin UNC (Universal Naming Convention) vers un lecteur qui n’a pas de lettre de lecteur. Si l’utilisateur entre un segment de fin pour le chemin d’accès non valide pour le volume actuel, le contrôle PathEdit ne peut pas transférer le focus vers le contrôle suivant.

Les contrôles PathEdit, [DirectoryCombo](directorycombo-control.md)et [DirectoryList](directorylist-control.md) sont associés à la même propriété de valeur de chaîne. Cette propriété est le chemin d’accès sélectionné par l’utilisateur. Entrez le nom de la propriété dans la colonne propriété de la [table de contrôle](control-table.md). Cette propriété doit avoir une valeur initiale contenant au moins un volume et un sous-niveau. Spécifiez la valeur initiale de la propriété dans la colonne valeur de la [table de propriétés](property-table.md).

Ce contrôle est destiné à être utilisé dans une [boîte de dialogue de navigation](browse-dialog.md) avec les contrôles PathEdit et [DirectoryList](directorylist-control.md) .

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec ce contrôle. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                                               | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Il s’agit du nom d’une propriété indirecte associée au contrôle. Si le bit d’attribut indirect est défini, le contrôle affiche ou modifie la valeur de la propriété portant ce nom. Si le bit d’attribut indirect est défini, ce nom est également la valeur de la propriété figurant dans la colonne propriété de la [table de contrôle](control-table.md).                                                                                                                                                                              |
| [Position](position-control-attribute.md)                         |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la [table de contrôle](control-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                                                                                                                                                                                                                   |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Il s’agit du nom de la propriété associée à ce contrôle. Si le bit d’attribut indirect n’est pas défini, le contrôle affiche ou modifie la valeur de la propriété portant ce nom. Cet attribut est spécifié dans la colonne propriété de la [table de contrôle](control-table.md).                                                                                                                                                                                                                                              |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valeur actuelle de la propriété affichée ou modifiée par ce contrôle. Si le bit d’attribut indirect n’est pas défini, il s’agit de la valeur de PropertyName. Si le bit d’attribut indirect est défini, il s’agit de la valeur de IndirectPropertyName. Si l’attribut change, le contrôle reflète la nouvelle valeur.                                                                                                                                                                                                                                 |
| [Text](text-control-attribute.md)                                 |                                  | Pour définir la police et le style de police d’une chaîne de texte, ajoutez le préfixe { \\ style} ou {&style} à la chaîne de caractères affichés. Où style est un identificateur figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md). Si aucun de ces deux n’est présent, mais que la propriété [**DefaultUIFont**](defaultuifont.md) est définie comme un style de texte valide, cette police sera utilisée. Pour spécifier le nombre de caractères que l’utilisateur peut entrer, ajoutez {n} après les spécifications de police, où n est un entier positif.<br/> |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs dans la [table de contrôle](control-table.md) pour rendre le contrôle visible ou masqué lors de sa création.<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                           |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Contrôle dans un état désactivé. Contrôle dans un état activé.<br/> Incluez ce bit dans le mot de bits dans la colonne attributs du [contrôle](control-table.md) pour activer le contrôle lors de la création.<br/> Vous pouvez également activer ou désactiver un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Affiche le style visuel par défaut. Affiche le contrôle avec une apparence enfoncée, 3D et un look.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                  |
| [Indirect](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Le contrôle affiche ou modifie la valeur de la propriété dans la colonne propriété de la [table de contrôle](control-table.md). Le contrôle affiche ou modifie la valeur de la propriété qui a l’identificateur figurant dans la colonne propriété de la table de contrôle.<br/> Détermine si la propriété associée à ce contrôle est référencée indirectement.<br/>                                                                                                                                                       |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Le texte du contrôle est affiché dans l’ordre de lecture de gauche à droite. Le texte du contrôle est affiché dans l’ordre de lecture de droite à gauche.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Le texte du contrôle est aligné à gauche. Le texte du contrôle est aligné à droite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Notes

Le contrôle PathEdit est dérivé du contrôle d' [édition](edit-control.md) .

Pour la compatibilité avec les lecteurs d’écran, lors de la création d’une boîte de dialogue avec un contrôle PathEdit comme premier contrôle actif, vous devez faire en sorte que le champ de texte appartenant au champ d’édition soit le premier contrôle actif de la [table de boîtes de dialogue](dialog-table.md). Étant donné que le texte statique ne peut pas prendre le focus, lorsque la boîte de dialogue est créée, le champ d’édition a le focus initialement comme prévu. Cela permet de s’assurer que les lecteurs d’écran affichent les informations correctes.

 

 




