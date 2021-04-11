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
# <a name="using-vbscript"></a><span data-ttu-id="19e73-103">Utilisation de VBScript</span><span class="sxs-lookup"><span data-stu-id="19e73-103">Using VBScript</span></span>

<span data-ttu-id="19e73-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="19e73-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="19e73-105">VBScript est un langage de programmation inclus dans Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="19e73-105">VBScript is a programming language included with Microsoft Internet Explorer.</span></span> <span data-ttu-id="19e73-106">Pour les autres navigateurs, contactez votre fournisseur pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="19e73-106">For other browsers, contact your vendor about support.</span></span> <span data-ttu-id="19e73-107">VBScript 2,0 (ou version ultérieure) est recommandé pour une utilisation avec l’agent.</span><span class="sxs-lookup"><span data-stu-id="19e73-107">VBScript 2.0 (or later) is recommended for use with Agent.</span></span> <span data-ttu-id="19e73-108">Bien que les versions antérieures de VBScript puissent fonctionner avec l’agent, elles ne disposent pas de certaines fonctions que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="19e73-108">Although earlier versions of VBScript may work with Agent, they lack certain functions that you may want to use.</span></span> <span data-ttu-id="19e73-109">Vous pouvez télécharger VBScript 2,0 et obtenir des informations supplémentaires sur VBScript sur le site Microsoft downloads et Microsoft VBScript.</span><span class="sxs-lookup"><span data-stu-id="19e73-109">You can download VBScript 2.0 and obtain further information on VBScript at the Microsoft Downloads site and the Microsoft VBScript site.</span></span>

<span data-ttu-id="19e73-110">Pour programmer Microsoft Agent à partir de VBScript, utilisez le code HTML</span><span class="sxs-lookup"><span data-stu-id="19e73-110">To program Microsoft Agent from VBScript, use the HTML</span></span> <SCRIPT> <span data-ttu-id="19e73-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span><span class="sxs-lookup"><span data-stu-id="19e73-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span></span>

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

<span data-ttu-id="19e73-112">Pour les événements, incluez le nom du contrôle suivi du nom de l’événement et de tous les paramètres :</span><span class="sxs-lookup"><span data-stu-id="19e73-112">For events, include the name of the control followed by the name of the event and any parameters:</span></span>

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

<span data-ttu-id="19e73-113">Vous pouvez également spécifier un gestionnaire d’événements à l’aide de l’expression</span><span class="sxs-lookup"><span data-stu-id="19e73-113">You can also specify an event handler using the</span></span> <SCRIPT> <span data-ttu-id="19e73-114">tag's **For...Event** syntax:</span><span class="sxs-lookup"><span data-stu-id="19e73-114">tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

<span data-ttu-id="19e73-115">Bien que Microsoft Internet Explorer prenne en charge cette dernière syntaxe, ce n’est pas le cas de tous les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="19e73-115">Although Microsoft Internet Explorer supports this latter syntax, not all browsers do.</span></span> <span data-ttu-id="19e73-116">Pour des fins de compatibilité, utilisez uniquement la syntaxe précédente pour les événements.</span><span class="sxs-lookup"><span data-stu-id="19e73-116">For compatibility, use only the former syntax for events.</span></span>

<span data-ttu-id="19e73-117">Avec VBScript (2,0 ou version ultérieure), vous pouvez vérifier si Microsoft Agent est installé en tentant de créer l’objet et en vérifiant s’il existe.</span><span class="sxs-lookup"><span data-stu-id="19e73-117">With VBScript (2.0 or later), you can verify whether Microsoft Agent is installed by trying to create the object and checking to see if it exists.</span></span> <span data-ttu-id="19e73-118">L’exemple suivant montre comment vérifier le contrôle de l’agent sans déclencher un téléchargement automatique du contrôle (comme si vous aviez inclus une <OBJECT> balise pour le contrôle sur la page) :</span><span class="sxs-lookup"><span data-stu-id="19e73-118">The following sample demonstrates how to check for the Agent control without triggering an auto-download of the control (as would happen if you included an <OBJECT> tag for the control on the page):</span></span>

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

 

 




