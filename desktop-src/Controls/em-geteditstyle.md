---
title: Message EM_GETEDITSTYLE (RichEdit. h)
description: Récupère les indicateurs de style de modification actuels.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- EM_GETEDITSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032975"
---
# <a name="em_geteditstyle-message"></a><span data-ttu-id="be602-104">\_Message em GETEDITSTYLE</span><span class="sxs-lookup"><span data-stu-id="be602-104">EM\_GETEDITSTYLE message</span></span>

<span data-ttu-id="be602-105">Récupère les indicateurs de style de modification actuels.</span><span class="sxs-lookup"><span data-stu-id="be602-105">Retrieves the current edit style flags.</span></span>

## <a name="parameters"></a><span data-ttu-id="be602-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be602-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be602-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be602-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be602-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="be602-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="be602-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be602-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be602-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="be602-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be602-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be602-111">Return value</span></span>

<span data-ttu-id="be602-112">Retourne les indicateurs de style de modification actuels, qui peuvent inclure une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="be602-112">Returns the current edit style flags, which can include one or more of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be602-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="be602-113">Return code</span></span></th>
<th><span data-ttu-id="be602-114">Description</span><span class="sxs-lookup"><span data-stu-id="be602-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-116">La modification complète appellera le bip système si l’utilisateur tente d’entrer plus de caractères que le nombre maximal.</span><span class="sxs-lookup"><span data-stu-id="be602-116">Rich Edit will call the system beeper if the user attempts to enter more than the maximum characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-117"><dt><strong>SES_BIDI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-117"><dt><strong>SES_BIDI</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-118">Active le traitement bidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="be602-118">Turns on bidirectional processing.</span></span> <span data-ttu-id="be602-119">Cela est automatiquement activé par la modification complète si l’un des styles de fenêtre suivants est actif : <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="be602-119">This is automatically turned on by Rich Edit if any of the following window styles are active: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span></span> <span data-ttu-id="be602-120">Toutefois, ce paramètre est utile pour gérer ces styles de fenêtre lors de l’utilisation d’une implémentation personnalisée de <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-120">However, this setting is useful for handling these window styles when using a custom implementation of <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-122"><strong>Windows XP avec SP1</strong>: autorisez l’insertion d’objets incorporés à l’aide de TSF (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-122"><strong>Windows XP with SP1</strong>: Allow embedded objects to be inserted using TSF (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-124"><strong>Windows XP avec SP1</strong>: autorise les conseils de vérification de la protection TSF (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-124"><strong>Windows XP with SP1</strong>: Allows TSF proofing tips (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-126"><strong>Windows XP avec SP1</strong>: autorise les conseils de TSF SmartTag (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-126"><strong>Windows XP with SP1</strong>: Allows TSF SmartTag tips (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-128"><strong>Windows 8</strong>: ne pas autoriser l’accès en lecture/écriture au verrou TSF.</span><span class="sxs-lookup"><span data-stu-id="be602-128"><strong>Windows 8</strong>: Do not allow the TSF lock read/write access.</span></span> <span data-ttu-id="be602-129">Cela suspend l’entrée TSF.</span><span class="sxs-lookup"><span data-stu-id="be602-129">This pauses TSF input.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-131"><strong>Windows 8</strong>: les polices avec une ligature fi sont affichées avec les fonctionnalités OpenType par défaut, ce qui améliore la typographie (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-131"><strong>Windows 8</strong>: Fonts with an fi ligature are displayed with default OpenType features resulting in improved typography (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-133"><strong>Windows XP avec SP1</strong>: utilisez les polices en mode brouillon pour afficher le texte.</span><span class="sxs-lookup"><span data-stu-id="be602-133"><strong>Windows XP with SP1</strong>: Use draft mode fonts to display text.</span></span> <span data-ttu-id="be602-134">Le mode brouillon est une option d’accessibilité dans laquelle le contrôle affiche le texte avec une seule police ; la police est déterminée par le paramètre système de la police utilisée dans les boîtes de message.</span><span class="sxs-lookup"><span data-stu-id="be602-134">Draft mode is an accessibility option where the control displays the text with a single font; the font is determined by the system setting for the font used in message boxes.</span></span> <span data-ttu-id="be602-135">Par exemple, les utilisateurs accessibles peuvent lire du texte plus facilement s’ils sont uniformes, au lieu d’une combinaison de polices et de styles (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-135">For example, accessible users may read text easier if it is uniform, rather than a mix of fonts and styles (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-136"><dt><strong>SES_EMULATE10</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-136"><dt><strong>SES_EMULATE10</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-137"><strong>Windows 8</strong>: émuler le comportement de RichEdit 1,0.</span><span class="sxs-lookup"><span data-stu-id="be602-137"><strong>Windows 8</strong>: Emulate RichEdit 1.0 behavior.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="be602-138">Si vous souhaitez vraiment ce comportement, utilisez le riched32.dll Windows au lieu de riched20.dll ou msftedit.dll.</span><span class="sxs-lookup"><span data-stu-id="be602-138">If you really want this behavior, use the Windows riched32.dll instead of riched20.dll or msftedit.dll.</span></span> <span data-ttu-id="be602-139">Riched32.dll possédait plus de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="be602-139">Riched32.dll had more functionality.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-141">Lorsque ce bit est activé, la modification riche tente d’émuler le contrôle d’édition système (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-141">When this bit is on, rich edit attempts to emulate the system edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-143">Étend la couleur d’arrière-plan jusqu’aux bords du rectangle client (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-143">Extends the background color all the way to the edges of the client rectangle (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-145"><strong>Windows XP avec SP1</strong>: si la largeur du quadrillage du tableau est égale à zéro, le quadrillage ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="be602-145"><strong>Windows XP with SP1</strong>: If the width of table gridlines is zero, gridlines are not displayed.</span></span> <span data-ttu-id="be602-146">Cela équivaut à la fonctionnalité masquer le quadrillage dans le menu Tableau de Word (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-146">This is equivalent to the hide gridlines feature in Word's table menu (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-148"><strong>Windows 8</strong>: lorsque le curseur se trouve sur un lien, affichez une info-bulle avec l’adresse du lien cible (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-148"><strong>Windows 8</strong>: When the cursor is over a link, display a tooltip with the target link address (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-150"><strong>Windows 8</strong>: fournissez des informations de signe insertion logique au lieu d’une image bitmap de signe insertion, comme décrit dans <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost :: TxSetCaretPos</strong></a> (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-150"><strong>Windows 8</strong>: Provide logical caret information instead of a caret bitmap as described in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-151"><dt><strong>SES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-151"><dt><strong>SES_LOWERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-152">Convertit tous les caractères d’entrée en minuscules (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-152">Converts all input characters to lowercase (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-153"><dt><strong>SES_MAPCPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-153"><dt><strong>SES_MAPCPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-154">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="be602-154">Obsolete.</span></span> <span data-ttu-id="be602-155">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="be602-155">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-156"><dt><strong>SES_MULTISELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-156"><dt><strong>SES_MULTISELECT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-157"><strong>Windows 8</strong>: activer la multisélection avec des sélections de souris individuelles effectuées pendant que la touche CTRL est enfoncée (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-157"><strong>Windows 8</strong>: Enable multiselection with individual mouse selections made while the Ctrl key is pressed (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-159"><strong>Windows 8</strong>: ne pas ajuster la hauteur de ligne pour le texte asiatique de l’est (valeur par défaut : 0 qui ajuste la hauteur de ligne de 15%).</span><span class="sxs-lookup"><span data-stu-id="be602-159"><strong>Windows 8</strong>: Do not adjust line height for East Asian text (default: 0 which adjusts the line height by 15%).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-161">Envoie <a href="en-link.md">EN_LINK</a> notification à partir des liens qui n’ont pas le focus.</span><span class="sxs-lookup"><span data-stu-id="be602-161">Sends <a href="en-link.md">EN_LINK</a> notification from links that do not have focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-162"><dt><strong>SES_NOIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-162"><dt><strong>SES_NOIME</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-163">Interdit les IME pour cette instance du contrôle RichEdit (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-163">Disallows IMEs for this instance of the rich edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-165">Lorsque ce bit est activé, Rich Edit ne vérifie pas la séquence de texte tapé.</span><span class="sxs-lookup"><span data-stu-id="be602-165">When this bit is on, rich edit does not verify the sequence of typed text.</span></span> <span data-ttu-id="be602-166">Certains langages (tels que thaï et vietnamien) requièrent la vérification de l’ordre des séquences d’entrée avant leur envoi au magasin de stockage (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-166">Some languages (such as Thai and Vietnamese) require verifying the input sequence order before submitting it to the backing store (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-168">Quand KillFocus se produit, fait défiler jusqu’au début du texte (position de caractère égale à 0) (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-168">When KillFocus occurs, scroll to the beginning of the text (character position equal to 0) (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-170"><strong>Windows 8</strong>: ajouter ou supprimer un espace en fonction du contexte lors de la suppression du texte (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-170"><strong>Windows 8</strong>: Add or delete a space according to the context when dropping text (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-171"><dt><strong>SES_USECRLF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-171"><dt><strong>SES_USECRLF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-172">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="be602-172">Obsolete.</span></span> <span data-ttu-id="be602-173">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="be602-173">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-175"><strong>Windows 8</strong>: si l’option Sélectionner un mot est active, assurez-vous que l’emplacement cible se trouve à la limite d’un mot (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-175"><strong>Windows 8</strong>: If word select is active, ensure that the drop location is at a word boundary (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-176"><dt><strong>SES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-176"><dt><strong>SES_UPPERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-177">Convertit tous les caractères d’entrée en majuscules (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-177">Converts all input characters to uppercase (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-178"><dt><strong>SES_USEAIMM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-178"><dt><strong>SES_USEAIMM</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-179">Utilise le composant de méthode d’entrée IMM actif fourni avec Internet Explorer 4,0 ou une version ultérieure (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="be602-179">Uses the Active IMM input method component that ships with Internet Explorer 4.0 or later (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-180"><dt><strong>SES_USEATFONT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-180"><dt><strong>SES_USEATFONT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-181"><strong>Windows XP avec SP1</strong>: utilise une police @, conçue pour le texte vertical ; utilisé avec le style de fenêtre <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="be602-181"><strong>Windows XP with SP1</strong>: Uses an @ font, which is designed for vertical text; this is used with the <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> window style.</span></span> <span data-ttu-id="be602-182">Le nom d’une @ font commence par le symbole @, par exemple, &quot; @Batang &quot; (valeur par défaut : 0, mais est automatiquement activé pour la disposition du texte vertical).</span><span class="sxs-lookup"><span data-stu-id="be602-182">The name of an @ font begins with the @ symbol, for example, &quot;@Batang&quot; (default: 0, but is automatically turned on for vertical text layout).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="be602-183"><dt><strong>SES_USECTF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-183"><dt><strong>SES_USECTF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-184"><strong>Windows XP avec SP1</strong>: active la prise en charge de TSF.</span><span class="sxs-lookup"><span data-stu-id="be602-184"><strong>Windows XP with SP1</strong>: Turns on TSF support.</span></span> <span data-ttu-id="be602-185">(valeur par défaut : 0)</span><span class="sxs-lookup"><span data-stu-id="be602-185">(default: 0)</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="be602-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="be602-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="be602-187">Active la traduction de CRCRLFs en CRs.</span><span class="sxs-lookup"><span data-stu-id="be602-187">Turns on translation of CRCRLFs to CRs.</span></span> <span data-ttu-id="be602-188">Lorsque ce bit est activé et qu’un fichier est lu, toutes les instances de CRCRLF sont converties en fichiers CRs en interne.</span><span class="sxs-lookup"><span data-stu-id="be602-188">When this bit is on and a file is read in, all instances of CRCRLF will be converted to hard CRs internally.</span></span> <span data-ttu-id="be602-189">Cela aura une incidence sur l’habillage du texte.</span><span class="sxs-lookup"><span data-stu-id="be602-189">This will affect the text wrapping.</span></span> <span data-ttu-id="be602-190">Notez que si un fichier de ce type est enregistré en texte brut, le Sir sera remplacé par CRLFs.</span><span class="sxs-lookup"><span data-stu-id="be602-190">Note that if such a file is saved as plain text, the CRs will be replaced by CRLFs.</span></span> <span data-ttu-id="be602-191">Il s’agit de la norme. txt pour le texte brut (valeur par défaut : 0, qui supprime CRCRLFs en entrée).</span><span class="sxs-lookup"><span data-stu-id="be602-191">This is the .txt standard for plain text (default: 0, which deletes CRCRLFs on input).</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="be602-192">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be602-192">Requirements</span></span>



| <span data-ttu-id="be602-193">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be602-193">Requirement</span></span> | <span data-ttu-id="be602-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="be602-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be602-195">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be602-195">Minimum supported client</span></span><br/> | <span data-ttu-id="be602-196">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be602-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be602-197">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be602-197">Minimum supported server</span></span><br/> | <span data-ttu-id="be602-198">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be602-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be602-199">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="be602-199">Redistributable</span></span><br/>          | <span data-ttu-id="be602-200">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="be602-200">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="be602-201">En-tête</span><span class="sxs-lookup"><span data-stu-id="be602-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="be602-202"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="be602-202"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be602-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be602-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be602-204">**\_SETEDITSTYLE em**</span><span class="sxs-lookup"><span data-stu-id="be602-204">**EM\_SETEDITSTYLE**</span></span>](em-seteditstyle.md)
</dt> </dl>

 

