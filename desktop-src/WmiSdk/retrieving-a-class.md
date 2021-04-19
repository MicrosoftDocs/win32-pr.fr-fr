---
description: Le premier type d’objet que vous pouvez récupérer est une classe WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Récupération d’une classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106543552"
---
# <a name="retrieving-a-wmi-class"></a>Récupération d’une classe WMI

Le premier type d’objet que vous pouvez récupérer est une classe WMI. Lorsque vous récupérez une classe WMI, vous récupérez en fait une définition de classe, qui est une liste des propriétés, des qualificateurs et des méthodes qui décrivent entièrement la classe. Toutefois, une définition de classe est fondamentalement la classe elle-même.

PowerShell utilise une requête standard pour récupérer les définitions de classe, à l’aide de la classe **meta \_ Class** .

**Pour récupérer une définition de classe dans PowerShell**

-   Utilisez la clause with [-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) avec une requête to **meta \_ Class**, avec la clause WHERE contenant le nom de la classe que vous souhaitez récupérer.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    L’applet de commande is [-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) est l’applet de commande standard utilisée par PowerShell pour récupérer des informations de classes et d’instances à partir de WMI. La classe de la **\_ classe Meta** définit la requête en tant que requête de schéma. Sans la classe de la classe **meta \_** , cette requête retourne toutes les instances de \_ disque logique Win32. Pour plus d’informations sur l’interrogation de WMI, consultez [instruction SELECT pour les requêtes de schéma](select-statement-for-schema-queries.md).

Le processus actuel de récupération d’une définition WMI en C# consiste à utiliser la classe **CIMInstance** .

**Pour récupérer une définition de classe en C# (Microsoft. Management. infrastructure)**

1.  À l’aide de l’espace de noms **Microsoft. Management. infrastructure** , créez une classe **CIMInstance** avec l’espace de noms et le nom de classe spécifiés.

    La classe créée contient toutes les informations de classe, mais pas de données d’instance.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  Comme avec PowerShell, vous pouvez également exécuter une requête à l’aide de la balise **meta \_ Class** dans le cadre de la requête.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Comme avec PowerShell, C# utilise une requête de **méta- \_ classe** pour récupérer les définitions de classe. Vous pouvez également créer un objet **ManagementClass** pour accéder directement à la définition de classe.

> [!Note]  
> **System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.

 

**Pour récupérer une définition de classe en C# (System. Management)**

1.  Vous pouvez utiliser [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) avec une requête à la **\_ classe Meta**, avec la clause WHERE contenant le nom de la classe que vous souhaitez récupérer.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) est la classe standard utilisée par .net pour récupérer des informations de classes et d’instances à partir de WMI. [ManagementObjectSerarcher. obtenir](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) retourne un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) qui contient la classe de définition de schéma. La classe de la **\_ classe Meta** définit la requête en tant que requête de schéma. Sans la classe de la classe **\_ meta** , cette requête retourne toutes les instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). Pour plus d’informations sur l’interrogation de WMI, consultez [instruction SELECT pour les requêtes de schéma](select-statement-for-schema-queries.md).

2.  Vous pouvez également créer un nouvel objet [ManagementClass](/dotnet/api/system.management.managementclass) , avec le nom comme chemin d’accès, pour récupérer la classe.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

Vous pouvez récupérer une définition de classe dans VBScript de la même façon pour récupérer une instance spécifique.

**Pour récupérer une définition de classe dans VBScript**

1.  Appelez [**SWbemServices. obtenir**](swbemservices-get.md) mais n’identifiez pas une instance spécifique dans le chemin d’accès de l’objet pour la classe.
2.  L’exemple de code suivant récupère la définition de classe pour la classe qui décrit les lecteurs logiques sur votre ordinateur.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows Script Host (WSH) prend également en charge les éléments suivants.

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    Sur Active Server pages (ASP), utilisez [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) ou [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) dans le script côté serveur. Pour plus d’informations, consultez [création de pages de Active Server pour WMI](creating-active-server-pages-for-wmi.md).

3.  Une classe ou une instance peut également être spécifiée, auquel cas l’objet retourné est un objet WMI, par exemple, une instance de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), plutôt qu’un objet services. Notez que vous ne pouvez pas utiliser les fonctions VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) pour créer une instance de l’objet générique [**SWbemObject**](swbemobject.md).
4.  Dans les pages HTML s’exécutant dans Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) et [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) peuvent échouer parce que les objets de script WMI, comme les contrôles ActiveX, ne sont pas marqués comme sécurisés pour l’écriture de scripts. La seule exception est l’objet [**SWbemDateTime**](swbemdatetime.md) . La seule façon dont ces appels peuvent être exécutés est lorsque vous réduisez les paramètres de sécurité d’Internet Explorer, ce qui n’est pas recommandé.

Lorsque vous récupérez une classe en C++, appelez la version de la fonction [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Pour récupérer une définition de classe en C++**

1.  Appelez les méthodes [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) pour récupérer la définition d’une classe.
2.  Une classe peut avoir plusieurs définitions de classe, ce qui se produit généralement lorsque plusieurs fournisseurs de classes sont chargés dans un même espace de noms. Quand une classe a plusieurs définitions de classe, WMI retourne le code d’état de la première définition découverte et du code d’état des **\_ \_ \_ objets en double WBEM** .

Comme [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retourne une définition de classe, elle est couramment utilisée comme première étape de la création d’une instance. Pour plus d’informations sur l’utilisation de **GetObject**, consultez [création et déclaration d’une instance à l’aide de C++](creating-and-declaring-an-instance-using-c-.md).

 

 
