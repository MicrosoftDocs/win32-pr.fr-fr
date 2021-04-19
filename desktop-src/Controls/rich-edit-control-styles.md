---
title: Styles de contrôle RichEdit (winuser. h)
description: Les styles de fenêtre suivants sont uniques aux contrôles RichEdit.
ms.assetid: 0f1b3e01-01cb-4b3e-b959-6f32498f0394
topic_type:
- apiref
api_name:
- ES_DISABLENOSCROLL
- ES_EX_NOCALLOLEINIT
- ES_NOIME
- ES_NOOLEDRAGDROP
- ES_SAVESEL
- ES_SELECTIONBAR
- ES_SELFIME
- ES_SUNKEN
- ES_VERTICAL
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620f73beb726eea065d8c8a63a635ff04fdeba37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520918"
---
# <a name="rich-edit-control-styles"></a>Styles de contrôle RichEdit

Les styles de fenêtre suivants sont uniques aux contrôles RichEdit.



| Constante                                                                                                                                                                         | Description                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_DISABLENOSCROLL"></span><span id="es_disablenoscroll"></span><dl> <dt>**\_DISABLENOSCROLL es**</dt> </dl>     | Désactive les barres de défilement au lieu de les masquer lorsqu’elles ne sont pas nécessaires.<br/>                                                                                                                                                                    |
| <span id="ES_EX_NOCALLOLEINIT"></span><span id="es_ex_nocalloleinit"></span><dl> <dt>**ES \_ ex \_ NOCALLOLEINIT**</dt> </dl> | Empêche le contrôle d’appeler la fonction [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) lors de sa création. Ce style de fenêtre est utile uniquement dans les modèles de boîte de dialogue, car [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) n’accepte pas ce style.<br/> |
| <span id="ES_NOIME_"></span><span id="es_noime_"></span><dl> <dt>**Es \_ NOIME**</dt> </dl>                                | Désactive l’opération IME. Ce style est disponible uniquement pour la prise en charge des langues asiatiques.<br/>                                                                                                                                                     |
| <span id="ES_NOOLEDRAGDROP"></span><span id="es_nooledragdrop"></span><dl> <dt>**\_NOOLEDRAGDROP es**</dt> </dl>           | Désactive la prise en charge du glisser-déplacer des objets OLE.<br/>                                                                                                                                                                                           |
| <span id="ES_SAVESEL"></span><span id="es_savesel"></span><dl> <dt>**\_SAVESEL es**</dt> </dl>                             | Conserve la sélection lorsque le contrôle perd le focus. Par défaut, l’ensemble du contenu du contrôle est sélectionné lorsqu’il obtient le focus.<br/>                                                                                         |
| <span id="ES_SELECTIONBAR"></span><span id="es_selectionbar"></span><dl> <dt>**\_SELECTIONBAR es**</dt> </dl>              | Ajoute de l’espace à la marge de gauche où le curseur se transforme en flèche vers le haut, ce qui permet à l’utilisateur de sélectionner des lignes de texte complètes. <br/>                                                                                                             |
| <span id="ES_SELFIME_"></span><span id="es_selfime_"></span><dl> <dt>**Es \_ SELFIME**</dt> </dl>                          | Dirige le contrôle Rich Edit pour permettre à l’application de gérer toutes les opérations IME. Ce style est disponible uniquement pour la prise en charge des langues asiatiques.<br/>                                                                                            |
| <span id="ES_SUNKEN"></span><span id="es_sunken"></span><dl> <dt>**ES en \_ 3D enfoncé**</dt> </dl>                                | Affiche le contrôle avec un style de bordure enfoncée afin que le contrôle Rich Edit apparaisse en retrait dans sa fenêtre parente. <br/>                                                                                                                  |
| <span id="ES_VERTICAL"></span><span id="es_vertical"></span><dl> <dt>**ES \_ verticales**</dt> </dl>                          | Dessine du texte et des objets dans le sens vertical. Ce style est disponible uniquement pour la prise en charge des langues asiatiques.<br/>                                                                                                                                 |



Les contrôles RichEdit prennent également en charge les styles de contrôle d’édition suivants.



| Constante                                                                                                                                                         | Description                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt>**\_AUTOHSCROLL es**</dt> </dl> | Fait défiler automatiquement le texte vers la droite de 10 caractères lorsque l’utilisateur tape un caractère à la fin de la ligne. Quand l’utilisateur appuie sur la touche entrée, le contrôle fait défiler tout le texte jusqu’à la position zéro.<br/>                                                                                                                                                    |
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt>**\_AUTOVSCROLL es**</dt> </dl> | Fait défiler automatiquement le texte d’une page vers le haut lorsque l’utilisateur appuie sur la touche entrée sur la dernière ligne.<br/>                                                                                                                                                                                                                                                                 |
| <span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt>**Centre des ES \_**</dt> </dl>                | Centre le texte dans un contrôle d’édition à une seule ligne ou multiligne.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt>**ES à \_ gauche**</dt> </dl>                      | Aligne à gauche le texte.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt>**ES \_ multiligne**</dt> </dl>       | Désigne un contrôle d’édition multiligne. La valeur par défaut est un contrôle d’édition sur une seule ligne.<br/>                                                                                                                                                                                                                                                                                |
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt>**\_NOHIDESEL es**</dt> </dl>       | Inverse le comportement par défaut d’un contrôle d’édition. Le comportement par défaut masque la sélection lorsque le contrôle perd le focus d’entrée et inverse la sélection lorsque le contrôle reçoit le focus d’entrée. Si vous spécifiez [**es \_ NOHIDESEL**](edit-control-styles.md), le texte sélectionné est inversé, même si le contrôle n’a pas le focus.<br/> |
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt>**\_numéro es**</dt> </dl>                | Autorise l’entrée de chiffres dans le contrôle d’édition.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt>**\_mot de passe es**</dt> </dl>          | Affiche un astérisque ( \* ) pour chaque caractère tapé dans le contrôle d’édition. Ce style est valide uniquement pour les contrôles d’édition sur une seule ligne.<br/>                                                                                                                                                                                                                            |
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt>**ES \_ ReadOnly**</dt> </dl>          | Empêche l’utilisateur de taper ou de modifier du texte dans le contrôle d’édition.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt>**ES à \_ droite**</dt> </dl>                   | Right aligne le texte sur un contrôle d’édition sur une seule ligne ou multiligne.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt>**\_WANTRETURN es**</dt> </dl>    | Spécifie qu’un retour chariot est inséré lorsque l’utilisateur appuie sur la touche entrée tout en entrant du texte dans un contrôle d’édition multiligne dans une boîte de dialogue. Si vous ne spécifiez pas ce style, le fait d’appuyer sur la touche entrée a le même effet que si vous appuyiez sur le bouton de commande par défaut de la boîte de dialogue. Ce style n’a aucun effet sur un contrôle d’édition sur une seule ligne.<br/>                   |



Les contrôles RichEdit ne prennent pas en charge les styles de contrôle d’édition suivants.

-   [**\_minuscules es**](edit-control-styles.md)
-   [**\_OEMCONVERT es**](edit-control-styles.md)
-   [**\_majuscules**](edit-control-styles.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

