---
description: L’exemple de code plus loin dans cette rubrique montre comment envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante GDI.
ms.assetid: 321f2333-d88e-4042-b9b1-0d918b3209d4
title: 'Procédure : envoyer des données directement à une imprimante GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1968b435068a62ce7a7d379a66c1500d04d8936a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536507"
---
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a>Procédure : envoyer des données directement à une imprimante GDI

L’exemple de code plus loin dans cette rubrique montre comment envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante GDI.

Les étapes suivantes décrivent comment envoyer des données directement à une imprimante. Ces étapes sont également illustrées dans l’exemple de code suivant.

1.  Appelez [**OpenPrinter**](openprinter.md) pour obtenir un descripteur de l’imprimante.
2.  Initialise une structure [**docinfo**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) avec les données de l’imprimante.
3.  Appelez [**StartDocPrinter**](startdocprinter.md) pour indiquer que l’application enverra les données de document à l’imprimante.
4.  Appelez [**StartPagePrinter**](startpageprinter.md) pour indiquer que l’application envoie une nouvelle page à l’imprimante.
5.  Appelez [**WritePrinter**](writeprinter.md) pour envoyer les données.
6.  Appelez [**EndPagePrinter**](endpageprinter.md) pour indiquer que toutes les données de la page en cours ont été envoyées.
7.  Appelez [**EndDocPrinter**](enddocprinter.md) pour indiquer que toutes les données de ce document ont été envoyées.
8.  Appelez [**ClosePrinter**](closeprinter.md) pour libérer les ressources.

Envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante GDI.


```C++
// 
// RawDataToPrinter - sends binary data directly to a printer 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToPrinter(LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1 DocInfo;
    DWORD      dwJob = 0L;
    DWORD      dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter( szPrinterName, &hPrinter, NULL );
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;
        DocInfo.pDatatype = (LPTSTR)_T("RAW");

        // Inform the spooler the document is beginning. 
        dwJob = StartDocPrinter( hPrinter, 1, (LPBYTE)&DocInfo );
        if (dwJob > 0) {
            // Start a page. 
            bStatus = StartPagePrinter( hPrinter );
            if (bStatus) {
                // Send the data to the printer. 
                bStatus = WritePrinter( hPrinter, lpData, dwCount, &dwBytesWritten);
                EndPagePrinter (hPrinter);
            }
            // Inform the spooler that the document is ending. 
            EndDocPrinter( hPrinter );
        }
        // Close the printer handle. 
        ClosePrinter( hPrinter );
    }
    // Check to see if correct number of bytes were written. 
    if (!bStatus || (dwBytesWritten != dwCount)) {
        bStatus = FALSE;
    } else {
        bStatus = TRUE;
    }
    return bStatus;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 
