---
title: Settings. balance
description: La propriété balance spécifie ou récupère le solde stéréo actuel.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Settings. balance du lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541010"
---
# <a name="settingsbalance"></a><span data-ttu-id="842ad-104">Settings. balance</span><span class="sxs-lookup"><span data-stu-id="842ad-104">Settings.balance</span></span>

<span data-ttu-id="842ad-105">La propriété **balance** spécifie ou récupère le solde stéréo actuel.</span><span class="sxs-lookup"><span data-stu-id="842ad-105">The **balance** property specifies or retrieves the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="842ad-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="842ad-106">Syntax</span></span>

<span data-ttu-id="842ad-107">Player. Settings. balance</span><span class="sxs-lookup"><span data-stu-id="842ad-107">player.settings.balance</span></span>

## <a name="possible-values"></a><span data-ttu-id="842ad-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="842ad-108">Possible Values</span></span>

<span data-ttu-id="842ad-109">Cette propriété est un **nombre** en lecture/écriture (**long**).</span><span class="sxs-lookup"><span data-stu-id="842ad-109">This property is a read/write **Number** (**long**).</span></span> <span data-ttu-id="842ad-110">Les valeurs sont comprises entre 100 et 100, avec une valeur par défaut de zéro.</span><span class="sxs-lookup"><span data-stu-id="842ad-110">Values range from  100 to 100, with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="842ad-111">Notes</span><span class="sxs-lookup"><span data-stu-id="842ad-111">Remarks</span></span>

<span data-ttu-id="842ad-112">La valeur zéro indique que le son est lu à un volume égal sur les canaux gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="842ad-112">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="842ad-113">Une valeur de 100 indique que l’audio est lu uniquement sur le canal de gauche.</span><span class="sxs-lookup"><span data-stu-id="842ad-113">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="842ad-114">Une valeur de 100 indique que l’audio est lu uniquement sur le canal approprié.</span><span class="sxs-lookup"><span data-stu-id="842ad-114">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="842ad-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="842ad-115">Requirements</span></span>



| <span data-ttu-id="842ad-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="842ad-116">Requirement</span></span> | <span data-ttu-id="842ad-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="842ad-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="842ad-118">Version</span><span class="sxs-lookup"><span data-stu-id="842ad-118">Version</span></span><br/> | <span data-ttu-id="842ad-119">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="842ad-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="842ad-120">DLL</span><span class="sxs-lookup"><span data-stu-id="842ad-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="842ad-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="842ad-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="842ad-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="842ad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842ad-123">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="842ad-123">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





