---
description: Un chemin d’accès à un objet de classe décrit l’emplacement d’une classe dans un espace de noms.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Description d’un chemin d’accès d’objet de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6801d91c4236a7892d7db121dc02c73d93640b7dbc4969c86db55a8789b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244399"
---
# <a name="describing-a-class-object-path"></a>Description d’un chemin d’accès d’objet de classe

Un chemin d’accès à un objet de classe décrit l’emplacement d’une classe dans un espace de noms.

Vous pouvez utiliser les méthodes suivantes pour spécifier un chemin d’accès à un objet :

-   Un chemin d’accès d’objet complet à une classe ajoute le nom de la classe à un chemin d’accès d’espace de noms.

    L’exemple suivant montre l’emplacement de la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans \\ l' \\ espace de noms CIMV2 racine sur le serveur nommé Admin.

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   Un chemin d’accès d’objet relatif représente une classe qui réside dans l’espace de noms actuel. Un chemin d’accès d’objet relatif à une classe contient uniquement le nom de la classe.

    L’exemple suivant montre le chemin d’accès relatif à la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

    ``` syntax
    Win32_LogicalDisk
    ```

Lorsque vous interrogez un nom de classe mais que vous ne spécifiez aucune instance, WMI retourne la définition de classe. La procédure suivante décrit comment récupérer une définition de classe dans VBScript.

**Pour récupérer une définition de classe dans VBScript**

-   Vous pouvez utiliser la connexion moniker à l’aide d’une requête ou de [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx). Vous pouvez également utiliser [**SWbemServices. obten**](swbemservices-get.md).

    L’exemple suivant montre comment utiliser [GetObject](/previous-versions//kdccchxa(v=vs.85)) pour obtenir une définition de classe.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    L’exemple suivant montre comment interroger une définition de classe.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

Vous pouvez récupérer une définition de classe en C++ en spécifiant uniquement le nom de la classe et aucun chemin d’accès à une instance particulière. La procédure suivante décrit comment récupérer une définition de classe en C++.

**Pour récupérer une définition de classe en C++**

-   Effectuez un appel aux fonctions [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

    L’exemple suivant montre comment appeler la fonction [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    L’exemple de code précédent requiert que l' \# instruction include suivante se compile correctement.

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
