---
title: Élément LISTBOX
description: Élément LISTBOX
ms.assetid: b83ba0cb-1838-494d-b4cb-55b4da18a038
keywords:
- skins Lecteur Windows Media, élément LISTBOX
- Skins, élément LISTBOX
- Élément LISTBOX
- informations de référence sur les habillages, élément LISTBOX
- éléments, LISTBOX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9108d8e252260a8aa7a2d9f654118d62ff84f0d53a6f80bc934323a1107ffe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054767"
---
# <a name="listbox-element"></a>Élément LISTBOX

L’élément **ListBox** offre aux utilisateurs la possibilité de sélectionner des éléments dans une liste. Ces éléments peuvent être spécifiés à l’aide d’éléments **Item** comme enfants de l’élément **ListBox** . Si vous avez besoin d’un contrôle de zone de liste qui s’affiche uniquement lorsque cela est nécessaire, utilisez l’élément **Popup** , qui est identique à l’élément **ListBox** , à l’exception de la valeur par défaut de l’attribut **Popup** , qui détermine son comportement d’affichage.

L’élément **ListBox** prend en charge les attributs suivants.



| Attribut                                        | Description                                                                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](listbox-backgroundcolor.md)   | Spécifie ou récupère la couleur d’arrière-plan dans le contrôle de zone de liste.                                                  |
| [2S](listbox-border.md)                     | Spécifie ou récupère une valeur indiquant si le contrôle de zone de liste a une bordure. Ne peut être défini qu’au moment de la conception.  |
| [firstVisibleItem](listbox-firstvisibleitem.md) | Spécifie ou récupère l’index de la première ligne visible dans le contrôle de zone de liste.                                   |
| [focusItem](listbox-focusitem.md)               | Spécifie ou récupère la ligne qui contient le focus.                                                                  |
| [fontFace](listbox-fontface.md)                 | Spécifie ou récupère la police du contrôle de zone de liste.                                                             |
| [fontSize](listbox-fontsize.md)                 | Spécifie ou récupère la taille de police pour le contrôle de zone de liste.                                                        |
| [fontStyle](listbox-fontstyle.md)               | Spécifie ou récupère le style de police pour le contrôle de zone de liste.                                                       |
| [foregroundColor](listbox-foregroundcolor.md)   | Spécifie ou récupère la couleur du texte dans le contrôle de zone de liste.                                                        |
| [itemCount](listbox-itemcount.md)               | Récupère le nombre d’éléments dans le contrôle de zone de liste.                                                                |
| [Sélection multiple](listbox-multiselect.md)           | Spécifie ou récupère une valeur indiquant si l’utilisateur peut sélectionner plusieurs lignes. Ne peut être défini qu’au moment de la conception. |
| [Messages](listbox-popup.md)                       | Spécifie une valeur indiquant si l’élément représente un contrôle Popup ou zone de liste.                              |
| [readOnly](listbox-readonly.md)                 | Spécifie ou récupère une valeur indiquant si le texte est en lecture seule ou si le texte peut être sélectionné par l’utilisateur.              |
| [selectedItem](listbox-selecteditem.md)         | Spécifie ou récupère l’index de l’élément sélectionné dans le contrôle de zone de liste.                                        |
| [triées](listbox-sorted.md)                     | Spécifie ou récupère une valeur indiquant si le contrôle de zone de liste est trié par ordre alphabétique.                      |



 

L’élément **ListBox** prend en charge les méthodes suivantes.



| Méthode                                                 | Description                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [appendItem](listbox-appenditem.md)                   | Insère un nouveau texte à la fin du contrôle de zone de liste.                                                                  |
| [deleteAll](listbox-deleteall.md)                     | Supprime tous les éléments du contrôle de zone de liste.                                                                          |
| [deleteItem](listbox-deleteitem.md)                   | Supprime l’élément de contrôle de zone de liste à l’index spécifié.                                                             |
| [licencie](listbox-dismiss.md)                         | Masque le contrôle.                                                                                                    |
| [findItem](listbox-finditem.md)                       | Recherche une chaîne donnée en commençant par l’élément qui suit l’index d’élément spécifié.                                |
| [getItem](listbox-getitem.md)                         | Récupère le texte de l’élément avec l’index spécifié.                                                             |
| [getNextSelectedItem](listbox-getnextselecteditem.md) | Récupère l’élément sélectionné suivant dans le contrôle de zone de liste à partir de l’élément après celui avec l’index spécifié. |
| [insertItem](listbox-insertitem.md)                   | Insère le texte spécifié à l’index spécifié dans le contrôle de zone de liste.                                            |
| [replaceItem](listbox-replaceitem.md)                 | Remplace le texte à l’index spécifié par le texte spécifié.                                                     |
| [setSelectedState](listbox-setselectedstate.md)       | Sélectionne ou désélectionne l’élément avec l’index spécifié.                                                               |
| [show](listbox-show.md)                               | Affiche le contrôle.                                                                                                 |



 

> [!Note]  
> cet élément requiert Lecteur Windows Media pour Windows XP ou version ultérieure.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**POPUP (élément)**](popup-element.md)
</dt> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




