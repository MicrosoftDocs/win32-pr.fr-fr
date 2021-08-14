---
title: Méthodes d’objet caractère
description: Méthodes d’objet caractère
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141c0fbcfe26e198984fd4a4d8c6c67858085e41178786d2cb78d2938231fdf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480313"
---
# <a name="character-object-methods"></a>Méthodes d’objet caractère

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le serveur expose également des méthodes pour chaque caractère dans une collection de [**caractères**](/windows/desktop/lwef/the-characters-object) . Les méthodes suivantes sont prises en charge :

-   [**Activer**](activate-method.md)
-   [**GestureAt**](gestureat-method.md)
-   [**Télécharger**](get-method.md)
-   [**Masquer**](hide-method.md)
-   [**Suspendre**](interrupt-method.md)
-   [**Journal**](listen-method.md)
-   [**DéplacerVers**](moveto-method.md)
-   [**Lire**](play-method.md)
-   [**Afficher**](show-method.md)
-   [**ShowPopupMenu**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**Erreur**](stop-method.md)
-   [**StopAll**](stopall-method.md)
-   [**Réflexion**](think-method.md)
-   [**Wait**](wait-method.md)

Pour utiliser une méthode, référencez le caractère dans la collection. dans VBScript et Visual Basic, vous pouvez le faire en spécifiant l’ID d’un caractère :


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



Pour simplifier la syntaxe de votre code, vous pouvez définir une variable objet et la définir pour qu’elle fasse référence à un objet caractère de la collection [**Characters**](/windows/desktop/lwef/the-characters-object) . vous pouvez ensuite utiliser votre variable pour référencer des méthodes ou des propriétés du caractère. l’exemple suivant montre comment effectuer cette opération à l’aide de l’instruction Visual Basic Set :


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



dans Visual Basic 5,0, vous pouvez également créer votre référence en déclarant votre variable en tant qu’objet [**caractère**](/windows/desktop/lwef/the-characters-object):


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



La déclaration de votre objet de type IAgentCtlCharacterEx permet une liaison précoce sur l’objet, ce qui améliore les performances.

Dans VBScript, vous ne pouvez pas déclarer une référence en tant que type particulier. Toutefois, vous pouvez simplement déclarer la référence de la variable :


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



Certains langages de programmation ne prennent pas en charge les collections. Toutefois, vous pouvez accéder aux méthodes d’un objet [**character**](/windows/desktop/lwef/the-characters-object) avec la méthode [**caractère**](character-method.md) :


```
   agent.Characters.Character("CharacterID").method
```



En outre, vous pouvez également créer une référence à l’objet [**caractère**](/windows/desktop/lwef/the-characters-object) pour faciliter le suivi de votre code de script :


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 