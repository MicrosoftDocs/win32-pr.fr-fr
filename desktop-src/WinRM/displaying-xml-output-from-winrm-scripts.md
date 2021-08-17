---
title: Affichage de la sortie XML des scripts WinRM
description: Windows Les scripts de gestion à distance renvoient du code XML plutôt que des objets. Le code XML n’est pas dans un format explicite. vous pouvez utiliser les méthodes de l’API MSXML et le fichier XSL préinstallé pour transformer les données au format lisible.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df5c27c1fe22ae87395357aeefe681af7c041420d32b7bccbf595fab38bb060b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680019"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Affichage de la sortie XML des scripts WinRM

Windows Les scripts de gestion à distance renvoient du code XML plutôt que des objets. Le code XML n’est pas dans un format explicite. vous pouvez utiliser les méthodes de l’API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) et le fichier XSL préinstallé pour transformer les données au format lisible.

pour plus d’informations sur la sortie xml WinRM et des exemples de données brutes et au format xml, consultez [script dans Windows Remote Management](scripting-in-windows-remote-management.md).

L’outil de ligne de commande **WinRM** est fourni avec un fichier de transformation nommé WsmTxt. xsl qui affiche la sortie sous forme de tableau. si votre script fournit ce fichier aux méthodes de MSXML qui exécutent transforme, la sortie apparaît comme la sortie de l’outil **Winrm** .

**Pour mettre en forme une sortie XML brute**

1.  Créez l’objet [**WSMan**](wsman.md) et créez une session.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  créez MSXML objets qui représentent la sortie de réponse XML et la transformation XSL.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Obtenir des données par le biais de méthodes d’objet de [**session**](session.md) .

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  fournissez la réponse à la méthode MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) et à la méthode [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) pour stocker le fichier de transformation.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  utilisez la méthode MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) et affichez ou enregistrez la sortie.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

L’exemple de code VBScript suivant montre le script complet.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>Ajout d’une sous-routine portable pour transformer du code XML en scripts

Vous pouvez ajouter une sous-routine à vos scripts qui utilisent le fichier XSL préinstallé pour convertir la sortie XML brute d’un script WinRM en un format tabulaire.

la sous-routine suivante utilise des appels aux méthodes de script MSXML pour fournir la sortie à WsmTxt. xsl.


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



La sous-routine suivante transforme chaque ligne de vos données comme indiqué dans l’exemple suivant.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
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

 

 