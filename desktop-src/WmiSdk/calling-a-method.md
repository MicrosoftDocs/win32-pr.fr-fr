---
description: WMI fournit des méthodes dans l’API COM et l’API de script pour obtenir des informations ou manipuler des objets dans un système d’entreprise.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Appel d’une méthode WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db6c8a74c8125e0bb1727839b8f59f4b486161d5ae629a0c7351481ade016ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820084"
---
# <a name="calling-a-wmi-method"></a>Appel d’une méthode WMI

WMI fournit des méthodes dans l' [API com](com-api-for-wmi.md) et l' [API de script](scripting-api-for-wmi.md) pour obtenir des informations ou manipuler des objets dans un système d’entreprise. Par exemple, la méthode de script WMI [**SWbemServices.Exe**](swbemservices-execquery.md) des requêtes cQuery pour les données. Les fournisseurs ont également des méthodes définies dans les classes qu’ils inscrivent. Exemples : les [**méthodes \_ logiques Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) et [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) fournies par le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider).

Les sections suivantes sont présentées dans cette rubrique :

-   [Comparaison des méthodes WMI et des méthodes de fournisseur](#wmi-methods-compared-to-provider-methods)
-   [Modes d’appel de méthode dans WMI](#method-calling-modes-in-wmi)
    -   [Mode synchrone](#synchronous-mode)
    -   [Mode asynchrone](#asynchronous-mode)
    -   [Mode semi-synchrone](#semisynchronous-mode)
-   [Rubriques connexes](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>Comparaison des méthodes WMI et des méthodes de fournisseur

En utilisant des appels de [*méthode WMI*](gloss-w.md) combinés aux appels de [*méthode de fournisseur*](gloss-p.md) , vous pouvez récupérer et manipuler les informations relatives à votre entreprise. Pour plus d’informations, consultez [appel d’une méthode WMI](calling-a-wmi-method.md) et [appel d’une méthode de fournisseur](calling-a-provider-method.md).

Les méthodes de l’objet de script WMI [**SWbemObject**](swbemobject.md) ont un état spécial, car elles peuvent s’appliquer à n’importe quelle classe de données WMI. Pour plus d’informations, consultez [Scripting with SWbemObject](scripting-with-swbemobject.md).

L’exemple de code suivant appelle les méthodes WMI et Provider.

Les méthodes WMI et Provider suivantes se trouvent dans l' [API de script pour WMI](scripting-api-for-wmi.md):

-   **objWMIService.ExecQuery** appelle la méthode de script WMI [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **objService. StopService ()** appelle la méthode du fournisseur [ **Win32 \_ service. StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

Vous pouvez rechercher le code qui peut s’afficher dans « retour » dans la section codes de retour [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a>Modes de Method-Calling dans WMI

Le mode d’appel semi-synchrone offre généralement le meilleur équilibre entre la sécurité et les performances.

Pour plus d’informations sur chacun des modes possibles, consultez les rubriques suivantes :

-   [Synchrone](#synchronous-mode)
-   [Asynchrone](#asynchronous-mode)
-   [Semi](#semisynchronous-mode)

### <a name="synchronous-mode"></a>Mode synchrone

Le mode synchrone se produit lorsque le programme ou les scripts s’interrompt jusqu’à ce que l’appel de méthode retourne un objet de collection [**SWbemObjectSet**](swbemobjectset.md) . WMI génère cette collection en mémoire avant de retourner l’objet de collection au programme ou au script appelant.

Le mode synchrone peut avoir un effet néfaste sur les performances des programmes ou des scripts sur l’ordinateur qui exécute le programme ou le script. Par exemple, la récupération synchrone de milliers d’événements à partir du journal des événements peut prendre beaucoup de temps et utiliser beaucoup de mémoire, car WMI crée un objet à partir de chaque événement, puis place ces objets dans une collection avant de passer la collection à la méthode.

Vous devez uniquement appeler les méthodes qui ne retournent pas de jeux de données de grande taille en mode synchrone. Les méthodes [**SWbemServices**](swbemservices.md) suivantes peuvent être appelées en toute sécurité en mode synchrone :

-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.**](swbemservices-get.md)

Toutes les méthodes [**SWbemServices**](swbemservices.md) sans le mot « Async » dans le nom peuvent être appelées en mode synchrone en définissant la valeur **wbemFlagReturnWhenComplete** dans le paramètre *IFlags* .

### <a name="asynchronous-mode"></a>Mode asynchrone

Le mode asynchrone se produit lorsque le programme ou le script continue à s’exécuter après l’appel de la méthode. WMI retourne tous les objets de la méthode à un objet [**SWbemSink**](swbemsink.md) lors de la création de chaque objet. Le programme ou le script appelant doit avoir un objet **SWbemSink** et un gestionnaire d’événements [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) pour traiter les objets retournés. Pour plus d’informations sur la création d’un gestionnaire d’événements pour le mode asynchrone, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).

Bien que ce mode ne présente pas les performances et les ressources du mode synchrone, le mode asynchrone peut créer des risques sérieux pour la sécurité, car les résultats stockés dans l’objet [**SWbemSink**](swbemsink.md) peuvent ne pas provenir du programme ou du script appelant. WMI réduit le niveau d’authentification sur l’objet **SWbemSink** jusqu’à ce que la méthode aboutisse. Pour plus d’informations sur la façon de réduire ces risques de sécurité, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

Les méthodes ajoutées au mot Async sont des méthodes pour le mode asynchrone. Les méthodes suivantes sont des appels asynchrones :

-   [**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
-   [**SWbemServices. DeleteAsync**](swbemservices-deleteasync.md)
-   [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
-   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)
-   [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
-   [**SWbemServices. InstancesOfAsync**](swbemservices-instancesofasync.md)
-   [**SWbemServices. ReferencesToAsync**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOfAsync**](swbemservices-subclassesofasync.md)

Pour plus d’informations sur le mode asynchrone, consultez :

-   [Exécution d’un appel asynchrone avec C++](making-an-asynchronous-call-with-c--.md)
-   [Exécution d’un appel asynchrone avec VBScript](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>Mode semi-synchrone

Le mode semi-synchrone est semblable au mode asynchrone en ce que le programme ou le script continue à s’exécuter après l’appel de la méthode. En mode semi-synchrone, WMI récupère les objets en arrière-plan au fur et à mesure que votre script ou votre programme continue de s’exécuter. WMI retourne chaque objet retourné à la méthode appelante juste après la création de l’objet.

Étant donné que WMI gère l’objet, le mode semi-synchrone est plus sécurisé que le mode asynchrone. Toutefois, si vous utilisez le mode semi-synchrone avec plus de 1 000 instances, la récupération d’instance peut monopoliser les ressources disponibles, ce qui peut dégrader les performances du programme ou du script et de l’ordinateur à l’aide du programme ou du script. Chaque objet utilise les ressources nécessaires jusqu’à ce que la mémoire soit libérée.

Pour contourner cette condition, vous pouvez appeler la méthode avec le paramètre *IFlags* défini avec les indicateurs **wbemFlagForwardOnly** et **wbemFlagReturnImmediately** pour indiquer à WMI de retourner une [**SWbemObjectSet**](swbemobjectset.md)avant uniquement. Un objet **SWbemObjectSet** avant uniquement élimine le problème de performance causé par un jeu de données volumineux en libérant la mémoire après l’énumération de l’objet.

Toute méthode [**SWbemServices**](swbemservices.md) qui ne peut pas être appelée en mode synchrone ou asynchrone est appelée en mode semi-synchrone.

Les méthodes suivantes sont appelées en mode semi-synchrone :

-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices.**](swbemservices-get.md)
-   [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)
-   [**SWbemServices. put**](swbemservicesex-put.md)

Pour plus d’informations sur le mode semi-synchrone, consultez [création d’un appel semi-synchrone avec C++](making-a-semisynchronous-call-with-c--.md) et [exécution d’un appel semi-synchrone avec VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Amélioration des performances d’énumération](improving-enumeration-performance.md)
</dt> <dt>

[Écriture de scripts avec SWbemObject](scripting-with-swbemobject.md)
</dt> <dt>

[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
