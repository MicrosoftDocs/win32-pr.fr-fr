---
description: L’API Shell fournit des fonctions que vous pouvez utiliser pour gérer des imprimantes en réseau. Si le verbe Print est associé à un fichier, vous pouvez utiliser la commande ShellExecuteEx pour l’imprimer.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Gestion des imprimantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226804"
---
# <a name="managing-printers"></a>Gestion des imprimantes

L’API Shell fournit des fonctions que vous pouvez utiliser pour gérer des imprimantes en réseau. Si le verbe **Print** est associé à un fichier, vous pouvez utiliser la commande [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour l’imprimer.

-   [Gestion des imprimantes](#printer-management)
-   [Impression de fichiers avec ShellExecuteEx](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>Gestion des imprimantes

Vous pouvez gérer les imprimantes sur un système à l’aide de la fonction [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) . Cette fonction vous permet d’effectuer les opérations suivantes :

-   Installez les imprimantes.
-   Ouvrez imprimantes.
-   Obtient les propriétés de l’imprimante.
-   Créer des liens d’imprimante.
-   Imprimez une page de test.

## <a name="printing-files-with-shellexecuteex"></a>Impression de fichiers avec ShellExecuteEx

Si un type de fichier est associé à une commande d’impression, vous pouvez imprimer le fichier en appelant [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) avec **Print** comme verbe. Cette commande est souvent la même que celle utilisée pour le verbe **Open** , avec l’ajout d’un indicateur pour indiquer à l’application d’imprimer le fichier. Par exemple, .txt fichiers peuvent être imprimés par Microsoft WordPad. Le verbe **Open** d’un fichier .txt correspond donc à une commande semblable à la suivante :


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



Quand vous utilisez [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour imprimer un fichier .txt, WordPad ouvre le fichier, l’imprime, puis ferme le contrôle à l’application. L’exemple de fonction suivant prend un chemin d’accès complet et utilise **ShellExecuteEx** pour l’imprimer, à l’aide de la commande Imprimer associée à son extension de nom de fichier.


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



