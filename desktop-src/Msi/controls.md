---
description: Les développeurs de packages d’installation peuvent créer une interface utilisateur contenant les contrôles abordés dans cette rubrique.
ms.assetid: ed9fa158-9dad-4d2d-8153-78122b19a34e
title: contrôles (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47755cafc3d4d3d04ed443410571a9c4fc2cf215a3efb3584265dcbeb2f9d520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143363"
---
# <a name="controls-windows-installer"></a>contrôles (Windows Installer)

Les développeurs de packages d’installation peuvent créer une interface utilisateur contenant les contrôles abordés dans cette rubrique. Pour plus d’informations sur l’ajout d’un contrôle particulier à une boîte de dialogue, consultez la rubrique relative à ce contrôle et lisez la section [Ajout de contrôles et de texte](adding-controls-and-text.md).

Certains contrôles, tels que CheckBox et ComboBox, sont associés à une propriété spécifiée dans la colonne propriété de la [table de contrôle](control-table.md). Un utilisateur modifie la valeur de cette propriété en interagissant avec le contrôle. Les contrôles passifs, tels que les panneaux et les bitmaps, ne sont pas associés à une telle propriété.

Pour la sécurité, les propriétés privées ne peuvent pas être modifiées par un utilisateur qui interagit avec l’interface utilisateur. Pour qu’une propriété soit définie par l’interface utilisateur, elle doit être une propriété publique et en majuscules. Voir aussi [à propos des propriétés](about-properties.md).

Dans certains cas, un contrôle peut être redessiné de manière incorrecte lors de l’annulation d’une boîte de dialogue. Cela s’effectue avec l’ordre dans lequel les contrôles reçoivent des \_ messages WM Paint après la suppression de la boîte de dialogue annuler. Pour résoudre ce problème, essayez de modifier l’ordre des contrôles dans la table de contrôle.



| Nom du contrôle                                       | Propriété associée | Brève description du contrôle                                                                                                                                                          |
|----------------------------------------------------|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Blanc](billboard-control.md)                 | Non                  | Affiche des panneaux en fonction des messages de progression.                                                                                                                                       |
| [Bitmap](bitmap-control.md)                       | Non                  | Affiche une image statique d’une image bitmap.                                                                                                                                                |
| [CheckBox](checkbox-control.md)                   | Oui                 | Case à cocher à deux États.                                                                                                                                                                |
| [ComboBox](combobox-control.md)                   | Oui                 | Liste déroulante avec un champ d’édition.                                                                                                                                                  |
| [DirectoryCombo](directorycombo-control.md)       | Oui                 | Sélectionnez tout sauf le dernier segment du chemin d’accès.                                                                                                                                       |
| [DirectoryList](directorylist-control.md)         | Oui                 | Affiche les dossiers sous la partie principale du chemin d’accès.                                                                                                                                         |
| [Modifier](edit-control.md)                           | Oui                 | Un champ de modification régulier pour une chaîne ou un entier.                                                                                                                                       |
| [GroupBox](groupbox-control.md)                   | Non                  | Affiche un rectangle qui regroupe d’autres contrôles.                                                                                                                             |
| [Lien hypertexte](hyperlink-control.md)                 | Non                  | Affiche un lien HTML vers une adresse, qui s’ouvre dans le navigateur par défaut. **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/> |
| [Icône](icon-control.md)                           | Non                  | Affiche une image statique d’une icône.                                                                                                                                                 |
| [Ligne](line-control.md)                           | Non                  | Affiche une ligne horizontale.                                                                                                                                                           |
| [ListBox](listbox-control.md)                     | Oui                 | Liste déroulante sans champ d’édition.                                                                                                                                               |
| [ListView](listview-control.md)                   | Oui                 | Affiche une colonne de valeurs avec des icônes pour la sélection.                                                                                                                                 |
| [MaskedEdit](maskededit-control.md)               | Oui                 | Un champ d’édition avec un masque dans le champ de texte.                                                                                                                                          |
| [PathEdit](pathedit-control.md)                   | Oui                 | Affiche le nom de dossier ou le chemin d’accès complet dans un champ d’édition.                                                                                                                                 |
| [ProgressBar, contrôle](progressbar-control.md)     | Non                  | Graphique à barres qui modifie la longueur quand elle reçoit des messages de progression.                                                                                                                       |
| [Boutons](pushbutton-control.md)               | Non                  | Affiche un bouton de commande de base.                                                                                                                                                         |
| [RadioButtonGroup](radiobuttongroup-control.md)   | Oui                 | Groupe de cases d’option.                                                                                                                                                             |
| [ScrollableText](scrollabletext-control.md)       | Non                  | Affiche une longue chaîne de texte.                                                                                                                                                       |
| [SelectionTree](selectiontree-control.md)         | Oui                 | Affiche des informations de la table de fonctionnalités et permet à l’utilisateur de modifier son état de sélection.                                                                                     |
| [Text](text-control.md)                           | Non                  | Affiche du texte statique.                                                                                                                                                                 |
| [VolumeCostList](volumecostlist-control.md)       | Non                  | Affiche des informations sur les coûts sur différents volumes.                                                                                                                                    |
| [VolumeSelectCombo](volumeselectcombo-control.md) | Oui                 | Sélectionne le volume à partir d’une liste alphabétique.                                                                                                                                             |



 

 

 




