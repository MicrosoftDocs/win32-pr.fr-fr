---
title: Définir le niveau de sécurité de processus par défaut avec VBScript
description: Un script peut utiliser les paramètres d’authentification et d’emprunt d’identité WMI par défaut. Toutefois, le script peut nécessiter une connexion avec davantage de sécurité ou peut se connecter à un espace de noms qui requiert une connexion chiffrée.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7def50c94a044a521b32b75d8e04175ebe3c37ee741f5c22663924c774be1806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050277"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a>Définir le niveau de sécurité de processus par défaut avec VBScript

Un script peut utiliser les paramètres d’authentification et d’emprunt d’identité WMI par défaut. Toutefois, le script peut nécessiter une connexion avec davantage de sécurité ou peut se connecter à un espace de noms qui requiert une connexion chiffrée. Pour plus d’informations, consultez [définition de descripteurs de sécurité espace](setting-namespace-security-descriptors.md) et [demande d’une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).

Dans le cas le plus simple, un script peut utiliser les paramètres d’authentification et d’emprunt d’identité par défaut. WMI s’exécute normalement dans un hôte de service partagé et partage la même authentification que les autres processus de l’hôte. Si vous souhaitez exécuter le processus WMI avec un autre niveau d’authentification, exécutez WMI avec la commande [**winmgmt**](winmgmt.md) avec le commutateur **/standalonehost** et définissez le niveau d’authentification pour WMI en général. Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).

Le script suivant utilise les paramètres par défaut pour l’emprunt d’identité et les niveaux d’authentification.


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



Vous pouvez également utiliser un [moniker](constructing-a-moniker-string.md) dans un appel à [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)et définir les paramètres de sécurité par défaut, comme dans l’exemple suivant.


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



Pour plus d’informations sur la définition d’un autre niveau d’emprunt d’identité ou d’authentification dans un script, ou pour définir les valeurs par défaut d’un ordinateur, consultez les rubriques suivantes :

-   [Modification des informations d’authentification par défaut à l’aide de VBScript](#changing-the-default-authentication-credentials-using-vbscript)
-   [modification de l’emprunt d’identité par défaut Paramètres à l’aide de VBScript](#changing-the-default-impersonation-levels-using-vbscript)
-   [Définition du niveau d’emprunt d’identité par défaut à l’aide du Registre](#setting-the-default-impersonation-level-using-the-registry)
-   [Accès à l’objet SWbemSecurity dans VBScript](#accessing-the-swbemsecurity-object-in-vbscript)
-   [**SWbemSecurity**](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a>Modification des informations d’authentification par défaut à l’aide de VBScript

Vous pouvez modifier le niveau d’authentification dans un script à l’aide d’une chaîne de [moniker](constructing-a-moniker-string.md) et des objets [**SWbemLocator**](swbemlocator.md) et [**SWbemSecurity**](swbemsecurity.md) .

Le niveau d’authentification doit être défini en fonction des exigences du système d’exploitation cible auquel vous vous connectez. Pour plus d’informations, consultez [connexion entre différents systèmes d’exploitation](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

L’exemple de code VBScript suivant montre comment modifier le niveau d’authentification dans un script qui obtient les données d’espace libre à partir d’un ordinateur distant nommé « Serveur1 ».


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



Dans connexions de moniker de script à WMI, utilisez le nom abrégé indiqué dans la colonne « Nom/Description du moniker » du tableau ci-dessous. Par exemple, dans le script suivant, le niveau d’authentification est défini sur **WbemAuthenticationLevelPktIntegrity**.


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



Le tableau suivant répertorie les niveaux d’authentification que vous pouvez définir. Ces niveaux sont définis dans wbemdisp. tlb dans l’énumération [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).



| Nom/valeur                                                      | Description                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WbemAuthenticationLevelDefault**<br/> 0<br/>      | Moniker : par défaut<br/> WMI utilise le paramètre d’authentification par défaut Windows. Il s’agit du paramètre recommandé qui permet à WMI de négocier au niveau requis par le serveur qui retourne des données. Toutefois, si l’espace de noms requiert le chiffrement, utilisez **WbemAuthenticationLevelPktPrivacy**.<br/> |
| **WbemAuthenticationLevelNone**<br/> 1<br/>         | Moniker : aucun<br/> N’utilise aucune authentification.<br/>                                                                                                                                                                                                                                            |
| **WbemAuthenticationLevelConnect**<br/> 2<br/>      | Moniker : Connecter<br/> Authentifie les informations d’identification du client uniquement lorsque le client établit une relation avec le serveur.<br/>                                                                                                                                                    |
| **WbemAuthenticationLevelCall**<br/> 3<br/>         | Appeler<br/> Authentifie uniquement au début de chaque appel lorsque le serveur reçoit la demande.<br/>                                                                                                                                                                                      |
| **WbemAuthenticationLevelPkt**<br/> 4<br/>          | Moniker : PKT<br/> Authentifie que toutes les données reçues proviennent du client attendu.<br/>                                                                                                                                                                                                   |
| **WbemAuthenticationLevelPktIntegrity**<br/> 5<br/> | Moniker : PktIntegrity<br/> Authentifie et vérifie qu’aucune des données transférées entre le client et le serveur n’a été modifiée.<br/>                                                                                                                                                  |
| **WbemAuthenticationLevelPktPrivacy**<br/> 6<br/>   | Moniker : PktPrivacy<br/> Authentifie tous les niveaux d’emprunt d’identité précédents et chiffre la valeur d’argument de chaque appel de procédure distante. Utilisez ce paramètre si l’espace de noms auquel vous vous connectez requiert une connexion chiffrée.<br/>                                               |



 

Pour déterminer si un appel a réussi, vérifiez la valeur de retour après avoir modifié le niveau d’authentification.

Par exemple, étant donné que les connexions locales ont toujours un niveau d’authentification de **wbemAuthenticationLevelPktPrivacy**, l’exemple suivant ne parvient pas à définir le niveau d’authentification, car il se connecte à l’ordinateur local.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



Un fournisseur peut définir la sécurité sur un espace de noms afin qu’aucune donnée ne soit retournée, sauf si vous utilisez la confidentialité des paquets (PktPrivacy) dans votre connexion à cet espace de noms. Cela permet de s’assurer que les données sont chiffrées lorsqu’elles traversent le réseau. Si vous essayez de définir un niveau d’authentification inférieur, vous obtiendrez un message d’accès refusé. Pour plus d’informations, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md).

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a>Modification des niveaux d’emprunt d’identité par défaut à l’aide de VBScript

Lorsque vous effectuez des appels à l’API de script pour WMI, il est recommandé d’utiliser les valeurs par défaut fournies par WMI pour le niveau d’emprunt d’identité. Les appels distants et certains fournisseurs avec plusieurs sauts réseau nécessitent un niveau d’emprunt d’identité supérieur à celui utilisé par WMI. Si le niveau d’emprunt d’identité n’est pas suffisant, un fournisseur peut refuser une demande ou fournir des informations incomplètes.

Si vous ne définissez pas le niveau d’emprunt d’identité dans un moniker ou en définissant [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) sur un objet sécurisable, définissez le niveau d’emprunt d’identité DCOM par défaut pour le système d’exploitation. Le niveau d’emprunt d’identité doit être défini en fonction des exigences du système d’exploitation cible auquel vous vous connectez. Pour plus d’informations, consultez [connexion entre différents systèmes d’exploitation](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

L’exemple de code VBScript suivant illustre la modification du niveau d’emprunt d’identité dans le script indiqué ci-dessus.


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



Le tableau suivant répertorie les niveaux d’authentification dans [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) qui utilisent.



| Nom/valeur                                                    | Description                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wbemImpersonationLevelAnonymous**<br/> 1<br/>   | Moniker : anonyme<br/> Masque les informations d'identification de l'appelant. Les appels à WMI peuvent échouer avec ce niveau d'emprunt d'identité.<br/>                                                                                                  |
| **wbemImpersonationLevelIdentify**<br/> 2<br/>    | Moniker : identifier<br/> Permet aux objets d'interroger les informations d'identification de l'appelant. Les appels à WMI peuvent échouer avec ce niveau d'emprunt d'identité.<br/>                                                                                 |
| **wbemImpersonationLevelImpersonate**<br/> 3<br/> | Moniker : emprunter l’identité<br/> Permet aux objets d'utiliser les informations d'identification de l'appelant. Il s’agit du niveau d’emprunt d’identité recommandé pour l’API de script pour les appels WMI.<br/>                                                        |
| **wbemImpersonationLevelDelegate**<br/> 4<br/>    | Moniker : délégué<br/> Permet aux objets d'autoriser d'autres objets à utiliser les informations d'identification de l'appelant. Cet emprunt d’identité fonctionne avec l’API de script pour les appels WMI, mais peut constituer un risque de sécurité inutile.<br/> |



 

L’exemple suivant montre comment définir l’emprunt d’identité dans une chaîne de moniker lors de l’obtention d’une instance spécifique de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).

## <a name="setting-the-default-impersonation-level-using-the-registry"></a>Définition du niveau d’emprunt d’identité par défaut à l’aide du Registre

Si vous avez accès au registre, vous pouvez également définir la clé de registre de niveau d’emprunt d’identité par défaut. Cette clé spécifie le niveau d’emprunt d’identité que l’API de script pour WMI utilise, sauf indication contraire. Le chemin d’accès suivant identifie le chemin d’accès au registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **niveau d’emprunt d’identité par défaut**

Par défaut, la clé de registre a la valeur 3, en spécifiant le niveau d’emprunt d’identité emprunter l’identité. Certains fournisseurs peuvent nécessiter un niveau d’emprunt d’identité plus élevé.

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a>Accès à l’objet SWbemSecurity dans VBScript

Vous pouvez également définir le niveau d’emprunt d’identité à partir de l’objet de sécurité [**SWbemSecurity**](swbemsecurity.md) , qui apparaît en tant que propriété de [**sécurité \_**](swbemservices-security-.md) des objets [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md)et [**SwbemLocator**](swbemlocator.md) .

WMI transmet le paramètre de sécurité d’un objet parent aux descendants de l’objet d’origine. Par conséquent, vous pouvez définir le niveau d’emprunt d’identité d’un objet [**SWbemServices**](swbemservices.md) après vous être connecté à WMI et les appels d’API à l’aide de cet objet ou des objets créés à partir de celui-ci, tels que des objets de type [**SWbemObject**](swbemobject.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Sécurisation des clients de script](securing-scripting-clients.md)
</dt> </dl>

 

