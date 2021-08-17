---
description: Si vous utilisez l’API de script pour WMI pour récupérer ou stocker des informations de classe localisées, spécifiez les paramètres régionaux dans le cadre d’un moniker.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Récupération des classes modifiées à l’aide de l’API de script pour WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47d01af2515b26ca308a1b258aa40508f227a0c1d0eaa5b2b332c1e7b3200420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130881"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a>Récupération des classes modifiées à l’aide de l’API de script pour WMI

Si vous utilisez l’API de script pour WMI pour récupérer ou stocker des informations de classe localisées, spécifiez les paramètres régionaux dans le cadre d’un moniker. Ou vous pouvez fournir le nom des paramètres régionaux dans le paramètre *strLocale* à la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) . Lors de la lecture ou de l’écriture de classes amendées, indiquez que vous souhaitez utiliser les définitions de classe localisées en spécifiant [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) comme indicateur pour le paramètre *IFlags* de la méthode que vous appelez. Pour PowerShell, vous pouvez utiliser le paramètre *-locale* sur [obtenir-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) pour spécifier les paramètres régionaux.

L’exemple de code suivant montre comment récupérer une classe localisée à l’aide d’un moniker de script WMI ou du paramètre-locale.


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





L’exemple de code suivant montre comment définir les paramètres régionaux et utiliser l’indicateur [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

Le tableau suivant répertorie les méthodes qui acceptent l’indicateur [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .



| Méthode synchrone                                                 | Méthode asynchrone                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)   | [**SWbemServices. SubclassesOfAsync**](swbemservices-subclassesofasync.md)   |
| [**SWbemObject. Subclasses\_**](swbemobject-subclasses-.md)        | [**SWbemObject. SubclassesAsync\_**](swbemobject-subclassesasync-.md)        |
| [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)     | [**SWbemServices. InstancesOfAsync**](swbemservices-instancesofasync.md)     |
| [**SWbemObject. instances\_**](swbemobject-instances-.md)          | [**SWbemObject. InstancesAsync\_**](swbemobject-instancesasync-.md)          |
| [**SWbemServices.ExecQuery**](swbemservices-execquery.md)         | [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)         |
| [**SWbemServices.**](swbemservices-get.md)                     | [**SWbemServices. GetAsync**](swbemservices-getasync.md)                     |
| [**SWbemObject. put\_**](swbemobject-put-.md)                      | [**SWbemObject. PutAsync\_**](swbemobject-putasync-.md)                      |
| [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)   | [**SWbemServices. ReferencesToAsync**](swbemservices-referencestoasync.md)   |
| [**SWbemObject. References\_**](swbemobject-references-.md)        | [**SWbemObject. ReferencesAsync\_**](swbemobject-referencesasync-.md)        |
| [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md) | [**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md) |
| [**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)      | [**SWbemObject. AssociatorsAsync\_**](swbemobject-associatorsasync-.md)      |



 

 

 
