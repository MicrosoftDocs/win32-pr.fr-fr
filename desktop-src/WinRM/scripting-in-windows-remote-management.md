---
title: Scripts dans Windows Remote Management
description: L’API de script dans WinRM et l’API COM associée pour C++ sont conçues pour refléter fidèlement les opérations du protocole WS-Management.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Scripts dans Windows Remote Management
- Windows Remote Management, écriture de scripts dans
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 75af10fea03853de99c884eda0a74ce340683b49
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101676"
---
# <a name="scripting-in-windows-remote-management"></a><span data-ttu-id="ebb1d-105">Scripts dans Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="ebb1d-105">Scripting in Windows Remote Management</span></span>

<span data-ttu-id="ebb1d-106">L' [API de script dans WinRM](winrm-scripting-api.md) et l’API COM associée pour C++ sont conçues pour refléter fidèlement les opérations du protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-106">The [Scripting API in WinRM](winrm-scripting-api.md) and the accompanying COM API for C++ are designed to closely reflect the operations of the WS-Management protocol.</span></span>

<span data-ttu-id="ebb1d-107">L’API de script WinRM dans Windows Remote Management prend en charge toutes les opérations de protocole WS-Management sauf une.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-107">The WinRM Scripting API in Windows Remote Management supports all the WS-Management protocol operations except one.</span></span> <span data-ttu-id="ebb1d-108">Elle n’autorise pas les abonnements aux événements.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-108">It does not allow subscriptions to events.</span></span> <span data-ttu-id="ebb1d-109">Pour vous abonner à des événements à partir du journal des événements système BMC, vous devez utiliser les outils en ligne de commande wecutil ou wevtutil.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-109">To subscribe to events from the BMC System Event Log, you must use the Wecutil or Wevtutil command-line tools.</span></span> <span data-ttu-id="ebb1d-110">Pour plus d’informations, consultez [Événements](events.md).</span><span class="sxs-lookup"><span data-stu-id="ebb1d-110">For more information, see [Events](events.md).</span></span>

<span data-ttu-id="ebb1d-111">L’API de script WinRM est appelée par Winrm.vbs, un outil en ligne de commande, qui est écrit en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="ebb1d-111">The WinRM Scripting API is called by Winrm.vbs, a command-line tool, which is written in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="ebb1d-112">Winrm.vbs fournit des exemples d’utilisation de l' [API de script WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ebb1d-112">Winrm.vbs provides examples of how to use the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

## <a name="using-wsman-compared-to-using-wmi-scripting"></a><span data-ttu-id="ebb1d-113">Utilisation de WSman par rapport à l’utilisation de scripts WMI</span><span class="sxs-lookup"><span data-stu-id="ebb1d-113">Using WSman Compared to Using WMI Scripting</span></span>

<span data-ttu-id="ebb1d-114">WMI se connecte à des ordinateurs distants via DCOM, ce qui nécessite la configuration décrite dans [connexion à WMI sur un ordinateur distant](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="ebb1d-114">WMI connects to remote computers through DCOM, which requires the configuration described in [Connecting to WMI on a Remote Computer](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span></span> <span data-ttu-id="ebb1d-115">WinRM n’utilise pas DCOM pour se connecter à un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-115">WinRM does not use DCOM to connect to a remote computer.</span></span> <span data-ttu-id="ebb1d-116">Au lieu de cela, le protocole WS-Management envoie des messages SOAP et le service utilise un port unique pour HTTP et un port pour le transport HTTPs.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-116">Instead, the WS-Management protocol sends SOAP messages and the service uses a single port for HTTP and a port for HTTPS transport.</span></span>

<span data-ttu-id="ebb1d-117">Contrairement à l’outil de ligne de commande **WinRM** , les scripts doivent fournir le XML requis pour passer aux messages du protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-117">Unlike the **winrm** command-line tool, scripts must provide the XML required to pass to the WS-Management protocol messages.</span></span> <span data-ttu-id="ebb1d-118">Ils doivent également fournir des URI.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-118">They must also provide URIs.</span></span> <span data-ttu-id="ebb1d-119">Pour plus d’informations, consultez [URI de ressource](resource-uris.md) et [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ebb1d-119">For more information, see [Resource URIs](resource-uris.md) and [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="ebb1d-120">L’API de script WMI fonctionne avec des objets, tels que des instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), qui représentent des ressources sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-120">The WMI Scripting API works with objects, such as instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which represent resources on a computer.</span></span> <span data-ttu-id="ebb1d-121">Cette classe WMI est définie dans les fichiers [*format MOF (MOF)*](/windows/desktop/WmiSdk/gloss-m) , qui sont stockés au format binaire dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-121">This WMI class is defined in [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) files, which are stored in binary form in the WMI repository.</span></span> <span data-ttu-id="ebb1d-122">Dans WMI, une opération d’extraction pour une seule ressource ou une requête pour plusieurs instances retourne des objets WMI.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-122">In WMI, a Get operation for a single resource or a query for multiple instances returns WMI objects.</span></span>

<span data-ttu-id="ebb1d-123">Un script WinRM ne retourne pas d’objets, mais plutôt des flux de texte XML.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-123">A WinRM script does not return objects, but rather streams of XML text.</span></span> <span data-ttu-id="ebb1d-124">Pour plus d’informations, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ebb1d-124">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="ebb1d-125">Affichage de la sortie XML des scripts WinRM</span><span class="sxs-lookup"><span data-stu-id="ebb1d-125">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="ebb1d-126">L’API de script WinRM obtient et reçoit des chaînes XML qui décrivent les ressources.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-126">The WinRM Scripting API gets and receives XML strings that describe resources.</span></span> <span data-ttu-id="ebb1d-127">Le code XML résultant se présente sous la forme d’un flux de texte et requiert l’affichage d’une transformation XML d’une autre façon.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-127">The resultant XML is in the form of a text stream and requires an XML transform to be displayed in some other way.</span></span>

<span data-ttu-id="ebb1d-128">Le script WinRM suivant produit une sortie XML brute.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-128">The following WinRM script produces raw XML output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



<span data-ttu-id="ebb1d-129">Le bloc de texte suivant illustre la sortie XML du script WinRM.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-129">The following block of text shows the XML output from the WinRM script.</span></span>


```XML
<p:Win32_Service xmlns:xsi="https://www.w3.org/2001/XMLSchema-
instance" xmlns:p="http://schemas.microsoft.com/wbem/wsman/1
/wmi/root/cimv2/Win32_Service" xmlns:cim="https://schemas.dmtf
.org/wbem/wsman/1/base" cim:Class="Win32_Service"><p:AcceptP
ause>false</p:AcceptPause><p:AcceptStop>true</p:AcceptStop>
<p:Caption>Print Spooler</p:Caption><p:CheckPoint>0</p:CheckP
oint><p:CreationClassName>Win32_Service</p:CreationClassName>
<p:Description>Loads files to memory for later printing</p:De
scription><p:DesktopInteract>true</p:DesktopInteract><p:Displ
ayName>Print Spooler</p:DisplayName><p:ErrorControl>Normal</p
:ErrorControl><p:ExitCode>0</p:ExitCode><p:InstallDate xsi:ni
l="true"/><p:Name>spooler</p:Name><p:PathName>C:\Windows\Syst
em32\spoolsv.exe</p:PathName><p:ProcessId>1720</p:ProcessId><
p:ServiceSpecificExitCode>0</p:ServiceSpecificExitCode><p:Ser
viceType>Own Process</p:ServiceType><p:Started>true</p:Starte
d><p:StartMode>Auto</p:StartMode><p:StartName>LocalSystem</p:
StartName><p:State>Running</p:State><p:Status>OK</p:Status><p
:SystemCreationClassName>Win32_ComputerSystem</p:SystemCreati
onClassName><p:SystemName>wsplab6-4</p:SystemName><p:TagId>0<
/p:TagId><p:WaitHint>0</p:WaitHint><cim:Location xmlns:cim="h
ttp://schemas.dmtf.org/wbem/wsman/1/base" xmlns:a="https://sc
hemas.xmlsoap.org/ws/2004/08/addressing" xmlns:w="https://sche
mas.dmtf.org/wbem/wsman/1/wsman"><a:Address>https://schemas.xm
lsoap.org/ws/2004/08/addressing/role/anonymous</a:Address><a:
ReferenceParameters><w:ResourceURI>https://schemas.microsoft.c
om/wbem/wsman/1/wmi/root/cimv2/Win32_Service</w:ResourceURI><
w:SelectorSet><w:Selector Name="Name">spooler</w:Selector></w
:SelectorSet></a:ReferenceParameters></cim:Location></p:Win32
_Service>
```



<span data-ttu-id="ebb1d-130">Vos scripts peuvent utiliser une transformation XML pour rendre cette sortie plus lisible.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-130">Your scripts can use an XML transform to make this output more readable.</span></span> <span data-ttu-id="ebb1d-131">Pour plus d’informations, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="ebb1d-131">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="ebb1d-132">La version suivante du script met en forme le XML en sortie lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-132">The following version of the script formats the XML into human-readable output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xslFile.Load( "WsmTxt.xsl" )
Wscript.Echo xmlFile.TransformNode( xslFile )
```



<span data-ttu-id="ebb1d-133">La transformation XSL crée la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-133">The XSL transform creates the following output.</span></span>


```XML
Win32_Service
    AcceptPause = false
    AcceptStop = true
    Caption = Print Spooler
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = Loads files to memory for later printing
    DesktopInteract = true
    DisplayName = Print Spooler
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = Spooler
    PathName = C:\Windows\System32\spoolsv.exe
    ProcessId = 1720
    ServiceSpecificExitCode = 0
    ServiceType = Own Process
    Started = true
    StartMode = Auto
    StartName = LocalSystem
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = wsplab6-4
    TagId = 0
    WaitHint = 0
```



## <a name="winrm-script-and-winrmcmd-output"></a><span data-ttu-id="ebb1d-134">Sortie de script WinRM et WinRM. cmd</span><span class="sxs-lookup"><span data-stu-id="ebb1d-134">WinRM Script and Winrm.cmd Output</span></span>

<span data-ttu-id="ebb1d-135">La sortie d’un script WinRM est encodée au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-135">The output from a WinRM script is encoded in Unicode.</span></span> <span data-ttu-id="ebb1d-136">Si vous créez un [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) et que vous écrivez un fichier à partir du script, le fichier résultant est Unicode.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-136">If you create a [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) and write a file from the script, the resulting file is Unicode.</span></span> <span data-ttu-id="ebb1d-137">Toutefois, si vous redirigez la sortie vers un fichier, l’encodage est ANSI.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-137">However, if you redirect the output to a file, the encoding is ANSI.</span></span> <span data-ttu-id="ebb1d-138">Si vous redirigez la sortie vers un fichier XML et que la sortie contient des caractères Unicode, le code XML n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-138">If you redirect the output to an XML file and there are Unicode characters in the output, the XML will be invalid.</span></span> <span data-ttu-id="ebb1d-139">N’oubliez pas que l’outil en ligne de commande **WinRM** génère une sortie ANSI.</span><span class="sxs-lookup"><span data-stu-id="ebb1d-139">Be aware that the **Winrm** command-line tool outputs ANSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebb1d-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ebb1d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebb1d-141">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="ebb1d-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ebb1d-142">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="ebb1d-142">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

<span data-ttu-id="ebb1d-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebb1d-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ebb1d-144">[Référence DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebb1d-144">[DOM Reference](/previous-versions/windows/desktop/ms764730(v=vs.85))</span></span>
</dt> </dl>

 

 