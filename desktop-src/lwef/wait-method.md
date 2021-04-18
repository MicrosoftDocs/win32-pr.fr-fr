---
title: Wait, méthode
description: Wait, méthode
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509246"
---
# <a name="wait-method"></a><span data-ttu-id="bdd48-103">Wait, méthode</span><span class="sxs-lookup"><span data-stu-id="bdd48-103">Wait Method</span></span>

<span data-ttu-id="bdd48-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bdd48-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bdd48-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="bdd48-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bdd48-106">Fait en sorte que la file d’attente d’animation du caractère spécifié attende jusqu’à la fin de la demande d’animation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bdd48-106">Causes the animation queue for the specified character to wait until the specified animation request completes.</span></span>

</dd> <dt>

<span data-ttu-id="bdd48-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="bdd48-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bdd48-108">*agent ***. Caractères («*** CharacterID ***»).*** Demande d’attente*</span><span class="sxs-lookup"><span data-stu-id="bdd48-108">*agent ***.Characters ("*** CharacterID ***").Wait*** Request*</span></span>



| <span data-ttu-id="bdd48-109">Partie</span><span class="sxs-lookup"><span data-stu-id="bdd48-109">Part</span></span>      | <span data-ttu-id="bdd48-110">Description</span><span class="sxs-lookup"><span data-stu-id="bdd48-110">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="bdd48-111">*Requête*</span><span class="sxs-lookup"><span data-stu-id="bdd48-111">*Request*</span></span> | <span data-ttu-id="bdd48-112">Objet de [**requête**](/windows/desktop/lwef/the-request-object) spécifiant une animation particulière.</span><span class="sxs-lookup"><span data-stu-id="bdd48-112">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation..</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bdd48-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bdd48-113">Remarks</span></span>

<span data-ttu-id="bdd48-114">Utilisez cette méthode uniquement lorsque vous prenez en charge plusieurs caractères (simultanés) et que vous essayez de séquencer l’interaction des caractères.</span><span class="sxs-lookup"><span data-stu-id="bdd48-114">Use this method only when you support multiple (simultaneous) characters and are trying to sequence the interaction of characters.</span></span> <span data-ttu-id="bdd48-115">(Pour un caractère unique, chaque demande d’animation est lue de manière séquentielle, à l’issue de la requête précédente.) Si vous avez deux caractères et que vous souhaitez que la demande d’animation d’un caractère attende la fin de l’animation de l’autre caractère, définissez la méthode **Wait** sur l’objet de [**requête**](/windows/desktop/lwef/the-request-object) d’animation de l’autre caractère.</span><span class="sxs-lookup"><span data-stu-id="bdd48-115">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and you want a character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="bdd48-116">Pour spécifier le paramètre de requête, vous devez créer une variable et assigner la demande d’animation que vous souhaitez interrompre :</span><span class="sxs-lookup"><span data-stu-id="bdd48-116">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



<span data-ttu-id="bdd48-117">Vous pouvez également simplifier votre code en appelant simplement **Wait** directement, à l’aide d’une demande d’animation spécifique.</span><span class="sxs-lookup"><span data-stu-id="bdd48-117">You can also streamline your code by just calling **Wait** directly, using a specific animation request.</span></span>


```
   Robby.Wait Genie.Play "GestureRight"
```



<span data-ttu-id="bdd48-118">Cela évite de devoir déclarer explicitement un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="bdd48-118">This avoids having to explicitly declare a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 