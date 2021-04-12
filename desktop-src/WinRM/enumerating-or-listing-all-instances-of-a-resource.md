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
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a><span data-ttu-id="3e9fa-103">Énumération ou liste de toutes les instances d’une ressource</span><span class="sxs-lookup"><span data-stu-id="3e9fa-103">Enumerating or Listing All Instances of a Resource</span></span>

<span data-ttu-id="3e9fa-104">La méthode [**session. Enumerate**](session-enumerate.md) est l’approche Windows Remote Management pour obtenir toutes les instances d’une ressource spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-104">The [**Session.Enumerate**](session-enumerate.md) method is the Windows Remote Management approach to obtaining all the instances of a specified resource.</span></span>

<span data-ttu-id="3e9fa-105">La méthode [**session. Enumerate**](session-enumerate.md) n’obtient pas de collection dans un objet [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) comme un [**SWbemService.Exeappel cQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) avec une [requête WMI](/windows/desktop/WmiSdk/querying-wmi) comme paramètre (par exemple, `ExecQuery("SELECT * from Win32_LogicalDisk")` ), ou un appel à une méthode telle que [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="3e9fa-105">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in a [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) object like a [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) call with a [WMI query](/windows/desktop/WmiSdk/querying-wmi) as a parameter (for example, `ExecQuery("SELECT * from Win32_LogicalDisk")`), or a call to a method like [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span> <span data-ttu-id="3e9fa-106">Les méthodes de l’objet **session. Enumerate** et [**Enumerator**](enumerator.md) sont bien plus similaires à celles de l’objet de script [TextStream](/previous-versions//312a5kbt(v=vs.85)) utilisé pour la lecture de fichiers en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-106">**Session.Enumerate** and the [**Enumerator**](enumerator.md) object methods are much more similar to the operation of the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object that is used for reading files as a stream.</span></span>

<span data-ttu-id="3e9fa-107">Pour lire des fichiers en tant que flux de texte, vous devez créer l’objet [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script et appeler la méthode [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) pour lire chaque ligne du fichier.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-107">To read files as a text stream, you must create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="3e9fa-108">De la même façon, vous pouvez appeler la méthode [**session. Enumerate**](session-enumerate.md) pour obtenir un objet [**énumérateur**](enumerator.md) et appeler la méthode [**Enumerator. ReadItem**](enumerator-readitem.md) pour obtenir l’élément suivant.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-108">In a similar way, you can call the [**Session.Enumerate**](session-enumerate.md) method to obtain an [**Enumerator**](enumerator.md) object and call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to get the next item.</span></span> <span data-ttu-id="3e9fa-109">Comme c’est le cas lors de la lecture à partir du fichier texte, vous pouvez appeler la propriété [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) pour vérifier si vous avez atteint la fin des éléments de données.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-109">As is the case when reading from the text file, you can call the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

<span data-ttu-id="3e9fa-110">**Pour énumérer une ressource**</span><span class="sxs-lookup"><span data-stu-id="3e9fa-110">**To enumerate a resource**</span></span>

1.  <span data-ttu-id="3e9fa-111">Créer une session.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-111">Create a session.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  <span data-ttu-id="3e9fa-112">Construisez l’URI pour identifier la ressource.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-112">Construct the URI to identify the resource.</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  <span data-ttu-id="3e9fa-113">Appelez la méthode [**session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="3e9fa-113">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="3e9fa-114">Cet appel démarre une énumération.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-114">This call starts an enumeration.</span></span> <span data-ttu-id="3e9fa-115">Dans WinRM, une opération d’énumération n’obtient pas de collection de la même façon que WMI.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-115">In WinRM, an enumeration operation does not obtain a collection in the same way that WMI does.</span></span> <span data-ttu-id="3e9fa-116">Au lieu de cela, la méthode **session. Enumerate** établit un contexte d’énumération de protocole WS-Management qui est conservé dans l’objet [**énumérateur**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="3e9fa-116">Instead, the **Session.Enumerate** method establishes a WS-Management protocol enumeration context that is maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  <span data-ttu-id="3e9fa-117">Appelez la méthode [**Enumerator. ReadItem**](enumerator-readitem.md) pour obtenir l’élément suivant des résultats.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-117">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="3e9fa-118">Dans WS-Management protocole, cela correspond à l’opération d’extraction.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-118">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="3e9fa-119">Utilisez la méthode [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) comme contrôle pour savoir quand arrêter la lecture.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-119">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

<span data-ttu-id="3e9fa-120">L’exemple de code VBScript suivant montre le script complet.</span><span class="sxs-lookup"><span data-stu-id="3e9fa-120">The following VBScript code example shows the complete script.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3e9fa-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e9fa-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e9fa-122">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="3e9fa-122">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="3e9fa-123">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="3e9fa-123">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="3e9fa-124">Référence Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="3e9fa-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 