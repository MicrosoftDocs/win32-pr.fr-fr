---
description: Si une application n’appelle pas la fonction SymInitialize avec le paramètre fInvadeProcess défini sur TRUE, elle doit charger les symboles pour un module lorsqu’ils sont requis.
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: Chargement d’un module de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110150"
---
# <a name="loading-a-symbol-module"></a>Chargement d’un module de symboles

Si une application n’appelle pas la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) avec le paramètre *FInvadeProcess* défini sur **true**, elle doit charger les symboles pour un module lorsqu’ils sont requis. Pour charger un module de symboles à la demande, l’application peut appeler la fonction [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) avec un chemin d’accès complet à un nom de module. Une fois le module chargé, le gestionnaire de symboles charge les symboles immédiatement ou diffère le chargement, selon les options définies à l’aide de la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .

Le code suivant charge un module de symboles. Notez qu’il suppose que vous avez initialisé le gestionnaire de symboles à l’aide du code dans [initialisation du gestionnaire de symboles](initializing-the-symbol-handler.md).


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



Notez que *szImageName* peut être un chemin d’accès à n’importe quel module exécutable contenant des informations de débogage (. exe,. dll,. drv,. sys,. scr,. cpl,. com). En outre, *dwBaseAddr* est l’adresse de base du module de symboles à charger. Si cette valeur est égale à 0, le gestionnaire de symboles obtient l’adresse de base à partir du module de symboles spécifié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déchargement d’un module de symboles](unloading-a-symbol-module.md)
</dt> </dl>

 

 



