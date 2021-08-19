---
title: Obtention de données à partir d’un ordinateur distant
description: Vous pouvez obtenir des données ou gérer des ressources sur des ordinateurs distants, ainsi que sur l’ordinateur local. la connexion à un ordinateur distant dans un script Windows Remote Management est très similaire à l’établissement d’une connexion locale.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf3531e19c0848691ededa0c3b6b2fad642de33c2a5f2d465ac899716970a512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823406"
---
# <a name="obtaining-data-from-a-remote-computer"></a>Obtention de données à partir d’un ordinateur distant

Vous pouvez obtenir des données ou gérer des ressources sur des ordinateurs distants, ainsi que sur l’ordinateur local. la connexion à un ordinateur distant dans un script Windows Remote Management est très similaire à l’établissement d’une connexion locale. Les données d’instance WMI sont disponibles et, si l’ordinateur distant dispose d’un matériel BMC capable de communiquer à l’aide du protocole WS-Management, les données [IPMI (Intelligent Platform Management Interface)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) sont également disponibles. pour plus d’informations, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md) et [gestion du matériel à distance](remote-hardware-management.md).

Vous devrez peut-être créer un objet [**ConnectionOptions**](connectionoptions.md) pour spécifier des informations sur le type d’authentification demandé pour l’ouverture de session.

Si le compte sur l’ordinateur distant possède les mêmes nom d’utilisateur et mot de passe d’ouverture de session, les seules informations supplémentaires dont vous avez besoin sont le transport, le nom de domaine et le nom de l’ordinateur. En raison du [contrôle de compte d’utilisateur (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), le compte distant doit être un compte de domaine et un membre du groupe administrateurs d’ordinateurs distants. Si le compte est un membre de l’ordinateur local du groupe administrateurs, le contrôle de compte d’utilisateur n’autorise pas l’accès au service WinRM. pour accéder à un service WinRM distant dans un groupe de travail, vous devez désactiver le filtrage UAC pour les comptes locaux en créant l’entrée de registre DWORD suivante et en définissant sa valeur sur 1 : **\[ HKEY \_ local \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ policies \\ System \] LocalAccountTokenFilterPolicy**.

**Pour vous connecter à un ordinateur distant en utilisant votre nom d’utilisateur et votre mot de passe d’ouverture de session**

1.  Spécifiez l’ordinateur cible avec un nom de domaine complet ou une adresse IP et affectez-le à une constante. Si une adresse IPv6 est spécifiée, l’adresse doit être placée entre crochets.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Créez un objet [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  Créez la session, en spécifiant le transport, HTTP ou HTTPs et en la concaténant avec la constante représentant l’ordinateur cible.

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

L’exemple de code VBScript suivant montre le script complet. Le script comprend une sous-routine permettant de transformer les données XML brutes au format lisible par l’utilisateur. Pour plus d’informations, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md).


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



**Pour se connecter à un ordinateur distant à l’aide d’un autre compte**

1.  Spécifiez l’ordinateur cible avec un nom de domaine complet ou une adresse IP et affectez-le à une constante. Si une adresse IPv6 est spécifiée, l’adresse doit être placée entre crochets.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Créez un objet [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  Appelez la méthode [**WSMan. CreateConnectionOptions**](wsman-createconnectionoptions.md) pour créer un objet [**ConnectionOptions**](connectionoptions.md) . Le compte sur l’ordinateur distant doit être membre du groupe administrateurs de l’ordinateur local.

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  Sur l’appel [**WSman. CreateSession**](wsman-createsession.md) , spécifiez les indicateurs de connexion de session appropriés dans le paramètre *Flags* . Pour plus d’informations, consultez [sessions, constantes](session-constants.md). Spécifiez l’ordinateur cible avec un nom d’ordinateur complet ou une adresse IP et le transport (http ou https). Ce script demande l’authentification [*Kerberos*](windows-remote-management-glossary.md) auprès du service WinRM distant.

    Contrairement aux scripts WMI, vous pouvez utiliser plusieurs méthodes d’authentification dans les scripts WinRM. Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md).

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  Une fois l’objet de session disponible, vous pouvez appeler n’importe quelle méthode d’objet de [**session**](session.md) pour obtenir des données pour une ressource. Vous pouvez obtenir des données pour toutes les ressources disponibles sur l’ordinateur sur lequel la session est en cours d’exécution. Pour plus d’informations, consultez [obtention de données à partir de l’ordinateur local](obtaining-data-from-the-local-computer.md).

L’exemple de code VBScript suivant montre le script complet. Le script comprend une sous-routine permettant de transformer les données XML brutes au format lisible par l’utilisateur. Pour plus d’informations, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md). Le script spécifie l’authentification Kerberos, mais si l’ordinateur distant se trouve dans un groupe de travail et non dans un domaine, la spécification de Kerberos génère une erreur.


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[Windows Informations de référence sur la gestion à distance](windows-remote-management-reference.md)
</dt> </dl>

 

 