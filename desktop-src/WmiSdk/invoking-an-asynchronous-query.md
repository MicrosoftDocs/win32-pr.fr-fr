---
description: Une requête asynchrone, bien qu’un peu plus complexe à écrire, est le type de requête par défaut, lorsque les performances du système ou du réseau seront affectées par l’interrogation d’un grand groupe de données.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Appel d’une requête asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ae188e3826562b1de68357db34dca6cea60a40e4be07c16946b13ed3eb3007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993069"
---
# <a name="invoking-an-asynchronous-query"></a>Appel d’une requête asynchrone

Une requête asynchrone, bien qu’un peu plus complexe à écrire, est le type de requête par défaut, lorsque les performances du système ou du réseau seront affectées par l’interrogation d’un grand groupe de données. Dans le script, créer un objet [**SWbemSink**](swbemsink.md) et des sous-routines pour gérer les événements que le récepteur peut recevoir sont les seules tâches supplémentaires au-delà de la requête de base.

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

Les requêtes de script abrégées suivantes pour tous les fichiers de données sur l’ordinateur local. Cette requête peut prendre beaucoup de temps si elle a été exécutée pour tous les ordinateurs d’un réseau. Un objet [**SWbemSink**](swbemsink.md) est configuré et le seul événement géré est l’événement OnCompleted.


```VB
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
    WScript.Echo "Asynchronous operation is done."
End Sub

Set service = GetObject("winmgmts:")
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
service.ExecQueryAsync sink, "SELECT * FROM Win32_DataFile"
WScript.Echo "Waiting for instances."
sink.Cancel()
set sink= Nothing
```



Pour plus d’informations sur la construction d’appels de méthode asynchrones dans un script, consultez [appel d’une méthode](calling-a-method.md).

Dans les applications C++, une requête asynchrone génère un processus distinct pour recevoir les données de la requête. Une requête asynchrone est plus complexe qu’une requête synchrone, car vous devez coder une application multithread. Toutefois, une requête asynchrone ne monopolise pas le thread principal de votre application.

La procédure suivante décrit comment exécuter une requête asynchrone en C++.

**Pour exécuter une requête asynchrone en C++**

1.  Implémentez un objet **IWbemSink** .

    Un objet **IWbemSink** reçoit des informations sur une opération asynchrone.

2.  Décrivez votre requête dans un appel à [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).

    WMI déplace immédiatement le processus qui interroge le CIM sur un autre thread et libère le thread qui a exécuté la requête pour une autre tâche.

3.  Attendez que WMI appelle la méthode [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

    Lorsque vous avez terminé, les appels WMI [**indiquent**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) à votre application que la requête est terminée. WMI retourne également les résultats de la requête au récepteur en tant que pointeur vers un pointeur d’interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Comme pour une requête synchrone, utilisez le pointeur pour accéder aux objets qui composent le résultat de votre requête.

L’exemple de code suivant ne se compile pas sans erreur, car la classe QuerySink n’a pas été définie. Pour obtenir la définition de la classe QuerySink, consultez [**IWbemObjectSink**](iwbemobjectsink.md). L’exemple de code requiert également les instructions de référence et \# include suivantes.


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



L’exemple de code suivant montre comment effectuer un appel asynchrone pour émettre une requête.


```C++
void ExecQuery(IWbemServices *pSvc)
{
    // Create a new sink object.
    QuerySink *pSink = new QuerySink;

    // Initialize the query and query language.
    BSTR strQuery = SysAllocString(L"SELECT * FROM ClassName");
    BSTR strQueryLang = SysAllocString(L"WQL");
    
    // Issue the query.
    HRESULT hRes = pSvc->ExecQueryAsync(strQueryLang, strQuery, 0,
        NULL, pSink);

    // Clean up.
    SysFreeString(strQuery);
    SysFreeString(strQueryLang);
    
    if (hRes)
    {
        printf("ExecQueryAsync failed with = 0x%X\n", hRes);
        return;
    }
    
    printf("Completed.\n");
}
```



Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

 



