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
# <a name="retrieving-symbol-information-by-name"></a>Récupération des informations de symbole par nom

Le code suivant montre comment appeler la fonction [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Cette fonction remplit une structure d' [**\_ informations de symbole**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Étant donné que le nom est de longueur variable, vous devez fournir une mémoire tampon suffisamment grande pour contenir le nom stocké à la fin de la structure des **\_ informations de symbole** . En outre, le membre **MaxNameLen** doit être défini sur le nombre d’octets réservés pour le nom. Dans cet exemple, szSymbolName est une mémoire tampon qui stocke le nom du symbole demandé. L’exemple suppose que vous avez initialisé le gestionnaire de symboles à l’aide du code dans [initialisation du gestionnaire de symboles](initializing-the-symbol-handler.md).


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



Si une application possède un nom de fichier de module ou de source, ainsi que des informations de numéro de ligne, elle peut utiliser [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) pour récupérer une adresse de code virtuel. Cette fonction requiert un pointeur vers une structure [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) pour recevoir l’adresse de code virtuel. Notez que le gestionnaire de symboles peut récupérer des informations sur les numéros de ligne uniquement lorsque \_ \_ l’option SYMOPT Load Lines est définie à l’aide de la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Cette option doit être définie avant le chargement du module. Le paramètre szModuleName contient le nom du module source ; Il est facultatif et peut avoir la **valeur null**. Le paramètre szFileName doit contenir le nom du fichier source, tandis que le paramètre dwLineNumber doit contenir le numéro de ligne pour lequel l’adresse virtuelle sera récupérée.


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



 

 



