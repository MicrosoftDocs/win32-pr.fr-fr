---
description: Vous pouvez créer une connexion à distance à WMI avec VBScript en créant un objet de connexion. Cet objet contient le nom de l’ordinateur, l’espace de noms WMI auquel vous souhaitez vous connecter, ainsi que les informations d’identification et les niveaux d’authentification appropriés.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Connexion à WMI à distance avec VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520229"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a>Connexion à WMI à distance avec VBScript

Vous pouvez créer une connexion à distance à WMI avec VBScript en créant un objet de connexion. Cet objet contient le nom de l’ordinateur, l’espace de noms WMI auquel vous souhaitez vous connecter, ainsi que les informations d’identification et les niveaux d’authentification appropriés.

**Pour vous connecter à un système distant à l’aide de VBScript**

1.  Spécifiez les informations de connexion, telles que le nom de l’ordinateur distant, les informations d’identification et le niveau d’authentification pour la connexion.

    Si vous vous connectez à un ordinateur distant à l’aide des mêmes informations d’identification (domaine et nom d’utilisateur) que vous avez ouvert une session, vous pouvez spécifier les informations de connexion dans un [moniker](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), comme décrit dans l’exemple de code suivant.

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    En règle générale, vous devez spécifier l’espace de noms WMI auquel se connecter sur l’ordinateur distant. En effet, il est possible que l’espace de noms par défaut ne soit pas le même sur des ordinateurs différents. La spécification de l’espace de noms garantit que vous vous connectez au même espace de noms sur tous les ordinateurs.

    Pour plus d’informations sur les constantes et les chaînes de script VBScript pour l’utilisation de la connexion moniker, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

2.  Si vous vous connectez à un ordinateur distant dans un autre domaine ou à l’aide d’un nom d’utilisateur et d’un mot de passe différents, vous devez utiliser la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

    Comme pour un moniker, vous utilisez **ConnectServer** pour spécifier les informations d’identification, le niveau d’authentification et l’espace de noms pour la connexion à distance. L’exemple de code suivant décrit l’utilisation de ConnectServer pour accéder à un ordinateur distant à l’aide d’un compte et d’un mot de passe d’administrateur.

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  Quand vous utilisez la fonction [**ConnectServer**](swbemlocator-connectserver.md) pour des connexions distantes, définissez l’emprunt d’identité et l’authentification sur l’objet de sécurité obtenu par un appel à [**SWbemServices. Security**](swbemservices-security-.md). Vous pouvez utiliser l’énumération [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) pour spécifier le niveau d’emprunt d’identité.

    L’exemple de code suivant définit le niveau d’emprunt d’identité pour l’exemple de code VBScript précédent.

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    Notez que certaines connexions nécessitent un niveau d’authentification spécifique. Pour plus d’informations, consultez Définition de la [sécurité des processus des applications clientes](setting-client-application-process-security.md) et [sécurisation des scripts des clients](securing-scripting-clients.md).

    En particulier, vous devez définir le niveau d’authentification sur la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C** ou 6 si l’espace de noms sur lequel vous vous connectez sur l’ordinateur distant requiert une connexion chiffrée avant de retourner des données. Vous pouvez également utiliser ce niveau d’authentification, même si l’espace de noms ne l’exige pas. Cela permet de s’assurer que les données sont chiffrées lorsqu’elles traversent le réseau. Si vous tentez de définir un niveau d’authentification inférieur à celui autorisé, un message d’accès refusé est retourné. Pour plus d’informations, consultez [la page exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).

Une fois que vous avez établi votre connexion, vous pouvez continuer à accéder aux données WMI. Pour plus d’informations, consultez [tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md).

## <a name="examples"></a>Exemples

Pour obtenir un exemple VBScript plus grand, consultez la section exemples dans la page de référence de [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

L’exemple de code VBScript suivant se connecte à un groupe d’ordinateurs distants dans le même domaine en créant un tableau de noms d’ordinateurs distants, puis en affichant les noms des appareils Plug-and-Play (instances de [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)) sur chaque ordinateur. Pour exécuter le script ci-dessous, vous devez être administrateur sur les ordinateurs distants. Notez que le « \\ \\ » requis avant le nom de l’ordinateur distant est ajouté par le script après le paramètre niveau d’emprunt d’identité. Pour plus d’informations sur les chemins d’accès WMI, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



L’exemple de code VBScript suivant vous permet de vous connecter à un ordinateur distant à l’aide d’autres informations d’identification. Par exemple, un ordinateur distant dans un domaine différent ou qui se connecte à un ordinateur distant nécessitant un nom d’utilisateur et un mot de passe différents. Dans ce cas, utilisez la connexion [**SWbemServices. ConnectServer**](swbemlocator-connectserver.md) .


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
