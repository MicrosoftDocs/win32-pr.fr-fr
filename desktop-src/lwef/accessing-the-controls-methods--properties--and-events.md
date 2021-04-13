---
title: Accès aux méthodes, propriétés et événements de contrôles
description: Accès aux méthodes, propriétés et événements de contrôles
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379873"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a><span data-ttu-id="986c5-103">Accès aux méthodes, propriétés et événements de contrôles</span><span class="sxs-lookup"><span data-stu-id="986c5-103">Accessing the Controls Methods, Properties, and Events</span></span>

<span data-ttu-id="986c5-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="986c5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="986c5-105">L’utilisation du contrôle Microsoft Agent avec Visual Basic est très similaire à l’utilisation du contrôle avec VBScript, sauf que les événements dans Visual Basic doivent inclure le type de données des paramètres passés.</span><span class="sxs-lookup"><span data-stu-id="986c5-105">Using Microsoft Agent's control with Visual Basic is very similar to using the control with VBScript, except that events in Visual Basic must include the data type of passed parameters.</span></span> <span data-ttu-id="986c5-106">L’ajout du contrôle Microsoft Agent à un formulaire inclut automatiquement les événements de Microsoft Agent avec les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="986c5-106">Adding the Microsoft Agent control to a form will automatically include Microsoft Agent's events with their appropriate parameters.</span></span> <span data-ttu-id="986c5-107">Elle crée également automatiquement une connexion au serveur de l’agent lors de l’exécution de l’application.</span><span class="sxs-lookup"><span data-stu-id="986c5-107">It will also automatically create a connection to the Agent server when the application runs.</span></span>

<span data-ttu-id="986c5-108">Vous pouvez également être en mesure d’utiliser la syntaxe de création de object’s de votre langage de programmation pour créer une instance du contrôle au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="986c5-108">You may also be able to use your programming language's object's creation syntax to create an instance of the control at runtime.</span></span> <span data-ttu-id="986c5-109">Par exemple, dans Visual Basic (5,0 ou version ultérieure), si vous incluez le contrôle Microsoft Agent 2,0 dans les références de votre projet, vous pouvez utiliser une [**avec des événements**](https://www.bing.com/search?q=**With+Events**). [**Nouvelle**](https://www.bing.com/search?q=**New**) déclaration.</span><span class="sxs-lookup"><span data-stu-id="986c5-109">For example, in Visual Basic (5.0 or later), if you include the Microsoft Agent 2.0 Control in your project's references, you can use a [**With Events**](https://www.bing.com/search?q=**With+Events**)..[**New**](https://www.bing.com/search?q=**New**) declaration.</span></span> <span data-ttu-id="986c5-110">Si vous n’incluez pas la référence, VB génère une erreur indiquant que Microsoft Agent n’a pas pu démarrer (code d’erreur 80042502).</span><span class="sxs-lookup"><span data-stu-id="986c5-110">If you do not include the reference, VB raises an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

<span data-ttu-id="986c5-111">Pour les versions de VB antérieures à 5,0, vous pouvez utiliser le mot clé VB [**New**](https://www.bing.com/search?q=**New**) sans déclaration [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) ou la fonction [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) VB, mais ces conventions n’exposent pas les événements du contrôle de l’agent.</span><span class="sxs-lookup"><span data-stu-id="986c5-111">For versions of VB prior to 5.0, you can use the VB [**New**](https://www.bing.com/search?q=**New**) keyword without [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) declaration or the VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) function, but these conventions will not expose the Agent control's events.</span></span> <span data-ttu-id="986c5-112">Vous devez également utiliser la propriété [**Connected**](https://www.bing.com/search?q=**Connected**) avant de référencer des méthodes ou des propriétés de l’agent.</span><span class="sxs-lookup"><span data-stu-id="986c5-112">You also need to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property before you reference any Agent methods or properties.</span></span> <span data-ttu-id="986c5-113">Si ce n’est pas le cas, VB génère une erreur indiquant que Microsoft Agent n’a pas pu démarrer (code d’erreur 80042502).</span><span class="sxs-lookup"><span data-stu-id="986c5-113">If this is not done, VB will raise an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

<span data-ttu-id="986c5-114">De même, pour d’autres langages de programmation, vous devrez peut-être utiliser la propriété [**Connected**](https://www.bing.com/search?q=**Connected**) pour établir une connexion au serveur COM (Component Object Model) de l’agent avant que votre code puisse appeler l’une des méthodes ou propriétés du contrôle de l’agent.</span><span class="sxs-lookup"><span data-stu-id="986c5-114">Similarly for other programming languages, you may have to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property to establish a connection to the Agent Component Object Model (COM) server before your code can call any of the Agent control's methods or properties.</span></span> <span data-ttu-id="986c5-115">En outre, pour certains langages de programmation, les méthodes et les propriétés de l’agent peuvent ne pas être exposées directement, sauf si vous déclarez le contrôle de l’agent à l’aide de son type.</span><span class="sxs-lookup"><span data-stu-id="986c5-115">In addition, for some programming languages, Agent's methods and properties may not be directly exposed unless you declare the Agent control using its type.</span></span> <span data-ttu-id="986c5-116">Par exemple, dans Microsoft Access 97, vous devez déclarer l’objet comme agent de type pour que les méthodes et les propriétés s’affichent dans la zone de liste déroulante répertorier automatiquement les membres lorsque vous tapez.</span><span class="sxs-lookup"><span data-stu-id="986c5-116">For example, in Microsoft Access 97, you will need to declare the object as type Agent to see the methods and properties display in the Auto List Members drop-down box when you type.</span></span>

<span data-ttu-id="986c5-117">La plupart des langages de programmation qui prennent en charge les contrôles ActiveX suivent des conventions similaires à celles de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="986c5-117">Most programming languages that support ActiveX controls follow conventions similar to Visual Basic.</span></span> <span data-ttu-id="986c5-118">Pour les langages de programmation qui ne prennent pas en charge les collections d’objets, vous pouvez utiliser la méthode de [**caractères**](https://www.bing.com/search?q=**Character**) et la méthode de [**commande**](https://www.bing.com/search?q=**Command**) pour accéder aux méthodes et aux propriétés des éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="986c5-118">For programming languages that do not support object collections, you can use the [**Character**](https://www.bing.com/search?q=**Character**) method and [**Command**](https://www.bing.com/search?q=**Command**) method to access methods and properties of items in the collection.</span></span>

<span data-ttu-id="986c5-119">Des langages de programmation comme Visual Basic, qui permettent d’accéder aux types d’objets exposés par le contrôle de l’agent, vous permettent de les utiliser dans vos déclarations d’objet.</span><span class="sxs-lookup"><span data-stu-id="986c5-119">Programming languages like Visual Basic, that provide access to the object types exposed by the Agent control, enable you to use these in your object declarations.</span></span> <span data-ttu-id="986c5-120">Par exemple, au lieu de déclarer un objet en tant que type générique :</span><span class="sxs-lookup"><span data-stu-id="986c5-120">For example, instead of declaring an object as a generic type:</span></span>

``` syntax
   Dim Genie as Object
```

<span data-ttu-id="986c5-121">Vous pouvez déclarer un objet en tant que type spécifique :</span><span class="sxs-lookup"><span data-stu-id="986c5-121">You can declare an object as a specific type:</span></span>

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

<span data-ttu-id="986c5-122">Cela peut améliorer les performances globales de votre application.</span><span class="sxs-lookup"><span data-stu-id="986c5-122">This may improve the overall performance of your application.</span></span>

<span data-ttu-id="986c5-123">Pour certains types d’objets, vous pouvez trouver deux types qui sont identiques, à l’exception du suffixe « ex ».</span><span class="sxs-lookup"><span data-stu-id="986c5-123">For some object types, you may find two types that are the same except for the "Ex" suffix.</span></span> <span data-ttu-id="986c5-124">Si les deux existent, utilisez le type « ex », car cela fournit toutes les fonctionnalités de l’agent.</span><span class="sxs-lookup"><span data-stu-id="986c5-124">Where both exist, use the "Ex" type because this provides the full functionality of Agent.</span></span> <span data-ttu-id="986c5-125">Les équivalents non-« ex » sont inclus uniquement pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="986c5-125">The non-"Ex" counterparts are included only for backward compatibility.</span></span>

 

 




