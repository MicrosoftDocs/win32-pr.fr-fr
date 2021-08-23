---
title: scripts dans Windows Remote Management
description: L’API de script dans WinRM et l’API COM associée pour C++ sont conçues pour refléter fidèlement les opérations du protocole WS-Management.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- scripts dans Windows Remote Management
- Windows Gestion à distance, scripts dans
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c10d36420b2826162a6ed5e3fb6bf69408a74032faafac75c84c25a754cf534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795429"
---
# <a name="scripting-in-windows-remote-management"></a>scripts dans Windows Remote Management

L' [API de script dans WinRM](winrm-scripting-api.md) et l’API COM associée pour C++ sont conçues pour refléter fidèlement les opérations du protocole WS-Management.

l’API de script WinRM dans Windows Remote Management prend en charge toutes les opérations de protocole WS-Management sauf une. Elle n’autorise pas les abonnements aux événements. Pour vous abonner à des événements à partir du journal des événements système BMC, vous devez utiliser les outils en ligne de commande wecutil ou wevtutil. Pour plus d’informations, consultez [Événements](events.md).

l’API de script WinRM est appelée par Winrm.vbs, un outil en ligne de commande, qui est écrit dans Visual Basic scripting Edition (VBScript). Winrm.vbs fournit des exemples d’utilisation de l' [API de script WinRM](winrm-scripting-api.md).

## <a name="using-wsman-compared-to-using-wmi-scripting"></a>Utilisation de WSman par rapport à l’utilisation de scripts WMI

WMI se connecte à des ordinateurs distants via DCOM, ce qui nécessite la configuration décrite dans [connexion à WMI sur un ordinateur distant](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer). WinRM n’utilise pas DCOM pour se connecter à un ordinateur distant. Au lieu de cela, le protocole WS-Management envoie des messages SOAP et le service utilise un port unique pour HTTP et un port pour le transport HTTPs.

Contrairement à l’outil de ligne de commande **WinRM** , les scripts doivent fournir le XML requis pour passer aux messages du protocole WS-Management. Ils doivent également fournir des URI. pour plus d’informations, consultez [uri de ressource](resource-uris.md) et [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).

L’API de script WMI fonctionne avec des objets, tels que des instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), qui représentent des ressources sur un ordinateur. Cette classe WMI est définie dans les fichiers [*format MOF (MOF)*](/windows/desktop/WmiSdk/gloss-m) , qui sont stockés au format binaire dans le référentiel WMI. Dans WMI, une opération d’extraction pour une seule ressource ou une requête pour plusieurs instances retourne des objets WMI.

Un script WinRM ne retourne pas d’objets, mais plutôt des flux de texte XML. pour plus d’informations, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).

## <a name="displaying-xml-output-from-winrm-scripts"></a>Affichage de la sortie XML des scripts WinRM

L’API de script WinRM obtient et reçoit des chaînes XML qui décrivent les ressources. Le code XML résultant se présente sous la forme d’un flux de texte et requiert l’affichage d’une transformation XML d’une autre façon.

Le script WinRM suivant produit une sortie XML brute.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



Le bloc de texte suivant illustre la sortie XML du script WinRM.


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



Vos scripts peuvent utiliser une transformation XML pour rendre cette sortie plus lisible. Pour plus d’informations, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md).

La version suivante du script met en forme le XML en sortie lisible par l’utilisateur.


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



La transformation XSL crée la sortie suivante.


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



## <a name="winrm-script-and-winrmcmd-output"></a>Sortie de script WinRM et WinRM. cmd

La sortie d’un script WinRM est encodée au format Unicode. Si vous créez un [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) et que vous écrivez un fichier à partir du script, le fichier résultant est Unicode. Toutefois, si vous redirigez la sortie vers un fichier, l’encodage est ANSI. Si vous redirigez la sortie vers un fichier XML et que la sortie contient des caractères Unicode, le code XML n’est pas valide. N’oubliez pas que l’outil en ligne de commande **WinRM** génère une sortie ANSI.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))
</dt> <dt>

[Référence DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))
</dt> </dl>

 

 