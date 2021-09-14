---
description: Utilisez SWbemServices. ExecQuery pour demander tous les événements existants.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Réception des notifications d’événements synchrones et semi-synchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008231"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a>Réception des notifications d’événements synchrones et semi-synchrones

Utilisez [**SWbemServices. ExecQuery**](swbemservices-execquery.md) pour demander tous les événements existants.

L’exemple de code suivant montre comment interroger les événements d’un journal.

`Select * from Win32_NTLogEvent`

pour plus d’informations, consultez [déterminer le Type d’événement à recevoir](determining-the-type-of-event-to-receive.md), recevoir [des notifications d’événements](receiving-event-notifications.md)et [WQL (SQL pour WMI)](wql-sql-for-wmi.md).

L’appel par défaut à [**SWbemServices. ExecNotificationQuery**](swbemservices-execnotificationquery.md) utilise la communication semi-synchrone. Les indicateurs **wbemFlagForwardOnly** et **wbemFlagReturnImmediately** sont définis par défaut pour le paramètre *IFlags* . Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

La procédure suivante décrit comment recevoir une notification d’événements semi-synchrone à l’aide de VBScript.

**Pour recevoir une notification d’événements semi-synchrone dans VBScript**

1.  Créez une requête pour le type d’événement que vous souhaitez recevoir. Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).

2.  Si vous demandez un type d’instance d’événement tel que [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), indiquez dans la requête un type d’instance cible, par exemple [**, \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).

3.  Si nécessaire, spécifiez une instance, par exemple, le nom d’un espace de noms lors de la demande de futures instances [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md) pour un espace de noms spécifique.

4.  spécifiez une fréquence d’interrogation de Windows Management Instrumentation (WMI) dans une requête, telle que « dans les 10 », pour interroger toutes les 10 secondes. Pour plus d’informations, consultez [dans la clause in](within-clause.md).

5.  Appelez [**SWbemServices. ExecNotificationQuery**](swbemservices-execnotificationquery.md) à l’aide de la requête.

6.  Parcourez la collection que vous recevez.

L’exemple suivant montre comment surveiller l’insertion et la suppression de disques à partir d’un lecteur de disquette sur un ordinateur local. Le script demande \_ des instances [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) pour l’instance [**disque \_ logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) du lecteur de disquette et interroge toutes les 10 secondes les nouvelles instances. Ce script est un exemple de consommateur d’événements temporaire et continue de s’exécuter jusqu’à ce qu’il soit arrêté dans le gestionnaire des tâches ou que le système soit redémarré. Pour plus d’informations, consultez [réception d’événements pendant la durée de votre application](receiving-events-for-the-duration-of-your-application.md).


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



La procédure suivante décrit comment recevoir une notification d’événements semi-synchrone à l’aide de C++.

**Pour recevoir une notification d’événements semi-synchrone en C++**

1.  Configurez l’application avec des appels aux fonctions [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    Étant donné que WMI est basé sur COM, l’appel de [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) est une étape obligatoire pour une application WMI. Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).

2.  Déterminez le type d’événement que vous souhaitez recevoir.

    WMI prend en charge les événements intrinsèques et extrinsèques. Un événement intrinsèque est un événement prédéfini par WMI. Un événement extrinsèque est un événement défini par un fournisseur tiers. Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).

3.  Inscrivez-vous pour recevoir une classe spécifique d’événements avec un appel à la méthode [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .

    Rendez chaque requête très spécifique. L’objectif de l’inscription est de s’inscrire pour recevoir uniquement les notifications requises. Notifications qui ne sont pas requises pour le traitement et le temps de remise des déchets.

    Vous pouvez concevoir un consommateur d’événements pour recevoir plusieurs événements. Par exemple, un consommateur peut exiger la notification des événements de modification d’instance pour une classe spécifique d’événements d’appareil et de violation de sécurité. Dans ce cas, les tâches qu’un consommateur effectue lors de la réception d’un événement de modification d’instance sont différentes pour les deux événements. Par conséquent, le consommateur doit effectuer un appel à [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) pour s’inscrire aux événements de modification d’instance, et un autre appel à **ExecNotificationQuery** pour s’inscrire aux événements de violation de sécurité.

    Dans l’appel à [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), définissez le paramètre *lFlags* sur **l' \_ indicateur WBEM \_ Return \_ immédiatement** et l' **\_ indicateur WBEM \_ Forward \_ uniquement**. L' **\_ indicateur WBEM \_ retourne \_ immédiatement** les demandes d’indicateur de traitement semi-synchrone, et l’indicateur **WBEM en \_ \_ avant \_ uniquement** demande un énumérateur avant uniquement. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md). La fonction **ExecNotificationQuery** retourne un pointeur vers une interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

4.  Interrogez les notifications d’événements enregistrées en effectuant des appels répétés à la méthode [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .
5.  Lorsque vous avez terminé, Libérez l’énumérateur qui pointe vers l’objet [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

    Vous pouvez libérer le pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) associé à l’inscription. Le fait de libérer le pointeur **IWbemServices** entraîne l’arrêt de la remise des événements par WMI à tous les consommateurs temporaires associés.

 

 
