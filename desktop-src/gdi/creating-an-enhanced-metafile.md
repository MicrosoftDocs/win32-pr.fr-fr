---
description: Cette section contient un exemple qui illustre la création d’un métafichier amélioré stocké sur un disque, à l’aide d’un nom de fichier spécifié par l’utilisateur.
ms.assetid: 084b2737-eb55-4587-b8e8-3eb3fa3688c4
title: Création d’un métafichier amélioré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4877481ed0a68d6379e7eaabb00bbe37cef74c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528384"
---
# <a name="creating-an-enhanced-metafile"></a><span data-ttu-id="7b6fe-103">Création d’un métafichier amélioré</span><span class="sxs-lookup"><span data-stu-id="7b6fe-103">Creating an Enhanced Metafile</span></span>

<span data-ttu-id="7b6fe-104">Cette section contient un exemple qui illustre la création d’un métafichier amélioré stocké sur un disque, à l’aide d’un nom de fichier spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b6fe-104">This section contains an example that demonstrates the creation of an enhanced metafile that is stored on a disk, using a file name specified by the user.</span></span>

<span data-ttu-id="7b6fe-105">L’exemple utilise un contexte de périphérique pour la fenêtre d’application comme contexte de périphérique de référence.</span><span class="sxs-lookup"><span data-stu-id="7b6fe-105">The example uses a device context for the application window as the reference device context.</span></span> <span data-ttu-id="7b6fe-106">(Le système stocke les données de résolution de cet appareil dans l’en-tête du métafichier amélioré.) L’application récupère un handle identifiant ce contexte de périphérique en appelant la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .</span><span class="sxs-lookup"><span data-stu-id="7b6fe-106">(The system stores the resolution data for this device in the enhanced-metafile's header.) The application retrieves a handle identifying this device context by calling the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="7b6fe-107">L’exemple utilise les dimensions de la zone cliente de l’application pour définir les dimensions du cadre de l’image.</span><span class="sxs-lookup"><span data-stu-id="7b6fe-107">The example uses the dimensions of the application's client area to define the dimensions of the picture frame.</span></span> <span data-ttu-id="7b6fe-108">À l’aide des dimensions de rectangle retournées par la fonction [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) , l’application convertit les unités de périphérique en unités 0,01-millimètres et transmet les valeurs converties à la fonction [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .</span><span class="sxs-lookup"><span data-stu-id="7b6fe-108">Using the rectangle dimensions returned by the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function, the application converts the device units to .01-millimeter units and passes the converted values to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="7b6fe-109">L’exemple affiche une boîte de dialogue **Enregistrer sous** courante qui permet à l’utilisateur de spécifier le nom de fichier du nouveau métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="7b6fe-109">The example displays a **Save As** common dialog box that enables the user to specify the file name of the new enhanced metafile.</span></span> <span data-ttu-id="7b6fe-110">Le système ajoute l’extension. EMF à trois caractères à ce nom de fichier et transmet le nom à la fonction [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .</span><span class="sxs-lookup"><span data-stu-id="7b6fe-110">The system appends the three-character .emf extension to this file name and passes the name to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="7b6fe-111">L’exemple incorpore également une description textuelle de l’image dans l’en-tête de métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="7b6fe-111">The example also embeds a text description of the picture in the enhanced-metafile header.</span></span> <span data-ttu-id="7b6fe-112">Cette description est spécifiée en tant que ressource dans la table de chaînes du fichier de ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b6fe-112">This description is specified as a resource in the string table of the application's resource file.</span></span> <span data-ttu-id="7b6fe-113">Toutefois, dans une application active, cette chaîne est récupérée à partir d’un contrôle personnalisé dans une boîte de dialogue commune ou dans une boîte de dialogue distincte affichée uniquement à cet effet.</span><span class="sxs-lookup"><span data-stu-id="7b6fe-113">However, in a working application, this string would be retrieved from a custom control in a common dialog box or from a separate dialog box displayed solely for this purpose.</span></span>


```C++
// Obtain a handle to a reference device context.  
 
hdcRef = GetDC(hWnd); 
 
// Determine the picture frame dimensions.  
// iWidthMM is the display width in millimeters.  
// iHeightMM is the display height in millimeters.  
// iWidthPels is the display width in pixels.  
// iHeightPels is the display height in pixels  
 
iWidthMM = GetDeviceCaps(hdcRef, HORZSIZE); 
iHeightMM = GetDeviceCaps(hdcRef, VERTSIZE); 
iWidthPels = GetDeviceCaps(hdcRef, HORZRES); 
iHeightPels = GetDeviceCaps(hdcRef, VERTRES); 
 
// Retrieve the coordinates of the client  
// rectangle, in pixels.  
 
GetClientRect(hWnd, &rect); 
 
// Convert client coordinates to .01-mm units.  
// Use iWidthMM, iWidthPels, iHeightMM, and  
// iHeightPels to determine the number of  
// .01-millimeter units per pixel in the x-  
//  and y-directions.  
 
rect.left = (rect.left * iWidthMM * 100)/iWidthPels; 
rect.top = (rect.top * iHeightMM * 100)/iHeightPels; 
rect.right = (rect.right * iWidthMM * 100)/iWidthPels; 
rect.bottom = (rect.bottom * iHeightMM * 100)/iHeightPels; 
 
// Load the filename filter from the string table.  
 
LoadString(hInst, IDS_FILTERSTRING, 
     (LPSTR)szFilter, sizeof(szFilter)); 
 
// Replace the '%' separators that are embedded  
// between the strings in the string-table entry  
// with '\0'.  
 
for (i=0; szFilter[i]!='\0'; i++) 
    if (szFilter[i] == '%') 
            szFilter[i] = '\0'; 
 
// Load the dialog title string from the table.  
 
LoadString(hInst, IDS_TITLESTRING, 
     (LPSTR)szTitle, sizeof(szTitle)); 
 
// Initialize the OPENFILENAME members.  
 
szFile[0] = '\0'; 
 
Ofn.lStructSize = sizeof(OPENFILENAME); 
Ofn.hwndOwner = hWnd; 
Ofn.lpstrFilter = szFilter; 
Ofn.lpstrFile= szFile; 
Ofn.nMaxFile = sizeof(szFile)/ sizeof(*szFile); 
Ofn.lpstrFileTitle = szFileTitle; 
Ofn.nMaxFileTitle = sizeof(szFileTitle); 
Ofn.lpstrInitialDir = (LPSTR)NULL; 
Ofn.Flags = OFN_SHOWHELP | OFN_OVERWRITEPROMPT; 
Ofn.lpstrTitle = szTitle; 
 
// Display the Filename common dialog box. The  
// filename specified by the user is passed  
// to the CreateEnhMetaFile function and used to  
// store the metafile on disk.  
 
GetSaveFileName(&Ofn); 
 
// Load the description from the string table.  
 
LoadString(hInst, IDS_DESCRIPTIONSTRING, 
     (LPSTR)szDescription, sizeof(szDescription)); 
 
// Replace the '%' string separators that are  
// embedded between strings in the string-table  
// entry with '\0'.  
 
for (i=0; szDescription[i]!='\0'; i++) 
{
    if (szDescription[i] == '%') 
            szDescription[i] = '\0'; 
}
 
// Create the metafile device context.  
 
hdcMeta = CreateEnhMetaFile(hdcRef, 
          (LPTSTR) Ofn.lpstrFile, 
          &rect, (LPSTR)szDescription); 
 
if (!hdcMeta) 
    errhandler("CreateEnhMetaFile", hWnd); 
 
// Release the reference device context.  
 
ReleaseDC(hWnd, hdcRef); 
```



 

 
