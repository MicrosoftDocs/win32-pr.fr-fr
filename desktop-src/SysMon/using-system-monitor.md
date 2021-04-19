---
title: Utilisation du moniteur système
description: Le moniteur système (SYSMON) peut être inclus dans n’importe quelle application qui prend en charge ActiveX \ 174 ; commandes. Par exemple, vous pouvez inclure SYSMON dans une application Microsoft Visual Basic ou dans un document HTML.
ms.assetid: 36931aae-b608-42d9-a3e3-09784e80f386
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd636c8b984f7c891c2222b4674dd8d0d7e747d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510614"
---
# <a name="using-system-monitor"></a><span data-ttu-id="3fda8-104">Utilisation du moniteur système</span><span class="sxs-lookup"><span data-stu-id="3fda8-104">Using System Monitor</span></span>

<span data-ttu-id="3fda8-105">Le moniteur système (SYSMON) peut être inclus dans n’importe quelle application qui prend en charge les contrôles de® ActiveX.</span><span class="sxs-lookup"><span data-stu-id="3fda8-105">System Monitor (SYSMON) can be included in any application that supports ActiveX® controls.</span></span> <span data-ttu-id="3fda8-106">Par exemple, vous pouvez inclure SYSMON dans une application Microsoft Visual Basic ou dans un document HTML.</span><span class="sxs-lookup"><span data-stu-id="3fda8-106">For example, you can include SYSMON in a Microsoft Visual Basic application or in an HTML document.</span></span>

<span data-ttu-id="3fda8-107">L’exemple suivant montre comment inclure SYSMON dans un document HTML.</span><span class="sxs-lookup"><span data-stu-id="3fda8-107">The following example shows how to include SYSMON in an HTML document.</span></span> <span data-ttu-id="3fda8-108">L’exemple utilise VBScript pour ajouter des compteurs dont les valeurs sont extraites de l’ordinateur local, modifie certaines des propriétés SYSMON qui contrôlent le mode d’affichage de l’analyse et traite l’événement OnCounterAdd.</span><span class="sxs-lookup"><span data-stu-id="3fda8-108">The example uses VBScript to add counters whose values are retrieved from the local computer, modifies some of the SYSMON properties that control how the monitor is displayed, and processes the OnCounterAdd event.</span></span> <span data-ttu-id="3fda8-109">L’exemple utilise le caractère générique ( \* ) pour ajouter toutes les instances du compteur de processus.</span><span class="sxs-lookup"><span data-stu-id="3fda8-109">The example uses the wildcard character (\*) to add all instances of the process counter.</span></span>

``` syntax
<HTML>
<BODY BGCOLOR=#C0C0C0>

<SCRIPT LANGUAGE="VBScript">
  Sub Monitor_OnCounterAdded(index)
    Monitor.Counters.Item(1).Width = 8
  End Sub
</Script>
<OBJECT
  CLASSID="clsid:C4D2D8E0-D1DD-11CE-940F-008029004347"
  ID="Monitor"
  HEIGHT=80%
  WIDTH=100%>
</OBJECT>

<SCRIPT LANGUAGE="VBScript">
  Sub Window_OnLoad
    On Error Resume Next
    Monitor.ShowValueBar = False
    Monitor.ShowHorizontalGrid = True
    Monitor.Counters.Add("\Process(*)\% Processor Time")
    Monitor.DisplayType=sysmonLineGraph
    Monitor.GraphTitle="System Performance Overview"
  End Sub
</SCRIPT>

</BODY>
</HTML>
```

 

 




