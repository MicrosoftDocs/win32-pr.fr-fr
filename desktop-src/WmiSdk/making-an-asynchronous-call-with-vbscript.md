---
description: Le fait d’effectuer un appel asynchrone à une méthode WMI ou à une méthode de fournisseur permet à un script de continuer à s’exécuter pendant que les objets retournent à un objet SWbemSink et sont gérés par des méthodes telles que SWbemSink. OnObjectReady.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Exécution d’un appel asynchrone avec VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008250"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a>Exécution d’un appel asynchrone avec VBScript

Le fait d’effectuer un appel asynchrone à une [*méthode WMI*](gloss-w.md) ou à une [*méthode de fournisseur*](gloss-p.md) permet à un script de continuer à s’exécuter pendant que les objets retournent à un objet [**SWbemSink**](swbemsink.md) et sont gérés par des méthodes telles que [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md). Toutefois, les appels asynchrones ne sont pas recommandés, car les données peuvent ne pas être retournées au même niveau de sécurité à mesure que l’appel est effectué.

Lorsque vous utilisez des appels de récepteur asynchrones comme [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) pour récupérer des données retournées, vous pouvez définir la valeur de Registre suivante.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**

La définition de cette valeur de Registre garantit l’authentification des objets de données renvoyés au récepteur. Si **UnsecAppAccessControlDefault** est défini sur un (1), WMI effectue la vérification de l’accès des données renvoyées. Les vérifications d’accès vérifient que les données proviennent de la source correcte. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

Les méthodes asynchrones avec des noms qui se terminent par « Async \_ » retournent toujours immédiatement après leur appel afin qu’un programme puisse continuer à s’exécuter. Par exemple, [**SWbemServices. ExecQuery**](swbemservices-execquery.md) est synchrone et bloque l’exécution jusqu’à ce que tous les objets soient retournés. La méthode [**SWbemServices. ExecQueryAsync**](swbemservices-execqueryasync.md) est la version asynchrone qui ne se bloque pas. Une façon plus sécurisée d’effectuer l’appel au non-blocage de **SWbemServices. ExecQuery** consiste à effectuer l’appel [*semisynchronously*](gloss-s.md). Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md) et [exécution d’un appel semi-synchrone avec VBScript](making-a-semisynchronous-call-with-vbscript.md).

Le paramètre *IFlags* pour les appels asynchrones est toujours défini par défaut sur zéro (0). Les méthodes asynchrones ne fournissent pas de collection [**SWbemObjectSet**](swbemobjectset.md) à la sous-routine sink. Au lieu de cela, la sous-routine d’événement [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) de votre script ou application reçoit chaque objet tel qu’il est fourni.

Lorsque l’appel asynchrone d’origine est terminé, il appelle l’événement [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) du récepteur d’objets et exécute le code que vous placez pour traiter le résultat de l’appel.

> [!Note]  
> Une page de Active Server (ASP) en tant qu’hôte de script ne prend pas en charge un appel asynchrone.

 

La procédure suivante décrit comment effectuer un appel asynchrone à l’aide de VBScript.

**Pour effectuer un appel asynchrone à l’aide de VBScript**

1.  Connecter à WMI et récupérez un objet [**SWbemServices**](swbemservices.md) .

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  créez le récepteur d’objets à l’aide de [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) ou (pour Windows Script Host 2,0 uniquement) la balise object avec un attribut events ayant la valeur **TRUE**.

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    -ou-

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  Créez une sous-routine pour chaque événement qu’un événement asynchrone peut déclencher. Ces événements sont définis en tant que méthodes sur [**SWbemObject**](swbemobject.md). Par exemple, WMI effectue un rappel à [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) à mesure que chaque instance retourne.

    Lorsque vous créez la sous-routine, placez le code dans la sous-routine pour gérer chaque événement lors de sa réception.

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    Examinez le paramètre *iHresult* retourné par l’événement [**OnCompleted**](swbemsink-oncompleted.md) pour déterminer si l’appel asynchrone a réussi ou non, ou si une erreur s’est produite. En cas de réussite, la valeur passée dans le paramètre *iHresult* est égale à zéro (0). Toute autre valeur peut indiquer une erreur, et vous devez vérifier les valeurs dans l’objet d’erreur qui est retourné dans le paramètre *objErrorObject* .

4.  Effectuez un appel asynchrone et transmettez le nom de votre récepteur dans le paramètre *objWbemSink* .

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  Effectuez un appel qui empêche le script de se terminer avant la réception de tous les événements. si votre script peut s’exécuter avec une interface d’écran, un moyen simple de le faire consiste à utiliser une commande Windows script Host (WSH) `Echo` , qui est illustrée dans l’exemple suivant.

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    Lorsque vous exécutez ce script, vous pouvez voir que la première instance est retournée avant le message **d’attente d’instances** ou que vous pouvez la voir après. Il s’agit de la nature du traitement asynchrone. Si vous fermez la boîte de message en **attente d’instances** trop tôt, vous ne verrez peut-être pas toutes les instances.

6.  Si vous avez des résultats de plusieurs appels asynchrones différents retournant au même récepteur, stockez toutes les données de différenciation nécessaires dans le paramètre de contexte *objWbemAsyncContext* .

7.  Lorsque vous avez terminé avec le récepteur, annulez votre appel asynchrone à l’aide de la méthode [**Cancel**](swbemsink-cancel.md) .

    ```VB
    objwbemsink.Cancel()
    ```

    

    La méthode [**Cancel**](swbemsink-cancel.md) indique à WSH d’annuler tous les appels asynchrones associés à un objet récepteur donné. Ainsi, vous souhaiterez peut-être utiliser des récepteurs distincts pour les opérations asynchrones qui doivent être indépendantes.

8.  Libérer l’objet récepteur en lui assignant l’objet récepteur `Nothing` .

    ```VB
    set objwbemsink= Nothing
    ```

    

L’exemple de code suivant montre une requête asynchrone pour toutes les instances [**du \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) sur l’ordinateur local. Pour obtenir une version semi-synchrone de la même méthode, consultez [appel d’une méthode](calling-a-method.md).


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
