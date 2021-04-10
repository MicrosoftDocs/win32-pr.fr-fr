---
title: Propriété SRStatus
description: Propriété SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029878"
---
# <a name="srstatus-property"></a><span data-ttu-id="d0e3a-103">Propriété SRStatus</span><span class="sxs-lookup"><span data-stu-id="d0e3a-103">SRStatus Property</span></span>

<span data-ttu-id="d0e3a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0e3a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d0e3a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="d0e3a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d0e3a-106">Retourne une valeur indiquant si l’entrée vocale peut être démarrée pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-106">Returns whether speech input can be started for the character.</span></span>

</dd> <dt>

<span data-ttu-id="d0e3a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="d0e3a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d0e3a-108">*agent. ***Caractères («*** CharacterID \* \* * »). SRStatus**</span><span class="sxs-lookup"><span data-stu-id="d0e3a-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").SRStatus**</span></span>



| <span data-ttu-id="d0e3a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0e3a-109">Value</span></span> | <span data-ttu-id="d0e3a-110">Description</span><span class="sxs-lookup"><span data-stu-id="d0e3a-110">Description</span></span>                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e3a-111">0</span><span class="sxs-lookup"><span data-stu-id="d0e3a-111">0</span></span>     | <span data-ttu-id="d0e3a-112">Les conditions prennent en charge l’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="d0e3a-113">1</span><span class="sxs-lookup"><span data-stu-id="d0e3a-113">1</span></span>     | <span data-ttu-id="d0e3a-114">Aucun périphérique d’entrée audio n’est disponible sur ce système.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="d0e3a-115">(Notez que cela ne détecte pas si un microphone est installé ; il peut détecter uniquement si l’utilisateur dispose d’une carte son compatible avec un pilote opérationnel.)</span><span class="sxs-lookup"><span data-stu-id="d0e3a-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="d0e3a-116">2</span><span class="sxs-lookup"><span data-stu-id="d0e3a-116">2</span></span>     | <span data-ttu-id="d0e3a-117">Un autre client est le client actif de ce caractère, ou le caractère actuel n’est pas au premier plan.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="d0e3a-118">3</span><span class="sxs-lookup"><span data-stu-id="d0e3a-118">3</span></span>     | <span data-ttu-id="d0e3a-119">Le canal d’entrée ou de sortie audio est actuellement occupé, une application utilise l’audio.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-119">The audio input or output channel is currently busy, an application is using audio.</span></span>                                                                                                                                                       |
| <span data-ttu-id="d0e3a-120">4</span><span class="sxs-lookup"><span data-stu-id="d0e3a-120">4</span></span>     | <span data-ttu-id="d0e3a-121">Une erreur non spécifiée s’est produite lors de l’initialisation du sous-système de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="d0e3a-122">Cela inclut la possibilité qu’aucun moteur vocal ne soit disponible correspondant au paramètre de langue du caractère.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="d0e3a-123">5</span><span class="sxs-lookup"><span data-stu-id="d0e3a-123">5</span></span>     | <span data-ttu-id="d0e3a-124">L’utilisateur a désactivé l’entrée vocale dans les options de caractères avancés.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-124">The user has disabled speech input in the Advanced Character Options.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="d0e3a-125">6</span><span class="sxs-lookup"><span data-stu-id="d0e3a-125">6</span></span>     | <span data-ttu-id="d0e3a-126">Une erreur s’est produite lors de la vérification de l’État audio, mais la cause de l’erreur n’a pas été retournée par le système.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0e3a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d0e3a-127">Remarks</span></span>

<span data-ttu-id="d0e3a-128">Cette propriété retourne les conditions nécessaires à la prise en charge de l’entrée vocale, y compris l’état du périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-128">This property returns the conditions necessary to support speech input, including the status of the audio device.</span></span> <span data-ttu-id="d0e3a-129">Vous pouvez vérifier cette propriété avant d’appeler la méthode [**Listen**](listen-method.md) pour mieux garantir sa réussite.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-129">You can check this property before you call the [**Listen**](listen-method.md) method to better ensure its success.</span></span>

<span data-ttu-id="d0e3a-130">Lorsque l’entrée vocale est activée dans la feuille de propriétés de l’agent (options de caractères avancés), l’interrogation de cette propriété chargera le moteur associé, s’il n’est pas déjà chargé, et démarrera les services de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-130">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying this property will load the associated engine, if it is not already loaded, and start speech services.</span></span> <span data-ttu-id="d0e3a-131">Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est automatiquement affichable.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-131">That is, the Listening key is available, and the Listening Tip is automatically displayable.</span></span> <span data-ttu-id="d0e3a-132">(La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-132">(The Listening key and Listening Tip are only enabled if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="d0e3a-133">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="d0e3a-133">This property only applies to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0e3a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0e3a-134">See Also</span></span>

[<span data-ttu-id="d0e3a-135">**Méthode Listen**</span><span class="sxs-lookup"><span data-stu-id="d0e3a-135">**Listen method**</span></span>](listen-method.md)


 

 




