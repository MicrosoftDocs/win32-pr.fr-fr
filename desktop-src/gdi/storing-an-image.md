---
description: De nombreuses applications stockent les images de manière permanente sous forme de fichiers. Par exemple, les applications de dessin stockent des images, des feuilles de calcul et des graphiques de magasin, des dessins de magasins d’applications CAO, etc.
ms.assetid: fc43ab78-c174-400b-a73a-c346d8bda8d2
title: Stockage d’une image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf47a869481d9ec7d71d594ddb238be14f9b152
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007753"
---
# <a name="storing-an-image"></a>Stockage d’une image

De nombreuses applications stockent les images de manière permanente sous forme de fichiers. Par exemple, les applications de dessin stockent des images, des feuilles de calcul et des graphiques de magasin, des dessins de magasins d’applications CAO, etc.

si vous écrivez une application qui stocke une image bitmap dans un fichier, vous devez utiliser le format de fichier bitmap décrit dans [bitmap Stockage](bitmap-storage.md). Pour stocker une image bitmap dans ce format, vous devez utiliser une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)ou [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) et un tableau de structures [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , ainsi qu’un tableau d’index de palette.

L’exemple de code suivant définit une fonction qui utilise une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) et alloue de la mémoire pour et initialise des membres dans une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) . Notez que la structure **BITMAPINFO,** ne peut pas être utilisée avec une structure [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) ou [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .


```C++
PBITMAPINFO CreateBitmapInfoStruct(HWND hwnd, HBITMAP hBmp)
{ 
    BITMAP bmp; 
    PBITMAPINFO pbmi; 
    WORD    cClrBits; 

    // Retrieve the bitmap color format, width, and height.  
    if (!GetObject(hBmp, sizeof(BITMAP), (LPSTR)&bmp)) 
        errhandler("GetObject", hwnd); 

    // Convert the color format to a count of bits.  
    cClrBits = (WORD)(bmp.bmPlanes * bmp.bmBitsPixel); 
    if (cClrBits == 1) 
        cClrBits = 1; 
    else if (cClrBits <= 4) 
        cClrBits = 4; 
    else if (cClrBits <= 8) 
        cClrBits = 8; 
    else if (cClrBits <= 16) 
        cClrBits = 16; 
    else if (cClrBits <= 24) 
        cClrBits = 24; 
    else cClrBits = 32; 

    // Allocate memory for the BITMAPINFO structure. (This structure  
    // contains a BITMAPINFOHEADER structure and an array of RGBQUAD  
    // data structures.)  

     if (cClrBits < 24) 
         pbmi = (PBITMAPINFO) LocalAlloc(LPTR, 
                    sizeof(BITMAPINFOHEADER) + 
                    sizeof(RGBQUAD) * (1<< cClrBits)); 

     // There is no RGBQUAD array for these formats: 24-bit-per-pixel or 32-bit-per-pixel 

     else 
         pbmi = (PBITMAPINFO) LocalAlloc(LPTR, 
                    sizeof(BITMAPINFOHEADER)); 

    // Initialize the fields in the BITMAPINFO structure.  

    pbmi->bmiHeader.biSize = sizeof(BITMAPINFOHEADER); 
    pbmi->bmiHeader.biWidth = bmp.bmWidth; 
    pbmi->bmiHeader.biHeight = bmp.bmHeight; 
    pbmi->bmiHeader.biPlanes = bmp.bmPlanes; 
    pbmi->bmiHeader.biBitCount = bmp.bmBitsPixel; 
    if (cClrBits < 24) 
        pbmi->bmiHeader.biClrUsed = (1<<cClrBits); 

    // If the bitmap is not compressed, set the BI_RGB flag.  
    pbmi->bmiHeader.biCompression = BI_RGB; 

    // Compute the number of bytes in the array of color  
    // indices and store the result in biSizeImage.  
    // The width must be DWORD aligned unless the bitmap is RLE 
    // compressed. 
    pbmi->bmiHeader.biSizeImage = ((pbmi->bmiHeader.biWidth * cClrBits +31) & ~31) /8
                                  * pbmi->bmiHeader.biHeight; 
    // Set biClrImportant to 0, indicating that all of the  
    // device colors are important.  
     pbmi->bmiHeader.biClrImportant = 0; 
     return pbmi; 
 } 
```



L’exemple de code suivant définit une fonction qui initialise les structures restantes, récupère le tableau des index de palette, ouvre le fichier, copie les données et ferme le fichier.


```C++
void CreateBMPFile(HWND hwnd, LPTSTR pszFile, PBITMAPINFO pbi, 
                  HBITMAP hBMP, HDC hDC) 
 { 
     HANDLE hf;                 // file handle  
    BITMAPFILEHEADER hdr;       // bitmap file-header  
    PBITMAPINFOHEADER pbih;     // bitmap info-header  
    LPBYTE lpBits;              // memory pointer  
    DWORD dwTotal;              // total count of bytes  
    DWORD cb;                   // incremental count of bytes  
    BYTE *hp;                   // byte pointer  
    DWORD dwTmp; 

    pbih = (PBITMAPINFOHEADER) pbi; 
    lpBits = (LPBYTE) GlobalAlloc(GMEM_FIXED, pbih->biSizeImage);

    if (!lpBits) 
         errhandler("GlobalAlloc", hwnd); 

    // Retrieve the color table (RGBQUAD array) and the bits  
    // (array of palette indices) from the DIB.  
    if (!GetDIBits(hDC, hBMP, 0, (WORD) pbih->biHeight, lpBits, pbi, 
        DIB_RGB_COLORS)) 
    {
        errhandler("GetDIBits", hwnd); 
    }

    // Create the .BMP file.  
    hf = CreateFile(pszFile, 
                   GENERIC_READ | GENERIC_WRITE, 
                   (DWORD) 0, 
                    NULL, 
                   CREATE_ALWAYS, 
                   FILE_ATTRIBUTE_NORMAL, 
                   (HANDLE) NULL); 
    if (hf == INVALID_HANDLE_VALUE) 
        errhandler("CreateFile", hwnd); 
    hdr.bfType = 0x4d42;        // 0x42 = "B" 0x4d = "M"  
    // Compute the size of the entire file.  
    hdr.bfSize = (DWORD) (sizeof(BITMAPFILEHEADER) + 
                 pbih->biSize + pbih->biClrUsed 
                 * sizeof(RGBQUAD) + pbih->biSizeImage); 
    hdr.bfReserved1 = 0; 
    hdr.bfReserved2 = 0; 

    // Compute the offset to the array of color indices.  
    hdr.bfOffBits = (DWORD) sizeof(BITMAPFILEHEADER) + 
                    pbih->biSize + pbih->biClrUsed 
                    * sizeof (RGBQUAD); 

    // Copy the BITMAPFILEHEADER into the .BMP file.  
    if (!WriteFile(hf, (LPVOID) &hdr, sizeof(BITMAPFILEHEADER), 
        (LPDWORD) &dwTmp,  NULL)) 
    {
       errhandler("WriteFile", hwnd); 
    }

    // Copy the BITMAPINFOHEADER and RGBQUAD array into the file.  
    if (!WriteFile(hf, (LPVOID) pbih, sizeof(BITMAPINFOHEADER) 
                  + pbih->biClrUsed * sizeof (RGBQUAD), 
                  (LPDWORD) &dwTmp, ( NULL)))
        errhandler("WriteFile", hwnd); 

    // Copy the array of color indices into the .BMP file.  
    dwTotal = cb = pbih->biSizeImage; 
    hp = lpBits; 
    if (!WriteFile(hf, (LPSTR) hp, (int) cb, (LPDWORD) &dwTmp,NULL)) 
           errhandler("WriteFile", hwnd); 

    // Close the .BMP file.  
     if (!CloseHandle(hf)) 
           errhandler("CloseHandle", hwnd); 

    // Free memory.  
    GlobalFree((HGLOBAL)lpBits);
}
```



 

 
