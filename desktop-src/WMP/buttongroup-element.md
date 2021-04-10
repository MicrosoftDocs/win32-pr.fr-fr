---
title: Élément BUTTONGROUP
description: Élément BUTTONGROUP
ms.assetid: 4756c016-3347-4129-be5e-e822270a24de
keywords:
- Apparences du lecteur Windows Media, élément BUTTONGROUP
- habillages, élément BUTTONGROUP
- Élément BUTTONGROUP
- informations de référence sur les habillages, élément BUTTONGROUP
- éléments, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4de489e779b5e20214778b56fd8d19c7627e444
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100789"
---
# <a name="buttongroup-element"></a>Élément BUTTONGROUP

L’élément **BUTTONGROUP** fournit un moyen de regrouper plusieurs boutons dans une apparence. Ces boutons peuvent être spécifiés en utilisant des éléments **BUTTONELEMENT** comme enfants de l’élément **BUTTONGROUP** .

L’élément **BUTTONGROUP** prend en charge les attributs suivants.



| Attribut                                              | Description                                                                                                                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [buttonCount](buttongroup-buttoncount.md)             | Récupère le nombre de boutons dans **BUTTONGROUP**.                                                                                                                                                                         |
| [cursor](buttongroup-cursor.md)                       | Spécifie ou récupère le type de curseur qui apparaît lorsque la souris se trouve sur un bouton dans le **BUTTONGROUP**.                                                                                                                  |
| [disabledImage](buttongroup-disabledimage.md)         | Spécifie ou récupère le nom de l’image représentant l’état désactivé des boutons dans le **BUTTONGROUP**.                                                                                                             |
| [downImage](buttongroup-downimage.md)                 | Spécifie ou récupère le nom de l’image représentant l’état inactif du **BUTTONGROUP**.                                                                                                                                |
| [hoverDownImage](buttongroup-hoverdownimage.md)       | Spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le **BUTTONGROUP**. L’état Survol se produit lorsque le bouton est à l’état inactif et que l’utilisateur pointe dessus avec la souris. |
| [hoverImage](buttongroup-hoverimage.md)               | Spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le **BUTTONGROUP**. L’état de survol se produit lorsque le bouton est à l’État haut et que l’utilisateur pointe dessus avec la souris.             |
| [hueShift](buttongroup-hueshift.md)                   | Spécifie ou récupère la valeur de décalage de la teinte des images **BUTTONGROUP** .                                                                                                                                    |
| [image](buttongroup-image.md)                         | Spécifie ou récupère le nom de l’image représentant les boutons d’un **BUTTONGROUP**.                                                                                                                                     |
| [mappingImage](buttongroup-mappingimage.md)           | Spécifie ou récupère le nom de l’image représentant le mappage de bouton du **BUTTONGROUP**.                                                                                                                                |
| [radio](buttongroup-radio.md)                         | Spécifie ou récupère une valeur indiquant si le **BUTTONGROUP** est composé de cases d’option.                                                                                                                             |
| [saturation](buttongroup-saturation.md)               | Spécifie ou récupère la valeur de saturation des images **BUTTONGROUP** .                                                                                                                                                      |
| [showBackground](buttongroup-showbackground.md)       | Spécifie ou récupère une valeur indiquant si le **BUTTONGROUP** affiche uniquement les boutons, ou affiche la bitmap complète spécifiée dans l’attribut **image** .                                                              |
| [Transparente](buttongroup-transparencycolor.md) | Spécifie ou récupère la couleur transparente des images **BUTTONGROUP** .                                                                                                                                                     |



 

L’élément **BUTTONGROUP** prend en charge les méthodes suivantes.



| Méthode                                 | Description                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [Cliquez sur](buttongroup-click.md)         | Appelle le gestionnaire d’événements **OnClick** défini pour le **BUTTONELEMENT** avec l’index spécifié. |
| [getButton](buttongroup-getbutton.md) | Récupère l' **BUTTONELEMENT** avec l’index spécifié.                                       |



 

L’élément **BUTTONGROUP** prend en charge les attributs ambiants et peut implémenter les gestionnaires d’événements ambiants. Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md) et [gestionnaires d’événements ambiants](ambient-event-handlers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




