---
title: Événement Player. CdromMediaChange
description: L’événement CdromMediaChange se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD. | Événement Player. CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Événement CdromMediaChange lecteur Windows Media
- Événement CdromMediaChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement CdromMediaChange
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523569"
---
# <a name="playercdrommediachange-event"></a><span data-ttu-id="be8ce-107">Événement Player. CdromMediaChange</span><span class="sxs-lookup"><span data-stu-id="be8ce-107">Player.CdromMediaChange event</span></span>

<span data-ttu-id="be8ce-108">L’événement **CdromMediaChange** se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="be8ce-108">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8ce-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be8ce-109">Syntax</span></span>


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a><span data-ttu-id="be8ce-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be8ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be8ce-111">*CdromNum*</span><span class="sxs-lookup"><span data-stu-id="be8ce-111">*CdromNum*</span></span> 
</dt> <dd>

<span data-ttu-id="be8ce-112">**Nombre** (**long**) spécifiant l’index du lecteur de CD ou de DVD.</span><span class="sxs-lookup"><span data-stu-id="be8ce-112">**Number** (**long**) specifying the index of the CD or DVD drive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be8ce-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be8ce-113">Return value</span></span>

<span data-ttu-id="be8ce-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="be8ce-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be8ce-115">Notes</span><span class="sxs-lookup"><span data-stu-id="be8ce-115">Remarks</span></span>

<span data-ttu-id="be8ce-116">L’index du lecteur de CD correspond à l’index d’un objet **cdrom** dans le **CdromCollection**.</span><span class="sxs-lookup"><span data-stu-id="be8ce-116">The index of the CD drive corresponds to the index of a **Cdrom** object in the **CdromCollection**.</span></span>

<span data-ttu-id="be8ce-117">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="be8ce-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="be8ce-118">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="be8ce-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="be8ce-119">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="be8ce-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="be8ce-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be8ce-120">Requirements</span></span>



| <span data-ttu-id="be8ce-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be8ce-121">Requirement</span></span> | <span data-ttu-id="be8ce-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="be8ce-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be8ce-123">Version</span><span class="sxs-lookup"><span data-stu-id="be8ce-123">Version</span></span><br/> | <span data-ttu-id="be8ce-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="be8ce-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="be8ce-125">DLL</span><span class="sxs-lookup"><span data-stu-id="be8ce-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="be8ce-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be8ce-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be8ce-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be8ce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8ce-128">**Objet cdrom**</span><span class="sxs-lookup"><span data-stu-id="be8ce-128">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="be8ce-129">**Objet CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="be8ce-129">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="be8ce-130">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="be8ce-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





