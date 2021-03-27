---
description: L’un des constructeurs de la classe Graphics reçoit un handle de contexte de périphérique et un handle d’imprimante.
ms.assetid: 9be67cb2-4bf9-4758-af03-7d92dd04feaf
title: Optimisation de l’impression en fournissant un handle d’imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a247af3de037e220432c424c408b4055690ff861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972158"
---
# <a name="optimizing-printing-by-providing-a-printer-handle"></a><span data-ttu-id="48044-103">Optimisation de l’impression en fournissant un handle d’imprimante</span><span class="sxs-lookup"><span data-stu-id="48044-103">Optimizing Printing by Providing a Printer Handle</span></span>

<span data-ttu-id="48044-104">L’un des constructeurs de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) reçoit un handle de contexte de périphérique et un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="48044-104">One of the constructors for the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class receives a device context handle and a printer handle.</span></span> <span data-ttu-id="48044-105">Lorsque vous envoyez des commandes GDI+ Windows à certaines imprimantes PostScript, les performances sont meilleures si vous créez votre objet **Graphics** avec ce constructeur particulier.</span><span class="sxs-lookup"><span data-stu-id="48044-105">When you send Windows GDI+ commands to certain PostScript printers, the performance will be better if you create your **Graphics** object with that particular constructor.</span></span>

<span data-ttu-id="48044-106">L’application console suivante appelle [GetDefaultPrinter](../printdocs/getdefaultprinter.md) pour récupérer le nom de l’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="48044-106">The following console application calls [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to get the name of the default printer.</span></span> <span data-ttu-id="48044-107">Le code transmet le nom de l’imprimante à [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) pour obtenir un handle de contexte de périphérique pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="48044-107">The code passes the printer name to [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) to obtain a device context handle for the printer.</span></span> <span data-ttu-id="48044-108">Le code transmet également le nom de l’imprimante à [OpenPrinter](../printdocs/openprinter.md) pour obtenir un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="48044-108">The code also passes the printer name to [OpenPrinter](../printdocs/openprinter.md) to obtain a printer handle.</span></span> <span data-ttu-id="48044-109">Le handle de contexte de périphérique et le descripteur d’imprimante sont passés au constructeur [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="48044-109">Both the device context handle and the printer handle are passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="48044-110">Deux figures sont ensuite dessinées sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="48044-110">Then two figures are drawn on the printer.</span></span>

> [!Note]  
> <span data-ttu-id="48044-111">La fonction [GetDefaultPrinter](../printdocs/getdefaultprinter.md) est prise en charge uniquement sur Windows 2000 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="48044-111">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   DWORD   size;
   HDC     hdcPrint;
   HANDLE  printerHandle;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the length of the printer name.
   GetDefaultPrinter(NULL, &size);
   TCHAR* buffer = new TCHAR[size];

   // Get the printer name.
   if(!GetDefaultPrinter(buffer, &size))
   {
      printf("Failure");
   }
   else
   {
      // Get a device context for the printer.
      hdcPrint = CreateDC(NULL, buffer, NULL, NULL);

      // Get a printer handle.
      OpenPrinter(buffer, &printerHandle, NULL);

      StartDoc(hdcPrint, &docInfo);
      StartPage(hdcPrint);
         Graphics* graphics = new Graphics(hdcPrint, printerHandle);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         delete(pen);
         delete(graphics);
      EndPage(hdcPrint);
      EndDoc(hdcPrint);

      ClosePrinter(printerHandle);
      DeleteDC(hdcPrint);
   }

   delete buffer;
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
