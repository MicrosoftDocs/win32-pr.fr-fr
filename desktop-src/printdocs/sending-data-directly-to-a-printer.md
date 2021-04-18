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
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a><span data-ttu-id="04945-103">Procédure : envoyer des données directement à une imprimante GDI</span><span class="sxs-lookup"><span data-stu-id="04945-103">How To: Send Data Directly to a GDI Printer</span></span>

<span data-ttu-id="04945-104">L’exemple de code plus loin dans cette rubrique montre comment envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante GDI.</span><span class="sxs-lookup"><span data-stu-id="04945-104">The code sample later in this topic shows how to send printer control data directly to printers that use GDI-based printer drivers.</span></span>

<span data-ttu-id="04945-105">Les étapes suivantes décrivent comment envoyer des données directement à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="04945-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="04945-106">Ces étapes sont également illustrées dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="04945-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="04945-107">Appelez [**OpenPrinter**](openprinter.md) pour obtenir un descripteur de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="04945-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="04945-108">Initialise une structure [**docinfo**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) avec les données de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="04945-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="04945-109">Appelez [**StartDocPrinter**](startdocprinter.md) pour indiquer que l’application enverra les données de document à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="04945-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="04945-110">Appelez [**StartPagePrinter**](startpageprinter.md) pour indiquer que l’application envoie une nouvelle page à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="04945-110">Call [**StartPagePrinter**](startpageprinter.md) to indicate that the application will be sending a new page to the printer.</span></span>
5.  <span data-ttu-id="04945-111">Appelez [**WritePrinter**](writeprinter.md) pour envoyer les données.</span><span class="sxs-lookup"><span data-stu-id="04945-111">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
6.  <span data-ttu-id="04945-112">Appelez [**EndPagePrinter**](endpageprinter.md) pour indiquer que toutes les données de la page en cours ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="04945-112">Call [**EndPagePrinter**](endpageprinter.md) to indicate that all data for the current page has been sent.</span></span>
7.  <span data-ttu-id="04945-113">Appelez [**EndDocPrinter**](enddocprinter.md) pour indiquer que toutes les données de ce document ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="04945-113">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
8.  <span data-ttu-id="04945-114">Appelez [**ClosePrinter**](closeprinter.md) pour libérer les ressources.</span><span class="sxs-lookup"><span data-stu-id="04945-114">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="04945-115">Envoyer des données de contrôle d’imprimante directement aux imprimantes qui utilisent des pilotes d’imprimante GDI.</span><span class="sxs-lookup"><span data-stu-id="04945-115">Send printer control data directly to printers that use GDI-based printer drivers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="04945-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04945-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04945-117">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="04945-117">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="04945-118">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="04945-118">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="04945-119">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="04945-119">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="04945-120">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="04945-120">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="04945-121">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="04945-121">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="04945-122">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="04945-122">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="04945-123">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="04945-123">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
