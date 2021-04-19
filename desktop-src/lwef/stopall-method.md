---
title: StopAll, méthode
description: StopAll, méthode
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510253"
---
# <a name="stopall-method"></a><span data-ttu-id="b6df5-103">StopAll, méthode</span><span class="sxs-lookup"><span data-stu-id="b6df5-103">StopAll Method</span></span>

<span data-ttu-id="b6df5-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b6df5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b6df5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="b6df5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b6df5-106">Arrête toutes les demandes d’animation ou les types de demandes spécifiés pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="b6df5-106">Stops all animation requests or specified types of requests for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="b6df5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="b6df5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b6df5-108">\*agent ***. Caractères («*** CharacterID \* \* * »). StopAll*, \*  \[ *type*\]</span><span class="sxs-lookup"><span data-stu-id="b6df5-108">*agent ***.Characters ("*** CharacterID\*\*\*").StopAll*\* \[*Type*\]</span></span>



| <span data-ttu-id="b6df5-109">Partie</span><span class="sxs-lookup"><span data-stu-id="b6df5-109">Part</span></span>   | <span data-ttu-id="b6df5-110">Description</span><span class="sxs-lookup"><span data-stu-id="b6df5-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6df5-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="b6df5-111">*Type*</span></span> | <span data-ttu-id="b6df5-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="b6df5-112">Optional.</span></span> <span data-ttu-id="b6df5-113">Pour utiliser ce paramètre, vous pouvez utiliser l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b6df5-113">To use this parameter you can use any of the following values.</span></span> <span data-ttu-id="b6df5-114">Vous pouvez également spécifier plusieurs types en les séparant par des virgules.</span><span class="sxs-lookup"><span data-stu-id="b6df5-114">You can also specify multiple types by separating them with commas.</span></span> <br/> <span data-ttu-id="b6df5-115">«**Récupérer**»</span><span class="sxs-lookup"><span data-stu-id="b6df5-115">"**Get**"</span></span> <br/> <span data-ttu-id="b6df5-116">Pour arrêter toutes les demandes d' [**extraction**](get-method.md) mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b6df5-116">To stop all queued [**Get**](get-method.md) requests.</span></span><br/> <span data-ttu-id="b6df5-117">«**NonQueuedGet**»</span><span class="sxs-lookup"><span data-stu-id="b6df5-117">"**NonQueuedGet**"</span></span> <br/> <span data-ttu-id="b6df5-118">Pour arrêter toutes les demandes d' [**extraction**](get-method.md) non mises en file d’attente (la méthode d'**extraction** avec le paramètre de **file d’attente** a la valeur **false**).</span><span class="sxs-lookup"><span data-stu-id="b6df5-118">To stop all non-queued [**Get**](get-method.md) requests (**Get** method with **Queue** parameter set to **False**).</span></span><br/> <span data-ttu-id="b6df5-119">«**Déplacer**»</span><span class="sxs-lookup"><span data-stu-id="b6df5-119">"**Move**"</span></span> <br/> <span data-ttu-id="b6df5-120">Pour arrêter toutes les demandes [**MoveTo**](moveto-method.md) mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b6df5-120">To stop all queued [**MoveTo**](moveto-method.md) requests.</span></span><br/> <span data-ttu-id="b6df5-121">«**Lecture**»</span><span class="sxs-lookup"><span data-stu-id="b6df5-121">"**Play**"</span></span> <br/> <span data-ttu-id="b6df5-122">Pour arrêter toutes les demandes de [**lecture**](play-method.md) mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b6df5-122">To stop all queued [**Play**](play-method.md) requests.</span></span><br/> <span data-ttu-id="b6df5-123">«**Speak**»</span><span class="sxs-lookup"><span data-stu-id="b6df5-123">"**Speak**"</span></span> <br/> <span data-ttu-id="b6df5-124">Pour arrêter toutes les demandes [**Speak**](speak-method.md) mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b6df5-124">To stop all queued [**Speak**](speak-method.md) requests.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6df5-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b6df5-125">Remarks</span></span>

<span data-ttu-id="b6df5-126">Si vous ne définissez pas le paramètre de **type** , le serveur arrête toutes les animations pour le caractère, y compris les demandes d' [**extraction**](get-method.md) mises en file d’attente et non mises en file d’attente, et efface sa file d’attente d’animation.</span><span class="sxs-lookup"><span data-stu-id="b6df5-126">If you don't set the **Type** parameter, the server stops all animations for the character, including queued and non-queued [**Get**](get-method.md) requests, and clears its animation queue.</span></span> <span data-ttu-id="b6df5-127">Elle arrête également la diffusion d’un caractère masqué ou présentant une animation.</span><span class="sxs-lookup"><span data-stu-id="b6df5-127">It also stops playing a character's Hiding or Showing animation.</span></span>

<span data-ttu-id="b6df5-128">Cette méthode ne génère pas d’objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="b6df5-128">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6df5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6df5-129">See Also</span></span>

[<span data-ttu-id="b6df5-130">**Stop, méthode**</span><span class="sxs-lookup"><span data-stu-id="b6df5-130">**Stop method**</span></span>](stop-method.md)


 

