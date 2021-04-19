---
title: Modifier les styles de contrôle (winuser. h)
description: Pour créer un contrôle d’édition à l’aide de la fonction CreateWindow ou CreateWindowEx, spécifiez la classe d’édition, les constantes de style de fenêtre appropriées et une combinaison des styles de contrôle d’édition suivants.
ms.assetid: 336c69b7-bc23-4b93-8968-ad63a1703385
topic_type:
- apiref
api_name:
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_LOWERCASE
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_OEMCONVERT
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_UPPERCASE
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 9b255aee665c32f9a14be4946dee0122dad626bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523578"
---
# <a name="edit-control-styles"></a>Modifier les styles de contrôle

Pour créer un contrôle d’édition à l’aide de la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , spécifiez la classe d’édition, les constantes de style de fenêtre appropriées et une combinaison des styles de contrôle d’édition suivants. Une fois le contrôle créé, ces styles ne peuvent pas être modifiés, sauf indication contraire.

## <a name="example"></a>Exemple

```cpp
LRESULT MsgCreate(HWND hwnd, UINT uMessage, WPARAM wparam, LPARAM lparam)
{
    lparam;
    wparam;
    uMessage;

    // Create Edit control for typing to be sent to server
    if (NULL == (hOutWnd = CreateWindow("EDIT",
                           NULL,
                           WS_BORDER | WS_CHILD | WS_VISIBLE | WS_VSCROLL | ES_LEFT | 
                           ES_MULTILINE | ES_AUTOVSCROLL,
                           0,0,0,0,
                           hwnd,
                           (HMENU) ID_OUTBOX,
                           (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE),
                           NULL)))
        return FALSE;
    return TRUE;
}
```

Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) sur GitHub.

## <a name="constants"></a>Constantes

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt><strong>ES_AUTOHSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Fait défiler automatiquement le texte vers la droite de 10 caractères lorsque l’utilisateur tape un caractère à la fin de la ligne. Quand l’utilisateur appuie sur la touche entrée, le contrôle fait défiler tout le texte jusqu’à la position zéro.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt><strong>ES_AUTOVSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Fait défiler automatiquement le texte d’une page vers le haut lorsque l’utilisateur appuie sur la touche entrée sur la dernière ligne.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt><strong>ES_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Centre le texte dans un contrôle d’édition à une seule ligne ou multiligne.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt><strong>ES_LEFT</strong></dt> </dl></td>
<td style="text-align: left;">Aligne le texte avec la marge de gauche.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <dt><strong>ES_LOWERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Convertit tous les caractères en minuscules au fur et à mesure qu’ils sont tapés dans le contrôle d’édition.<br/> Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt><strong>ES_MULTILINE</strong></dt> </dl></td>
<td style="text-align: left;">Désigne un contrôle d’édition multiligne. La valeur par défaut est un contrôle d’édition sur une seule ligne. <br/> Lorsque le contrôle d’édition multiligne se trouve dans une boîte de dialogue, la réponse par défaut à l’appui sur la touche entrée consiste à activer le bouton par défaut. Pour utiliser la touche entrée comme retour chariot, utilisez le style <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .<br/> Lorsque le contrôle d’édition multiligne ne figure pas dans une boîte de dialogue et que le style de <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> est spécifié, le contrôle d’édition affiche autant de lignes que possible et fait défiler verticalement quand l’utilisateur appuie sur la touche entrée. Si vous ne spécifiez pas <strong>ES_AUTOVSCROLL</strong>, le contrôle d’édition affiche autant de lignes que possible et émet un bip si l’utilisateur appuie sur la touche entrée quand il n’y a plus de lignes à afficher.<br/> Si vous spécifiez le style de <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , le contrôle d’édition multiligne défile horizontalement lorsque le signe insertion dépasse le bord droit du contrôle. Pour commencer une nouvelle ligne, l’utilisateur doit appuyer sur la touche entrée. Si vous ne spécifiez pas <strong>ES_AUTOHSCROLL</strong>, le contrôle encapsule automatiquement les mots au début de la ligne suivante lorsque cela est nécessaire. Une nouvelle ligne est également démarrée si l’utilisateur appuie sur la touche entrée. La taille de la fenêtre détermine la position du WordWrap. Si la taille de la fenêtre change, la position Wordwrapping change et le texte est réaffiché.<br/> Les contrôles d’édition multiligne peuvent avoir des barres de défilement. Un contrôle d’édition avec des barres de défilement traite ses propres messages de barre de défilement. Notez que les contrôles d’édition sans barres de défilement défilent comme décrit dans les paragraphes précédents et traitent les messages de défilement envoyés par la fenêtre parente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt><strong>ES_NOHIDESEL</strong></dt> </dl></td>
<td style="text-align: left;">Inverse le comportement par défaut d’un contrôle d’édition. Le comportement par défaut masque la sélection lorsque le contrôle perd le focus d’entrée et inverse la sélection lorsque le contrôle reçoit le focus d’entrée. Si vous spécifiez <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, le texte sélectionné est inversé, même si le contrôle n’a pas le focus.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt><strong>ES_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Autorise l’entrée de chiffres dans le contrôle d’édition. Notez que, même avec cet ensemble, il est toujours possible de coller des non-chiffres dans le contrôle d’édition. <br/> Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/> Pour traduire le texte entré dans le contrôle d’édition en une valeur entière, utilisez la fonction <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> . Pour définir le texte du contrôle d’édition sur la représentation sous forme de chaîne d’un entier spécifié, utilisez la fonction <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <dt><strong>ES_OEMCONVERT</strong></dt> </dl></td>
<td style="text-align: left;">Convertit le texte entré dans le contrôle d’édition. Le texte est converti du jeu de caractères Windows en jeu de caractères OEM, puis renvoyé au jeu de caractères Windows. Cela garantit une conversion de caractères correcte lorsque l’application appelle la fonction <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> pour convertir une chaîne Windows du contrôle d’édition en caractères OEM. Ce style est particulièrement utile pour les contrôles d’édition qui contiennent des noms de fichiers qui seront utilisés sur des systèmes de fichiers qui ne prennent pas en charge Unicode. <br/> Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt><strong>ES_PASSWORD</strong></dt> </dl></td>
<td style="text-align: left;">Affiche un astérisque (*) pour chaque caractère tapé dans le contrôle d’édition. Ce style est valide uniquement pour les contrôles d’édition sur une seule ligne. <br/> Pour modifier les caractères affichés, ou bien définir ou désélectionner ce style, utilisez le message <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> . <br/>
<blockquote>
[!Note]<br />
Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste. Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt><strong>ES_READONLY</strong></dt> </dl></td>
<td style="text-align: left;">Empêche l’utilisateur de taper ou de modifier du texte dans le contrôle d’édition.<br/> Pour modifier ce style une fois que le contrôle a été créé, utilisez le message <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> . <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt><strong>ES_RIGHT</strong></dt> </dl></td>
<td style="text-align: left;">Aligne à droite le texte dans un contrôle d’édition sur une seule ligne ou multiligne.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <dt><strong>ES_UPPERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Convertit tous les caractères en majuscules au fur et à mesure qu’ils sont tapés dans le contrôle d’édition. <br/> Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt><strong>ES_WANTRETURN</strong></dt> </dl></td>
<td style="text-align: left;">Spécifie qu’un retour chariot est inséré lorsque l’utilisateur appuie sur la touche entrée tout en entrant du texte dans un contrôle d’édition multiligne dans une boîte de dialogue. Si vous ne spécifiez pas ce style, le fait d’appuyer sur la touche entrée a le même effet que si vous appuyiez sur le bouton de commande par défaut de la boîte de dialogue. Ce style n’a aucun effet sur un contrôle d’édition sur une seule ligne. <br/> Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winuser. h</dt> </dl> |



