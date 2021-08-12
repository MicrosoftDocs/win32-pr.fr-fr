---
description: Pour recevoir des notifications du fournisseur de Registre système, une application de gestion doit s’inscrire en tant que consommateur d’événements temporaires.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Inscription pour les événements du Registre système
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c6f60b21dee729a879aaeab676da67b06ca0a822bcfd6509bc0f406f96fecec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554244"
---
# <a name="registering-for-system-registry-events"></a>Inscription pour les événements du Registre système

Pour recevoir des notifications du fournisseur de [Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) , une application de gestion doit s’inscrire en tant que consommateur d’événements temporaires. La plupart des conditions requises pour s’inscrire pour le fournisseur de Registre système sont les mêmes que pour toute autre inscription d’événement, sauf que vous devez également effectuer la procédure suivante.

Le fournisseur Registry fournit des classes d’événements pour les événements dans le registre système. Pour plus d’informations sur l’inscription générale des événements, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).

La procédure suivante décrit comment s’inscrire pour les événements du Registre système.

**Pour s’inscrire aux événements du Registre système**

1.  Appeler une méthode de requête de notification.

    Dans script ou C++, utilisez une requête de notification comme [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) ou [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync). Créez une chaîne de requête pour le paramètre *bstrQuery* de **IWbemServices :: ExecNotificationQueryAsync** ou *strQuery* dans le script.

2.  Déterminez le type d’événement que vous souhaitez recevoir et créez la requête.

    Le tableau suivant répertorie les classes d’événements de registre que vous pouvez utiliser.

    

    | Classe d'événements                                                      | Emplacement Hive        | Description                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)                       | N/A<br/>       | Classe de base abstraite pour les modifications dans le registre.<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | Surveille les modifications apportées à une hiérarchie de clés.<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | KeyPath<br/>   | Analyse les modifications apportées à une clé unique.<br/>                |
    | [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Analyse les modifications apportées à une valeur unique.<br/>              |

    

     

    Ces classes ont une propriété appelée **Hive** qui identifie la hiérarchie des clés dont la modification doit être surveillée, telle que **HKEY \_ local \_ machine**.

    Les modifications apportées aux ruches **\_ \_ racine** et **HKEY \_ Current \_ User** ne sont pas prises en charge par les [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) ou les classes qui en sont dérivées, par exemple [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).

3.  Créez la clause WHERE pour votre inscription d’événement.

    Le fournisseur de Registre système a des règles spécifiques pour les clauses WHERE. Pour plus d’informations, consultez [création d’une clause WHERE appropriée pour le fournisseur de Registre](creating-a-proper-where-clause-for-the-registry-provider.md). Pour plus d’informations générales sur la création d’une clause WHERE, consultez [interrogation avec WQL](querying-with-wql.md).

4.  Déterminez si votre consommateur reçoit des événements.

    Le fournisseur de Registre système ne garantit pas que tous les événements envoyés sont remis. Pour plus d’informations, consultez [réception d’événements de Registre](receiving-registry-events.md).

L’exemple de code VBScript suivant montre comment détecter une modification du Registre dans la ruche ou la sous-arborescence Microsoft **HKEY \_ local \_ machine** \\ **Software** \\  . Il s’agit d’un script d’analyse qui, à des fins de démonstration, s’exécute dans un processus nommé Wscript.exe jusqu’à ce qu’il soit terminé dans le **Gestionnaire des tâches**, que WMI soit arrêté ou que le système d’exploitation soit redémarré. Le script utilise un appel [*semi-synchrone*](gloss-s.md) pour [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Pour plus d’informations sur les appels semi-synchrones, consultez [création d’un appel semi-synchrone avec VBScript](making-a-semisynchronous-call-with-vbscript.md).


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



L’exemple de code VBScript suivant montre comment surveiller la modification des valeurs d’une clé en vous inscrivant pour le type d’événement du fournisseur de Registre [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Le script appelle une méthode asynchrone, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Pour plus d’informations sur les appels asynchrones et la sécurité, consultez [création d’un appel asynchrone avec VBScript](making-an-asynchronous-call-with-vbscript.md).

Le script suivant s’exécute indéfiniment jusqu’à ce que l’ordinateur soit redémarré, que WMI soit arrêté ou que le script soit arrêté. Pour arrêter le script manuellement, utilisez le gestionnaire des tâches pour arrêter le processus. Pour l’arrêter par programmation, utilisez la méthode [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) dans la classe de \_ processus Win32.


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

