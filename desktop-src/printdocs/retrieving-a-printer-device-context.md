---
description: Cette rubrique explique comment récupérer un contexte de périphérique d’impression.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: 'Comment : récupérer un contexte de périphérique d’impression'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f723ece0e00d58ed684029e0eb3202d637443bd7f0e9d8878024346b9d79ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600559"
---
# <a name="how-to-retrieve-a-printer-device-context"></a>Comment : récupérer un contexte de périphérique d’impression

Cette rubrique explique comment récupérer un contexte de périphérique d’impression. Vous pouvez récupérer un contexte de périphérique d’impression en appelant la fonction [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) directement, ou elle peut être retournée par une boîte de dialogue d' **impression** commune.

Lorsque vous affichez une boîte de dialogue d' **impression** courante, un utilisateur peut sélectionner l’imprimante, les pages du document et le nombre de copies de documents qu’il souhaite imprimer. La boîte de dialogue d' **impression** commune retourne ces sélections dans une structure de données.

Cette rubrique explique comment obtenir un contexte de périphérique d’impression à l’aide des méthodes suivantes.

-   [Appeler CreateDC](#call-createdc)
-   [Afficher une boîte de dialogue d’impression courante](#display-a-print-common-dialog-box)
    -   [Utilisation de la fonction PrintDlgEx](#using-the-printdlgex-function)
    -   [Utilisation de la fonction PrintDlg](#using-the-printdlg-function)

## <a name="call-createdc"></a>Appeler CreateDC

Si vous connaissez l’appareil sur lequel vous souhaitez imprimer, vous pouvez appeler [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) et transmettre ces informations directement à la fonction. **CreateDC** retourne un contexte de périphérique dans lequel vous pouvez afficher le contenu à imprimer.

L’appel le plus simple pour récupérer un contexte de périphérique (Device Context) est illustré dans l’exemple de code suivant. Dans cet exemple, le code récupère un contexte de périphérique (Device Context) sur le périphérique d’affichage par défaut.


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



Pour effectuer un rendu sur une imprimante spécifique, vous devez spécifier « WINSPOOL » comme périphérique et transmettre le nom correct de l’imprimante à [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca). Vous pouvez également passer une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) dans l’appel à **CreateDC** si vous souhaitez fournir des données d’initialisation spécifiques à l’appareil pour le pilote de périphérique lors de la création du contexte de périphérique.

L’exemple suivant montre un appel à [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) dans lequel le pilote « Winspool » est sélectionné et le nom de l’imprimante est spécifié par son nom.


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



Vous pouvez obtenir la chaîne de nom d’imprimante exacte à transmettre à [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) en appelant la fonction [**EnumPrinters**](enumprinters.md) . L’exemple de code suivant montre comment appeler **EnumPrinters** et récupérer les noms des imprimantes locales et connectées localement. Étant donné que la taille de la mémoire tampon requise ne peut pas être connue à l’avance, **EnumPrinters** est appelé deux fois. Le premier appel retourne la taille de la mémoire tampon requise. Ces informations sont utilisées pour allouer une mémoire tampon de la taille requise, et le deuxième appel à **EnumPrinters** retourne les données souhaitées.


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



## <a name="display-a-print-common-dialog-box"></a>Afficher une boîte de dialogue d’impression courante

Vous pouvez choisir entre deux boîtes de dialogue d' **impression** communes à afficher à un utilisateur. la boîte de dialogue plus récente, que vous pouvez afficher en appelant la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) et la boîte de dialogue ancien style, que vous pouvez afficher en appelant la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Les sections suivantes décrivent comment appeler chaque boîte de dialogue à partir d’une application.

### <a name="using-the-printdlgex-function"></a>Utilisation de la fonction PrintDlgEx

Appelez la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) pour afficher la feuille de propriétés d' **impression** . À l’aide de la feuille de propriétés, l’utilisateur peut spécifier des informations sur le travail d’impression. Par exemple, l’utilisateur peut sélectionner une plage de pages à imprimer, le nombre de copies, etc. Le **PrintDlgEx** peut également récupérer un handle vers un contexte de périphérique pour l’imprimante sélectionnée. Vous pouvez utiliser le descripteur pour afficher la sortie sur l’imprimante.

Pour obtenir un exemple de code illustrant l’utilisation de [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) pour récupérer un contexte de périphérique d’impression, consultez « Utilisation de la feuille de propriétés d’impression » dans [utilisation des boîtes de dialogue courantes](../dlgbox/using-common-dialog-boxes.md).

### <a name="using-the-printdlg-function"></a>Utilisation de la fonction PrintDlg

si votre application doit s’exécuter sur un système qui ne prend pas en charge la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , par exemple sur un système qui exécute une version de Windows antérieure à Windows 2000, ou qui n’a pas besoin des fonctionnalités supplémentaires fournies par la fonction **PrintDlgEx** , utilisez la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Les étapes suivantes décrivent comment afficher la boîte de dialogue d' **impression** commune de style plus ancien.

1.  Initialisez la structure de données [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .
2.  Appelez [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) pour afficher la boîte de dialogue d' **impression** commune à l’utilisateur.
3.  Si l’appel [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retourne la **valeur true**, verrouillez la mémoire de la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retournée. Si l’appel **PrintDlg** retourne la **valeur false**, l’utilisateur a appuyé sur le bouton **Annuler** dans la boîte de dialogue d' **impression** courante afin qu’il n’y ait rien à traiter.
4.  Allouez une mémoire tampon de mémoire locale suffisamment grande pour contenir une copie de la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .
5.  Copiez la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retournée dans le local alloué localement.
6.  Enregistrez d’autres informations qui sont retournées dans la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) et dont vous aurez besoin pour traiter le travail d’impression.
7.  Libérez le [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) et les tampons de mémoire qu’il référence.

L’exemple de code suivant illustre l’utilisation de la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) pour récupérer le contexte de périphérique et le nom de l’imprimante sélectionnée.


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



Pour plus d’informations sur la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , consultez « Affichage de la boîte de dialogue Imprimer » dans [utilisation des boîtes de dialogue courantes](../dlgbox/using-common-dialog-boxes.md).

 

 
