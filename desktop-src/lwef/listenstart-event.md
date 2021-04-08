---
title: Événement ListenStart
description: Événement ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840673"
---
# <a name="listenstart-event"></a><span data-ttu-id="17a26-103">Événement ListenStart</span><span class="sxs-lookup"><span data-stu-id="17a26-103">ListenStart Event</span></span>

<span data-ttu-id="17a26-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17a26-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="17a26-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="17a26-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="17a26-106">Se produit lorsque le mode d’écoute (reconnaissance vocale) commence.</span><span class="sxs-lookup"><span data-stu-id="17a26-106">Occurs when Listening mode (speech recognition) begins.</span></span>

</dd> <dt>

<span data-ttu-id="17a26-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="17a26-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="17a26-108">**Sous** - *agent. \* \* \* ListenStart (ByVal* \*  *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="17a26-108">**Sub** *agent.\*\*\*ListenStart (ByVal*\* *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="17a26-109">Partie</span><span class="sxs-lookup"><span data-stu-id="17a26-109">Part</span></span>          | <span data-ttu-id="17a26-110">Description</span><span class="sxs-lookup"><span data-stu-id="17a26-110">Description</span></span>                                            |
|---------------|--------------------------------------------------------|
| <span data-ttu-id="17a26-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="17a26-111">*CharacterID*</span></span> | <span data-ttu-id="17a26-112">Retourne l’ID du caractère d’écoute sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="17a26-112">Returns the ID of the listening character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="17a26-113">Notes</span><span class="sxs-lookup"><span data-stu-id="17a26-113">Remarks</span></span>

<span data-ttu-id="17a26-114">Cet événement est envoyé à tous les clients lorsque le mode d’écoute commence parce que l’utilisateur a appuyé sur la touche d’écoute ou sur le client d’entrée-actif appelé la méthode [**Listen**](listen-method.md) avec la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="17a26-114">This event is sent to all clients when Listening mode begins because the user pressed the Listening key or the input-active client called the [**Listen**](listen-method.md) method with **True**.</span></span> <span data-ttu-id="17a26-115">Vous pouvez utiliser cet événement pour éviter que votre caractère ne parle alors que le mode d’écoute est activé.</span><span class="sxs-lookup"><span data-stu-id="17a26-115">You can use this event to avoid having your character speak while the Listening mode is on.</span></span>

<span data-ttu-id="17a26-116">Si vous activez le mode d’écoute avec la méthode [**Listen**](listen-method.md) , puis que l’utilisateur appuie sur la touche d’écoute, le mode d’écoute se réinitialise et se poursuit jusqu’à ce que le délai d’attente de la clé d’écoute se termine, que la clé d’écoute soit libérée ou que l’utilisateur finisse de parler, selon la date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="17a26-116">If you turn on Listening mode with the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="17a26-117">Dans ce cas, lorsque le mode d’écoute est déjà activé, vous n’obtiendrez pas d’événement **ListenStart** supplémentaire lorsque l’utilisateur appuie sur la touche d’écoute.</span><span class="sxs-lookup"><span data-stu-id="17a26-117">In this situation, when Listening mode is already on, you will not get an additional **ListenStart** event when the user presses the Listening key.</span></span>

<span data-ttu-id="17a26-118">L’événement retourne le caractère aux clients pour lesquels ce caractère est actuellement chargé.</span><span class="sxs-lookup"><span data-stu-id="17a26-118">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="17a26-119">Tous les autres clients reçoivent un caractère null (chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="17a26-119">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="17a26-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17a26-120">See Also</span></span>

<span data-ttu-id="17a26-121">[**Événement ListenComplete**](listencomplete-event.md), [ **méthode Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="17a26-121">[**ListenComplete event**](listencomplete-event.md), [**Listen method**](listen-method.md)</span></span>


 

 




