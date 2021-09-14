---
title: Utilisation du moniteur système
description: le moniteur système (SYSMON) peut être inclus dans toutes les applications qui prennent en charge ActiveX \ 174 ; commandes. par exemple, vous pouvez inclure SYSMON dans une application Microsoft Visual Basic ou dans un document HTML.
ms.assetid: 36931aae-b608-42d9-a3e3-09784e80f386
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd636c8b984f7c891c2222b4674dd8d0d7e747d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193648"
---
# <a name="using-system-monitor"></a>Utilisation du moniteur système

le moniteur système (SYSMON) peut être inclus dans n’importe quelle application qui prend en charge les contrôles ActiveX®. par exemple, vous pouvez inclure SYSMON dans une application Microsoft Visual Basic ou dans un document HTML.

L’exemple suivant montre comment inclure SYSMON dans un document HTML. L’exemple utilise VBScript pour ajouter des compteurs dont les valeurs sont extraites de l’ordinateur local, modifie certaines des propriétés SYSMON qui contrôlent le mode d’affichage de l’analyse et traite l’événement OnCounterAdd. L’exemple utilise le caractère générique ( \* ) pour ajouter toutes les instances du compteur de processus.

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

 

 




