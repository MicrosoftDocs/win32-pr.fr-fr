---
description: Une façon d’obtenir un handle de contexte de périphérique pour une imprimante consiste à afficher une boîte de dialogue Imprimer et à autoriser l’utilisateur à choisir une imprimante.
ms.assetid: 73a74186-c916-4ad9-b768-6bc887fd5231
title: Affichage d’une boîte de dialogue Imprimer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113c9235e70712a4923ebdc3ad239f533160eb2f84f76ae729d7fadf203ca612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036827"
---
# <a name="displaying-a-print-dialog-box"></a>Affichage d’une boîte de dialogue Imprimer

Une façon d’obtenir un handle de contexte de périphérique pour une imprimante consiste à afficher une boîte de dialogue Imprimer et à autoriser l’utilisateur à choisir une imprimante. La fonction [PrintDlg](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) (qui affiche la boîte de dialogue) a un paramètre qui est l’adresse d’une structure [PrintDlg](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) . La structure PRINTDLG a plusieurs membres, mais vous pouvez conserver la plupart des valeurs par défaut. Les deux membres que vous devez définir sont **lStructSize** et **Flags**. Affectez à **lStructSize** la taille d’une variable PRINTDLG et définissez **Flags** sur PD \_ RETURNDC. La définition des **indicateurs** sur PC \_ RETURNDC spécifie que vous souhaitez que la fonction PrintDlg remplisse le champ **HDC** avec un handle de contexte de périphérique pour l’imprimante choisie par l’utilisateur.


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
   
   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";
   
   // Create a PRINTDLG structure, and initialize the appropriate fields.
   PRINTDLG printDlg;
   ZeroMemory(&printDlg, sizeof(printDlg));
   printDlg.lStructSize = sizeof(printDlg);
   printDlg.Flags = PD_RETURNDC;
   
   // Display a print dialog box.
   if(!PrintDlg(&printDlg))
   {
      printf("Failure\n");
   }
   else
   {
      // Now that PrintDlg has returned, a device context handle
      // for the chosen printer is in printDlg->hDC.
      
      StartDoc(printDlg.hDC, &docInfo);
      StartPage(printDlg.hDC);
         Graphics* graphics = new Graphics(printDlg.hDC);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         graphics->DrawLine(pen, 200, 500, 400, 650);
         delete pen;
         delete graphics;
      EndPage(printDlg.hDC);
      EndDoc(printDlg.hDC); 
   }
   if(printDlg.hDevMode) 
      GlobalFree(printDlg.hDevMode);
   if(printDlg.hDevNames) 
      GlobalFree(printDlg.hDevNames);
   if(printDlg.hDC)
      DeleteDC(printDlg.hDC);
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
