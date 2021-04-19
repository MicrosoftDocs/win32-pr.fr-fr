---
title: Interrogation d’instances spécifiques d’une ressource
description: L’appel à session. Enumerate possède des paramètres facultatifs qui réduisent l’énumération dans une requête.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510684"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Interrogation d’instances spécifiques d’une ressource

L’appel à [**session. Enumerate**](session-enumerate.md) possède des paramètres facultatifs qui réduisent l’énumération dans une requête. Étant donné que l' [API de script WinRM](winrm-scripting-api.md) et l' [API C++ WinRM](winrm-c---api.md) sont étroitement modélisées sur le protocole de WS-Management sous-jacent, les paramètres utilisent la même terminologie pour l’interrogation que le protocole : le langage de *filtre* et de *filtre*.

Vous pouvez utiliser les paramètres de filtre et de dialecte de [**session. Enumerate**](session-enumerate.md) , ou vous pouvez créer et fournir un objet [**ResourceLocator**](resourcelocator.md) et la méthode [**AddSelector**](resourcelocator-addselector.md) , mais vous ne pouvez pas les deux.

Cette procédure exécute une requête pour les cartes réseau pour lesquelles TCP/IP est lié et activé. La requête demande toutes les instances de [**\_ NetworkAdapterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) dont la propriété **IpEnabled** a la valeur **true**. À l’exception de l’ajout du *filtre* et du *dialecte*, la requête est gérée comme une énumération simple.

Dans cet exemple, le nom de ressource de la constante de ressource est représenté par un astérisque « \* », car le nom de la classe, [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), est déjà mentionné dans la chaîne *strFilter* .

**Pour interroger des instances spécifiques d’une ressource**

1.  Pour faciliter la lecture, définissez les URI en tant que constantes.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  Créer une session.

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  Construire la chaîne de filtrage. Windows Remote Management prend en charge [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) comme dialecte de filtre.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  Définissez toutes les [**constantes d’énumération**](enumeration-constants.md) requises dans le paramètre *Flags* .

    Sachez que si les indicateurs incluent les [**constantes d’énumération**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow** , le service WinRM retourne le code d’erreur le **mode de \_ \_ polymorphisme WSMan n’est \_ \_ pas pris en charge**.

5.  Appelez la méthode [**session. Enumerate**](session-enumerate.md) . Cet appel démarre une énumération. La méthode **session. Enumerate** établit un contexte d’énumération de protocole WS-Management, conservé dans l’objet [**énumérateur**](enumerator.md) .

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Appelez la méthode [**Enumerator. ReadItem**](enumerator-readitem.md) pour obtenir l’élément suivant des résultats. Dans WS-Management protocole, cela correspond à l’opération d’extraction. Utilisez la méthode [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) comme contrôle pour savoir quand arrêter la lecture.

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

L’exemple de code VBScript suivant montre le script complet.


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
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

[Utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[Énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 