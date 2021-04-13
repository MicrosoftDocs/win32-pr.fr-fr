---
title: Événement ListenComplete
description: Événement ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380300"
---
# <a name="listencomplete-event"></a><span data-ttu-id="03c99-103">Événement ListenComplete</span><span class="sxs-lookup"><span data-stu-id="03c99-103">ListenComplete Event</span></span>

<span data-ttu-id="03c99-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="03c99-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="03c99-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="03c99-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="03c99-106">Se produit lorsque le mode d’écoute (reconnaissance vocale) est terminé.</span><span class="sxs-lookup"><span data-stu-id="03c99-106">Occurs when Listening mode (speech recognition) has ended.</span></span>

</dd> <dt>

<span data-ttu-id="03c99-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="03c99-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="03c99-108">**Sub** *agent. \* \* \* ListenComplete (ByVal* \*  *CharacterID*, **ByVal** *cause \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="03c99-108">**Sub** *agent.\*\*\*ListenComplete (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="03c99-109">Partie</span><span class="sxs-lookup"><span data-stu-id="03c99-109">Part</span></span>          | <span data-ttu-id="03c99-110">Description</span><span class="sxs-lookup"><span data-stu-id="03c99-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c99-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="03c99-111">*CharacterID*</span></span> | <span data-ttu-id="03c99-112">Retourne l’ID du caractère d’écoute sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="03c99-112">Returns the ID of the listening character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="03c99-113">*Cause*</span><span class="sxs-lookup"><span data-stu-id="03c99-113">*Cause*</span></span>       | <span data-ttu-id="03c99-114">Retourne la cause de l’événement complet sous la forme d’un entier pouvant être l’un des suivants : 1 le mode d’écoute a été désactivé par le code de programme.</span><span class="sxs-lookup"><span data-stu-id="03c99-114">Returns the cause of the complete event as an integer that may be one of the following: 1 Listening mode was turned off by program code.</span></span><br/> <span data-ttu-id="03c99-115">2 le mode d’écoute (activé par code de programme) a expiré.</span><span class="sxs-lookup"><span data-stu-id="03c99-115">2 Listening mode (turned on by program code) timed out.</span></span><br/> <span data-ttu-id="03c99-116">3 le mode d’écoute (activé par la clé d’écoute) a expiré.</span><span class="sxs-lookup"><span data-stu-id="03c99-116">3 Listening mode (turned on by the Listening key) timed out.</span></span><br/> <span data-ttu-id="03c99-117">4 le mode d’écoute a été désactivé, car l’utilisateur a relâché la clé d’écoute.</span><span class="sxs-lookup"><span data-stu-id="03c99-117">4 Listening mode was turned off because the user released the Listening key.</span></span><br/> <span data-ttu-id="03c99-118">5 mode d’écoute terminé, car l’utilisateur a terminé de parler.</span><span class="sxs-lookup"><span data-stu-id="03c99-118">5 Listening mode ended because the user finished speaking.</span></span><br/> <span data-ttu-id="03c99-119">6 mode d’écoute terminé car le client d’entrée-actif a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="03c99-119">6 Listening mode ended because the input-active client was deactivated.</span></span><br/> <span data-ttu-id="03c99-120">7 mode d’écoute terminé car le caractère par défaut a été modifié.</span><span class="sxs-lookup"><span data-stu-id="03c99-120">7 Listening mode ended because the default character was changed.</span></span><br/> <span data-ttu-id="03c99-121">8 mode d’écoute terminé, car l’utilisateur a désactivé l’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="03c99-121">8 Listening mode ended because the user disabled speech input.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="03c99-122">Notes</span><span class="sxs-lookup"><span data-stu-id="03c99-122">Remarks</span></span>

<span data-ttu-id="03c99-123">Cet événement est envoyé à tous les clients lorsque le délai d’attente du mode d’écoute se termine, après que l’utilisateur a libéré la clé d’écoute, lorsque le client actif d’entrée appelle la méthode [**Listen**](listen-method.md) avec la **valeur false** ou que l’utilisateur a terminé de parler.</span><span class="sxs-lookup"><span data-stu-id="03c99-123">This event is sent to all clients when the Listening mode time-out ends, after the user releases the Listening key, when the input active client calls the [**Listen**](listen-method.md) method with **False**, or the user finished speaking.</span></span> <span data-ttu-id="03c99-124">Vous pouvez utiliser cet événement pour déterminer à quel moment reprendre la sortie de caractères parlés (audio).</span><span class="sxs-lookup"><span data-stu-id="03c99-124">You can use this event to determine when to resume character spoken (audio) output.</span></span>

<span data-ttu-id="03c99-125">Si vous activez le mode d’écoute à l’aide de la méthode [**Listen**](listen-method.md) , puis que l’utilisateur appuie sur la touche d’écoute, le mode d’écoute se réinitialise et se poursuit jusqu’à ce que le délai d’attente de la clé d’écoute se termine, que la clé d’écoute soit libérée ou que l’utilisateur finisse de parler, selon la date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="03c99-125">If you turn on Listening mode using the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="03c99-126">Dans ce cas, vous ne recevrez pas d’événement **ListenComplete** tant que le mode de la clé d’écoute n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="03c99-126">In this situation, you will not receive a **ListenComplete** event until the listening key's mode completes.</span></span>

<span data-ttu-id="03c99-127">L’événement retourne le caractère aux clients pour lesquels ce caractère est actuellement chargé.</span><span class="sxs-lookup"><span data-stu-id="03c99-127">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="03c99-128">Tous les autres clients reçoivent un caractère null (chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="03c99-128">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="03c99-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03c99-129">See Also</span></span>

<span data-ttu-id="03c99-130">[**Événement ListenStart**](listenstart-event.md), [ **méthode Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="03c99-130">[**ListenStart event**](listenstart-event.md), [**Listen method**](listen-method.md)</span></span>


 

 





