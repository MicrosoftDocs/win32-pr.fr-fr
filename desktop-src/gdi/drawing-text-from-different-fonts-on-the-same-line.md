---
description: Différents styles de type dans une famille de polices peuvent avoir des largeurs différentes.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Dessin de texte à partir de différentes polices sur la même ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2eae2a7a332bd929b9a965462ce802734679f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202043"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a><span data-ttu-id="d08e8-103">Dessin de texte à partir de différentes polices sur la même ligne</span><span class="sxs-lookup"><span data-stu-id="d08e8-103">Drawing Text from Different Fonts on the Same Line</span></span>

<span data-ttu-id="d08e8-104">Différents styles de type dans une famille de polices peuvent avoir des largeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="d08e8-104">Different type styles within a font family can have different widths.</span></span> <span data-ttu-id="d08e8-105">Par exemple, les styles gras et italique d’une famille sont toujours plus larges que le style romain pour une taille de point spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d08e8-105">For example, bold and italic styles of a family are always wider than the roman style for a specified point size.</span></span> <span data-ttu-id="d08e8-106">Lorsque vous affichez ou imprimez plusieurs styles de type sur une seule ligne, vous devez effectuer le suivi de la largeur de la ligne pour éviter que des caractères s’affichent ou s’impriment les uns au-dessus des autres.</span><span class="sxs-lookup"><span data-stu-id="d08e8-106">When you display or print several type styles on a single line, you must keep track of the width of the line to avoid having characters displayed or printed on top of one another.</span></span>

<span data-ttu-id="d08e8-107">Vous pouvez utiliser deux fonctions pour récupérer la largeur (ou l’étendue) du texte dans la police actuelle.</span><span class="sxs-lookup"><span data-stu-id="d08e8-107">You can use two functions to retrieve the width (or extent) of text in the current font.</span></span> <span data-ttu-id="d08e8-108">La fonction [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) calcule la largeur et la hauteur d’une chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="d08e8-108">The [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) function computes the width and height of a character string.</span></span> <span data-ttu-id="d08e8-109">Si la chaîne contient un ou plusieurs caractères de tabulation, la largeur de la chaîne est basée sur un tableau spécifié de positions de taquet de tabulation.</span><span class="sxs-lookup"><span data-stu-id="d08e8-109">If the string contains one or more tab characters, the width of the string is based upon a specified array of tab-stop positions.</span></span> <span data-ttu-id="d08e8-110">La fonction [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) calcule la largeur et la hauteur d’une ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="d08e8-110">The [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function computes the width and height of a line of text.</span></span>

<span data-ttu-id="d08e8-111">Le cas échéant, le système synthétise une police en modifiant les bitmaps de caractères.</span><span class="sxs-lookup"><span data-stu-id="d08e8-111">When necessary, the system synthesizes a font by changing the character bitmaps.</span></span> <span data-ttu-id="d08e8-112">Pour synthétiser un caractère dans une police en gras, le système dessine le caractère deux fois : au point de départ, et à nouveau un pixel à droite du point de départ.</span><span class="sxs-lookup"><span data-stu-id="d08e8-112">To synthesize a character in a bold font, the system draws the character twice: at the starting point, and again one pixel to the right of the starting point.</span></span> <span data-ttu-id="d08e8-113">Pour synthétiser un caractère dans une police en italique, le système trace deux lignes de pixels en bas de la cellule de caractère, déplace le point de départ d’un pixel vers la droite, dessine les deux lignes suivantes et continue jusqu’à ce que le caractère soit dessiné.</span><span class="sxs-lookup"><span data-stu-id="d08e8-113">To synthesize a character in an italic font, the system draws two rows of pixels at the bottom of the character cell, moves the starting point one pixel to the right, draws the next two rows, and continues until the character has been drawn.</span></span> <span data-ttu-id="d08e8-114">En décalant les pixels, chaque caractère semble être incliné vers la droite.</span><span class="sxs-lookup"><span data-stu-id="d08e8-114">By shifting pixels, each character appears to be sheared to the right.</span></span> <span data-ttu-id="d08e8-115">La quantité de cisaillement est une fonction de la hauteur du caractère.</span><span class="sxs-lookup"><span data-stu-id="d08e8-115">The amount of shear is a function of the height of the character.</span></span>

<span data-ttu-id="d08e8-116">Une façon d’écrire une ligne de texte qui contient plusieurs polices consiste à utiliser la fonction [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) après chaque appel à [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) et à ajouter la longueur à une position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d08e8-116">One way to write a line of text that contains multiple fonts is to use the [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function after each call to [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) and add the length to a current position.</span></span> <span data-ttu-id="d08e8-117">L’exemple suivant écrit la ligne « This is a sample String ».</span><span class="sxs-lookup"><span data-stu-id="d08e8-117">The following example writes the line "This is a sample string."</span></span> <span data-ttu-id="d08e8-118">à l’aide de caractères gras pour « This is a », bascule vers caractères italiques pour « Sample », puis retourne en caractères gras pour « String ».</span><span class="sxs-lookup"><span data-stu-id="d08e8-118">using bold characters for "This is a", switches to italic characters for "sample", then returns to bold characters for "string."</span></span> <span data-ttu-id="d08e8-119">Une fois toutes les chaînes imprimées, les caractères par défaut du système sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="d08e8-119">After printing all the strings, it restores the system default characters.</span></span>


```C++
int XIncrement; 
int YStart; 
TEXTMETRIC tm; 
HFONT hfntDefault, hfntItalic, hfntBold; 
SIZE sz; 
LPSTR lpszString1 = "This is a "; 
LPSTR lpszString2 = "sample "; 
LPSTR lpszString3 = "string."; 
HRESULT hr;
size_t * pcch;
 
// Create a bold and an italic logical font.  
 
hfntItalic = MyCreateFont(); 
hfntBold = MyCreateFont(); 
 
 
// Select the bold font and draw the first string  
// beginning at the specified point (XIncrement, YStart).  
 
XIncrement = 10; 
YStart = 50; 
hfntDefault = SelectObject(hdc, hfntBold); 
hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
TextOut(hdc, XIncrement, YStart, lpszString1, *pcch); 
 
// Compute the length of the first string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
GetTextExtentPoint32(hdc, lpszString1, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Retrieve the overhang value from the TEXTMETRIC  
// structure and subtract it from the x-increment.  
// (This is only necessary for non-TrueType raster  
// fonts.)  
 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang; 
 
// Select an italic font and draw the second string  
// beginning at the point (XIncrement, YStart).  
 
hfntBold = SelectObject(hdc, hfntItalic); 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang;
hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
TextOut(hdc, XIncrement, YStart, lpszString2, *pcch); 
 
// Compute the length of the second string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
GetTextExtentPoint32(hdc, lpszString2, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Reselect the bold font and draw the third string  
// beginning at the point (XIncrement, YStart).  
 
SelectObject(hdc, hfntBold);
hr = StringCchLength(lpszString3, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
TextOut(hdc, XIncrement - tm.tmOverhang, YStart, lpszString3, 
            *pcch); 
 
// Reselect the original font.  
 
SelectObject(hdc, hfntDefault); 
 
// Delete the bold and italic fonts.  
 
DeleteObject(hfntItalic); 
DeleteObject(hfntBold); 
```



<span data-ttu-id="d08e8-120">Dans cet exemple, la fonction [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) initialise les membres d’une structure de [taille](/previous-versions//dd145106(v=vs.85)) avec la longueur et la hauteur de la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d08e8-120">In this example, the [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function initializes the members of a [SIZE](/previous-versions//dd145106(v=vs.85)) structure with the length and height of the specified string.</span></span> <span data-ttu-id="d08e8-121">La fonction [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) récupère le dépassement pour la police actuelle.</span><span class="sxs-lookup"><span data-stu-id="d08e8-121">The [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) function retrieves the overhang for the current font.</span></span> <span data-ttu-id="d08e8-122">Étant donné que le dépassement est égal à zéro si la police est une police TrueType, la valeur de dépassement ne change pas le placement de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d08e8-122">Because the overhang is zero if the font is a TrueType font, the overhang value does not change the string placement.</span></span> <span data-ttu-id="d08e8-123">Toutefois, pour les polices Raster, il est important d’utiliser la valeur de dépassement.</span><span class="sxs-lookup"><span data-stu-id="d08e8-123">For raster fonts, however, it is important to use the overhang value.</span></span>

<span data-ttu-id="d08e8-124">Le dépassement est soustrait de la chaîne en gras, pour amener les caractères suivants plus près de la fin de la chaîne si la police est une police raster.</span><span class="sxs-lookup"><span data-stu-id="d08e8-124">The overhang is subtracted from the bold string once, to bring subsequent characters closer to the end of the string if the font is a raster font.</span></span> <span data-ttu-id="d08e8-125">Étant donné que le dépassement affecte à la fois le début et la fin de la chaîne italique dans une police raster, les glyphes commencent à droite de l’emplacement spécifié et se terminent à gauche du point de terminaison de la dernière cellule de caractère.</span><span class="sxs-lookup"><span data-stu-id="d08e8-125">Because overhang affects both the beginning and end of the italic string in a raster font, the glyphs start at the right of the specified location and end at the left of the endpoint of the last character cell.</span></span> <span data-ttu-id="d08e8-126">(La fonction [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) récupère l’étendue des cellules de caractères, et non l’étendue des glyphes.) Pour tenir compte du dépassement dans la chaîne en italiques raster, l’exemple soustrait le dépassement avant de placer la chaîne et le soustrait à nouveau avant de placer les caractères suivants.</span><span class="sxs-lookup"><span data-stu-id="d08e8-126">(The [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function retrieves the extent of the character cells, not the extent of the glyphs.) To account for the overhang in the raster italic string, the example subtracts the overhang before placing the string and subtracts it again before placing subsequent characters.</span></span>

<span data-ttu-id="d08e8-127">La fonction [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) ajoute de l’espace supplémentaire aux caractères de saut de ligne dans une ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="d08e8-127">The [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) function adds extra space to the break characters in a line of text.</span></span> <span data-ttu-id="d08e8-128">Vous pouvez utiliser la fonction [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) pour déterminer l’étendue d’une chaîne, puis soustraire cette étendue de la quantité totale d’espace occupée par la ligne et utiliser la fonction [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) pour répartir l’espace supplémentaire parmi les caractères de saut de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d08e8-128">You can use the [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) function to determine the extent of a string, then subtract that extent from the total amount of space the line should occupy, and use the [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) function to distribute the extra space among the break characters in the string.</span></span> <span data-ttu-id="d08e8-129">La fonction [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) ajoute de l’espace supplémentaire à chaque cellule de caractère dans la police sélectionnée, y compris le caractère de saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="d08e8-129">The [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) function adds extra space to every character cell in the selected font, including the break character.</span></span> <span data-ttu-id="d08e8-130">(Vous pouvez utiliser la fonction [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) pour déterminer la quantité d’espace supplémentaire en cours d’ajout aux cellules de caractères ; le paramètre par défaut est zéro.)</span><span class="sxs-lookup"><span data-stu-id="d08e8-130">(You can use the [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) function to determine the current amount of extra space being added to the character cells; the default setting is zero.)</span></span>

<span data-ttu-id="d08e8-131">Vous pouvez placer les caractères avec une plus grande précision à l’aide de la fonction [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) ou [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) pour récupérer les largeurs des caractères individuels dans une police.</span><span class="sxs-lookup"><span data-stu-id="d08e8-131">You can place characters with greater precision by using the [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) or [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) function to retrieve the widths of individual characters in a font.</span></span> <span data-ttu-id="d08e8-132">La fonction [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) est plus précise que la fonction [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , mais elle ne peut être utilisée qu’avec des polices TrueType.</span><span class="sxs-lookup"><span data-stu-id="d08e8-132">The [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) function is more accurate than the [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) function, but it can only be used with TrueType fonts.</span></span>

<span data-ttu-id="d08e8-133">L’espacement ABC permet également à une application d’effectuer un alignement de texte très précis.</span><span class="sxs-lookup"><span data-stu-id="d08e8-133">ABC spacing also allows an application to perform very accurate text alignment.</span></span> <span data-ttu-id="d08e8-134">Par exemple, lorsque le droit de l’application aligne une police raster roman sans utiliser l’espacement ABC, la largeur d’avance est calculée comme la largeur des caractères.</span><span class="sxs-lookup"><span data-stu-id="d08e8-134">For example, when the application right aligns a raster roman font without using ABC spacing, the advance width is calculated as the character width.</span></span> <span data-ttu-id="d08e8-135">Cela signifie que l’espace blanc à droite du glyphe dans la bitmap est aligné, et non le glyphe lui-même.</span><span class="sxs-lookup"><span data-stu-id="d08e8-135">This means the white space to the right of the glyph in the bitmap is aligned, not the glyph itself.</span></span> <span data-ttu-id="d08e8-136">En utilisant des largeurs ABC, les applications ont plus de souplesse dans le placement et la suppression d’espaces blancs lors de l’alignement du texte, car elles contiennent des informations qui permettent de contrôler précisément l’espacement entre les caractères.</span><span class="sxs-lookup"><span data-stu-id="d08e8-136">By using ABC widths, applications have more flexibility in the placement and removal of white space when aligning text, because they have information that allows them to finely control intercharacter spacing.</span></span>

 

 
