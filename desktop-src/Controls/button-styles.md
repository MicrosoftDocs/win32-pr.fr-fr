---
title: Styles de bouton (winuser. h)
description: Spécifie une combinaison de styles de bouton. Si vous créez un bouton à l’aide de la classe BUTTON avec la fonction CreateWindow ou CreateWindowEx, vous pouvez spécifier n’importe quel style de bouton listé ci-dessous.
ms.assetid: 30254cb5-43cd-407f-8ad6-bd7f9ec3edc7
topic_type:
- apiref
api_name:
- BS_3STATE
- BS_AUTO3STATE
- BS_AUTOCHECKBOX
- BS_AUTORADIOBUTTON
- BS_BITMAP
- BS_BOTTOM
- BS_CENTER
- BS_CHECKBOX
- BS_COMMANDLINK
- BS_DEFCOMMANDLINK
- BS_DEFPUSHBUTTON
- BS_DEFSPLITBUTTON
- BS_GROUPBOX
- BS_ICON
- BS_FLAT
- BS_LEFT
- BS_LEFTTEXT
- BS_MULTILINE
- BS_NOTIFY
- BS_OWNERDRAW
- BS_PUSHBUTTON
- BS_PUSHLIKE
- BS_RADIOBUTTON
- BS_RIGHT
- BS_RIGHTBUTTON
- BS_SPLITBUTTON
- BS_TEXT
- BS_TOP
- BS_TYPEMASK
- BS_USERBUTTON
- BS_VCENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 60419d947036516e093d481f3fc0d8caa097671c13bd4fe3fc8e95d21cc3cb83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832479"
---
# <a name="button-styles"></a>Styles des boutons

Spécifie une combinaison de styles de bouton. Si vous créez un bouton à l’aide de la classe BUTTON avec la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , vous pouvez spécifier n’importe quel style de bouton listé ci-dessous.

## <a name="example"></a>Exemple

```cpp
HRESULT Button::CreateText(HWND hParent, const TCHAR *szCaption, int nID, 
                               const Rect& rcBound)
{
    CREATESTRUCT create;
    ZeroMemory(&create, sizeof(CREATESTRUCT));

    create.x = rcBound.left;
    create.y = rcBound.top;
    create.cx = rcBound.right - create.x;
    create.cy = rcBound.bottom - create.y;

    create.hwndParent = hParent;
    create.lpszName = szCaption;
    create.hMenu = (HMENU)(INT_PTR)nID;
    create.lpszClass = TEXT("BUTTON");
    create.style = BS_PUSHBUTTON | BS_FLAT;
    return Control::Create(create);
}
```
exemple de [Windows exemples classiques](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp) sur GitHub.


## <a name="constants"></a>Constantes
| Constante                                                                                                                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**BS \_ 3STATE**</dt> </dl>                            | Crée un bouton qui est le même qu’une case à cocher, à la différence près que la zone peut être grisée et activée ou désactivée. Utilisez l’État grisé pour montrer que l’état de la case à cocher n’est pas déterminé.<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**BS \_ AUTO3STATE**</dt> </dl>                | Crée un bouton qui est identique à une case à cocher à trois États, sauf que la zone modifie son état lorsque l’utilisateur la sélectionne. L’État parcourt les cases cochées, indéterminées et désactivées.<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**\_case d’option BS AUTOcase**</dt> </dl>          | Crée un bouton qui est le même qu’une case à cocher, sauf que l’état d’activation bascule automatiquement entre activé et désactivé chaque fois que l’utilisateur active la case à cocher.<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**RadioButton BS \_**</dt> </dl> | Crée un bouton qui est le même qu’une case d’option, sauf que lorsque l’utilisateur le sélectionne, le système définit automatiquement l’état de vérification du bouton sur coché et définit automatiquement l’état d’activation de tous les autres boutons du même groupe sur effacé.<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**\_bitmap BS**</dt> </dl>                            | Spécifie que le bouton affiche une image bitmap. Consultez la section Notes pour son interaction avec l' \_ icône BS.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**BS \_ bas**</dt> </dl>                            | Place le texte en bas du rectangle du bouton.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**\_Centre BS**</dt> </dl>                            | Centre le texte horizontalement dans le rectangle du bouton.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**\_case à cocher BS**</dt> </dl>                      | Crée une petite case à cocher vide avec du texte. Par défaut, le texte est affiché à droite de la case à cocher. Pour afficher le texte à gauche de la case à cocher, combinez cet indicateur avec le \_ style BS LEFTTEXT (ou avec le \_ style BS RIGHTBUTTON équivalent).<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**BS \_ COMMANDLINK**</dt> </dl>             | Crée un bouton de lien de commande qui se comporte comme un \_ bouton de style BS PUSHBUTTON, mais le bouton de liaison de commande a une flèche verte sur la gauche qui pointe sur le texte du bouton. Vous pouvez définir une légende pour le texte du bouton en envoyant le \_ message SETNOTE BCM au bouton.<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**BS \_ DEFCOMMANDLINK**</dt> </dl>    | Crée un bouton de lien de commande qui se comporte comme un \_ bouton de style BS PushButton. Si le bouton se trouve dans une boîte de dialogue, l’utilisateur peut sélectionner le bouton de lien de commande en appuyant sur la touche entrée, même si le bouton de lien de commande n’a pas le focus d’entrée. Ce style est utile pour permettre à l’utilisateur de sélectionner rapidement l’option la plus probable (par défaut).<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**BS \_ DEFPUSHBUTTON**</dt> </dl>       | Crée un bouton de commande qui se comporte comme un \_ bouton de style BS PUSHBUTTON, mais présente une apparence distincte. Si le bouton se trouve dans une boîte de dialogue, l’utilisateur peut sélectionner le bouton en appuyant sur la touche entrée, même si le bouton n’a pas le focus d’entrée. Ce style est utile pour permettre à l’utilisateur de sélectionner rapidement l’option la plus probable (par défaut).<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**BS \_ DEFSPLITBUTTON**</dt> </dl>    | Crée un bouton partagé qui se comporte comme un bouton de \_ style BS PUSHBUTTON, mais a également une apparence distinctive. Si le bouton partagé se trouve dans une boîte de dialogue, l’utilisateur peut sélectionner le bouton partagé en appuyant sur la touche entrée, même lorsque le bouton partagé n’a pas le focus d’entrée. Ce style est utile pour permettre à l’utilisateur de sélectionner rapidement l’option la plus probable (par défaut).<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**zone de \_ zone BS**</dt> </dl>                      | Crée un rectangle dans lequel d’autres contrôles peuvent être regroupés. Tout texte associé à ce style est affiché dans le coin supérieur gauche du rectangle.<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**\_icône BS**</dt> </dl>                                  | Spécifie que le bouton affiche une icône. Consultez la section Notes pour son interaction avec la \_ bitmap BS.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**BS \_ bémol**</dt> </dl>                                  | Spécifie que le bouton est à deux dimensions ; elle n’utilise pas l’ombrage par défaut pour créer une image 3D. <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**BS \_ gauche**</dt> </dl>                                  | Aligne à gauche le texte dans le rectangle du bouton. Toutefois, si le bouton est une case à cocher ou une case d’option qui n’a pas le \_ style BS RIGHTBUTTON, le texte est justifié à gauche du côté droit de la case à cocher ou de la case d’option.<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**BS \_ LEFTTEXT**</dt> </dl>                      | Place le texte sur le côté gauche de la case d’option ou de la case à cocher lorsqu’il est combiné avec un style de case d’option ou de case à cocher. Identique au style BS \_ RIGHTBUTTON.<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**BS \_ multiligne**</dt> </dl>                   | Encapsule le texte du bouton sur plusieurs lignes si la chaîne de texte est trop longue pour tenir sur une seule ligne dans le rectangle de bouton.<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**BS- \_ notifier**</dt> </dl>                            | Permet à un bouton d’envoyer des codes de notification de la [ \_ KILLFOCUS](bn-killfocus.md) [et de la \_ ](bn-setfocus.md) valeur de la plage de la fenêtre parente. <br/> Notez que les boutons envoient le code de notification sur lequel l' [ \_ utilisateur a cliqué](bn-clicked.md) , qu’il ait ce style ou non. Pour obtenir les codes de notification [ \_ DBLCLK](bn-dblclk.md) de la valeur de la ligne, le bouton doit avoir le \_ style de RadioButton BS ou BS \_ OwnerDraw.<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**BS \_ OwnerDraw**</dt> </dl>                   | Crée un bouton owner-drawn. La fenêtre propriétaire reçoit un message [**WM \_ DRAWITEM**](wm-drawitem.md) lorsqu’un aspect visuel du bouton a changé. Ne combinez pas le \_ style BS OwnerDraw avec d’autres styles de bouton.<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**BS- \_ poussoir**</dt> </dl>                | Crée un bouton de commande qui publie un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) dans la fenêtre propriétaire lorsque l’utilisateur sélectionne le bouton.<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**BS \_ PUSHLIKE**</dt> </dl>                      | Rend un bouton (tel qu’une case à cocher, une case à cocher à trois États ou une case d’option) se présente et agit comme un bouton de commande. Le bouton est levé lorsqu’il n’est pas poussé ou coché, et en 3D enfoncé lorsqu’il est poussé ou activé.<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**RadioButton BS \_**</dt> </dl>             | Crée un petit cercle avec du texte. Par défaut, le texte est affiché à droite du cercle. Pour afficher le texte à gauche du cercle, combinez cet indicateur avec le style BS \_ LEFTTEXT (ou avec le \_ style BS RIGHTBUTTON équivalent). Utilisez les cases d’option pour les groupes de choix associés mutuellement exclusifs.<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**BS \_ droit**</dt> </dl>                               | Aligne le texte à droite dans le rectangle du bouton. Toutefois, si le bouton est une case à cocher ou une case d’option qui n’a pas le \_ style BS RIGHTBUTTON, le texte est justifié à droite sur le côté droit de la case à cocher ou de la case d’option.<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**BS \_ RIGHTBUTTON**</dt> </dl>             | Positionne le cercle d’un bouton radio ou le carré d’une case à cocher sur le côté droit du rectangle du bouton. Identique au style BS \_ LEFTTEXT.<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**BS \_**</dt> </dl>             | Crée un bouton partagé. Un bouton partagé a une flèche déroulante.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**texte de BS \_**</dt> </dl>                                  | Spécifie que le bouton affiche du texte.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**BS \_ haut**</dt> </dl>                                     | Place le texte en haut du rectangle du bouton.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**BS \_ TYPEMASK**</dt> </dl>                      | N’utilisez pas ce style. Un bit de style composite qui résulte de l’utilisation de l’opérateur OR sur les \_ \* bits de type BS. Il peut être utilisé pour masquer les bits BS valides \_ \* à partir d’un masque de bits donné. Notez que ce n’est pas à jour et qu’il n’inclut pas correctement tous les styles valides. Par conséquent, vous ne devez pas utiliser ce style.<br/>                                                                                               |
| <span id="BS_USERBUTTON"></span><span id="bs_userbutton"></span><dl> <dt>**BS \_ UserButton**</dt> </dl>                | Obsolète, mais fourni à des fins de compatibilité avec les versions 16 bits de Windows. Les applications doivent utiliser BS OwnerDraw à la \_ place.<br/>                                                                                                                                                                                                                                                                        |
| <span id="BS_VCENTER"></span><span id="bs_vcenter"></span><dl> <dt>**BS \_ VCENTER**</dt> </dl>                         | Place le texte au milieu (verticalement) du rectangle du bouton.<br/>                                                                                                                                                                                                                                                                                                                                 |



## <a name="remarks"></a>Remarques

Pour obtenir des illustrations des styles de bouton principal, tels que la \_ case à cocher BS et la zone de zone \_ , consultez [types de boutons](button-types-and-styles.md).

L’apparence d’un texte ou d’une icône ou les deux sur un contrôle Button dépend de l' \_ icône BS et des \_ styles bitmap BS, et de l’envoi ou non du message [**\_ SETIMAGE BM**](bm-setimage.md) . Les résultats possibles sont les suivants.



| \_Icône BS ou \_ ensemble de bitmaps BS ? | BM \_ SETIMAGE appelé ? | Résultat              |
|-----------------------------|----------------------|---------------------|
| Oui                         | Oui                  | Afficher l’icône uniquement.     |
| Non                          | Oui                  | Affichez l’icône et le texte. |
| Oui                         | Non                   | Afficher uniquement le texte.     |
| Non                          | Non                   | Afficher le texte uniquement      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

