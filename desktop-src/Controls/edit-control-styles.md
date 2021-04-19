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
# <a name="edit-control-styles"></a><span data-ttu-id="2b28e-103">Modifier les styles de contrôle</span><span class="sxs-lookup"><span data-stu-id="2b28e-103">Edit Control Styles</span></span>

<span data-ttu-id="2b28e-104">Pour créer un contrôle d’édition à l’aide de la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , spécifiez la classe d’édition, les constantes de style de fenêtre appropriées et une combinaison des styles de contrôle d’édition suivants.</span><span class="sxs-lookup"><span data-stu-id="2b28e-104">To create an edit control using the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specify the EDIT class, appropriate window style constants, and a combination of the following edit control styles.</span></span> <span data-ttu-id="2b28e-105">Une fois le contrôle créé, ces styles ne peuvent pas être modifiés, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="2b28e-105">After the control has been created, these styles cannot be modified, except as noted.</span></span>

## <a name="example"></a><span data-ttu-id="2b28e-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="2b28e-106">Example</span></span>

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

<span data-ttu-id="2b28e-107">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="2b28e-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="2b28e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="2b28e-108">Constants</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2b28e-109">Constante</span><span class="sxs-lookup"><span data-stu-id="2b28e-109">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2b28e-110">Description</span><span class="sxs-lookup"><span data-stu-id="2b28e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <span data-ttu-id="2b28e-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-112">Fait défiler automatiquement le texte vers la droite de 10 caractères lorsque l’utilisateur tape un caractère à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="2b28e-112">Automatically scrolls text to the right by 10 characters when the user types a character at the end of the line.</span></span> <span data-ttu-id="2b28e-113">Quand l’utilisateur appuie sur la touche entrée, le contrôle fait défiler tout le texte jusqu’à la position zéro.</span><span class="sxs-lookup"><span data-stu-id="2b28e-113">When the user presses the ENTER key, the control scrolls all text back to position zero.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <span data-ttu-id="2b28e-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-115">Fait défiler automatiquement le texte d’une page vers le haut lorsque l’utilisateur appuie sur la touche entrée sur la dernière ligne.</span><span class="sxs-lookup"><span data-stu-id="2b28e-115">Automatically scrolls text up one page when the user presses the ENTER key on the last line.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <span data-ttu-id="2b28e-116"><dt><strong>ES_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-116"><dt><strong>ES_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-117">Centre le texte dans un contrôle d’édition à une seule ligne ou multiligne.</span><span class="sxs-lookup"><span data-stu-id="2b28e-117">Centers text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <span data-ttu-id="2b28e-118"><dt><strong>ES_LEFT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-118"><dt><strong>ES_LEFT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-119">Aligne le texte avec la marge de gauche.</span><span class="sxs-lookup"><span data-stu-id="2b28e-119">Aligns text with the left margin.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <span data-ttu-id="2b28e-120"><dt><strong>ES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-120"><dt><strong>ES_LOWERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-121">Convertit tous les caractères en minuscules au fur et à mesure qu’ils sont tapés dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2b28e-121">Converts all characters to lowercase as they are typed into the edit control.</span></span><br/> <span data-ttu-id="2b28e-122">Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2b28e-122">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <span data-ttu-id="2b28e-123"><dt><strong>ES_MULTILINE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-123"><dt><strong>ES_MULTILINE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-124">Désigne un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="2b28e-124">Designates a multiline edit control.</span></span> <span data-ttu-id="2b28e-125">La valeur par défaut est un contrôle d’édition sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="2b28e-125">The default is single-line edit control.</span></span> <br/> <span data-ttu-id="2b28e-126">Lorsque le contrôle d’édition multiligne se trouve dans une boîte de dialogue, la réponse par défaut à l’appui sur la touche entrée consiste à activer le bouton par défaut.</span><span class="sxs-lookup"><span data-stu-id="2b28e-126">When the multiline edit control is in a dialog box, the default response to pressing the ENTER key is to activate the default button.</span></span> <span data-ttu-id="2b28e-127">Pour utiliser la touche entrée comme retour chariot, utilisez le style <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b28e-127">To use the ENTER key as a carriage return, use the <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> style.</span></span><br/> <span data-ttu-id="2b28e-128">Lorsque le contrôle d’édition multiligne ne figure pas dans une boîte de dialogue et que le style de <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> est spécifié, le contrôle d’édition affiche autant de lignes que possible et fait défiler verticalement quand l’utilisateur appuie sur la touche entrée.</span><span class="sxs-lookup"><span data-stu-id="2b28e-128">When the multiline edit control is not in a dialog box and the <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> style is specified, the edit control shows as many lines as possible and scrolls vertically when the user presses the ENTER key.</span></span> <span data-ttu-id="2b28e-129">Si vous ne spécifiez pas <strong>ES_AUTOVSCROLL</strong>, le contrôle d’édition affiche autant de lignes que possible et émet un bip si l’utilisateur appuie sur la touche entrée quand il n’y a plus de lignes à afficher.</span><span class="sxs-lookup"><span data-stu-id="2b28e-129">If you do not specify <strong>ES_AUTOVSCROLL</strong>, the edit control shows as many lines as possible and beeps if the user presses the ENTER key when no more lines can be displayed.</span></span><br/> <span data-ttu-id="2b28e-130">Si vous spécifiez le style de <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , le contrôle d’édition multiligne défile horizontalement lorsque le signe insertion dépasse le bord droit du contrôle.</span><span class="sxs-lookup"><span data-stu-id="2b28e-130">If you specify the <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> style, the multiline edit control automatically scrolls horizontally when the caret goes past the right edge of the control.</span></span> <span data-ttu-id="2b28e-131">Pour commencer une nouvelle ligne, l’utilisateur doit appuyer sur la touche entrée.</span><span class="sxs-lookup"><span data-stu-id="2b28e-131">To start a new line, the user must press the ENTER key.</span></span> <span data-ttu-id="2b28e-132">Si vous ne spécifiez pas <strong>ES_AUTOHSCROLL</strong>, le contrôle encapsule automatiquement les mots au début de la ligne suivante lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2b28e-132">If you do not specify <strong>ES_AUTOHSCROLL</strong>, the control automatically wraps words to the beginning of the next line when necessary.</span></span> <span data-ttu-id="2b28e-133">Une nouvelle ligne est également démarrée si l’utilisateur appuie sur la touche entrée.</span><span class="sxs-lookup"><span data-stu-id="2b28e-133">A new line is also started if the user presses the ENTER key.</span></span> <span data-ttu-id="2b28e-134">La taille de la fenêtre détermine la position du WordWrap.</span><span class="sxs-lookup"><span data-stu-id="2b28e-134">The window size determines the position of the Wordwrap.</span></span> <span data-ttu-id="2b28e-135">Si la taille de la fenêtre change, la position Wordwrapping change et le texte est réaffiché.</span><span class="sxs-lookup"><span data-stu-id="2b28e-135">If the window size changes, the Wordwrapping position changes and the text is redisplayed.</span></span><br/> <span data-ttu-id="2b28e-136">Les contrôles d’édition multiligne peuvent avoir des barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="2b28e-136">Multiline edit controls can have scroll bars.</span></span> <span data-ttu-id="2b28e-137">Un contrôle d’édition avec des barres de défilement traite ses propres messages de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="2b28e-137">An edit control with scroll bars processes its own scroll bar messages.</span></span> <span data-ttu-id="2b28e-138">Notez que les contrôles d’édition sans barres de défilement défilent comme décrit dans les paragraphes précédents et traitent les messages de défilement envoyés par la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="2b28e-138">Note that edit controls without scroll bars scroll as described in the previous paragraphs and process any scroll messages sent by the parent window.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <span data-ttu-id="2b28e-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-140">Inverse le comportement par défaut d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2b28e-140">Negates the default behavior for an edit control.</span></span> <span data-ttu-id="2b28e-141">Le comportement par défaut masque la sélection lorsque le contrôle perd le focus d’entrée et inverse la sélection lorsque le contrôle reçoit le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2b28e-141">The default behavior hides the selection when the control loses the input focus and inverts the selection when the control receives the input focus.</span></span> <span data-ttu-id="2b28e-142">Si vous spécifiez <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, le texte sélectionné est inversé, même si le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="2b28e-142">If you specify <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, the selected text is inverted, even if the control does not have the focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <span data-ttu-id="2b28e-143"><dt><strong>ES_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-143"><dt><strong>ES_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-144">Autorise l’entrée de chiffres dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2b28e-144">Allows only digits to be entered into the edit control.</span></span> <span data-ttu-id="2b28e-145">Notez que, même avec cet ensemble, il est toujours possible de coller des non-chiffres dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2b28e-145">Note that, even with this set, it is still possible to paste non-digits into the edit control.</span></span> <br/> <span data-ttu-id="2b28e-146">Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2b28e-146">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/> <span data-ttu-id="2b28e-147">Pour traduire le texte entré dans le contrôle d’édition en une valeur entière, utilisez la fonction <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b28e-147">To translate text that was entered into the edit control to an integer value, use the <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> function.</span></span> <span data-ttu-id="2b28e-148">Pour définir le texte du contrôle d’édition sur la représentation sous forme de chaîne d’un entier spécifié, utilisez la fonction <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b28e-148">To set the text of the edit control to the string representation of a specified integer, use the <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <span data-ttu-id="2b28e-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-150">Convertit le texte entré dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2b28e-150">Converts text entered in the edit control.</span></span> <span data-ttu-id="2b28e-151">Le texte est converti du jeu de caractères Windows en jeu de caractères OEM, puis renvoyé au jeu de caractères Windows.</span><span class="sxs-lookup"><span data-stu-id="2b28e-151">The text is converted from the Windows character set to the OEM character set and then back to the Windows character set.</span></span> <span data-ttu-id="2b28e-152">Cela garantit une conversion de caractères correcte lorsque l’application appelle la fonction <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> pour convertir une chaîne Windows du contrôle d’édition en caractères OEM.</span><span class="sxs-lookup"><span data-stu-id="2b28e-152">This ensures proper character conversion when the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> function to convert a Windows string in the edit control to OEM characters.</span></span> <span data-ttu-id="2b28e-153">Ce style est particulièrement utile pour les contrôles d’édition qui contiennent des noms de fichiers qui seront utilisés sur des systèmes de fichiers qui ne prennent pas en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="2b28e-153">This style is most useful for edit controls that contain file names that will be used on file systems that do not support Unicode.</span></span> <br/> <span data-ttu-id="2b28e-154">Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2b28e-154">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <span data-ttu-id="2b28e-155"><dt><strong>ES_PASSWORD</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-155"><dt><strong>ES_PASSWORD</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-156">Affiche un astérisque (\*) pour chaque caractère tapé dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2b28e-156">Displays an asterisk (\*) for each character typed into the edit control.</span></span> <span data-ttu-id="2b28e-157">Ce style est valide uniquement pour les contrôles d’édition sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="2b28e-157">This style is valid only for single-line edit controls.</span></span> <br/> <span data-ttu-id="2b28e-158">Pour modifier les caractères affichés, ou bien définir ou désélectionner ce style, utilisez le message <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b28e-158">To change the characters that is displayed, or set or clear this style, use the <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> message.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2b28e-159">Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste.</span><span class="sxs-lookup"><span data-stu-id="2b28e-159">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="2b28e-160">Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.</span><span class="sxs-lookup"><span data-stu-id="2b28e-160">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <span data-ttu-id="2b28e-161"><dt><strong>ES_READONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-161"><dt><strong>ES_READONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-162">Empêche l’utilisateur de taper ou de modifier du texte dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2b28e-162">Prevents the user from typing or editing text in the edit control.</span></span><br/> <span data-ttu-id="2b28e-163">Pour modifier ce style une fois que le contrôle a été créé, utilisez le message <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b28e-163">To change this style after the control has been created, use the <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> message.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <span data-ttu-id="2b28e-164"><dt><strong>ES_RIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-164"><dt><strong>ES_RIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-165">Aligne à droite le texte dans un contrôle d’édition sur une seule ligne ou multiligne.</span><span class="sxs-lookup"><span data-stu-id="2b28e-165">Right-aligns text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <span data-ttu-id="2b28e-166"><dt><strong>ES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-166"><dt><strong>ES_UPPERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-167">Convertit tous les caractères en majuscules au fur et à mesure qu’ils sont tapés dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2b28e-167">Converts all characters to uppercase as they are typed into the edit control.</span></span> <br/> <span data-ttu-id="2b28e-168">Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2b28e-168">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <span data-ttu-id="2b28e-169"><dt><strong>ES_WANTRETURN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2b28e-169"><dt><strong>ES_WANTRETURN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2b28e-170">Spécifie qu’un retour chariot est inséré lorsque l’utilisateur appuie sur la touche entrée tout en entrant du texte dans un contrôle d’édition multiligne dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2b28e-170">Specifies that a carriage return be inserted when the user presses the ENTER key while entering text into a multiline edit control in a dialog box.</span></span> <span data-ttu-id="2b28e-171">Si vous ne spécifiez pas ce style, le fait d’appuyer sur la touche entrée a le même effet que si vous appuyiez sur le bouton de commande par défaut de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2b28e-171">If you do not specify this style, pressing the ENTER key has the same effect as pressing the dialog box's default push button.</span></span> <span data-ttu-id="2b28e-172">Ce style n’a aucun effet sur un contrôle d’édition sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="2b28e-172">This style has no effect on a single-line edit control.</span></span> <br/> <span data-ttu-id="2b28e-173">Pour modifier ce style après avoir créé le contrôle, utilisez <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2b28e-173">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="2b28e-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b28e-174">Requirements</span></span>



| <span data-ttu-id="2b28e-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b28e-175">Requirement</span></span> | <span data-ttu-id="2b28e-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b28e-176">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b28e-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b28e-177">Header</span></span><br/> | <dl> <span data-ttu-id="2b28e-178"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b28e-178"><dt>Winuser.h</dt></span></span> </dl> |



