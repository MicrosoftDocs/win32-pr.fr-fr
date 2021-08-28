---
title: Utilisation de VBScript
description: Utilisation de VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bc64419af4d8dc47de5a2393fcf5cb259374ed
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881018"
---
# <a name="using-vbscript"></a>Utilisation de VBScript

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

VBScript est un langage de programmation inclus dans Microsoft Internet Explorer. Pour les autres navigateurs, contactez votre fournisseur pour obtenir de l’aide. VBScript 2,0 (ou version ultérieure) est recommandé pour une utilisation avec l’agent. Bien que les versions antérieures de VBScript puissent fonctionner avec l’agent, elles ne disposent pas de certaines fonctions que vous pouvez utiliser. Vous pouvez télécharger VBScript 2,0 et obtenir des informations supplémentaires sur VBScript sur le site Microsoft downloads et Microsoft VBScript.

Pour programmer Microsoft Agent à partir de VBScript, utilisez &lt; les &gt; balises de script HTML. Pour accéder à l’interface de programmation, utilisez le nom du contrôle que vous attribuez dans la &lt; &gt; balise Object, suivi du sous-objet (le cas échéant), du nom de la méthode ou de la propriété, et de tous les paramètres ou valeurs pris en charge par la méthode ou la propriété :

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

Vous pouvez également spécifier un gestionnaire d’événements à l’aide de la &lt; &gt; balise **de script for...** Syntaxe de l’événement :

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Bien que Microsoft Internet Explorer prenne en charge cette dernière syntaxe, ce n’est pas le cas de tous les navigateurs. Pour des fins de compatibilité, utilisez uniquement la syntaxe précédente pour les événements.

Avec VBScript (2,0 ou version ultérieure), vous pouvez vérifier si Microsoft Agent est installé en tentant de créer l’objet et en vérifiant s’il existe. L’exemple suivant montre comment vérifier le contrôle de l’agent sans déclencher un téléchargement automatique du contrôle (comme cela se produit si vous avez inclus une &lt; &gt; balise d’objet pour le contrôle sur la page) :

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

 

 




