---
description: Différents styles de type dans une famille de polices peuvent avoir des largeurs différentes.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Dessin de texte à partir de différentes polices sur la même ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad28f13c94e568073504f07e8722e5d688cb12aa1b376b0f52fad752574e6f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038047"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>Dessin de texte à partir de différentes polices sur la même ligne

Différents styles de type dans une famille de polices peuvent avoir des largeurs différentes. Par exemple, les styles gras et italique d’une famille sont toujours plus larges que le style romain pour une taille de point spécifiée. Lorsque vous affichez ou imprimez plusieurs styles de type sur une seule ligne, vous devez effectuer le suivi de la largeur de la ligne pour éviter que des caractères s’affichent ou s’impriment les uns au-dessus des autres.

Vous pouvez utiliser deux fonctions pour récupérer la largeur (ou l’étendue) du texte dans la police actuelle. La fonction [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) calcule la largeur et la hauteur d’une chaîne de caractères. Si la chaîne contient un ou plusieurs caractères de tabulation, la largeur de la chaîne est basée sur un tableau spécifié de positions de taquet de tabulation. La fonction [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) calcule la largeur et la hauteur d’une ligne de texte.

Le cas échéant, le système synthétise une police en modifiant les bitmaps de caractères. Pour synthétiser un caractère dans une police en gras, le système dessine le caractère deux fois : au point de départ, et à nouveau un pixel à droite du point de départ. Pour synthétiser un caractère dans une police en italique, le système trace deux lignes de pixels en bas de la cellule de caractère, déplace le point de départ d’un pixel vers la droite, dessine les deux lignes suivantes et continue jusqu’à ce que le caractère soit dessiné. En décalant les pixels, chaque caractère semble être incliné vers la droite. La quantité de cisaillement est une fonction de la hauteur du caractère.

Une façon d’écrire une ligne de texte qui contient plusieurs polices consiste à utiliser la fonction [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) après chaque appel à [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) et à ajouter la longueur à une position actuelle. L’exemple suivant écrit la ligne « This is a sample String ». à l’aide de caractères gras pour « This is a », bascule vers caractères italiques pour « Sample », puis retourne en caractères gras pour « String ». Une fois toutes les chaînes imprimées, les caractères par défaut du système sont restaurés.


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



Dans cet exemple, la fonction [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) initialise les membres d’une structure de [taille](/previous-versions//dd145106(v=vs.85)) avec la longueur et la hauteur de la chaîne spécifiée. La fonction [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) récupère le dépassement pour la police actuelle. Étant donné que le dépassement est égal à zéro si la police est une police TrueType, la valeur de dépassement ne change pas le placement de la chaîne. Toutefois, pour les polices Raster, il est important d’utiliser la valeur de dépassement.

Le dépassement est soustrait de la chaîne en gras, pour amener les caractères suivants plus près de la fin de la chaîne si la police est une police raster. Étant donné que le dépassement affecte à la fois le début et la fin de la chaîne italique dans une police raster, les glyphes commencent à droite de l’emplacement spécifié et se terminent à gauche du point de terminaison de la dernière cellule de caractère. (La fonction [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) récupère l’étendue des cellules de caractères, et non l’étendue des glyphes.) Pour tenir compte du dépassement dans la chaîne en italiques raster, l’exemple soustrait le dépassement avant de placer la chaîne et le soustrait à nouveau avant de placer les caractères suivants.

La fonction [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) ajoute de l’espace supplémentaire aux caractères de saut de ligne dans une ligne de texte. Vous pouvez utiliser la fonction [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) pour déterminer l’étendue d’une chaîne, puis soustraire cette étendue de la quantité totale d’espace occupée par la ligne et utiliser la fonction [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) pour répartir l’espace supplémentaire parmi les caractères de saut de la chaîne. La fonction [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) ajoute de l’espace supplémentaire à chaque cellule de caractère dans la police sélectionnée, y compris le caractère de saut de ligne. (Vous pouvez utiliser la fonction [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) pour déterminer la quantité d’espace supplémentaire en cours d’ajout aux cellules de caractères ; le paramètre par défaut est zéro.)

Vous pouvez placer les caractères avec une plus grande précision à l’aide de la fonction [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) ou [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) pour récupérer les largeurs des caractères individuels dans une police. La fonction [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) est plus précise que la fonction [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , mais elle ne peut être utilisée qu’avec des polices TrueType.

L’espacement ABC permet également à une application d’effectuer un alignement de texte très précis. Par exemple, lorsque le droit de l’application aligne une police raster roman sans utiliser l’espacement ABC, la largeur d’avance est calculée comme la largeur des caractères. Cela signifie que l’espace blanc à droite du glyphe dans la bitmap est aligné, et non le glyphe lui-même. En utilisant des largeurs ABC, les applications ont plus de souplesse dans le placement et la suppression d’espaces blancs lors de l’alignement du texte, car elles contiennent des informations qui permettent de contrôler précisément l’espacement entre les caractères.

 

 
