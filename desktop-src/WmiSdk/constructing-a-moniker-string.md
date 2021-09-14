---
description: Le format de chaîne de moniker est semblable à celui d’un chemin d’accès d’objet WMI standard. Pour plus d’informations, consultez Configuration requise pour le chemin d’accès de l’objet WMI.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Construction d’une chaîne de moniker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120469"
---
# <a name="constructing-a-moniker-string"></a>Construction d’une chaîne de moniker

Le format de chaîne de moniker est semblable à celui d’un chemin d’accès d’objet WMI standard. Pour plus d’informations, consultez [Configuration requise pour le chemin d’accès de l’objet WMI](wmi-object-path-requirements.md).

Un moniker comprend les parties suivantes :

-   Préfixe WinMgmts : (obligatoire). le préfixe indique à l’hôte de script Windows (WSH) que le code suivant utilisera les objets de l' [API de script](scripting-api-objects.md).
-   Un composant paramètres de sécurité (facultatif)
-   Composant de chemin d’accès d’objet WMI (facultatif)

Vous ne pouvez pas spécifier un mot de passe dans une chaîne de moniker WMI. Si vous devez modifier le mot de passe (paramètre *strPassword* ) ou le type d’authentification (paramètre *strAuthority* ) lors de la connexion à WMI, appelez [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). N’oubliez pas que vous pouvez uniquement spécifier le mot de passe et l’autorité dans connexions aux ordinateurs distants. Toute tentative de définition de ces paramètres dans un script en cours d’exécution sur l’ordinateur local génère une erreur. pour plus d’informations sur l’utilisation des paramètres de sécurité et des composants de chemin d’accès de l’objet, consultez [Paramètres de sécurité WMI](/previous-versions/tn-archive/ee156574(v=technet.10)).

Le moniker suivant spécifie l’objet [**SWbemServices**](swbemservices.md) qui représente la valeur par défaut racine de l’espace de noms \\ , avec l’emprunt d’identité activé et le privilège wbemPrivilegeDebug (SeDebugPrivilege) activé, et le privilège wbemPrivilegeSecurity (SeSecurityPrivilege) désactivé.


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> Tous les littéraux de chaîne ne respectent pas la casse.
>
> Le préfixe «  ! » sur un privilège indique que le privilège doit être désactivé. l’omission de ce préfixe implique que le privilège doit être activé.
>
> Le préfixe «  ! » est utilisé sur le nom ou l’espace de noms de l’ordinateur lorsque les paramètres de sécurité sont spécifiés entre crochets avant le nom ou l’espace de noms de l’ordinateur.

 

Les assignations par défaut suivantes sont autorisées lors de la spécification du chemin d’accès à l’objet :

-   Le nom de l’ordinateur peut être omis du chemin d’accès de l’objet. dans ce cas, le nom de l’ordinateur local est utilisé.
-   L’espace de noms peut être omis du chemin d’accès de l’objet, auquel cas l’espace de noms par défaut est utilisé.

    Cela est déterminé par la valeur de la clé de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **par défaut espace de noms**, la valeur par défaut est « root \\ cimv2 ».

-   Une classe ou une instance peut également être spécifiée, auquel cas l’objet retourné est un objet WMI plutôt qu’un objet services.

> [!Note]  
> Si une classe ou une instance est spécifiée, vous ne pouvez pas omettre l’espace de noms lors de la spécification du nom de l’ordinateur.

 

Pour obtenir une référence des constantes de privilège utilisées sur la chaîne de moniker WMI, consultez [constantes de privilège](privilege-constants.md)et descripteurs « Scripting Short Name ».

## <a name="valid-moniker-strings"></a>Chaînes de moniker valides

Les exemples suivants illustrent des chaînes de moniker valides.

Le moniker suivant identifie l’espace de noms par défaut sur l’ordinateur local. Un objet [**SWbemServices**](swbemservices.md) est retourné.


```VB
WinMgmts:
```



Le moniker suivant identifie l’espace de noms par défaut sur l’ordinateur MonServeur. Un objet [**SWbemServices**](swbemservices.md) est retourné.


```VB
"WinMgmts://myServer"
```



Le moniker suivant identifie l' \\ espace de noms CIMV2 racine sur l’ordinateur MonServeur. Un objet [**SWbemServices**](swbemservices.md) est retourné.


```VB
"WinMgmts://myServer/root/cimv2"
```



Le moniker suivant identifie l' \\ espace de noms CIMV2 racine sur le serveur local. Un objet [**SWbemServices**](swbemservices.md) est retourné.


```VB
"WinMgmts:root/cimv2"
```



Le moniker suivant identifie la classe de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans l' \\ espace de noms CIMV2 racine sur le serveur MyServer. Un objet [**SWbemObject**](swbemobject.md) est retourné.


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



Le moniker suivant identifie la classe de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans l' \\ espace de noms CIMV2 racine sur le serveur local. Un objet [**SWbemObject**](swbemobject.md) est retourné.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



Le moniker suivant identifie la classe de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans l’espace de noms par défaut sur le serveur local. Un objet [**SWbemObject**](swbemobject.md) est retourné.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



Le moniker suivant identifie l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondant au lecteur C : dans l’espace de noms de script par défaut sur le serveur local. Un objet [**SWbemObject**](swbemobject.md) est retourné. L’espace de noms par défaut pour les scripts est déterminé par le paramètre de configuration de l’espace de noms par défaut tel que spécifié dans le contrôle WMI. Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



Le moniker suivant identifie l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondant au lecteur C : dans l' \\ espace de noms CIMV2 racine sur le serveur monserveur. Un objet [**SWbemObject**](swbemobject.md) est retourné.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



Le moniker suivant identifie l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondant au lecteur C : dans l' \\ espace de noms CIMV2 racine sur le serveur local. Un objet [**SWbemObject**](swbemobject.md) est retourné.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



Le moniker suivant identifie l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondant au lecteur C : dans l’espace de noms par défaut sur le serveur local. Un objet [**SWbemObject**](swbemobject.md) est retourné.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



le moniker suivant définit le niveau d’emprunt d’identité sur emprunter l’identité et définit le SE \_ privilège de débogage.


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



le moniker suivant définit le niveau d’emprunt d’identité sur emprunter l’identité et définit le SE \_ privilège de débogage. elle révoque également le privilège d' \_ arrêt SE.


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



Le moniker suivant récupère les descriptions localisées de l’anglais américain pour la classe **MyClass** à partir de l' \\ espace de noms WMI racine.


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



Le moniker suivant demande l’authentification Kerberos à l’aide du serveur mondomaine principal \\ .


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



Le moniker suivant demande l’authentification NTLM à l’aide du domaine mydomain.


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



L’exemple de code VBScript suivant montre comment combiner des paramètres de sécurité et de paramètres régionaux dans un moniker.


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Bien que les monikers fournissent un accès plus direct aux objets, dans certains cas, l’utilisation répétée de monikers peut être moins efficace que le code équivalent qui se connecte explicitement à WMI. Si les performances de l’application sont un facteur important, envisagez d’utiliser les autres mécanismes.
>
> Il n’est pas possible d’utiliser la fonction **GetObject** fournie par VBScript pour mettre à jour ou définir des données lors de l’exécution de scripts incorporés dans une page HTML, car Microsoft Internet Explorer refuse l’utilisation de cet appel pour des raisons de sécurité.

 

 

 
