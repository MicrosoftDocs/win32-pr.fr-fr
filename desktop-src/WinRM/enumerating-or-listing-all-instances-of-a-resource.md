---
title: Énumération ou liste de toutes les instances d’une ressource
description: La méthode session. Enumerate est l’approche Windows Remote Management pour obtenir toutes les instances d’une ressource spécifiée.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54587ce97ec6ed5e87af8b0424a6a18d684f7698
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199321"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Énumération ou liste de toutes les instances d’une ressource

La méthode [**session. Enumerate**](session-enumerate.md) est l’approche Windows Remote Management pour obtenir toutes les instances d’une ressource spécifiée.

La méthode [**session. Enumerate**](session-enumerate.md) n’obtient pas de collection dans un objet [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) comme un [**SWbemService.Exeappel cQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) avec une [requête WMI](/windows/desktop/WmiSdk/querying-wmi) comme paramètre (par exemple, `ExecQuery("SELECT * from Win32_LogicalDisk")` ), ou un appel à une méthode telle que [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-). Les méthodes de l’objet **session. Enumerate** et [**Enumerator**](enumerator.md) sont bien plus similaires à celles de l’objet de script [TextStream](/previous-versions//312a5kbt(v=vs.85)) utilisé pour la lecture de fichiers en tant que flux.

Pour lire des fichiers en tant que flux de texte, vous devez créer l’objet [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script et appeler la méthode [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) pour lire chaque ligne du fichier. De la même façon, vous pouvez appeler la méthode [**session. Enumerate**](session-enumerate.md) pour obtenir un objet [**énumérateur**](enumerator.md) et appeler la méthode [**Enumerator. ReadItem**](enumerator-readitem.md) pour obtenir l’élément suivant. Comme c’est le cas lors de la lecture à partir du fichier texte, vous pouvez appeler la propriété [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) pour vérifier si vous avez atteint la fin des éléments de données.

**Pour énumérer une ressource**

1.  Créer une session.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  Construisez l’URI pour identifier la ressource.

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  Appelez la méthode [**session. Enumerate**](session-enumerate.md) . Cet appel démarre une énumération. Dans WinRM, une opération d’énumération n’obtient pas de collection de la même façon que WMI. Au lieu de cela, la méthode **session. Enumerate** établit un contexte d’énumération de protocole WS-Management qui est conservé dans l’objet [**énumérateur**](enumerator.md) .

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Appelez la méthode [**Enumerator. ReadItem**](enumerator-readitem.md) pour obtenir l’élément suivant des résultats. Dans WS-Management protocole, cela correspond à l’opération d’extraction. Utilisez la méthode [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) comme contrôle pour savoir quand arrêter la lecture.

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

L’exemple de code VBScript suivant montre le script complet.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[Utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[Référence Windows Remote Management](windows-remote-management-reference.md)
</dt> </dl>

 

 