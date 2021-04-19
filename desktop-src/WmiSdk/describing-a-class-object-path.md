---
description: Un chemin d’accès à un objet de classe décrit l’emplacement d’une classe dans un espace de noms.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Description d’un chemin d’accès d’objet de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfd603ea3b6de151d297a7f4b6fc8a2a27dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521877"
---
# <a name="describing-a-class-object-path"></a><span data-ttu-id="201f0-103">Description d’un chemin d’accès d’objet de classe</span><span class="sxs-lookup"><span data-stu-id="201f0-103">Describing a Class Object Path</span></span>

<span data-ttu-id="201f0-104">Un chemin d’accès à un objet de classe décrit l’emplacement d’une classe dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="201f0-104">A class object path describes the location of a class within a namespace.</span></span>

<span data-ttu-id="201f0-105">Vous pouvez utiliser les méthodes suivantes pour spécifier un chemin d’accès à un objet :</span><span class="sxs-lookup"><span data-stu-id="201f0-105">You can use the following methods to specify an object path:</span></span>

-   <span data-ttu-id="201f0-106">Un chemin d’accès d’objet complet à une classe ajoute le nom de la classe à un chemin d’accès d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="201f0-106">A full object path to a class appends the class name to a namespace path.</span></span>

    <span data-ttu-id="201f0-107">L’exemple suivant montre l’emplacement de la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans \\ l' \\ espace de noms CIMV2 racine sur le serveur nommé Admin.</span><span class="sxs-lookup"><span data-stu-id="201f0-107">The following example shows the location of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class within the \\root\\cimv2 namespace on the server named Admin.</span></span>

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   <span data-ttu-id="201f0-108">Un chemin d’accès d’objet relatif représente une classe qui réside dans l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="201f0-108">A relative object path represents a class that resides in the current namespace.</span></span> <span data-ttu-id="201f0-109">Un chemin d’accès d’objet relatif à une classe contient uniquement le nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="201f0-109">A relative object path to a class contains only the class name.</span></span>

    <span data-ttu-id="201f0-110">L’exemple suivant montre le chemin d’accès relatif à la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="201f0-110">The following example shows the relative path to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

    ``` syntax
    Win32_LogicalDisk
    ```

<span data-ttu-id="201f0-111">Lorsque vous interrogez un nom de classe mais que vous ne spécifiez aucune instance, WMI retourne la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="201f0-111">When you query for a class name but specify no instances, WMI returns the class definition.</span></span> <span data-ttu-id="201f0-112">La procédure suivante décrit comment récupérer une définition de classe dans VBScript.</span><span class="sxs-lookup"><span data-stu-id="201f0-112">The following procedure describes how to retrieve a class definition in VBScript.</span></span>

<span data-ttu-id="201f0-113">**Pour récupérer une définition de classe dans VBScript**</span><span class="sxs-lookup"><span data-stu-id="201f0-113">**To retrieve a class definition in VBScript**</span></span>

-   <span data-ttu-id="201f0-114">Vous pouvez utiliser la connexion moniker à l’aide d’une requête ou de [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="201f0-114">You can use the moniker connection either with a query or [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span></span> <span data-ttu-id="201f0-115">Vous pouvez également utiliser [**SWbemServices. obten**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="201f0-115">You can also use [**SWbemServices.Get**](swbemservices-get.md).</span></span>

    <span data-ttu-id="201f0-116">L’exemple suivant montre comment utiliser [GetObject](/previous-versions//kdccchxa(v=vs.85)) pour obtenir une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="201f0-116">The following example shows how to use [GetObject](/previous-versions//kdccchxa(v=vs.85)) to get a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    <span data-ttu-id="201f0-117">L’exemple suivant montre comment interroger une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="201f0-117">The following example shows how to query for a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

<span data-ttu-id="201f0-118">Vous pouvez récupérer une définition de classe en C++ en spécifiant uniquement le nom de la classe et aucun chemin d’accès à une instance particulière.</span><span class="sxs-lookup"><span data-stu-id="201f0-118">You can retrieve a class definition in C++ by specifying only the class name and no path to a particular instance.</span></span> <span data-ttu-id="201f0-119">La procédure suivante décrit comment récupérer une définition de classe en C++.</span><span class="sxs-lookup"><span data-stu-id="201f0-119">The following procedure describes how to retrieve a class definition in C++.</span></span>

<span data-ttu-id="201f0-120">**Pour récupérer une définition de classe en C++**</span><span class="sxs-lookup"><span data-stu-id="201f0-120">**To retrieve a class definition in C++**</span></span>

-   <span data-ttu-id="201f0-121">Effectuez un appel aux fonctions [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="201f0-121">Make a call to the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) functions.</span></span>

    <span data-ttu-id="201f0-122">L’exemple suivant montre comment appeler la fonction [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="201f0-122">The following example shows how to call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) function.</span></span>

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    <span data-ttu-id="201f0-123">L’exemple de code précédent requiert que l' \# instruction include suivante se compile correctement.</span><span class="sxs-lookup"><span data-stu-id="201f0-123">The previous code example requires the following \#include statement to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
