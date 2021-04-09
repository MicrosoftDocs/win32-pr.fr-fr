---
description: Le code suivant montre comment appeler la fonction SymFromName.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Récupération des informations de symbole par nom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f5f4477be4f494383c7d9c1ca462f3beb69690
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110454"
---
# <a name="retrieving-symbol-information-by-name"></a><span data-ttu-id="e6541-103">Récupération des informations de symbole par nom</span><span class="sxs-lookup"><span data-stu-id="e6541-103">Retrieving Symbol Information by Name</span></span>

<span data-ttu-id="e6541-104">Le code suivant montre comment appeler la fonction [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) .</span><span class="sxs-lookup"><span data-stu-id="e6541-104">The following code demonstrates how to call the [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) function.</span></span> <span data-ttu-id="e6541-105">Cette fonction remplit une structure d' [**\_ informations de symbole**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="e6541-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="e6541-106">Étant donné que le nom est de longueur variable, vous devez fournir une mémoire tampon suffisamment grande pour contenir le nom stocké à la fin de la structure des **\_ informations de symbole** .</span><span class="sxs-lookup"><span data-stu-id="e6541-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="e6541-107">En outre, le membre **MaxNameLen** doit être défini sur le nombre d’octets réservés pour le nom.</span><span class="sxs-lookup"><span data-stu-id="e6541-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="e6541-108">Dans cet exemple, szSymbolName est une mémoire tampon qui stocke le nom du symbole demandé.</span><span class="sxs-lookup"><span data-stu-id="e6541-108">In this example, szSymbolName is a buffer that stores the name of the requested symbol.</span></span> <span data-ttu-id="e6541-109">L’exemple suppose que vous avez initialisé le gestionnaire de symboles à l’aide du code dans [initialisation du gestionnaire de symboles](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="e6541-109">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
TCHAR szSymbolName[MAX_SYM_NAME];
ULONG64 buffer[(sizeof(SYMBOL_INFO) +
    MAX_SYM_NAME * sizeof(TCHAR) +
    sizeof(ULONG64) - 1) /
    sizeof(ULONG64)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

_tcscpy_s(szSymbolName, MAX_SYM_NAME, TEXT("WinMain"));
pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromName(hProcess, szSymbolName, pSymbol))
{
    // SymFromName returned success
}
else
{
    // SymFromName failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymFromName returned error : %d\n"), error);
}
```



<span data-ttu-id="e6541-110">Si une application possède un nom de fichier de module ou de source, ainsi que des informations de numéro de ligne, elle peut utiliser [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) pour récupérer une adresse de code virtuel.</span><span class="sxs-lookup"><span data-stu-id="e6541-110">If an application has a module or source file name as well as line number information, it can use [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) to retrieve a virtual code address.</span></span> <span data-ttu-id="e6541-111">Cette fonction requiert un pointeur vers une structure [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) pour recevoir l’adresse de code virtuel.</span><span class="sxs-lookup"><span data-stu-id="e6541-111">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the virtual code address.</span></span> <span data-ttu-id="e6541-112">Notez que le gestionnaire de symboles peut récupérer des informations sur les numéros de ligne uniquement lorsque \_ \_ l’option SYMOPT Load Lines est définie à l’aide de la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="e6541-112">Note that the symbol handler can retrieve line number information only when SYMOPT\_LOAD\_LINES option is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="e6541-113">Cette option doit être définie avant le chargement du module.</span><span class="sxs-lookup"><span data-stu-id="e6541-113">This option must be set before loading the module.</span></span> <span data-ttu-id="e6541-114">Le paramètre szModuleName contient le nom du module source ; Il est facultatif et peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e6541-114">The szModuleName parameter contains the source module name; it is optional and can be **NULL**.</span></span> <span data-ttu-id="e6541-115">Le paramètre szFileName doit contenir le nom du fichier source, tandis que le paramètre dwLineNumber doit contenir le numéro de ligne pour lequel l’adresse virtuelle sera récupérée.</span><span class="sxs-lookup"><span data-stu-id="e6541-115">The szFileName parameter should contain the source file name, and dwLineNumber parameter should contain the line number for which the virtual address will be retrieved.</span></span>


```C++
TCHAR  szModuleName[MAX_PATH];
TCHAR  szFileName[MAX_PATH];
DWORD  dwLineNumber;
LONG   lDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
_tcscpy_s(szModuleName, MAX_PATH, TEXT("MyApp"));
_tcscpy_s(szFileName, MAX_PATH, TEXT("main.c"));
dwLineNumber = 248;

if (SymGetLineFromName64(hProcess, szModuleName, szFileName,
    dwLineNumber, &lDisplacement, &line))
{
    // SymGetLineFromName64 returned success
}
else
{
    // SymGetLineFromName64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromName64 returned error : %d\n"), error);
}
```



 

 



