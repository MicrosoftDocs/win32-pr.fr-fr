---
description: Les scripts WMI peuvent condenser la plupart des étapes requises dans un programme C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Connexion à WMI avec VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866897"
---
# <a name="connecting-to-wmi-with-vbscript"></a>Connexion à WMI avec VBScript

Les scripts WMI peuvent condenser la plupart des étapes requises dans un programme C++. Ils peuvent se connecter à WMI, non seulement via un objet [**SWbemLocator**](swbemlocator.md) , mais également par le moniker « winmgmts : ». Un moniker est un nom abrégé qui localise un espace de noms, une classe ou une instance dans WMI. Le nom « winmgmts : » est le moniker WMI qui indique à Windows Script Host d’utiliser les objets WMI, se connecte à l’espace de noms par défaut et obtient un objet [**SWbemServices**](swbemservices.md) . D’autres informations de connexion, telles qu’un niveau d’emprunt d’identité ou une classe ou une instance spécifique, apparaissent dans la chaîne qui suit le nom du moniker. Vous pouvez utiliser des monikers dans les appels qui créent ou obtiennent des objets WMI. Pour plus d’informations, consultez [construction d’une chaîne de moniker](constructing-a-moniker-string.md).

La procédure suivante décrit comment se connecter à WMI à l’aide de **SWbemLocator**.

**Pour se connecter à WMI à l’aide de SWbemLocator**

1.  Récupérez un objet localisateur avec un appel à [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  Connectez-vous à l’espace de noms à l’aide d’un appel à la méthode [**ConnectServer**](swbemlocator-connectserver.md) .

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    Si vous ne spécifiez pas d’ordinateur dans l’appel à [**ConnectServer**](swbemlocator-connectserver.md), WMI se connecte à l’ordinateur local. Si vous ne spécifiez pas d’espace de noms, WMI se connecte à l’espace de noms spécifié dans la clé de registre.

    **HKEY \_ Logiciel de l' \_ ordinateur local** espace de \\  \\  \\  \\  \\ **noms par défaut** de script WBEM Microsoft

    L’espace de noms par défaut est le \\ \\ cimv2 racine. Pour plus d’informations sur les espaces de noms, consultez [création de hiérarchies dans WMI](creating-hierarchies-within-wmi.md).

3.  Définissez le niveau d’emprunt d’identité avec un appel à la méthode [**SWbemServices \_ . Security**](swbemservices-security-.md) .

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

4.  Implémentez l’objectif de votre script.

    WMI expose un ensemble d’objets de script qui utilisent pour accéder et manipuler des données sur votre réseau. Pour plus d’informations, consultez [manipulation d’informations de classes et d’instances](manipulating-class-and-instance-information.md) et [API de script pour WMI](scripting-api-for-wmi.md).

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

La procédure suivante décrit comment se connecter à WMI et récupérer un objet à l’aide d’un moniker.

**Pour se connecter à WMI et récupérer un objet à l’aide d’un moniker**

1.  Appelez [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) avec un moniker dans le paramètre d’entrée.

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    Le moiniker contient un certain nombre d’éléments que vous pouvez utiliser pour vous connecter à WMI :

    -   « Winmgmts : » indique à WSH d’utiliser les objets de l' [API de script](scripting-api-objects.md). Dans cet exemple, WSH sait qu’il doit retourner un SWbemObject qui décrit le premier \_ ScheduledJob Win32 sur le système. Les autres objets possibles à retourner sont un objet SWbemCollection ou [**SWbemServices**](swbemservices.md) , en fonction de ce que le moniker a décrit.

    -   Vous pouvez éventuellement définir les niveaux de sécurité pour la connexion. Notez cependant que vous ne pouvez pas définir les informations de nom et de mot de passe dans un moniker. Pour plus d’informations, consultez [sécurisation des scripts pour les clients](securing-scripting-clients.md).

    -   Vous pouvez éventuellement définir le chemin d’accès à l’objet WMI. Cela comprend l’ordinateur local ou distant, l’espace de noms, ainsi que le nom de la classe. Pour plus d’informations sur l’utilisation de la [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) VBScript dans les scripts WMI, consultez [création d’une instance](creating-an-instance.md) et [récupération d’une instance WMI](retrieving-an-instance.md).

2.  Au lieu de récupérer un seul élément ou une seule collection, vous pouvez également choisir de récupérer l’objet [**SWbemServices**](swbemservices.md) (comme décrit dans l’exemple précédent). Ensuite, vous pouvez ensuite appeler des requêtes supplémentaires sur l’objet retourné.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    Dans l’exemple précédent, Impersonate, ou impersonationLevel = 3, est le niveau de sécurité de processus par défaut. Dans l’exemple suivant, il n’est pas nécessaire de spécifier ce niveau de sécurité de processus, sauf si vous devez modifier la sécurité du processus en **délégué**. Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
