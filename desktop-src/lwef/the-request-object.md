---
title: Objet de la requête
description: Objet de la requête
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509436"
---
# <a name="the-request-object"></a><span data-ttu-id="8c953-103">Objet de la requête</span><span class="sxs-lookup"><span data-stu-id="8c953-103">The Request Object</span></span>

<span data-ttu-id="8c953-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8c953-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="8c953-105">Le serveur traite certaines méthodes de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="8c953-105">The server processes some methods asynchronously.</span></span> <span data-ttu-id="8c953-106">Cela permet à votre code d’application de continuer pendant que la méthode se termine.</span><span class="sxs-lookup"><span data-stu-id="8c953-106">This enables your application code to continue while the method is completing.</span></span> <span data-ttu-id="8c953-107">Quand une application cliente appelle l’une de ces méthodes, le contrôle crée et retourne un objet de [**demande**](/windows/desktop/lwef/the-request-object) pour la demande.</span><span class="sxs-lookup"><span data-stu-id="8c953-107">When a client application calls one of these methods, the control creates and returns a [**Request**](/windows/desktop/lwef/the-request-object) object for the request.</span></span> <span data-ttu-id="8c953-108">Vous pouvez utiliser l’objet de **requête** pour suivre l’état de la méthode en affectant une variable objet à la méthode.</span><span class="sxs-lookup"><span data-stu-id="8c953-108">You can use the **Request** object to track the status of the method by assigning an object variable to the method.</span></span> <span data-ttu-id="8c953-109">Dans Visual Basic, commencez par déclarer une variable objet :</span><span class="sxs-lookup"><span data-stu-id="8c953-109">In Visual Basic, first declare an object variable:</span></span>


```
   Dim MyRequest as Object
```



<span data-ttu-id="8c953-110">Dans VBScript, vous n’incluez pas le type de variable dans votre déclaration :</span><span class="sxs-lookup"><span data-stu-id="8c953-110">In VBScript, you don't include the variable type in your declaration:</span></span>


```
   Dim MyRequest
```



<span data-ttu-id="8c953-111">Et utilisent l’instruction Set de Visual Basic pour assigner la variable à l’appel de méthode :</span><span class="sxs-lookup"><span data-stu-id="8c953-111">And use Visual Basic's Set statement to assign the variable to the method call:</span></span>


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



<span data-ttu-id="8c953-112">Cela ajoute une référence à l’objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="8c953-112">This adds a reference to the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="8c953-113">L’objet de **requête** sera détruit lorsqu’il n’y aura plus de références à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="8c953-113">The **Request** object will be destroyed when there are no more references to it.</span></span> <span data-ttu-id="8c953-114">L’endroit où vous déclarez l’objet de **requête** et la manière dont vous l’utilisez détermine sa durée de vie.</span><span class="sxs-lookup"><span data-stu-id="8c953-114">Where you declare the **Request** object and how you use it determines its lifetime.</span></span> <span data-ttu-id="8c953-115">Si l’objet est déclaré local à une sous-routine ou une fonction, il sera détruit lorsqu’il sera hors de portée. autrement dit, lorsque la sous-routine ou la fonction se termine.</span><span class="sxs-lookup"><span data-stu-id="8c953-115">If the object is declared local to a subroutine or function, it will be destroyed when it goes out of scope; that is, when the subroutine or function ends.</span></span> <span data-ttu-id="8c953-116">Si l’objet est déclaré globalement, il n’est pas détruit tant que le programme n’est pas terminé ou qu’une nouvelle valeur (ou une valeur définie sur "Empty") n’est pas assignée à l’objet.</span><span class="sxs-lookup"><span data-stu-id="8c953-116">If the object is declared globally, it will not be destroyed until either the program terminates or a new value (or a value set to "empty") is assigned to the object.</span></span>

<span data-ttu-id="8c953-117">L’objet de [**requête**](/windows/desktop/lwef/the-request-object) fournit plusieurs propriétés que vous pouvez interroger.</span><span class="sxs-lookup"><span data-stu-id="8c953-117">The [**Request**](/windows/desktop/lwef/the-request-object) object provides several properties you can query.</span></span> <span data-ttu-id="8c953-118">Par exemple, la propriété [**Status**](status-property.md) retourne l’état actuel de la demande.</span><span class="sxs-lookup"><span data-stu-id="8c953-118">For example, the [**Status**](status-property.md) property returns the current status of the request.</span></span> <span data-ttu-id="8c953-119">Vous pouvez utiliser cette propriété pour vérifier l’état de votre demande :</span><span class="sxs-lookup"><span data-stu-id="8c953-119">You can use this property to check the status of your request:</span></span>


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



<span data-ttu-id="8c953-120">La propriété [**Status**](status-property.md) retourne l’état d’un objet [**Request**](/windows/desktop/lwef/the-request-object) sous la forme d’une valeur entière longue.</span><span class="sxs-lookup"><span data-stu-id="8c953-120">The [**Status**](status-property.md) property returns the status of a [**Request**](/windows/desktop/lwef/the-request-object) object as a Long integer value.</span></span>



| <span data-ttu-id="8c953-121">Statut</span><span class="sxs-lookup"><span data-stu-id="8c953-121">Status</span></span> | <span data-ttu-id="8c953-122">Définition</span><span class="sxs-lookup"><span data-stu-id="8c953-122">Definition</span></span>                                        |
|--------|---------------------------------------------------|
| <span data-ttu-id="8c953-123">0</span><span class="sxs-lookup"><span data-stu-id="8c953-123">0</span></span>      | <span data-ttu-id="8c953-124">La demande s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="8c953-124">Request successfully completed.</span></span>                   |
| <span data-ttu-id="8c953-125">1</span><span class="sxs-lookup"><span data-stu-id="8c953-125">1</span></span>      | <span data-ttu-id="8c953-126">Échec de la requête.</span><span class="sxs-lookup"><span data-stu-id="8c953-126">Request failed.</span></span>                                   |
| <span data-ttu-id="8c953-127">2</span><span class="sxs-lookup"><span data-stu-id="8c953-127">2</span></span>      | <span data-ttu-id="8c953-128">Demande en attente (dans la file d’attente, mais pas terminée).</span><span class="sxs-lookup"><span data-stu-id="8c953-128">Request pending (in the queue, but not complete).</span></span> |
| <span data-ttu-id="8c953-129">3</span><span class="sxs-lookup"><span data-stu-id="8c953-129">3</span></span>      | <span data-ttu-id="8c953-130">Demande interrompue.</span><span class="sxs-lookup"><span data-stu-id="8c953-130">Request interrupted.</span></span>                              |
| <span data-ttu-id="8c953-131">4</span><span class="sxs-lookup"><span data-stu-id="8c953-131">4</span></span>      | <span data-ttu-id="8c953-132">Demande en cours.</span><span class="sxs-lookup"><span data-stu-id="8c953-132">Request in progress.</span></span>                              |



 

<span data-ttu-id="8c953-133">L’objet de [**requête**](/windows/desktop/lwef/the-request-object) comprend également une valeur d’entier long dans la propriété [**Number**](https://www.bing.com/search?q=**Number**) qui retourne l’erreur ou la cause du code d' [**État**](status-property.md) .</span><span class="sxs-lookup"><span data-stu-id="8c953-133">The [**Request**](/windows/desktop/lwef/the-request-object) object also includes a Long integer value in the [**Number**](https://www.bing.com/search?q=**Number**) property that returns the error or cause of the [**Status**](status-property.md) code.</span></span> <span data-ttu-id="8c953-134">Si aucune valeur n’est, cette valeur est égale à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="8c953-134">If none, this value is zero (0).</span></span> <span data-ttu-id="8c953-135">La propriété [**Description**](description-property.md) contient une valeur de chaîne qui correspond au numéro d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8c953-135">The [**Description**](description-property.md) property contains a string value that corresponds to the error number.</span></span> <span data-ttu-id="8c953-136">Si la chaîne n’existe pas, la **Description** contient « erreur définie par l’application ou définie par l’objet ».</span><span class="sxs-lookup"><span data-stu-id="8c953-136">If the string doesn't exist, **Description** contains "Application-defined or object-defined error".</span></span>

<span data-ttu-id="8c953-137">Pour connaître les valeurs et la signification retournées par la propriété [**Number**](https://www.bing.com/search?q=**Number**) , consultez [codes d’erreur](microsoft-agent-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8c953-137">For the values and meaning returned by the [**Number**](https://www.bing.com/search?q=**Number**) property, see [Error Codes](microsoft-agent-error-codes.md).</span></span>

<span data-ttu-id="8c953-138">Le serveur place les demandes d’animation dans la file d’attente du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="8c953-138">The server places animation requests in the specified character's queue.</span></span> <span data-ttu-id="8c953-139">Cela permet au serveur de lire l’animation sur un thread distinct et le code de votre application peut continuer pendant que les animations sont lues.</span><span class="sxs-lookup"><span data-stu-id="8c953-139">This enables the server to play the animation on a separate thread, and your application's code can continue while animations play.</span></span> <span data-ttu-id="8c953-140">Si vous créez une référence d’objet de [**demande**](/windows/desktop/lwef/the-request-object) , le serveur vous avertit automatiquement quand une demande d’animation a démarré ou est terminée par le biais des événements [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) et [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) .</span><span class="sxs-lookup"><span data-stu-id="8c953-140">If you create a [**Request**](/windows/desktop/lwef/the-request-object) object reference, the server automatically notifies you when an animation request has started or completed through the [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) and [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) events.</span></span> <span data-ttu-id="8c953-141">Étant donné que les méthodes qui retournent des objets de **demande** sont asynchrones et peuvent ne pas se terminer pendant la portée de la fonction appelante, déclarez votre référence à l’objet de **requête** globalement.</span><span class="sxs-lookup"><span data-stu-id="8c953-141">Because methods that return **Request** objects are asynchronous and may not complete during the scope of the calling function, declare your reference to the **Request** object globally.</span></span>

<span data-ttu-id="8c953-142">Les méthodes suivantes peuvent être utilisées pour retourner un objet de [**requête**](/windows/desktop/lwef/the-request-object) : [**GestureAt**](gestureat-method.md), [**obtenir**](get-method.md), [**Masquer**](hide-method.md), [**interrompre**](interrupt-method.md), [**charger**](load-method.md), [**MoveTo**](moveto-method.md), [**lire**](play-method.md), [**Afficher**](show-method.md), [**parler**](speak-method.md)et [**attendre**](https://www.bing.com/search?q=**Wait**).</span><span class="sxs-lookup"><span data-stu-id="8c953-142">The following methods can be used to return a [**Request**](/windows/desktop/lwef/the-request-object) object: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md), and [**Wait**](https://www.bing.com/search?q=**Wait**).</span></span>

 

 