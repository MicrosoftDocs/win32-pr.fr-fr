---
description: Cette rubrique explique comment envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante XPSDrv.
ms.assetid: 7e98e08a-d572-451d-befb-18fc86f0e505
title: 'Procédure : envoyer des données directement à une imprimante XPS'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78a8c36d6862860862059f9bbcc8db25e171b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534242"
---
# <a name="how-to-send-data-directly-to-an-xps-printer"></a>Procédure : envoyer des données directement à une imprimante XPS

Cette rubrique explique comment envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante XPSDrv.

Les étapes suivantes décrivent comment envoyer des données directement à une imprimante. Ces étapes sont également illustrées dans l’exemple de code suivant.

1.  Appelez [**OpenPrinter**](openprinter.md) pour obtenir un descripteur de l’imprimante.
2.  Initialise une structure [**docinfo**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) avec les données de l’imprimante.
3.  Appelez [**StartDocPrinter**](startdocprinter.md) pour indiquer que l’application enverra les données de document à l’imprimante.
4.  Appelez [**WritePrinter**](writeprinter.md) pour envoyer les données.
5.  Appelez [**EndDocPrinter**](enddocprinter.md) pour indiquer que toutes les données de ce document ont été envoyées.
6.  Appelez [**ClosePrinter**](closeprinter.md) pour libérer les ressources.

Envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante XPSDrv.


```C++
// 
//  RawDataToXpsPrinter - sends binary data directly to a printer 
//          with an XPSDrv Printer Driver 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToXpsPrinter (LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1       DocInfo;
    DWORD    dwPrtJob = 0L;
    DWORD    dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter (szPrinterName, &hPrinter, NULL);
    
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;

        // Enter the datatype of this buffer.
        //  Use "XPS_PASS" when the data buffer should bypass the 
        //    print filter pipeline of the XPSDrv printer driver. 
        //    This datatype would be used to send the buffer directly 
        //    to the printer, such as when sending print head alignment 
        //    commands. Normally, a data buffer would be sent as the
        //    "RAW" datatype.
        //
        DocInfo.pDatatype = (LPTSTR)_T("XPS_PASS");

        dwPrtJob = StartDocPrinter (
                        hPrinter,
                        1,
                        (LPBYTE)&DocInfo);

        if (dwPrtJob > 0) {
                // Send the data to the printer. 
                bStatus = WritePrinter (
                hPrinter,
                lpData,
                dwCount,
                &dwBytesWritten);
        }
        
        EndDocPrinter (hPrinter);

        // Close the printer handle. 
        bStatus = ClosePrinter(hPrinter);
    }
    
    if (!bStatus || (dwCount != dwBytesWritten)) {
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

 

 
