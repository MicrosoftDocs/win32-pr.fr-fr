---
description: Fournit des fonctionnalités d’accès semi-synchrone et un exemple de code pour effectuer un appel de méthode semi-synchrone.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Exécution d’un appel semi-synchrone avec VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9df081d9b7ff238b347f7068f3631c17a8921c3fef1a567ee151dae93b5dda52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923750"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a>Exécution d’un appel semi-synchrone avec VBScript

Certaines méthodes WMI peuvent retourner des collections volumineuses, provoquant ainsi un blocage des scripts. dans le script, l’accès semi-synchrone est la valeur par défaut, et Windows Management Instrumentation (WMI) définit **wbemFlagReturnImmediately** pour les appels qui peuvent retourner des collections d’objets volumineuses, telles que les méthodes [**SWbemServices**](swbemservices.md) suivantes : [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md)et [**ReferencesTo**](swbemservices-referencesto.md).

L’accès semi-synchrone qui utilise **wbemFlagReturnImmediately** défini dans le paramètre *IFlags* est également la valeur par défaut pour les appels qui peuvent retourner des jeux d’objets volumineux pour les méthodes [**SWbemObject**](swbemobject.md) suivantes : [**instances \_**](swbemobject-instances-.md), [**sous-classes \_**](swbemobject-subclasses-.md), [**\_ associateurs**](swbemobject-associators-.md)et [**références \_**](swbemobject-references-.md).

Pour réduire l’utilisation des ressources de mémoire WMI lors du traitement d’une grande collection d’objets, incluez la valeur de **wbemFlagForwardOnly** dans le paramètre *IFlags* . L’utilisation de **wbemFlagForwardOnly** amène WMI à créer un énumérateur avant uniquement qui ne permet pas de rembobiner la collection et d’accéder de nouveau aux éléments.

WMI élimine la mémoire pour chaque objet lorsque l’instruction **for each** traite un objet. Vous ne pouvez pas appeler la méthode **Count** pour une collection lorsque l’indicateur **wbemFlagForwardOnly** a été défini sur l’appel qui a obtenu la collection. Notez que le paramètre *IFlags* a **wbemFlagReturnImmediately** et **wbemFlagForwardOnly** définis par défaut pour la méthode [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) .

La procédure suivante décrit comment utiliser VBScript pour effectuer un appel semi-synchrone.

**Pour effectuer un appel semi-synchrone dans VBScript**

1.  Définissez le paramètre *IFlags* sur la valeur de [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).
2.  Effectuez l’appel synchrone normal pour [**SWbemServices.ExecQuery**](swbemservices-execquery.md) ou [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) avec la valeur *IFlags* .
3.  Si vous souhaitez traiter les objets retournés par l’appel comme une collection, utilisez une syntaxe d’énumération telle que VBScript **pour chaque**. À mesure que chaque objet est retourné, il est traité en tant qu’élément suivant dans la collection.
4.  Créez un énumérateur avant uniquement en associant la valeur de **wbemFlagReturnImmediately** à la valeur de **wbemFlagForwardOnly**. La valeur décimale de cette opération ou est 48. Ces constantes sont définies dans la bibliothèque de types wbemdisp. tlb pour Visual Basic. La plupart des langages de script utilisent la valeur numérique ou définissent une constante. Pour plus d’informations, consultez [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).

L’exemple de code suivant montre comment effectuer un appel de méthode semi-synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

 



