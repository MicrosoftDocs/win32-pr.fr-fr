---
description: Le code suivant montre comment initialiser le gestionnaire de symboles.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Initialisation du gestionnaire de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950441"
---
# <a name="initializing-the-symbol-handler"></a>Initialisation du gestionnaire de symboles

Le code suivant montre comment initialiser le gestionnaire de symboles. La fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) diffère le chargement de symboles jusqu’à ce que les informations de symbole soient demandées. Le code charge les symboles pour chaque module dans le processus spécifié en passant la valeur **true** pour le paramètre *bInvade* de la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . (Cette fonction appelle la fonction [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) pour chaque module que le processus a mappé dans son espace d’adressage.)

Si le processus spécifié n’est pas le processus qui a appelé [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), le code passe un identificateur de processus comme premier paramètre de **syminitialize**.

La spécification de **null** comme deuxième paramètre de [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indique que le gestionnaire de symboles doit utiliser le chemin de recherche par défaut pour localiser les fichiers de symboles. Pour plus d’informations sur la façon dont le gestionnaire de symboles localise les fichiers de symboles ou sur la façon dont une application peut spécifier un chemin de recherche de symboles, consultez [chemins d'](symbol-paths.md)accès aux symboles.


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



