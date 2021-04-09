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
# <a name="retrieving-symbol-information-by-address"></a>Récupération des informations de symbole par adresse

Le code suivant montre comment appeler la fonction [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Cette fonction remplit une structure d' [**\_ informations de symbole**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Étant donné que le nom est de longueur variable, vous devez fournir une mémoire tampon suffisamment grande pour contenir le nom stocké à la fin de la structure des **\_ informations de symbole** . En outre, le membre **MaxNameLen** doit être défini sur le nombre d’octets réservés pour le nom. Dans cet exemple, *dwAddress* est l’adresse à mapper à un symbole. La fonction **SymFromAddr** stocke un offset au début du symbole à l’adresse dans *dwDisplacement*. L’exemple suppose que vous avez initialisé le gestionnaire de symboles à l’aide du code dans [initialisation du gestionnaire de symboles](initializing-the-symbol-handler.md).


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



Pour récupérer le numéro de la ligne de code source pour une adresse spécifiée, une application peut utiliser [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr). Cette fonction requiert un pointeur vers une structure [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) pour recevoir le nom du fichier source et le numéro de ligne correspondant à une adresse de code spécifiée. Notez que le gestionnaire de symboles peut récupérer des informations sur les numéros de ligne uniquement lorsque les **\_ \_ lignes de charge SYMOPT** sont définies à l’aide de la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Cette option doit être définie avant le chargement du module. Le paramètre dwAddress contient l’adresse de code pour laquelle le nom du fichier source et le numéro de ligne se trouvent.


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



 

 



