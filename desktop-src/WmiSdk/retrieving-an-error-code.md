---
description: Comme avec toutes les applications, WMI reçoit les codes d’erreur du système d’exploitation Windows.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Récupération d’un code d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516988"
---
# <a name="retrieving-an-error-code"></a>Récupération d’un code d’erreur

Comme avec toutes les applications, WMI reçoit les codes d’erreur du système d’exploitation Windows.

Lorsque vous recevez un code d’erreur, vous disposez des options suivantes :

-   Examinez le journal des événements.

    WMI envoie des messages d’erreur au service journal des événements qui vérifie les journaux des événements pour déterminer la cause d’une erreur. Vous pouvez utiliser les classes prises en charge par le fournisseur de [journaux des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider) pour accéder aux journaux des événements par programmation.

-   Récupérez le code d’erreur normalement.

    WMI prend en charge les techniques standard pour récupérer les codes d’erreur, qui sont des codes d’erreur COM pour C++, et des objets d’erreur natifs, tels que [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), ou [**SWbemLastError**](swbemlasterror.md) si le fournisseur fournit des informations sur l’erreur.

Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

Les sections suivantes sont présentées dans cette rubrique :

-   [Gestion d’une erreur avec VBScript](#handling-an-error-with-vbscript)
-   [Gestion d’une erreur à l’aide de C++](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a>Gestion d’une erreur avec VBScript

Si un appel à WMI par le biais de l’API de script pour WMI provoque une erreur, vous disposez des options suivantes pour accéder aux informations d’erreur :

-   Utilisez des mécanismes d’erreur natifs du langage de script. par exemple, dans VBScript, utilisez [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) pour prendre en charge la gestion des erreurs.
-   Créez un objet [**SWbemLastError**](swbemlasterror.md) pour recevoir un rapport d’erreurs.

Le script suivant illustre l’utilisation de l' [objet Native Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)). Lorsqu’une valeur incorrecte pour le handle de processus est spécifiée, une erreur est générée.


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> La propriété **Description** de l' [objet Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) est vide lors de la connexion à WMI par le biais du moniker « winmgmts : ». Toutefois, si vous vous connectez à l’aide de [**SWbemLocator**](swbemlocator.md), la description est disponible.
>
> Le tableau suivant répertorie les propriétés de l' [objet Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).
>
> 
>
> | Propriété                   | Contient                                                       |
> |----------------------------|----------------------------------------------------------------|
> | **Description**<br/> | Description localisée et explicite de l’erreur.<br/> |
> | **Nombre**<br/>      | **HRESULT** retourné par l’API de script pour WMI.<br/>  |
> | **Source**<br/>      | Identifie l’objet qui a déclenché l’erreur.<br/>        |
>
> 
>
>  

 

Le script suivant illustre l’utilisation d’un objet [**SWbemLastError**](swbemlasterror.md) pour obtenir des informations détaillées sur l’erreur. Notez que tous les fournisseurs ne fournissent pas d’informations à **SWbemLastError**. Pour plus d’informations sur les codes d’erreur dans le script, consultez [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a>Gestion d’une erreur à l’aide de C++

Une application cliente WMI peut recevoir des erreurs spécifiques à COM ou à WMI. Les erreurs COM sont conformes à la structure des codes d’erreur COM. Toutes les interfaces WMI peuvent retourner une erreur spécifique à COM, à l’exception des interfaces [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)et [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) . Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md). Les pages de référence des interfaces WMI répertorient les codes d’erreur WMI appropriés dans la section Codes d’erreur.

Une application cliente doit suivre les normes COM pour vérifier l’État et les codes de retour d’erreur. La principale différence que vous devez choisir est de savoir si vous souhaitez récupérer le code d’erreur à partir d’un appel synchrone, semi-synchrone ou asynchrone.

**Pour accéder aux messages d’erreur synchrones et semi-synchrones à l’aide de C++**

1.  Récupérez les informations d’erreur avec un appel à la fonction com [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .

    Veillez à appeler [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immédiatement après qu’une méthode d’interface indique une erreur. Cela comprend l’une des méthodes [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) que vous appelez lors du traitement d’un processus semi-synchrone.

2.  Examinez l’objet d’erreur COM retourné avec un appel à la méthode [**IErrorInterface :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

    Veillez à spécifier IID \_ WbemClassObject pour le paramètre *riid* dans l’appel [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) . La méthode **QueryInterface** retourne une instance d’une classe WMI, généralement [**\_ \_ ExtendedStatus**](--extendedstatus.md).

WMI ne remet pas l’objet d’erreur via [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) pour un appel asynchrone, car il n’existe aucun moyen de savoir quand, ou sur quel thread l’appel asynchrone s’est produit. Par conséquent, votre code peut uniquement gérer des erreurs spécifiques ou passer l’échec de l’appel par le biais de COM.

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

**Pour accéder aux messages d’erreur asynchrones à l’aide de C++**

-   Récupérez l’objet d’erreur COM à partir de votre implémentation de [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).

    Le pseudo-code suivant illustre une implémentation de gestion des erreurs typique pour une application cliente.

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

