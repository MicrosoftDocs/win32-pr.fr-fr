---
title: Affichage de la sortie XML des scripts WinRM
description: Les scripts de Windows Remote Management renvoient du code XML plutôt que des objets. Le code XML n’est pas dans un format explicite. Vous pouvez utiliser les méthodes de l’API MSXML et le fichier XSL préinstallé pour transformer les données au format lisible.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c70dd0a61181f6fc61e685641ff0ed5e3d43ffe8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031633"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="e1978-105">Affichage de la sortie XML des scripts WinRM</span><span class="sxs-lookup"><span data-stu-id="e1978-105">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="e1978-106">Les scripts de Windows Remote Management renvoient du code XML plutôt que des objets.</span><span class="sxs-lookup"><span data-stu-id="e1978-106">Windows Remote Management scripts return XML rather than objects.</span></span> <span data-ttu-id="e1978-107">Le code XML n’est pas dans un format explicite.</span><span class="sxs-lookup"><span data-stu-id="e1978-107">The XML is not in a human-readable format.</span></span> <span data-ttu-id="e1978-108">Vous pouvez utiliser les méthodes de l’API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) et le fichier XSL préinstallé pour transformer les données au format lisible.</span><span class="sxs-lookup"><span data-stu-id="e1978-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API and the preinstalled XSL file to transform the data into human-readable format.</span></span>

<span data-ttu-id="e1978-109">Pour plus d’informations sur la sortie XML WinRM et des exemples de données brutes et au format XML, consultez [script dans Windows Remote Management](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="e1978-109">For more information about WinRM XML output and examples of raw and formatted XML, see [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="e1978-110">L’outil de ligne de commande **WinRM** est fourni avec un fichier de transformation nommé WsmTxt. xsl qui affiche la sortie sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="e1978-110">The **Winrm** command-line tool comes with a transform file named WsmTxt.xsl that displays output in a tabular form.</span></span> <span data-ttu-id="e1978-111">Si votre script fournit ce fichier aux méthodes MSXML qui exécutent transforme, la sortie apparaît comme la sortie de l’outil **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="e1978-111">If your script supplies this file to the MSXML methods that perform tranforms, the output appears the same as the output from the **Winrm** tool.</span></span>

<span data-ttu-id="e1978-112">**Pour mettre en forme une sortie XML brute**</span><span class="sxs-lookup"><span data-stu-id="e1978-112">**To format raw XML output**</span></span>

1.  <span data-ttu-id="e1978-113">Créez l’objet [**WSMan**](wsman.md) et créez une session.</span><span class="sxs-lookup"><span data-stu-id="e1978-113">Create the [**WSMan**](wsman.md) object and create a session.</span></span>

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  <span data-ttu-id="e1978-114">Créez des objets MSXML qui représentent la sortie de réponse XML et la transformation XSL.</span><span class="sxs-lookup"><span data-stu-id="e1978-114">Create MSXML objects that represent the XML response output and the XSL transform.</span></span>

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  <span data-ttu-id="e1978-115">Obtenir des données par le biais de méthodes d’objet de [**session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="e1978-115">Obtain data through [**Session**](session.md) object methods.</span></span>

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  <span data-ttu-id="e1978-116">Fournissez la réponse à la méthode MSXML [LoadXml](/previous-versions/windows/desktop/ms754585(v=vs.85)) et la méthode [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) pour stocker le fichier de transformation.</span><span class="sxs-lookup"><span data-stu-id="e1978-116">Supply the response to the MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) method and the [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) method to store the transform file.</span></span>

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  <span data-ttu-id="e1978-117">Utilisez la méthode MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) et affichez ou enregistrez la sortie.</span><span class="sxs-lookup"><span data-stu-id="e1978-117">Use the MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) method and display or save the output.</span></span>

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

<span data-ttu-id="e1978-118">L’exemple de code VBScript suivant montre le script complet.</span><span class="sxs-lookup"><span data-stu-id="e1978-118">The following VBScript code example shows the complete script.</span></span>


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



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a><span data-ttu-id="e1978-119">Ajout d’une sous-routine portable pour transformer du code XML en scripts</span><span class="sxs-lookup"><span data-stu-id="e1978-119">Adding a Portable Subroutine to Transform XML to Your Scripts</span></span>

<span data-ttu-id="e1978-120">Vous pouvez ajouter une sous-routine à vos scripts qui utilisent le fichier XSL préinstallé pour convertir la sortie XML brute d’un script WinRM en un format tabulaire.</span><span class="sxs-lookup"><span data-stu-id="e1978-120">You can add a subroutine to your scripts that uses the preinstalled XSL file to convert the raw XML output from a WinRM script to a tabular form.</span></span>

<span data-ttu-id="e1978-121">La sous-routine suivante utilise des appels aux méthodes de script MSXML pour fournir la sortie à WsmTxt. Xsl.</span><span class="sxs-lookup"><span data-stu-id="e1978-121">The following subroutine uses calls to the MSXML scripting methods to supply the output to WsmTxt.xsl.</span></span>


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



<span data-ttu-id="e1978-122">La sous-routine suivante transforme chaque ligne de vos données comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e1978-122">The following subroutine transforms each line of your data as shown in the following example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e1978-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1978-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1978-124">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="e1978-124">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="e1978-125">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="e1978-125">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="e1978-126">Référence Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="e1978-126">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 