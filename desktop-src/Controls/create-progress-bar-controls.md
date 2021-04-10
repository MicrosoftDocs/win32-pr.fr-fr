---
title: Comment utiliser les contrôles de barre de progression
description: Cette rubrique explique comment utiliser une barre de progression pour indiquer la progression d’une opération longue d’analyse de fichiers.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c71ff33a14f2d2af5fa8735c5197c50acaa948b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941417"
---
# <a name="how-to-use-progress-bar-controls"></a><span data-ttu-id="566f8-103">Comment utiliser les contrôles de barre de progression</span><span class="sxs-lookup"><span data-stu-id="566f8-103">How to Use Progress Bar Controls</span></span>

<span data-ttu-id="566f8-104">Cette rubrique explique comment utiliser une barre de progression pour indiquer la progression d’une opération longue d’analyse de fichiers.</span><span class="sxs-lookup"><span data-stu-id="566f8-104">This topic explains how to use a progress bar to indicate the progress of a lengthy file-parsing operation.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="566f8-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="566f8-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="566f8-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="566f8-106">Technologies</span></span>

-   [<span data-ttu-id="566f8-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="566f8-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="566f8-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="566f8-108">Prerequisites</span></span>

-   <span data-ttu-id="566f8-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="566f8-109">C/C++</span></span>
-   <span data-ttu-id="566f8-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="566f8-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="566f8-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="566f8-111">Instructions</span></span>

### <a name="create-a-progress-bar-control"></a><span data-ttu-id="566f8-112">Créer un contrôle de barre de progression</span><span class="sxs-lookup"><span data-stu-id="566f8-112">Create a Progress Bar Control</span></span>

<span data-ttu-id="566f8-113">L’exemple de code suivant crée une barre de progression et la positionne le long de la partie inférieure de la zone cliente de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="566f8-113">The following example code creates a progress bar and positions it along the bottom of the parent window's client area.</span></span> <span data-ttu-id="566f8-114">La hauteur de la barre de progression est basée sur la hauteur de la bitmap de direction utilisée dans une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="566f8-114">The height of the progress bar is based on the height of the arrow bitmap used in a scroll bar.</span></span> <span data-ttu-id="566f8-115">La plage est basée sur la taille du fichier divisée par 2 048, qui correspond à la taille de chaque « segment » des données lues à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="566f8-115">The range is based on the size of the file divided by 2,048, which is the size of each "chunk" of data that is read from the file.</span></span> <span data-ttu-id="566f8-116">L’exemple définit également un incrément et avance la position actuelle de la barre de progression par incrément après l’analyse de chaque segment.</span><span class="sxs-lookup"><span data-stu-id="566f8-116">The example also sets an increment and advances the current position of the progress bar by the increment after parsing each chunk.</span></span>


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a><span data-ttu-id="566f8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="566f8-117">Remarks</span></span>

<span data-ttu-id="566f8-118">Vous devez veiller à utiliser la fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) correctement pour garantir la sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="566f8-118">You must make sure to use the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function correctly, to ensure the security of your application.</span></span> <span data-ttu-id="566f8-119">Par exemple, dans l’exemple de code, vous devez vérifier que `ReadFile` lit réellement toutes les données demandées.</span><span class="sxs-lookup"><span data-stu-id="566f8-119">For instance, in the example code, you should check to make sure that `ReadFile` actually reads all of the requested data.</span></span>

<span data-ttu-id="566f8-120">Notez également que le quatrième paramètre de [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)(( \_ attributs LPSECURITY)**null**) définit les valeurs de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="566f8-120">Also notice that the fourth parameter of [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)—(LPSECURITY\_ATTRIBUTES)**NULL**—sets default security values.</span></span> <span data-ttu-id="566f8-121">Si vous avez besoin de paramètres de sécurité spécifiques, vous devez définir les valeurs appropriées dans les membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="566f8-121">If you need specific security settings, you must set the appropriate values in the structure's members.</span></span> <span data-ttu-id="566f8-122">Appelez **sizeof** pour définir la taille correcte de la structure d' **\_ attributs LPSECURITY** .</span><span class="sxs-lookup"><span data-stu-id="566f8-122">Call **sizeof** to set the correct size of the **LPSECURITY\_ATTRIBUTES** structure.</span></span>

<span data-ttu-id="566f8-123">Pour plus d’informations, consultez [Considérations sur la sécurité : contrôles Microsoft Windows](sec-comctls.md).</span><span class="sxs-lookup"><span data-stu-id="566f8-123">For more information, see [Security Considerations: Microsoft Windows Controls](sec-comctls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="566f8-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="566f8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="566f8-125">Utilisation des contrôles de barre de progression</span><span class="sxs-lookup"><span data-stu-id="566f8-125">Using Progress Bar Controls</span></span>](using-progress-bar-controls.md)
</dt> <dt>

[<span data-ttu-id="566f8-126">Considérations relatives à la sécurité : contrôles Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="566f8-126">Security Considerations: Microsoft Windows Controls</span></span>](sec-comctls.md)
</dt> </dl>

 

 