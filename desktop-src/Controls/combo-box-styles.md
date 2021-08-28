---
title: Styles de zone de liste déroulante (CommCtrl. h)
description: Pour créer une zone de liste déroulante à l’aide de la fonction CreateWindow ou CreateWindowEx, spécifiez la classe de liste déroulante, les constantes de style de fenêtre appropriées et une combinaison des styles de zone de liste déroulante suivants.
ms.assetid: 4dc347b2-7da7-4aa0-b61f-781acf652d84
topic_type:
- apiref
api_name:
- CBS_AUTOHSCROLL
- CBS_DISABLENOSCROLL
- CBS_DROPDOWN
- CBS_DROPDOWNLIST
- CBS_HASSTRINGS
- CBS_LOWERCASE
- CBS_NOINTEGRALHEIGHT
- CBS_OEMCONVERT
- CBS_OWNERDRAWFIXED
- CBS_OWNERDRAWVARIABLE
- CBS_SIMPLE
- CBS_SORT
- CBS_UPPERCASE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652a6392cf8ce50f01efa215e8d6472d1fd1ff344b35fb36d72f0e5dc3c48c68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968499"
---
# <a name="combo-box-styles"></a>Styles de zone de liste déroulante

Pour créer une zone de liste déroulante à l’aide de la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , spécifiez la classe de liste déroulante, les constantes de style de fenêtre appropriées et une combinaison des styles de zone de liste déroulante suivants.



| Constante                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBS_AUTOHSCROLL"></span><span id="cbs_autohscroll"></span><dl> <dt>**\_AUTOHSCROLL SCC**</dt> </dl>                   | Fait défiler automatiquement le texte d’un contrôle d’édition vers la droite lorsque l’utilisateur tape un caractère à la fin de la ligne. Si ce style n’est pas défini, seul le texte qui rentre dans la limite rectangulaire est autorisé.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CBS_DISABLENOSCROLL"></span><span id="cbs_disablenoscroll"></span><dl> <dt>**\_DISABLENOSCROLL SCC**</dt> </dl>       | Affiche une barre de défilement verticale désactivée dans la zone de liste lorsque la zone ne contient pas assez d’éléments pour faire défiler. Sans ce style, la barre de défilement est masquée lorsque la zone de liste ne contient pas assez d'éléments.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="CBS_DROPDOWN"></span><span id="cbs_dropdown"></span><dl> <dt>**\_liste déroulante CBS**</dt> </dl>                            | Semblable à CBS \_ simple, sauf que la zone de liste n’est pas affichée, sauf si l’utilisateur sélectionne une icône en regard du contrôle d’édition.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_DROPDOWNLIST"></span><span id="cbs_dropdownlist"></span><dl> <dt>**\_DropDownList SCC**</dt> </dl>                | Semblable à \_ la liste déroulante CBS, à ceci près que le contrôle d’édition est remplacé par un élément de texte statique qui affiche la sélection actuelle dans la zone de liste.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CBS_HASSTRINGS"></span><span id="cbs_hasstrings"></span><dl> <dt>**\_HASSTRINGS SCC**</dt> </dl>                      | Spécifie qu’une zone de liste déroulante owner-drawn contient des éléments composés de chaînes. La zone de liste déroulante conserve la mémoire et l’adresse des chaînes afin que l’application puisse utiliser le message [**CB \_ GETLBTEXT**](cb-getlbtext.md) pour récupérer le texte d’un élément particulier.<br/> Pour les problèmes d’accessibilité, consultez [exposition de Owner-Drawn éléments de zone de liste déroulante](/windows/desktop/WinAuto/exposing-owner-drawn-combo-box-items)<br/>                                                                                               |
| <span id="CBS_LOWERCASE"></span><span id="cbs_lowercase"></span><dl> <dt>**\_minuscules CBS**</dt> </dl>                         | Convertit en minuscules tout le texte dans le champ de sélection et la liste. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CBS_NOINTEGRALHEIGHT"></span><span id="cbs_nointegralheight"></span><dl> <dt>**\_NOINTEGRALHEIGHT SCC**</dt> </dl>    | Spécifie que la taille de la zone de liste déroulante correspond exactement à la taille spécifiée par l’application lors de la création de la zone de liste déroulante. Normalement, le système redimensionne une zone de liste modifiable pour qu’elle n’affiche pas d’éléments partiels.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="CBS_OEMCONVERT"></span><span id="cbs_oemconvert"></span><dl> <dt>**\_OEMCONVERT SCC**</dt> </dl>                      | convertit le texte entré dans le contrôle d’édition de la zone de liste déroulante du jeu de caractères Windows en jeu de caractères OEM, puis revient au jeu de caractères Windows. cela garantit une conversion de caractères correcte lorsque l’application appelle la fonction [**CharToOem**](/windows/desktop/api/winuser/nf-winuser-chartooema) pour convertir une chaîne Windows dans la zone de liste déroulante en caractères OEM. Ce style est particulièrement utile pour les zones de liste déroulante qui contiennent des noms de fichiers et s’applique uniquement aux zones de liste modifiable créées avec le \_ \_ style de liste déroulante simple ou CBS SCC.<br/> |
| <span id="CBS_OWNERDRAWFIXED"></span><span id="cbs_ownerdrawfixed"></span><dl> <dt>**\_OWNERDRAWFIXED SCC**</dt> </dl>          | Spécifie que le propriétaire de la zone de liste est chargé de dessiner son contenu et que les éléments de la zone de liste sont tous de la même hauteur. La fenêtre propriétaire reçoit un message [**WM \_ MEASUREITEM**](wm-measureitem.md) lorsque la zone de liste déroulante est créée et un message [**WM \_ DRAWITEM**](wm-drawitem.md) lorsqu’un aspect visuel de la zone de liste déroulante a changé.<br/>                                                                                                                                     |
| <span id="CBS_OWNERDRAWVARIABLE"></span><span id="cbs_ownerdrawvariable"></span><dl> <dt>**\_OWNERDRAWVARIABLE SCC**</dt> </dl> | Spécifie que le propriétaire de la zone de liste est chargé de dessiner son contenu et que les éléments de la zone de liste sont des variables de la hauteur. La fenêtre propriétaire reçoit un message [**WM \_ MEASUREITEM**](wm-measureitem.md) pour chaque élément de la zone de liste déroulante lorsque vous créez la zone de liste déroulante et un message [**WM \_ DRAWITEM**](wm-drawitem.md) lorsqu’un aspect visuel de la zone de liste déroulante a changé.<br/>                                                                                                       |
| <span id="CBS_SIMPLE"></span><span id="cbs_simple"></span><dl> <dt>**CBS \_ simple**</dt> </dl>                                  | Affiche la zone de liste à tout moment. La sélection actuelle dans la zone de liste s’affiche dans le contrôle d’édition.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_SORT"></span><span id="cbs_sort"></span><dl> <dt>**\_Tri SCC**</dt> </dl>                                        | Trie automatiquement les chaînes ajoutées à la zone de liste.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="CBS_UPPERCASE"></span><span id="cbs_uppercase"></span><dl> <dt>**\_majuscules CBS**</dt> </dl>                         | Convertit en majuscules tout le texte dans le champ de sélection et la liste.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

