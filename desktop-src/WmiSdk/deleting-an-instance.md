---
description: La suppression d’une instance est la commande de suppression la plus courante que vous êtes susceptible d’effectuer dans WMI.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Suppression d’une instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519840"
---
# <a name="deleting-an-instance"></a>Suppression d’une instance

La suppression d’une instance est la commande de suppression la plus courante que vous êtes susceptible d’effectuer dans WMI. À l’instar de la suppression d’une classe, la commande réelle est assez simple. Toutefois, WMI fonctionne de façon très différente selon le type d’instance que vous supprimez. Si l’instance est statique, WMI supprime simplement l’instance de l’espace de stockage WMI. Pour plus d’informations sur la suppression de classes et d’instances de l’espace de stockage WMI, consultez la commande de préprocesseur [**pragma deleteclass**](pragma-deleteclass.md) .

Si l’instance est dynamique, WMI doit appeler [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) sur les fournisseurs qui sont responsables des classes suivantes :

-   Classe qui possède l’instance de.
-   Chaque classe parente de la classe qui possède l’instance de.
-   Chaque sous-classe de la classe qui possède l’instance.

La réussite de la suppression dépend de la classe non abstraite la plus grande pour l’instance d’origine. Si le fournisseur de toute classe non abstraite de niveau supérieur réussit à terminer la suppression, l’opération réussit. Pour plus d’informations, consultez la section Notes de [**IWbemServices ::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).

L' [API com pour WMI](com-api-for-wmi.md) a différentes méthodes pour supprimer une instance et supprimer un objet.

La procédure suivante décrit comment utiliser C++ pour supprimer une instance d’une classe de base ou d’une classe dérivée.

**Pour supprimer une instance d’une classe de base ou d’une classe dérivée à l’aide de C++**

-   Appelez les méthodes [**IWbemServices ::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) ou [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) .

    Comme son nom l’indique, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) supprime une instance de façon asynchrone tandis que [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) supprime une instance de façon synchrone. Pour utiliser **DeleteInstanceAsync**, vous devez également implémenter un objet [**IWbemObjectSink**](iwbemobjectsink.md) .

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

L' [API de script pour WMI](scripting-api-for-wmi.md) utilise les mêmes méthodes pour supprimer un objet de classe ou une instance.

La procédure suivante décrit comment utiliser VBScript pour supprimer une instance d’une classe de base ou d’une classe dérivée.

**Pour supprimer une instance d’une classe de base ou d’une classe dérivée à l’aide de VBScript**

-   Appelez les méthodes [**SWbemObject. Delete \_**](swbemobject-delete-.md) ou [**SWbemObject. DeleteAsync \_**](swbemobject-deleteasync-.md) .

    Comme son nom l’indique [**, \_ Delete**](swbemobject-delete-.md) supprime une instance de façon synchrone, tandis que [**DeleteAsync \_**](swbemobject-deleteasync-.md) supprime une instance de façon asynchrone. Pour plus d’informations sur la suppression d’une instance de façon asynchrone, consultez [appel d’une méthode](calling-a-method.md).

    L’exemple suivant décrit comment supprimer une instance de à l’aide de VBScript.

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

 

 



