---
title: Utilisation des flux
description: Vous pouvez utiliser des flux pour transférer des données vers ou à partir d’un contrôle RichEdit. Un flux est défini par une structure EDITSTREAM, qui spécifie une mémoire tampon et une fonction de rappel définie par l’application.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104101384"
---
# <a name="how-to-use-streams"></a><span data-ttu-id="5656a-104">Utilisation des flux</span><span class="sxs-lookup"><span data-stu-id="5656a-104">How to Use Streams</span></span>

<span data-ttu-id="5656a-105">Vous pouvez utiliser des flux pour transférer des données vers ou à partir d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="5656a-105">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="5656a-106">Un flux est défini par une structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) , qui spécifie une mémoire tampon et une fonction de rappel définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="5656a-106">A stream is defined by an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure, which specifies a buffer and an application-defined callback function.</span></span>

<span data-ttu-id="5656a-107">Pour lire des données dans un contrôle Rich Edit (autrement dit, un flux de données), utilisez le message de [**\_ flux em**](em-streamin.md) .</span><span class="sxs-lookup"><span data-stu-id="5656a-107">To read data into a rich edit control (that is, stream in the data), use the [**EM\_STREAMIN**](em-streamin.md) message.</span></span> <span data-ttu-id="5656a-108">Le contrôle appelle à plusieurs reprises la fonction de rappel de l’application, qui transfère à chaque fois une partie des données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5656a-108">The control repeatedly calls the application's callback function, which transfers a portion of the data into the buffer each time.</span></span>

<span data-ttu-id="5656a-109">Pour enregistrer le contenu d’un contrôle RichEdit (autrement dit, diffuser en continu les données), vous pouvez utiliser le message [**em \_ STREAMOUT**](em-streamout.md) .</span><span class="sxs-lookup"><span data-stu-id="5656a-109">To save the contents of a rich edit control (that is, stream out the data), you can use the [**EM\_STREAMOUT**](em-streamout.md) message.</span></span> <span data-ttu-id="5656a-110">Le contrôle écrit à plusieurs reprises dans la mémoire tampon, puis appelle la fonction de rappel de l’application.</span><span class="sxs-lookup"><span data-stu-id="5656a-110">The control repeatedly writes to the buffer and then calls the application's callback function.</span></span> <span data-ttu-id="5656a-111">Pour chaque appel, la fonction de rappel enregistre le contenu de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5656a-111">For each call, the callback function saves the contents of the buffer.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5656a-112">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="5656a-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5656a-113">Technologies</span><span class="sxs-lookup"><span data-stu-id="5656a-113">Technologies</span></span>

-   [<span data-ttu-id="5656a-114">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="5656a-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5656a-115">Prérequis</span><span class="sxs-lookup"><span data-stu-id="5656a-115">Prerequisites</span></span>

-   <span data-ttu-id="5656a-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="5656a-116">C/C++</span></span>
-   <span data-ttu-id="5656a-117">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="5656a-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5656a-118">Instructions</span><span class="sxs-lookup"><span data-stu-id="5656a-118">Instructions</span></span>

### <a name="use-a-stream"></a><span data-ttu-id="5656a-119">Utiliser un flux</span><span class="sxs-lookup"><span data-stu-id="5656a-119">Use a Stream</span></span>

<span data-ttu-id="5656a-120">L’exemple de code suivant montre comment lire un fichier. rtf dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="5656a-120">The following code example shows how to read an .rtf file into a rich edit control.</span></span> <span data-ttu-id="5656a-121">Le descripteur de fichier est passé à la fonction de rappel via le membre **dwCookie** de la structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="5656a-121">The file handle is passed to the callback function through the **dwCookie** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span>


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="5656a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5656a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5656a-123">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="5656a-123">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="5656a-124">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="5656a-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




