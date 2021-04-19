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
# <a name="querying-for-specific-instances-of-a-resource"></a><span data-ttu-id="dec22-103">Interrogation d’instances spécifiques d’une ressource</span><span class="sxs-lookup"><span data-stu-id="dec22-103">Querying for Specific Instances of a Resource</span></span>

<span data-ttu-id="dec22-104">L’appel à [**session. Enumerate**](session-enumerate.md) possède des paramètres facultatifs qui réduisent l’énumération dans une requête.</span><span class="sxs-lookup"><span data-stu-id="dec22-104">The call to [**Session.Enumerate**](session-enumerate.md) has optional parameters that narrow the enumeration into a query.</span></span> <span data-ttu-id="dec22-105">Étant donné que l' [API de script WinRM](winrm-scripting-api.md) et l' [API C++ WinRM](winrm-c---api.md) sont étroitement modélisées sur le protocole de WS-Management sous-jacent, les paramètres utilisent la même terminologie pour l’interrogation que le protocole : le langage de *filtre* et de *filtre*.</span><span class="sxs-lookup"><span data-stu-id="dec22-105">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) are closely modeled on the underlying WS-Management protocol, the parameters use the same terminology for querying as the protocol—*filter* and *filter dialect*.</span></span>

<span data-ttu-id="dec22-106">Vous pouvez utiliser les paramètres de filtre et de dialecte de [**session. Enumerate**](session-enumerate.md) , ou vous pouvez créer et fournir un objet [**ResourceLocator**](resourcelocator.md) et la méthode [**AddSelector**](resourcelocator-addselector.md) , mais vous ne pouvez pas les deux.</span><span class="sxs-lookup"><span data-stu-id="dec22-106">You can either use the filter and dialect parameters of [**Session.Enumerate**](session-enumerate.md) or you can construct and supply a [**ResourceLocator**](resourcelocator.md) object and the [**AddSelector**](resourcelocator-addselector.md) method, but you cannot do both.</span></span>

<span data-ttu-id="dec22-107">Cette procédure exécute une requête pour les cartes réseau pour lesquelles TCP/IP est lié et activé.</span><span class="sxs-lookup"><span data-stu-id="dec22-107">This procedure executes a query for network adapters that have TCP/IP bound and enabled.</span></span> <span data-ttu-id="dec22-108">La requête demande toutes les instances de [**\_ NetworkAdapterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) dont la propriété **IpEnabled** a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="dec22-108">The query requests all the instances of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) that have the **IpEnabled** property set to **True**.</span></span> <span data-ttu-id="dec22-109">À l’exception de l’ajout du *filtre* et du *dialecte*, la requête est gérée comme une énumération simple.</span><span class="sxs-lookup"><span data-stu-id="dec22-109">Except for the addition of the *filter* and *dialect*, the query is handled like a simple enumeration.</span></span>

<span data-ttu-id="dec22-110">Dans cet exemple, le nom de ressource de la constante de ressource est représenté par un astérisque « \* », car le nom de la classe, [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), est déjà mentionné dans la chaîne *strFilter* .</span><span class="sxs-lookup"><span data-stu-id="dec22-110">In this example, the resource name for the Resource constant is represented by an asterisk "\*" because the class name, [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), is already mentioned in the *strFilter* string.</span></span>

<span data-ttu-id="dec22-111">**Pour interroger des instances spécifiques d’une ressource**</span><span class="sxs-lookup"><span data-stu-id="dec22-111">**To query for specific instances of a resource**</span></span>

1.  <span data-ttu-id="dec22-112">Pour faciliter la lecture, définissez les URI en tant que constantes.</span><span class="sxs-lookup"><span data-stu-id="dec22-112">For ease-of-reading, define URIs as constants.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  <span data-ttu-id="dec22-113">Créer une session.</span><span class="sxs-lookup"><span data-stu-id="dec22-113">Create a session.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  <span data-ttu-id="dec22-114">Construire la chaîne de filtrage.</span><span class="sxs-lookup"><span data-stu-id="dec22-114">Construct the filter string.</span></span> <span data-ttu-id="dec22-115">Windows Remote Management prend en charge [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) comme dialecte de filtre.</span><span class="sxs-lookup"><span data-stu-id="dec22-115">Windows Remote Management supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as the filter dialect.</span></span>

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  <span data-ttu-id="dec22-116">Définissez toutes les [**constantes d’énumération**](enumeration-constants.md) requises dans le paramètre *Flags* .</span><span class="sxs-lookup"><span data-stu-id="dec22-116">Set any required [**enumeration constants**](enumeration-constants.md) in the *flags* parameter.</span></span>

    <span data-ttu-id="dec22-117">Sachez que si les indicateurs incluent les [**constantes d’énumération**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow** , le service WinRM retourne le code d’erreur le **mode de \_ \_ polymorphisme WSMan n’est \_ \_ pas pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="dec22-117">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then WinRM service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

5.  <span data-ttu-id="dec22-118">Appelez la méthode [**session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="dec22-118">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="dec22-119">Cet appel démarre une énumération.</span><span class="sxs-lookup"><span data-stu-id="dec22-119">This call starts an enumeration.</span></span> <span data-ttu-id="dec22-120">La méthode **session. Enumerate** établit un contexte d’énumération de protocole WS-Management, conservé dans l’objet [**énumérateur**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="dec22-120">The **Session.Enumerate** method establishes a WS-Management protocol enumeration context, maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  <span data-ttu-id="dec22-121">Appelez la méthode [**Enumerator. ReadItem**](enumerator-readitem.md) pour obtenir l’élément suivant des résultats.</span><span class="sxs-lookup"><span data-stu-id="dec22-121">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="dec22-122">Dans WS-Management protocole, cela correspond à l’opération d’extraction.</span><span class="sxs-lookup"><span data-stu-id="dec22-122">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="dec22-123">Utilisez la méthode [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) comme contrôle pour savoir quand arrêter la lecture.</span><span class="sxs-lookup"><span data-stu-id="dec22-123">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

<span data-ttu-id="dec22-124">L’exemple de code VBScript suivant montre le script complet.</span><span class="sxs-lookup"><span data-stu-id="dec22-124">The following VBScript code example shows the complete script.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="dec22-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dec22-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dec22-126">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="dec22-126">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="dec22-127">Énumération ou liste de toutes les instances d’une ressource</span><span class="sxs-lookup"><span data-stu-id="dec22-127">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="dec22-128">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="dec22-128">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 