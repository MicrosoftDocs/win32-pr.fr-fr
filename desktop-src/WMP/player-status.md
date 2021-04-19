---
title: Player. Status
description: La propriété Status récupère une valeur indiquant l’état du lecteur Windows Media.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Lecteur Windows Media Player. Status
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539556"
---
# <a name="playerstatus"></a><span data-ttu-id="61249-104">Player. Status</span><span class="sxs-lookup"><span data-stu-id="61249-104">Player.status</span></span>

<span data-ttu-id="61249-105">La propriété **Status** récupère une valeur indiquant l’état du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="61249-105">The **status** property retrieves a value indicating the status of Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="61249-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61249-106">Syntax</span></span>

<span data-ttu-id="61249-107">*lecteur* . **État**</span><span class="sxs-lookup"><span data-stu-id="61249-107">*player* .**status**</span></span>

## <a name="possible-values"></a><span data-ttu-id="61249-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="61249-108">Possible Values</span></span>

<span data-ttu-id="61249-109">Cette propriété est une chaîne en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="61249-109">This property is a read-only String.</span></span>

## <a name="remarks"></a><span data-ttu-id="61249-110">Notes</span><span class="sxs-lookup"><span data-stu-id="61249-110">Remarks</span></span>

<span data-ttu-id="61249-111">Les valeurs contenues dans cette propriété sont sujettes à modification à tout moment et doivent être utilisées à des fins d’affichage uniquement.</span><span class="sxs-lookup"><span data-stu-id="61249-111">The values contained in this property are subject to change at any time, and should be used for display purposes only.</span></span>

<span data-ttu-id="61249-112">L’événement **statuschange** est déclenché à chaque modification de la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="61249-112">The **StatusChange** event is fired whenever this property changes value.</span></span>

## <a name="requirements"></a><span data-ttu-id="61249-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61249-113">Requirements</span></span>



| <span data-ttu-id="61249-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61249-114">Requirement</span></span> | <span data-ttu-id="61249-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="61249-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61249-116">Version</span><span class="sxs-lookup"><span data-stu-id="61249-116">Version</span></span><br/> | <span data-ttu-id="61249-117">Lecteur Windows Media 7,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="61249-117">Windows Media Player 7.0 or later.</span></span><br/>                                      |
| <span data-ttu-id="61249-118">DLL</span><span class="sxs-lookup"><span data-stu-id="61249-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="61249-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61249-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61249-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61249-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61249-121">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="61249-121">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="61249-122">**Événement Player. StatusChange**</span><span class="sxs-lookup"><span data-stu-id="61249-122">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
</dt> </dl>

 

 





