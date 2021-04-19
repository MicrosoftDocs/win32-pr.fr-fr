---
description: Cette rubrique explique comment récupérer un contexte de périphérique d’impression.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: 'Comment : récupérer un contexte de périphérique d’impression'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39fde55450273e42f3429f173150296fdd67a1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531723"
---
# <a name="how-to-retrieve-a-printer-device-context"></a><span data-ttu-id="18d64-103">Comment : récupérer un contexte de périphérique d’impression</span><span class="sxs-lookup"><span data-stu-id="18d64-103">How To: Retrieve a Printer Device Context</span></span>

<span data-ttu-id="18d64-104">Cette rubrique explique comment récupérer un contexte de périphérique d’impression.</span><span class="sxs-lookup"><span data-stu-id="18d64-104">This topic describes how to retrieve a printer device context.</span></span> <span data-ttu-id="18d64-105">Vous pouvez récupérer un contexte de périphérique d’impression en appelant la fonction [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) directement, ou elle peut être retournée par une boîte de dialogue d' **impression** commune.</span><span class="sxs-lookup"><span data-stu-id="18d64-105">You can retrieve a printer device context by calling the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function directly, or it can be returned by a **Print** common dialog box.</span></span>

<span data-ttu-id="18d64-106">Lorsque vous affichez une boîte de dialogue d' **impression** courante, un utilisateur peut sélectionner l’imprimante, les pages du document et le nombre de copies de documents qu’il souhaite imprimer.</span><span class="sxs-lookup"><span data-stu-id="18d64-106">When you display a **Print** common dialog box a user will be able to select the printer, the pages of the document, and the number of document copies they want to print.</span></span> <span data-ttu-id="18d64-107">La boîte de dialogue d' **impression** commune retourne ces sélections dans une structure de données.</span><span class="sxs-lookup"><span data-stu-id="18d64-107">The **Print** common dialog box returns these selections in a data structure.</span></span>

<span data-ttu-id="18d64-108">Cette rubrique explique comment obtenir un contexte de périphérique d’impression à l’aide des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="18d64-108">This topic describes how to obtain a printer device context by using the following methods.</span></span>

-   [<span data-ttu-id="18d64-109">Appeler CreateDC</span><span class="sxs-lookup"><span data-stu-id="18d64-109">Call CreateDC</span></span>](#call-createdc)
-   [<span data-ttu-id="18d64-110">Afficher une boîte de dialogue d’impression courante</span><span class="sxs-lookup"><span data-stu-id="18d64-110">Display a Print Common Dialog Box</span></span>](#display-a-print-common-dialog-box)
    -   [<span data-ttu-id="18d64-111">Utilisation de la fonction PrintDlgEx</span><span class="sxs-lookup"><span data-stu-id="18d64-111">Using the PrintDlgEx Function</span></span>](#using-the-printdlgex-function)
    -   [<span data-ttu-id="18d64-112">Utilisation de la fonction PrintDlg</span><span class="sxs-lookup"><span data-stu-id="18d64-112">Using the PrintDlg Function</span></span>](#using-the-printdlg-function)

## <a name="call-createdc"></a><span data-ttu-id="18d64-113">Appeler CreateDC</span><span class="sxs-lookup"><span data-stu-id="18d64-113">Call CreateDC</span></span>

<span data-ttu-id="18d64-114">Si vous connaissez l’appareil sur lequel vous souhaitez imprimer, vous pouvez appeler [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) et transmettre ces informations directement à la fonction.</span><span class="sxs-lookup"><span data-stu-id="18d64-114">If you know the device to which you want to print, you can call [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) and pass that information directly to the function.</span></span> <span data-ttu-id="18d64-115">**CreateDC** retourne un contexte de périphérique dans lequel vous pouvez afficher le contenu à imprimer.</span><span class="sxs-lookup"><span data-stu-id="18d64-115">**CreateDC** returns a device context into which you can render the content to print.</span></span>

<span data-ttu-id="18d64-116">L’appel le plus simple pour récupérer un contexte de périphérique (Device Context) est illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="18d64-116">The simplest call to retrieve a device context is shown in the code example that follows.</span></span> <span data-ttu-id="18d64-117">Dans cet exemple, le code récupère un contexte de périphérique (Device Context) sur le périphérique d’affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="18d64-117">The code in this example retrieves a device context to the default display device.</span></span>


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



<span data-ttu-id="18d64-118">Pour effectuer un rendu sur une imprimante spécifique, vous devez spécifier « WINSPOOL » comme périphérique et transmettre le nom correct de l’imprimante à [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span><span class="sxs-lookup"><span data-stu-id="18d64-118">To render to a specific printer, you must specify "WINSPOOL" as the device and pass the correct name of the printer to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="18d64-119">Vous pouvez également passer une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) dans l’appel à **CreateDC** si vous souhaitez fournir des données d’initialisation spécifiques à l’appareil pour le pilote de périphérique lors de la création du contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="18d64-119">You can also pass a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure in the call to **CreateDC** if you want to provide device-specific initialization data for the device driver when you create the device context.</span></span>

<span data-ttu-id="18d64-120">L’exemple suivant montre un appel à [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) dans lequel le pilote « Winspool » est sélectionné et le nom de l’imprimante est spécifié par son nom.</span><span class="sxs-lookup"><span data-stu-id="18d64-120">The following example shows a call to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in which the "WINSPOOL" driver is selected and the printer name is specified by name.</span></span>


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



<span data-ttu-id="18d64-121">Vous pouvez obtenir la chaîne de nom d’imprimante exacte à transmettre à [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) en appelant la fonction [**EnumPrinters**](enumprinters.md) .</span><span class="sxs-lookup"><span data-stu-id="18d64-121">You can obtain the exact printer name string to pass to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) by calling the [**EnumPrinters**](enumprinters.md) function.</span></span> <span data-ttu-id="18d64-122">L’exemple de code suivant montre comment appeler **EnumPrinters** et récupérer les noms des imprimantes locales et connectées localement.</span><span class="sxs-lookup"><span data-stu-id="18d64-122">The following code example shows how to call **EnumPrinters** and get the names of the local and locally connected printers.</span></span> <span data-ttu-id="18d64-123">Étant donné que la taille de la mémoire tampon requise ne peut pas être connue à l’avance, **EnumPrinters** est appelé deux fois.</span><span class="sxs-lookup"><span data-stu-id="18d64-123">Because the size of the required buffer cannot be known in advance, the **EnumPrinters** is called two times.</span></span> <span data-ttu-id="18d64-124">Le premier appel retourne la taille de la mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="18d64-124">The first call returns the size of the required buffer.</span></span> <span data-ttu-id="18d64-125">Ces informations sont utilisées pour allouer une mémoire tampon de la taille requise, et le deuxième appel à **EnumPrinters** retourne les données souhaitées.</span><span class="sxs-lookup"><span data-stu-id="18d64-125">That information is used to allocate a buffer of the required size, and the second call to **EnumPrinters** returns the data that you want.</span></span>


```C++
    fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)NULL,
                0L,
                &dwNeeded,
                &dwReturned);
    
    if (dwNeeded > 0)
    {
        pInfo = (PRINTER_INFO_1 *)HeapAlloc(
                    GetProcessHeap(), 0L, dwNeeded);
    }

    if (NULL != pInfo)
    {
        dwReturned = 0;
        fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)pInfo,
                dwNeeded,
                &dwNeeded,
                &dwReturned);
    }

    if (fnReturn)
    {
        // Review the information from all the printers
        //  returned by EnumPrinters.
        for (i=0; i < dwReturned; i++)
        {
            // pThisInfo[i]->pName contains the printer
            //  name to use in the CreateDC function call.
            //
            // When this desired printer is found in the list of
            //  returned printer, set the printerName value to 
            //  use in the call to CreateDC.

            // printerName = pThisInfo[i]->pName
        }
    }
```



## <a name="display-a-print-common-dialog-box"></a><span data-ttu-id="18d64-126">Afficher une boîte de dialogue d’impression courante</span><span class="sxs-lookup"><span data-stu-id="18d64-126">Display a Print Common Dialog Box</span></span>

<span data-ttu-id="18d64-127">Vous pouvez choisir entre deux boîtes de dialogue d' **impression** communes à afficher à un utilisateur. la boîte de dialogue plus récente, que vous pouvez afficher en appelant la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) et la boîte de dialogue ancien style, que vous pouvez afficher en appelant la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="18d64-127">You can choose from two **Print** common dialog boxes to display to a user; the newer dialog box, which you can display by calling the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, and the older style dialog box, which you can display by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="18d64-128">Les sections suivantes décrivent comment appeler chaque boîte de dialogue à partir d’une application.</span><span class="sxs-lookup"><span data-stu-id="18d64-128">The following sections describe how to call each dialog box from an application.</span></span>

### <a name="using-the-printdlgex-function"></a><span data-ttu-id="18d64-129">Utilisation de la fonction PrintDlgEx</span><span class="sxs-lookup"><span data-stu-id="18d64-129">Using the PrintDlgEx Function</span></span>

<span data-ttu-id="18d64-130">Appelez la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) pour afficher la feuille de propriétés d' **impression** .</span><span class="sxs-lookup"><span data-stu-id="18d64-130">Call the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the **Print** property sheet.</span></span> <span data-ttu-id="18d64-131">À l’aide de la feuille de propriétés, l’utilisateur peut spécifier des informations sur le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="18d64-131">By using the property sheet, the user can specify information about the print job.</span></span> <span data-ttu-id="18d64-132">Par exemple, l’utilisateur peut sélectionner une plage de pages à imprimer, le nombre de copies, etc.</span><span class="sxs-lookup"><span data-stu-id="18d64-132">For example, the user can select a range of pages to print, the number of copies, and so on.</span></span> <span data-ttu-id="18d64-133">Le **PrintDlgEx** peut également récupérer un handle vers un contexte de périphérique pour l’imprimante sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="18d64-133">The **PrintDlgEx** can also retrieve a handle to a device context for the selected printer.</span></span> <span data-ttu-id="18d64-134">Vous pouvez utiliser le descripteur pour afficher la sortie sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="18d64-134">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="18d64-135">Pour obtenir un exemple de code illustrant l’utilisation de [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) pour récupérer un contexte de périphérique d’impression, consultez « Utilisation de la feuille de propriétés d’impression » dans [utilisation des boîtes de dialogue courantes](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="18d64-135">For sample code that illustrates the use of [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) to retrieve a printer device context, see "Using the Print Property Sheet" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

### <a name="using-the-printdlg-function"></a><span data-ttu-id="18d64-136">Utilisation de la fonction PrintDlg</span><span class="sxs-lookup"><span data-stu-id="18d64-136">Using the PrintDlg Function</span></span>

<span data-ttu-id="18d64-137">Si votre application doit s’exécuter sur un système qui ne prend pas en charge la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , par exemple sur un système qui exécute une version de Windows antérieure à Windows 2000, ou qui n’a pas besoin des fonctionnalités supplémentaires fournies par la fonction **PrintDlgEx** , utilisez la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="18d64-137">If your application must run on a system that does not support the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, such as on a system that is running a version of Windows earlier than Windows 2000, or does not need the extra functionality that the **PrintDlgEx** function provides, use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="18d64-138">Les étapes suivantes décrivent comment afficher la boîte de dialogue d' **impression** commune de style plus ancien.</span><span class="sxs-lookup"><span data-stu-id="18d64-138">The following steps describe how to display the older style **Print** common dialog box.</span></span>

1.  <span data-ttu-id="18d64-139">Initialisez la structure de données [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="18d64-139">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>
2.  <span data-ttu-id="18d64-140">Appelez [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) pour afficher la boîte de dialogue d' **impression** commune à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18d64-140">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to display the **Print** common dialog box to the user.</span></span>
3.  <span data-ttu-id="18d64-141">Si l’appel [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retourne la **valeur true**, verrouillez la mémoire de la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retournée.</span><span class="sxs-lookup"><span data-stu-id="18d64-141">If the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) call returns **TRUE**, lock the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure memory.</span></span> <span data-ttu-id="18d64-142">Si l’appel **PrintDlg** retourne la **valeur false**, l’utilisateur a appuyé sur le bouton **Annuler** dans la boîte de dialogue d' **impression** courante afin qu’il n’y ait rien à traiter.</span><span class="sxs-lookup"><span data-stu-id="18d64-142">If the **PrintDlg** call returns **FALSE**, the user pressed the **Cancel** button in the **Print** common dialog box so there is nothing more to process.</span></span>
4.  <span data-ttu-id="18d64-143">Allouez une mémoire tampon de mémoire locale suffisamment grande pour contenir une copie de la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="18d64-143">Allocate a local memory buffer that is large enough to contain a copy of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
5.  <span data-ttu-id="18d64-144">Copiez la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retournée dans le local alloué localement.</span><span class="sxs-lookup"><span data-stu-id="18d64-144">Copy the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to the locally allocated one.</span></span>
6.  <span data-ttu-id="18d64-145">Enregistrez d’autres informations qui sont retournées dans la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) et dont vous aurez besoin pour traiter le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="18d64-145">Save other information that is returned in the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and that you will need to process the print job.</span></span>
7.  <span data-ttu-id="18d64-146">Libérez le [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) et les tampons de mémoire qu’il référence.</span><span class="sxs-lookup"><span data-stu-id="18d64-146">Free the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) and the memory buffers it references.</span></span>

<span data-ttu-id="18d64-147">L’exemple de code suivant illustre l’utilisation de la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) pour récupérer le contexte de périphérique et le nom de l’imprimante sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="18d64-147">The following example code illustrates how to use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to get the device context and the name of selected printer.</span></span>


```C++
// Display the printer dialog box so the user can select the 
//  printer and the number of copies to print.
BOOL            printDlgReturn = FALSE;
HDC                printerDC = NULL;
PRINTDLG        printDlgInfo = {0};
LPWSTR            localPrinterName = NULL;
PDEVMODE        returnedDevmode = NULL;
PDEVMODE        localDevmode = NULL;
int                localNumberOfCopies = 0;

// Initialize the print dialog box's data structure.
printDlgInfo.lStructSize = sizeof( printDlgInfo );
printDlgInfo.Flags = 
    // Return a printer device context.
    PD_RETURNDC 
    // Don't allow separate print to file.
    // Remove these flags if you want to support this feature.
    | PD_HIDEPRINTTOFILE        
    | PD_DISABLEPRINTTOFILE 
    // Don't allow selecting individual document pages to print.
    // Remove this flag if you want to support this feature.
    | PD_NOSELECTION;

// Display the printer dialog and retrieve the printer DC.
printDlgReturn = PrintDlg(&printDlgInfo);

// Check the return value.
if (TRUE == printDlgReturn)
{
    // The user clicked OK so the printer dialog box data 
    //  structure was returned with the user's selections.
    //  Copy the relevant data from the data structure and 
    //  save them to a local data structure.

    //
    // Get the HDC of the selected printer
    printerDC = printDlgInfo.hDC;
    
    // In this example, the DEVMODE structure returned by 
    //    the printer dialog box is copied to a local memory
    //    block and a pointer to the printer name that is 
    //    stored in the copied DEVMODE structure is saved.

    //
    //  Lock the handle to get a pointer to the DEVMODE structure.
    returnedDevmode = (PDEVMODE)GlobalLock(printDlgInfo.hDevMode);

    localDevmode = (LPDEVMODE)HeapAlloc(
                        GetProcessHeap(), 
                        HEAP_ZERO_MEMORY | HEAP_GENERATE_EXCEPTIONS, 
                        returnedDevmode->dmSize);

    if (NULL != localDevmode) 
    {
        memcpy(
            (LPVOID)localDevmode,
            (LPVOID)returnedDevmode, 
            returnedDevmode->dmSize);

        // Save the printer name from the DEVMODE structure.
        //  This is done here just to illustrate how to access
        //  the name field. The printer name can also be accessed
        //  by referring to the dmDeviceName in the local 
        //  copy of the DEVMODE structure.
        localPrinterName = localDevmode->dmDeviceName;

        // Save the number of copies as entered by the user
        localNumberOfCopies = printDlgInfo.nCopies;    
    }
    else
    {
        // Unable to allocate a new structure so leave
        //  the pointer as NULL to indicate that it's empty.
    }

    // Free the DEVMODE structure returned by the print 
    //  dialog box.
    if (NULL != printDlgInfo.hDevMode) 
    {
        GlobalFree(printDlgInfo.hDevMode);
    }
}
else
{
    // The user cancelled out of the print dialog box.
}
```



<span data-ttu-id="18d64-148">Pour plus d’informations sur la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , consultez « Affichage de la boîte de dialogue Imprimer » dans [utilisation des boîtes de dialogue courantes](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="18d64-148">For more information about the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, see "Displaying the Print Dialog Box" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

 

 
