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
# <a name="how-to-send-data-directly-to-an-xps-printer"></a><span data-ttu-id="c932d-103">Procédure : envoyer des données directement à une imprimante XPS</span><span class="sxs-lookup"><span data-stu-id="c932d-103">How To: Send Data Directly to an XPS Printer</span></span>

<span data-ttu-id="c932d-104">Cette rubrique explique comment envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="c932d-104">This topic describes how to send printer control data directly to printers that use XPSDrv printer drivers.</span></span>

<span data-ttu-id="c932d-105">Les étapes suivantes décrivent comment envoyer des données directement à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="c932d-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="c932d-106">Ces étapes sont également illustrées dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="c932d-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="c932d-107">Appelez [**OpenPrinter**](openprinter.md) pour obtenir un descripteur de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c932d-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="c932d-108">Initialise une structure [**docinfo**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) avec les données de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c932d-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="c932d-109">Appelez [**StartDocPrinter**](startdocprinter.md) pour indiquer que l’application enverra les données de document à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c932d-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="c932d-110">Appelez [**WritePrinter**](writeprinter.md) pour envoyer les données.</span><span class="sxs-lookup"><span data-stu-id="c932d-110">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
5.  <span data-ttu-id="c932d-111">Appelez [**EndDocPrinter**](enddocprinter.md) pour indiquer que toutes les données de ce document ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="c932d-111">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
6.  <span data-ttu-id="c932d-112">Appelez [**ClosePrinter**](closeprinter.md) pour libérer les ressources.</span><span class="sxs-lookup"><span data-stu-id="c932d-112">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="c932d-113">Envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="c932d-113">Send printer control data directly to printers that use XPSDrv printer drivers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c932d-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c932d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c932d-115">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="c932d-115">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="c932d-116">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="c932d-116">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="c932d-117">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="c932d-117">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="c932d-118">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c932d-118">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="c932d-119">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="c932d-119">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="c932d-120">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="c932d-120">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="c932d-121">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="c932d-121">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
