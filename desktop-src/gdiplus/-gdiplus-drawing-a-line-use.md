---
description: Cette rubrique montre comment dessiner une ligne à l’aide de GDI plus.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Dessin d’une ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5284a178baab624633dd427cad84b35933a72fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972895"
---
# <a name="drawing-a-line"></a><span data-ttu-id="a35b9-103">Dessin d’une ligne</span><span class="sxs-lookup"><span data-stu-id="a35b9-103">Drawing a Line</span></span>

<span data-ttu-id="a35b9-104">Cette rubrique montre comment dessiner une ligne à l’aide de GDI plus.</span><span class="sxs-lookup"><span data-stu-id="a35b9-104">This topic demonstrates how to draw a line using GDI Plus.</span></span>

<span data-ttu-id="a35b9-105">Pour dessiner une ligne dans GDI+ Windows, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et d’un objet [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="a35b9-105">To draw a line in Windows GDI+ you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="a35b9-106">L’objet **Graphics** fournit la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) et l’objet **Pen** contient les attributs de la ligne, tels que la couleur et la largeur.</span><span class="sxs-lookup"><span data-stu-id="a35b9-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object holds attributes of the line, such as color and width.</span></span> <span data-ttu-id="a35b9-107">L’adresse de l’objet **Pen** est passée comme argument à la méthode **DrawLine** .</span><span class="sxs-lookup"><span data-stu-id="a35b9-107">The address of the **Pen** object is passed as an argument to the **DrawLine** method.</span></span>

<span data-ttu-id="a35b9-108">Le programme suivant, qui dessine une ligne de (0,0) à (200, 100), se compose de trois fonctions : **WinMain**, **WndProc** et **OnPaint**.</span><span class="sxs-lookup"><span data-stu-id="a35b9-108">The following program, which draws a line from (0, 0) to (200, 100), consists of three functions: **WinMain**, **WndProc**, and **OnPaint**.</span></span> <span data-ttu-id="a35b9-109">Les fonctions **WinMain** et **WndProc** fournissent le code fondamental commun à la plupart des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="a35b9-109">The **WinMain** and **WndProc** functions provide the fundamental code common to most Windows applications.</span></span> <span data-ttu-id="a35b9-110">Il n’y a aucun code GDI+ dans la fonction **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="a35b9-110">There is no GDI+ code in the **WndProc** function.</span></span> <span data-ttu-id="a35b9-111">La fonction **WinMain** a une petite quantité de code GDI+, à savoir les appels requis à [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) et [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span><span class="sxs-lookup"><span data-stu-id="a35b9-111">The **WinMain** function has a small amount of GDI+ code, namely the required calls to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) and [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span></span> <span data-ttu-id="a35b9-112">Le code GDI+ qui crée réellement un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et dessine une ligne se trouve dans la fonction **OnPaint** .</span><span class="sxs-lookup"><span data-stu-id="a35b9-112">The GDI+ code that actually creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and draws a line is in the **OnPaint** function.</span></span>

<span data-ttu-id="a35b9-113">La fonction **OnPaint** reçoit un handle vers un contexte de périphérique et passe ce handle à un constructeur [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a35b9-113">The **OnPaint** function receives a handle to a device context and passes that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="a35b9-114">L’argument passé au constructeur [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) est une référence à un objet [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="a35b9-114">The argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor is a reference to a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="a35b9-115">Les quatre nombres passés au constructeur Color représentent les composants alpha, rouge, vert et bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="a35b9-115">The four numbers passed to the color constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="a35b9-116">Le composant alpha détermine la transparence de la couleur ; 0 est entièrement transparent et 255 est entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="a35b9-116">The alpha component determines the transparency of the color; 0 is fully transparent and 255 is fully opaque.</span></span> <span data-ttu-id="a35b9-117">Les quatre nombres passés à la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) représentent le point de départ (0, 0) et le point de fin (200, 100) de la ligne.</span><span class="sxs-lookup"><span data-stu-id="a35b9-117">The four numbers passed to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method represent the starting point (0, 0) and the ending point (200, 100) of the line.</span></span>


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



<span data-ttu-id="a35b9-118">Notez l’appel à [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) dans la fonction **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="a35b9-118">Note the call to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) in the **WinMain** function.</span></span> <span data-ttu-id="a35b9-119">Le premier paramètre de la fonction **GdiplusStartup** est l’adresse d’un \_ ptr ulong.</span><span class="sxs-lookup"><span data-stu-id="a35b9-119">The first parameter of the **GdiplusStartup** function is the address of a ULONG\_PTR.</span></span> <span data-ttu-id="a35b9-120">**GdiplusStartup** remplit cette variable avec un jeton qui est ensuite passé à la fonction [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) .</span><span class="sxs-lookup"><span data-stu-id="a35b9-120">**GdiplusStartup** fills that variable with a token that is later passed to the [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) function.</span></span> <span data-ttu-id="a35b9-121">Le deuxième paramètre de la fonction **GdiplusStartup** est l’adresse d’une structure [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) .</span><span class="sxs-lookup"><span data-stu-id="a35b9-121">The second parameter of the **GdiplusStartup** function is the address of a [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) structure.</span></span> <span data-ttu-id="a35b9-122">Le code précédent s’appuie sur le constructeur **GdiplusStartupInput** par défaut pour définir les membres de la structure de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="a35b9-122">The preceding code relies on the default **GdiplusStartupInput** constructor to set the structure members appropriately.</span></span>

 

 



