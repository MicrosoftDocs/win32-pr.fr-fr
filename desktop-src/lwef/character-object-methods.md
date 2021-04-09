---
title: Méthodes d’objet caractère
description: Méthodes d’objet caractère
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940856"
---
# <a name="character-object-methods"></a><span data-ttu-id="0541b-103">Méthodes d’objet caractère</span><span class="sxs-lookup"><span data-stu-id="0541b-103">Character Object Methods</span></span>

<span data-ttu-id="0541b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0541b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0541b-105">Le serveur expose également des méthodes pour chaque caractère dans une collection de [**caractères**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="0541b-105">The server also exposes methods for each character in a [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span> <span data-ttu-id="0541b-106">Les méthodes suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="0541b-106">The following methods are supported:</span></span>

-   [<span data-ttu-id="0541b-107">**Déclencher**</span><span class="sxs-lookup"><span data-stu-id="0541b-107">**Activate**</span></span>](activate-method.md)
-   [<span data-ttu-id="0541b-108">**GestureAt**</span><span class="sxs-lookup"><span data-stu-id="0541b-108">**GestureAt**</span></span>](gestureat-method.md)
-   [<span data-ttu-id="0541b-109">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="0541b-109">**Get**</span></span>](get-method.md)
-   [<span data-ttu-id="0541b-110">**Masquer**</span><span class="sxs-lookup"><span data-stu-id="0541b-110">**Hide**</span></span>](hide-method.md)
-   [<span data-ttu-id="0541b-111">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="0541b-111">**Interrupt**</span></span>](interrupt-method.md)
-   [<span data-ttu-id="0541b-112">**Écouter**</span><span class="sxs-lookup"><span data-stu-id="0541b-112">**Listen**</span></span>](listen-method.md)
-   [<span data-ttu-id="0541b-113">**DéplacerVers**</span><span class="sxs-lookup"><span data-stu-id="0541b-113">**MoveTo**</span></span>](moveto-method.md)
-   [<span data-ttu-id="0541b-114">**Lire**</span><span class="sxs-lookup"><span data-stu-id="0541b-114">**Play**</span></span>](play-method.md)
-   [<span data-ttu-id="0541b-115">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="0541b-115">**Show**</span></span>](show-method.md)
-   [<span data-ttu-id="0541b-116">**ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="0541b-116">**ShowPopupMenu**</span></span>](showpopupmenu-method.md)
-   [<span data-ttu-id="0541b-117">**Speak**</span><span class="sxs-lookup"><span data-stu-id="0541b-117">**Speak**</span></span>](speak-method.md)
-   [<span data-ttu-id="0541b-118">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="0541b-118">**Stop**</span></span>](stop-method.md)
-   [<span data-ttu-id="0541b-119">**StopAll**</span><span class="sxs-lookup"><span data-stu-id="0541b-119">**StopAll**</span></span>](stopall-method.md)
-   [<span data-ttu-id="0541b-120">**Réflexion**</span><span class="sxs-lookup"><span data-stu-id="0541b-120">**Think**</span></span>](think-method.md)
-   [<span data-ttu-id="0541b-121">**Wait**</span><span class="sxs-lookup"><span data-stu-id="0541b-121">**Wait**</span></span>](wait-method.md)

<span data-ttu-id="0541b-122">Pour utiliser une méthode, référencez le caractère dans la collection.</span><span class="sxs-lookup"><span data-stu-id="0541b-122">To use a method, reference the character in the collection.</span></span> <span data-ttu-id="0541b-123">Dans VBScript et Visual Basic, vous pouvez le faire en spécifiant l’ID d’un caractère :</span><span class="sxs-lookup"><span data-stu-id="0541b-123">In VBScript and Visual Basic, you do this by specifying the ID for a character:</span></span>


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



<span data-ttu-id="0541b-124">Pour simplifier la syntaxe de votre code, vous pouvez définir une variable objet et la définir pour qu’elle fasse référence à un objet caractère de la collection [**Characters**](/windows/desktop/lwef/the-characters-object) . vous pouvez ensuite utiliser votre variable pour référencer des méthodes ou des propriétés du caractère.</span><span class="sxs-lookup"><span data-stu-id="0541b-124">To simplify the syntax of your code, you can define an object variable and set it to reference a character object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection; then you can use your variable to reference methods or properties of the character.</span></span> <span data-ttu-id="0541b-125">L’exemple suivant montre comment effectuer cette opération à l’aide de l’instruction Visual Basic Set :</span><span class="sxs-lookup"><span data-stu-id="0541b-125">The following example demonstrates how you can do this using the Visual Basic Set statement:</span></span>


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



<span data-ttu-id="0541b-126">Dans Visual Basic 5,0, vous pouvez également créer votre référence en déclarant votre variable en tant qu’objet [**caractère**](/windows/desktop/lwef/the-characters-object):</span><span class="sxs-lookup"><span data-stu-id="0541b-126">In Visual Basic 5.0, you can also create your reference by declaring your variable as a [**Character**](/windows/desktop/lwef/the-characters-object)object:</span></span>


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



<span data-ttu-id="0541b-127">La déclaration de votre objet de type IAgentCtlCharacterEx permet une liaison précoce sur l’objet, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="0541b-127">Declaring your object of type IAgentCtlCharacterEx enables early binding on the object, which results in better performance.</span></span>

<span data-ttu-id="0541b-128">Dans VBScript, vous ne pouvez pas déclarer une référence en tant que type particulier.</span><span class="sxs-lookup"><span data-stu-id="0541b-128">In VBScript, you cannot declare a reference as a particular type.</span></span> <span data-ttu-id="0541b-129">Toutefois, vous pouvez simplement déclarer la référence de la variable :</span><span class="sxs-lookup"><span data-stu-id="0541b-129">However, you can simply declare the variable reference:</span></span>


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



<span data-ttu-id="0541b-130">Certains langages de programmation ne prennent pas en charge les collections.</span><span class="sxs-lookup"><span data-stu-id="0541b-130">Some programming languages do not support collections.</span></span> <span data-ttu-id="0541b-131">Toutefois, vous pouvez accéder aux méthodes d’un objet [**character**](/windows/desktop/lwef/the-characters-object) avec la méthode [**caractère**](character-method.md) :</span><span class="sxs-lookup"><span data-stu-id="0541b-131">However, you can access a [**Character**](/windows/desktop/lwef/the-characters-object) object's methods with the [**Character**](character-method.md) method:</span></span>


```
   agent.Characters.Character("CharacterID").method
```



<span data-ttu-id="0541b-132">En outre, vous pouvez également créer une référence à l’objet [**caractère**](/windows/desktop/lwef/the-characters-object) pour faciliter le suivi de votre code de script :</span><span class="sxs-lookup"><span data-stu-id="0541b-132">In addition, you can also create a reference to the [**Character**](/windows/desktop/lwef/the-characters-object) object to make your script code easier to follow:</span></span>


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



 

 