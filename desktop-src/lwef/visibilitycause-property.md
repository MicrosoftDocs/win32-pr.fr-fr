---
title: Propriété VisibilityCause
description: Propriété VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379978"
---
# <a name="visibilitycause-property"></a><span data-ttu-id="00d06-103">Propriété VisibilityCause</span><span class="sxs-lookup"><span data-stu-id="00d06-103">VisibilityCause Property</span></span>

<span data-ttu-id="00d06-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="00d06-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="00d06-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="00d06-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="00d06-106">Retourne une valeur entière qui spécifie ce qui a provoqué l’état visible du caractère.</span><span class="sxs-lookup"><span data-stu-id="00d06-106">Returns an integer value that specifies what caused the character's visible state.</span></span>

</dd> <dt>

<span data-ttu-id="00d06-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="00d06-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="00d06-108">*agent*. **Caractères («***CharacterID***»). VisibilityCause**</span><span class="sxs-lookup"><span data-stu-id="00d06-108">*agent*.**Characters("***CharacterID***").VisibilityCause**</span></span>



| <span data-ttu-id="00d06-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="00d06-109">Value</span></span> | <span data-ttu-id="00d06-110">Description</span><span class="sxs-lookup"><span data-stu-id="00d06-110">Description</span></span>                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d06-111">0</span><span class="sxs-lookup"><span data-stu-id="00d06-111">0</span></span>     | <span data-ttu-id="00d06-112">Le caractère n’a pas été affiché.</span><span class="sxs-lookup"><span data-stu-id="00d06-112">The character has not been shown.</span></span>                                                                            |
| <span data-ttu-id="00d06-113">1</span><span class="sxs-lookup"><span data-stu-id="00d06-113">1</span></span>     | <span data-ttu-id="00d06-114">Utilisateur a masqué le caractère à l’aide de la commande dans le menu contextuel de l’icône de la barre des tâches du caractère ou à l’aide de l’entrée vocale..</span><span class="sxs-lookup"><span data-stu-id="00d06-114">User hid the character using the command on the character's taskbar icon pop-up menu or using speech input..</span></span> |
| <span data-ttu-id="00d06-115">2</span><span class="sxs-lookup"><span data-stu-id="00d06-115">2</span></span>     | <span data-ttu-id="00d06-116">L’utilisateur a affiché le caractère.</span><span class="sxs-lookup"><span data-stu-id="00d06-116">The user showed the character.</span></span>                                                                               |
| <span data-ttu-id="00d06-117">3</span><span class="sxs-lookup"><span data-stu-id="00d06-117">3</span></span>     | <span data-ttu-id="00d06-118">Votre application a masqué le caractère.</span><span class="sxs-lookup"><span data-stu-id="00d06-118">Your application hid the character.</span></span>                                                                          |
| <span data-ttu-id="00d06-119">4</span><span class="sxs-lookup"><span data-stu-id="00d06-119">4</span></span>     | <span data-ttu-id="00d06-120">Votre application a affiché le caractère.</span><span class="sxs-lookup"><span data-stu-id="00d06-120">Your application showed the character.</span></span>                                                                       |
| <span data-ttu-id="00d06-121">5</span><span class="sxs-lookup"><span data-stu-id="00d06-121">5</span></span>     | <span data-ttu-id="00d06-122">Une autre application cliente a masqué le caractère.</span><span class="sxs-lookup"><span data-stu-id="00d06-122">Another client application hid the character.</span></span>                                                                |
| <span data-ttu-id="00d06-123">6</span><span class="sxs-lookup"><span data-stu-id="00d06-123">6</span></span>     | <span data-ttu-id="00d06-124">Une autre application cliente a affiché le caractère.</span><span class="sxs-lookup"><span data-stu-id="00d06-124">Another client application showed the character.</span></span>                                                             |
| <span data-ttu-id="00d06-125">7</span><span class="sxs-lookup"><span data-stu-id="00d06-125">7</span></span>     | <span data-ttu-id="00d06-126">L’utilisateur a masqué le caractère à l’aide de la commande dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="00d06-126">The user hid the character using the command on the character's pop-up menu.</span></span>                                 |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00d06-127">Notes</span><span class="sxs-lookup"><span data-stu-id="00d06-127">Remarks</span></span>

<span data-ttu-id="00d06-128">Vous pouvez utiliser cette propriété pour déterminer ce qui a provoqué le déplacement du caractère lorsque plusieurs applications partagent le même caractère.</span><span class="sxs-lookup"><span data-stu-id="00d06-128">You can use this property to determine what caused the character to move when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="00d06-129">Ces valeurs sont les mêmes que celles retournées par les événements d' [**affichage**](show-event.md) et de [**masquage**](hide-event.md) .</span><span class="sxs-lookup"><span data-stu-id="00d06-129">These values are the same as those returned by the [**Show**](show-event.md) and [**Hide**](hide-event.md) events.</span></span>

## <a name="see-also"></a><span data-ttu-id="00d06-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00d06-130">See Also</span></span>

<span data-ttu-id="00d06-131">[**Masquer les événements**](hide-event.md), [**afficher les événements**](show-event.md), masquer la [**méthode**](hide-method.md), afficher la [**méthode**](show-method.md)</span><span class="sxs-lookup"><span data-stu-id="00d06-131">[**Hide event**](hide-event.md), [**Show event**](show-event.md), [**Hide method**](hide-method.md), [**Show method**](show-method.md)</span></span>


 

 




