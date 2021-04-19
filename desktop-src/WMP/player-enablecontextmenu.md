---
title: Player. enableContextMenu
description: La propriété enableContextMenu spécifie ou récupère une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Lecteur Windows Media Player. enableContextMenu
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528629"
---
# <a name="playerenablecontextmenu"></a><span data-ttu-id="7268a-104">Player. enableContextMenu</span><span class="sxs-lookup"><span data-stu-id="7268a-104">Player.enableContextMenu</span></span>

<span data-ttu-id="7268a-105">La propriété **enableContextMenu** spécifie ou récupère une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="7268a-105">The **enableContextMenu** property specifies or retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="7268a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7268a-106">Syntax</span></span>

<span data-ttu-id="7268a-107">*lecteur*. **enableContextMenu**</span><span class="sxs-lookup"><span data-stu-id="7268a-107">*player*.**enableContextMenu**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7268a-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7268a-108">Possible Values</span></span>

<span data-ttu-id="7268a-109">Cette propriété est une valeur booléenne en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7268a-109">This property is a read/write Boolean.</span></span>



| <span data-ttu-id="7268a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="7268a-110">Value</span></span> | <span data-ttu-id="7268a-111">Description</span><span class="sxs-lookup"><span data-stu-id="7268a-111">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="7268a-112">true</span><span class="sxs-lookup"><span data-stu-id="7268a-112">true</span></span>  | <span data-ttu-id="7268a-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="7268a-113">Default.</span></span> <span data-ttu-id="7268a-114">Activez le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7268a-114">Enable the context menu.</span></span> |
| <span data-ttu-id="7268a-115">false</span><span class="sxs-lookup"><span data-stu-id="7268a-115">false</span></span> | <span data-ttu-id="7268a-116">N’activez pas le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7268a-116">Do not enable the context menu.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="7268a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7268a-117">Remarks</span></span>

<span data-ttu-id="7268a-118">Pendant la lecture en plein écran, le lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **UIMODE** est égal à « None ».</span><span class="sxs-lookup"><span data-stu-id="7268a-118">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="7268a-119">**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7268a-119">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="7268a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7268a-120">Requirements</span></span>



| <span data-ttu-id="7268a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7268a-121">Requirement</span></span> | <span data-ttu-id="7268a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7268a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7268a-123">Version</span><span class="sxs-lookup"><span data-stu-id="7268a-123">Version</span></span><br/> | <span data-ttu-id="7268a-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7268a-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7268a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7268a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7268a-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7268a-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7268a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7268a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7268a-128">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="7268a-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





