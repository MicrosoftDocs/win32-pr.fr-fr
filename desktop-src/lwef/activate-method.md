---
title: Activate, méthode
description: Activate, méthode
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509248"
---
# <a name="activate-method"></a><span data-ttu-id="50c10-103">Activate, méthode</span><span class="sxs-lookup"><span data-stu-id="50c10-103">Activate Method</span></span>

<span data-ttu-id="50c10-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="50c10-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="50c10-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Descriptive**](../wmformat/description.md)</span><span class="sxs-lookup"><span data-stu-id="50c10-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Description**](../wmformat/description.md)</span></span>
</dt> <dd>

<span data-ttu-id="50c10-106">Définit le client ou le caractère actif.</span><span class="sxs-lookup"><span data-stu-id="50c10-106">Sets the active client or character.</span></span>

</dd> <dt>

<span data-ttu-id="50c10-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="50c10-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="50c10-108">\*agent ***. Caractères («*** CharacterID \* \* * »). Activer* l' \*  \[ *État*\]</span><span class="sxs-lookup"><span data-stu-id="50c10-108">*agent ***.Characters ("*** CharacterID\*\*\*").Activate*\* \[*State*\]</span></span>



| <span data-ttu-id="50c10-109">Partie</span><span class="sxs-lookup"><span data-stu-id="50c10-109">Part</span></span>    | <span data-ttu-id="50c10-110">Description</span><span class="sxs-lookup"><span data-stu-id="50c10-110">Description</span></span>                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c10-111">*State*</span><span class="sxs-lookup"><span data-stu-id="50c10-111">*State*</span></span> | <span data-ttu-id="50c10-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="50c10-112">Optional.</span></span> <span data-ttu-id="50c10-113">Vous pouvez spécifier les valeurs suivantes pour ce paramètre : 0 n’est pas le client actif.</span><span class="sxs-lookup"><span data-stu-id="50c10-113">You can specify the following values for this parameter: 0 Not the active client.</span></span><br/> <span data-ttu-id="50c10-114">1 le client actif.</span><span class="sxs-lookup"><span data-stu-id="50c10-114">1 The active client.</span></span> <br/> <span data-ttu-id="50c10-115">2 (valeur par défaut) le caractère le plus haut.</span><span class="sxs-lookup"><span data-stu-id="50c10-115">2 (Default) The topmost character.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50c10-116">Notes</span><span class="sxs-lookup"><span data-stu-id="50c10-116">Remarks</span></span>

<span data-ttu-id="50c10-117">Lorsque plusieurs caractères sont visibles, un seul des caractères reçoit les entrées vocales à la fois.</span><span class="sxs-lookup"><span data-stu-id="50c10-117">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="50c10-118">De même, lorsque plusieurs applications clientes partagent le même caractère, un seul des clients reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent).</span><span class="sxs-lookup"><span data-stu-id="50c10-118">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="50c10-119">Le jeu de caractères pour recevoir l’entrée de la souris et de la parole est le caractère le plus élevé et le client qui reçoit l’entrée est le client actif de ce caractère.</span><span class="sxs-lookup"><span data-stu-id="50c10-119">The character set to receive mouse and speech input is the topmost character and the client that receives the input is the active client of that character.</span></span> <span data-ttu-id="50c10-120">(La fenêtre du caractère supérieur s’affiche également en haut de l’ordre de plan de la fenêtre de caractères.) En règle générale, l’utilisateur détermine le caractère supérieur en sélectionnant explicitement le caractère.</span><span class="sxs-lookup"><span data-stu-id="50c10-120">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines the topmost character by explicitly selecting the character.</span></span> <span data-ttu-id="50c10-121">Toutefois, l’activation de niveau supérieur change également lorsqu’un caractère est affiché ou masqué (le caractère devient ou n’est plus le premier niveau, respectivement).</span><span class="sxs-lookup"><span data-stu-id="50c10-121">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="50c10-122">Vous pouvez également utiliser cette méthode pour gérer explicitement quand votre client reçoit une entrée dirigée vers le caractère, par exemple lorsque votre application est elle-même active.</span><span class="sxs-lookup"><span data-stu-id="50c10-122">You can also use this method to explicitly manage when your client receives input directed to the character such as when your application itself becomes active.</span></span> <span data-ttu-id="50c10-123">Par exemple, la définition de l' *État* sur 2 rend le caractère le plus haut et votre client reçoit tous les événements d’entrée de la souris et de la parole générés par l’interaction de l’utilisateur avec le caractère.</span><span class="sxs-lookup"><span data-stu-id="50c10-123">For example, setting *State* to 2 makes the character topmost and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="50c10-124">Par conséquent, il rend également votre client le client d’entrée-actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="50c10-124">Therefore, it also makes your client the input-active client of the character.</span></span>

<span data-ttu-id="50c10-125">Toutefois, vous pouvez également vous définir comme client actif pour un caractère sans rendre le caractère le plus haut, en définissant l' *État* sur 1.</span><span class="sxs-lookup"><span data-stu-id="50c10-125">However, you can also set yourself to be the active client for a character without making the character topmost, by setting *State* to 1.</span></span> <span data-ttu-id="50c10-126">Cela permet à votre client de recevoir l’entrée dirigée vers ce caractère lorsque le caractère devient le plus haut.</span><span class="sxs-lookup"><span data-stu-id="50c10-126">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="50c10-127">De même, vous pouvez configurer votre client pour qu’il ne soit pas le client actif (et non recevoir l’entrée) lorsque le caractère devient le plus haut, en définissant l' *État* sur 0.</span><span class="sxs-lookup"><span data-stu-id="50c10-127">Similarly, you can set your client to not be the active client (not to receive input) when the character becomes topmost, by setting *State* to 0.</span></span>

<span data-ttu-id="50c10-128">Évitez d’appeler cette méthode directement après une méthode [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) .</span><span class="sxs-lookup"><span data-stu-id="50c10-128">Avoid calling this method directly after a [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) method.</span></span> <span data-ttu-id="50c10-129">**Afficher** définit automatiquement le client d’entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="50c10-129">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="50c10-130">Lorsque le caractère est masqué, l’appel d' [**activation**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) peut échouer s’il est traité avant la fin de la méthode **Show** .</span><span class="sxs-lookup"><span data-stu-id="50c10-130">When the character is hidden, the [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) call may fail if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="50c10-131">Si vous appelez cette méthode sur une fonction, elle retourne une valeur booléenne qui indique si la méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="50c10-131">If you call this method to a function, it returns a Boolean value that indicates whether the method succeeded.</span></span> <span data-ttu-id="50c10-132">Toute tentative d’appel à cette méthode avec le paramètre d' *État* défini sur la valeur 2 lorsque le caractère spécifié est masqué échoue.</span><span class="sxs-lookup"><span data-stu-id="50c10-132">Attempting to call this method with the *State* parameter set to 2 when the specified character is hidden will fail.</span></span> <span data-ttu-id="50c10-133">De même, si vous affectez à l' *État* la valeur 0 et que votre application est le seul client, cet appel échoue parce qu’un caractère doit toujours avoir un client le plus haut.</span><span class="sxs-lookup"><span data-stu-id="50c10-133">Similarly, if you set *State* to 0 and your application is the only client, this call fails because a character must always have a topmost client.</span></span>


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> <span data-ttu-id="50c10-134">L’appel de cette méthode avec un *État* défini sur 1 ne génère généralement pas d’événement [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) , sauf si aucun autre caractère n’est chargé ou si votre application est déjà en entrée-active.</span><span class="sxs-lookup"><span data-stu-id="50c10-134">Calling this method with *State* set to 1 does not typically generate an [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="50c10-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50c10-135">See Also</span></span>

<span data-ttu-id="50c10-136">[**Événement ActivateInput**](activateinput-event.md), [ **événement DeactivateInput**](deactivateinput-event.md)</span><span class="sxs-lookup"><span data-stu-id="50c10-136">[**ActivateInput event**](activateinput-event.md), [**DeactivateInput event**](deactivateinput-event.md)</span></span>


 

