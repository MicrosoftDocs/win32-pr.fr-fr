---
title: Interrupt, méthode
description: Interrupt, méthode
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381962"
---
# <a name="interrupt-method"></a><span data-ttu-id="0ee5f-103">Interrupt, méthode</span><span class="sxs-lookup"><span data-stu-id="0ee5f-103">Interrupt Method</span></span>

<span data-ttu-id="0ee5f-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0ee5f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0ee5f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0ee5f-106">Interrompt l’animation pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-106">Interrupts the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="0ee5f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0ee5f-108">\*agent ***. Caractères («*** CharacterID \* \* * »).* \*  *Demande* d’interruption</span><span class="sxs-lookup"><span data-stu-id="0ee5f-108">*agent ***.Characters ("*** CharacterID\*\*\*").Interrupt*\* *Request*</span></span>



| <span data-ttu-id="0ee5f-109">Partie</span><span class="sxs-lookup"><span data-stu-id="0ee5f-109">Part</span></span>      | <span data-ttu-id="0ee5f-110">Description</span><span class="sxs-lookup"><span data-stu-id="0ee5f-110">Description</span></span>                                                                  |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="0ee5f-111">*Requête*</span><span class="sxs-lookup"><span data-stu-id="0ee5f-111">*Request*</span></span> | <span data-ttu-id="0ee5f-112">Objet de [**demande**](/windows/desktop/lwef/the-request-object) pour un appel d’animation particulier.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-112">A [**Request**](/windows/desktop/lwef/the-request-object) object for a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ee5f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0ee5f-113">Remarks</span></span>

<span data-ttu-id="0ee5f-114">Vous pouvez l’utiliser pour synchroniser l’animation entre les caractères.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-114">You can use this to sync up animation between characters.</span></span> <span data-ttu-id="0ee5f-115">Par exemple, si un autre caractère se trouve dans une animation de bouclage, cette méthode arrête la boucle et passe à l’animation suivante dans la file d’attente du caractère.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-115">For example, if another character is in a looping animation, this method will stop the loop and move to the next animation in the character's queue.</span></span> <span data-ttu-id="0ee5f-116">Vous ne pouvez pas interrompre une animation de caractères que vous n’utilisez pas (que vous n’avez pas chargée).</span><span class="sxs-lookup"><span data-stu-id="0ee5f-116">You cannot interrupt a character animation that you are not using (that you have not loaded).</span></span>

<span data-ttu-id="0ee5f-117">Pour spécifier le paramètre de requête, vous devez créer une variable et assigner la demande d’animation que vous souhaitez interrompre :</span><span class="sxs-lookup"><span data-stu-id="0ee5f-117">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



<span data-ttu-id="0ee5f-118">Vous ne pouvez pas interrompre l’animation du même caractère que celui que vous spécifiez dans cette méthode, car le serveur met en file d’attente la méthode d' **interruption** dans la file d’attente d’animation de ce caractère.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-118">You cannot interrupt the animation of the same character you specify in this method because the server queues the **Interrupt** method in that character's animation queue.</span></span> <span data-ttu-id="0ee5f-119">Par conséquent, vous ne pouvez utiliser l' **interruption** que pour arrêter l’animation d’un autre caractère que vous avez chargé.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-119">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

<span data-ttu-id="0ee5f-120">Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="0ee5f-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

> [!Note]  
> <span data-ttu-id="0ee5f-121">**Interrupt** n’efface pas la file d’attente du caractère ; il arrête l’animation existante et passe à l’animation suivante dans la file d’attente du caractère.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-121">**Interrupt** does not flush the character's queue; it halts the existing animation and moves on to the next animation in the character's queue.</span></span> <span data-ttu-id="0ee5f-122">Pour arrêter et vider la file d’attente d’un caractère, utilisez la méthode [**Stop**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="0ee5f-122">To halt and flush a character's queue, use the [**Stop**](stop-method.md) method.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0ee5f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ee5f-123">See Also</span></span>

[<span data-ttu-id="0ee5f-124">**Stop, méthode**</span><span class="sxs-lookup"><span data-stu-id="0ee5f-124">**Stop method**</span></span>](stop-method.md)


 

 