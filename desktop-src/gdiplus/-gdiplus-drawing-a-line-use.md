---
description: Cette rubrique montre comment dessiner une ligne à l’aide de GDI plus.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Dessin d’une ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e2a330f24cd0d1771458d02b264cdaa493835477b40c95d05ca4bf71c8a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036807"
---
# <a name="drawing-a-line"></a>Dessin d’une ligne

Cette rubrique montre comment dessiner une ligne à l’aide de GDI plus.

pour dessiner une ligne dans Windows GDI+ vous avez besoin d’un objet [**graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et d’un objet [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . L’objet **Graphics** fournit la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) et l’objet **Pen** contient les attributs de la ligne, tels que la couleur et la largeur. L’adresse de l’objet **Pen** est passée comme argument à la méthode **DrawLine** .

Le programme suivant, qui dessine une ligne de (0,0) à (200, 100), se compose de trois fonctions : **WinMain**, **WndProc** et **OnPaint**. les fonctions **WinMain** et **WndProc** fournissent le code fondamental commun à la plupart des applications Windows. il n’y a pas de code GDI+ dans la fonction **WndProc** . la fonction **WinMain** a une petite quantité de GDI+ code, à savoir les appels requis à [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) et [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). le GDI+ le code qui crée réellement un objet [**graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et dessine une ligne dans la fonction **OnPaint** .

La fonction **OnPaint** reçoit un handle vers un contexte de périphérique et passe ce handle à un constructeur [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . L’argument passé au constructeur [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) est une référence à un objet [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Les quatre nombres passés au constructeur Color représentent les composants alpha, rouge, vert et bleu de la couleur. Le composant alpha détermine la transparence de la couleur ; 0 est entièrement transparent et 255 est entièrement opaque. Les quatre nombres passés à la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) représentent le point de départ (0, 0) et le point de fin (200, 100) de la ligne.


```C++
#include <stdafx.h>
#include <windows.h>
#include <objidl.h>
#include <gdiplus.h>
using namespace Gdiplus;
#pragma comment (lib,"Gdiplus.lib")

VOID OnPaint(HDC hdc)
{
   Graphics graphics(hdc);
   Pen      pen(Color(255, 0, 0, 255));
   graphics.DrawLine(&pen, 0, 0, 200, 100);
}

LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);

INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE, PSTR, INT iCmdShow)
{
   HWND                hWnd;
   MSG                 msg;
   WNDCLASS            wndClass;
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR           gdiplusToken;
   
   // Initialize GDI+.
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   
   wndClass.style          = CS_HREDRAW | CS_VREDRAW;
   wndClass.lpfnWndProc    = WndProc;
   wndClass.cbClsExtra     = 0;
   wndClass.cbWndExtra     = 0;
   wndClass.hInstance      = hInstance;
   wndClass.hIcon          = LoadIcon(NULL, IDI_APPLICATION);
   wndClass.hCursor        = LoadCursor(NULL, IDC_ARROW);
   wndClass.hbrBackground  = (HBRUSH)GetStockObject(WHITE_BRUSH);
   wndClass.lpszMenuName   = NULL;
   wndClass.lpszClassName  = TEXT("GettingStarted");
   
   RegisterClass(&wndClass);
   
   hWnd = CreateWindow(
      TEXT("GettingStarted"),   // window class name
      TEXT("Getting Started"),  // window caption
      WS_OVERLAPPEDWINDOW,      // window style
      CW_USEDEFAULT,            // initial x position
      CW_USEDEFAULT,            // initial y position
      CW_USEDEFAULT,            // initial x size
      CW_USEDEFAULT,            // initial y size
      NULL,                     // parent window handle
      NULL,                     // window menu handle
      hInstance,                // program instance handle
      NULL);                    // creation parameters
      
   ShowWindow(hWnd, iCmdShow);
   UpdateWindow(hWnd);
   
   while(GetMessage(&msg, NULL, 0, 0))
   {
      TranslateMessage(&msg);
      DispatchMessage(&msg);
   }
   
   GdiplusShutdown(gdiplusToken);
   return msg.wParam;
}  // WinMain

LRESULT CALLBACK WndProc(HWND hWnd, UINT message, 
   WPARAM wParam, LPARAM lParam)
{
   HDC          hdc;
   PAINTSTRUCT  ps;
   
   switch(message)
   {
   case WM_PAINT:
      hdc = BeginPaint(hWnd, &ps);
      OnPaint(hdc);
      EndPaint(hWnd, &ps);
      return 0;
   case WM_DESTROY:
      PostQuitMessage(0);
      return 0;
   default:
      return DefWindowProc(hWnd, message, wParam, lParam);
   }
} // WndProc
```



Notez l’appel à [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) dans la fonction **WinMain** . Le premier paramètre de la fonction **GdiplusStartup** est l’adresse d’un \_ ptr ulong. **GdiplusStartup** remplit cette variable avec un jeton qui est ensuite passé à la fonction [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) . Le deuxième paramètre de la fonction **GdiplusStartup** est l’adresse d’une structure [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) . Le code précédent s’appuie sur le constructeur **GdiplusStartupInput** par défaut pour définir les membres de la structure de manière appropriée.

 

 



