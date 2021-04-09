---
description: Le code suivant montre comment appeler la fonction SymFromAddr.
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: Récupération des informations de symbole par adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ad9d2879dbfd5820c4aa6c2e7563a1575ebe1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110455"
---
# <a name="retrieving-symbol-information-by-address"></a><span data-ttu-id="2b36d-103">Récupération des informations de symbole par adresse</span><span class="sxs-lookup"><span data-stu-id="2b36d-103">Retrieving Symbol Information by Address</span></span>

<span data-ttu-id="2b36d-104">Le code suivant montre comment appeler la fonction [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) .</span><span class="sxs-lookup"><span data-stu-id="2b36d-104">The following code demonstrates how to call the [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) function.</span></span> <span data-ttu-id="2b36d-105">Cette fonction remplit une structure d' [**\_ informations de symbole**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="2b36d-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="2b36d-106">Étant donné que le nom est de longueur variable, vous devez fournir une mémoire tampon suffisamment grande pour contenir le nom stocké à la fin de la structure des **\_ informations de symbole** .</span><span class="sxs-lookup"><span data-stu-id="2b36d-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="2b36d-107">En outre, le membre **MaxNameLen** doit être défini sur le nombre d’octets réservés pour le nom.</span><span class="sxs-lookup"><span data-stu-id="2b36d-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="2b36d-108">Dans cet exemple, *dwAddress* est l’adresse à mapper à un symbole.</span><span class="sxs-lookup"><span data-stu-id="2b36d-108">In this example, *dwAddress* is the address to be mapped to a symbol.</span></span> <span data-ttu-id="2b36d-109">La fonction **SymFromAddr** stocke un offset au début du symbole à l’adresse dans *dwDisplacement*.</span><span class="sxs-lookup"><span data-stu-id="2b36d-109">The **SymFromAddr** function will store an offset to the beginning of the symbol to the address in *dwDisplacement*.</span></span> <span data-ttu-id="2b36d-110">L’exemple suppose que vous avez initialisé le gestionnaire de symboles à l’aide du code dans [initialisation du gestionnaire de symboles](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="2b36d-110">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
DWORD64  dwDisplacement = 0;
DWORD64  dwAddress = SOME_ADDRESS;

char buffer[sizeof(SYMBOL_INFO) + MAX_SYM_NAME * sizeof(TCHAR)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromAddr(hProcess, dwAddress, &dwDisplacement, pSymbol))
{
    // SymFromAddr returned success
}
else
{
    // SymFromAddr failed
    DWORD error = GetLastError();
    printf("SymFromAddr returned error : %d\n", error);
}
```



<span data-ttu-id="2b36d-111">Pour récupérer le numéro de la ligne de code source pour une adresse spécifiée, une application peut utiliser [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span><span class="sxs-lookup"><span data-stu-id="2b36d-111">To retrieve the source code line number for a specified address, an application can use [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span></span> <span data-ttu-id="2b36d-112">Cette fonction requiert un pointeur vers une structure [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) pour recevoir le nom du fichier source et le numéro de ligne correspondant à une adresse de code spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b36d-112">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the source file name and line number corresponding to a specified code address.</span></span> <span data-ttu-id="2b36d-113">Notez que le gestionnaire de symboles peut récupérer des informations sur les numéros de ligne uniquement lorsque les **\_ \_ lignes de charge SYMOPT** sont définies à l’aide de la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="2b36d-113">Note that the symbol handler can retrieve line number information only when **SYMOPT\_LOAD\_LINES** is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="2b36d-114">Cette option doit être définie avant le chargement du module.</span><span class="sxs-lookup"><span data-stu-id="2b36d-114">This option must be set before loading the module.</span></span> <span data-ttu-id="2b36d-115">Le paramètre dwAddress contient l’adresse de code pour laquelle le nom du fichier source et le numéro de ligne se trouvent.</span><span class="sxs-lookup"><span data-stu-id="2b36d-115">The dwAddress parameter contains the code address for which the source file name and line number will be located.</span></span>


```C++
DWORD64  dwAddress;
DWORD  dwDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
dwAddress = 0x1000000; // Address you want to check on.

if (SymGetLineFromAddr64(hProcess, dwAddress, &dwDisplacement, &line))
{
    // SymGetLineFromAddr64 returned success
}
else
{
    // SymGetLineFromAddr64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromAddr64 returned error : %d\n"), error);
}
```



 

 



