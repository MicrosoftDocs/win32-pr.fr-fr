---
description: l’utilisation de Windows GDI+ pour dessiner sur une imprimante est semblable à l’utilisation de GDI+ pour dessiner sur un écran d’ordinateur. Pour dessiner sur une imprimante, obtenez un handle de contexte de périphérique pour l’imprimante, puis transmettez ce handle à un constructeur Graphics.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Envoi d’une sortie GDI+ vers une imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c1c4f6c05e4918663284e6d7747952040dcddf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122301"
---
# <a name="sending-gdi-output-to-a-printer"></a>Envoi d’une sortie GDI+ vers une imprimante

l’utilisation de Windows GDI+ pour dessiner sur une imprimante est semblable à l’utilisation de GDI+ pour dessiner sur un écran d’ordinateur. Pour dessiner sur une imprimante, obtenez un handle de contexte de périphérique pour l’imprimante, puis transmettez ce handle à un constructeur [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

L’application console suivante dessine une ligne, un rectangle et une ellipse sur une imprimante nommée MyPrinter :


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

   // Get a device context for the printer.
   HDC hdcPrint = CreateDC(NULL, TEXT("\\\\printserver\\print1"), NULL, NULL);

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   StartDoc(hdcPrint, &docInfo);
   StartPage(hdcPrint);
      Graphics* graphics = new Graphics(hdcPrint);
      Pen* pen = new Pen(Color(255, 0, 0, 0));
      graphics->DrawLine(pen, 50, 50, 350, 550);
      graphics->DrawRectangle(pen, 50, 50, 300, 500);
      graphics->DrawEllipse(pen, 50, 50, 300, 500);
      delete pen;
      delete graphics;
   EndPage(hdcPrint);
   EndDoc(hdcPrint);
   
   DeleteDC(hdcPrint);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



dans le code précédent, les trois commandes de dessin GDI+ se trouvent entre les appels aux fonctions [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) et [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) , chacune recevant le handle de contexte de périphérique d’impression. Toutes les commandes graphiques entre StartDoc et EndDoc sont routées vers un métafichier temporaire. Après l’appel à EndDoc, le pilote d’imprimante convertit les données du métafichier au format requis par l’imprimante spécifique utilisée.

> [!Note]  
> Si la mise en file d’attente n’est pas activée pour l’imprimante en cours d’utilisation, la sortie graphique n’est pas acheminée vers un métafichier. Au lieu de cela, les commandes graphiques individuelles sont traitées par le pilote d’imprimante, puis envoyées à l’imprimante.

 

En règle générale, vous ne souhaitez pas coder en dur le nom d’une imprimante telle qu’elle a été effectuée dans l’application console précédente. Une alternative au codage en dur du nom consiste à appeler [GetDefaultPrinter](../printdocs/getdefaultprinter.md) pour obtenir le nom de l’imprimante par défaut. Avant d’appeler GetDefaultPrinter, vous devez allouer une mémoire tampon suffisamment grande pour contenir le nom de l’imprimante. Vous pouvez déterminer la taille de la mémoire tampon requise en appelant GetDefaultPrinter, en transmettant **null** comme premier argument.

> [!Note]  
> la fonction [GetDefaultPrinter](../printdocs/getdefaultprinter.md) est prise en charge uniquement sur Windows 2000 et versions ultérieures.

 

L’application console suivante obtient le nom de l’imprimante par défaut, puis dessine un rectangle et une ellipse sur cette imprimante. L’appel [**Graphics ::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) se trouve entre les appels à [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) et [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), de sorte que le rectangle se trouve sur une page par lui-même. De même, l’ellipse se trouve sur une page par elle-même.


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

   DWORD size;
   HDC hdcPrint;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the size of the default printer name.
   GetDefaultPrinter(NULL, &size);

   // Allocate a buffer large enough to hold the printer name.
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

      StartDoc(hdcPrint, &docInfo);
         Graphics* graphics;
         Pen* pen = new Pen(Color(255, 0, 0, 0));

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawRectangle(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawEllipse(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         delete pen;
      EndDoc(hdcPrint);

      DeleteDC(hdcPrint);
   }

   delete buffer;

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
