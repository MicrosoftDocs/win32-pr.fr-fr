---
title: Utilisation de VBScript
description: Utilisation de VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691ed6bf520c83e4b679bb174274abb984eaa2f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196902"
---
# <a name="using-vbscript"></a>Utilisation de VBScript

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

VBScript est un langage de programmation inclus dans Microsoft Internet Explorer. Pour les autres navigateurs, contactez votre fournisseur pour obtenir de l’aide. VBScript 2,0 (ou version ultérieure) est recommandé pour une utilisation avec l’agent. Bien que les versions antérieures de VBScript puissent fonctionner avec l’agent, elles ne disposent pas de certaines fonctions que vous pouvez utiliser. Vous pouvez télécharger VBScript 2,0 et obtenir des informations supplémentaires sur VBScript sur le site Microsoft downloads et Microsoft VBScript.

Pour programmer Microsoft Agent à partir de VBScript, utilisez le code HTML <SCRIPT> tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

Pour les événements, incluez le nom du contrôle suivi du nom de l’événement et de tous les paramètres :

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

Vous pouvez également spécifier un gestionnaire d’événements à l’aide de l’expression <SCRIPT> tag's **For...Event** syntax:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Bien que Microsoft Internet Explorer prenne en charge cette dernière syntaxe, ce n’est pas le cas de tous les navigateurs. Pour des fins de compatibilité, utilisez uniquement la syntaxe précédente pour les événements.

Avec VBScript (2,0 ou version ultérieure), vous pouvez vérifier si Microsoft Agent est installé en tentant de créer l’objet et en vérifiant s’il existe. L’exemple suivant montre comment vérifier le contrôle de l’agent sans déclencher un téléchargement automatique du contrôle (comme si vous aviez inclus une <OBJECT> balise pour le contrôle sur la page) :

``` syntax
<!-- WARNING - This code requires VBScript 2.0.
It will always fail to detect the Agent control
in VbScript 1.x, because CreateObject doesn't work.
-->

<SCRIPT LANGUAGE=VBSCRIPT>
If HaveAgent() Then
      'Microsoft Agent control was found.
document.write "<H2 align=center>Found</H2>"
Else
      'Microsoft Agent control was not found.
document.write "<H2 align=center>Not Found</H2>"
End If

Function HaveAgent()
' This procedure attempts to create an Agent Control object.
' If it succeeds, it returns True.
'    This means the control is available on the client.
' If it fails, it returns False.
'    This means the control hasn't been installed on the client.

   Dim agent
   HaveAgent = False
   On Error Resume Next
   Set agent = CreateObject("Agent.Control.1")
   HaveAgent = IsObject(agent)

End Function

</SCRIPT>
```

 

 




