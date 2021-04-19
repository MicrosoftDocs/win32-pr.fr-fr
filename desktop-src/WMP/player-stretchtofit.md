---
title: Player. stretchToFit
description: La propriété stretchToFit spécifie ou récupère une valeur indiquant si la vidéo affichée par le contrôle du lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Lecteur Windows Media Player. stretchToFit
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541265"
---
# <a name="playerstretchtofit"></a><span data-ttu-id="eb91c-104">Player. stretchToFit</span><span class="sxs-lookup"><span data-stu-id="eb91c-104">Player.stretchToFit</span></span>

<span data-ttu-id="eb91c-105">La propriété **stretchToFit** spécifie ou récupère une valeur indiquant si la vidéo affichée par le contrôle du lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="eb91c-105">The **stretchToFit** property specifies or retrieves a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb91c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb91c-106">Syntax</span></span>

<span data-ttu-id="eb91c-107">*lecteur*. **stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="eb91c-107">*player*.**stretchToFit**</span></span>

## <a name="possible-values"></a><span data-ttu-id="eb91c-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="eb91c-108">Possible Values</span></span>

<span data-ttu-id="eb91c-109">Cette propriété est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="eb91c-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="eb91c-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb91c-110">Value</span></span> | <span data-ttu-id="eb91c-111">Description</span><span class="sxs-lookup"><span data-stu-id="eb91c-111">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="eb91c-112">true</span><span class="sxs-lookup"><span data-stu-id="eb91c-112">true</span></span>  | <span data-ttu-id="eb91c-113">La vidéo est étirée pour s’ajuster à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="eb91c-113">The video will stretch to fit the window.</span></span>              |
| <span data-ttu-id="eb91c-114">false</span><span class="sxs-lookup"><span data-stu-id="eb91c-114">false</span></span> | <span data-ttu-id="eb91c-115">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="eb91c-115">Default.</span></span> <span data-ttu-id="eb91c-116">La vidéo n’est pas étirée pour s’ajuster à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="eb91c-116">The video will not stretch to fit the window.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eb91c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="eb91c-117">Remarks</span></span>

<span data-ttu-id="eb91c-118">Quand **stretchToFit** a la valeur true, le contrôle du lecteur Windows Media conserve les proportions d’origine de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="eb91c-118">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="eb91c-119">Si les proportions de la vidéo ne correspondent pas aux proportions de la fenêtre vidéo, les zones de masque noires peuvent apparaître en haut et en bas, ou à gauche et à droite de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="eb91c-119">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="eb91c-120">Cette propriété s’applique au contrôle du lecteur Windows Media uniquement lorsqu’il est incorporé dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="eb91c-120">This property applies to the Windows Media Player control only when embedded in a webpage.</span></span>

<span data-ttu-id="eb91c-121">**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="eb91c-121">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb91c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb91c-122">Requirements</span></span>



| <span data-ttu-id="eb91c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb91c-123">Requirement</span></span> | <span data-ttu-id="eb91c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb91c-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb91c-125">Version</span><span class="sxs-lookup"><span data-stu-id="eb91c-125">Version</span></span><br/> | <span data-ttu-id="eb91c-126">Lecteur Windows Media version 7,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="eb91c-126">Windows Media Player version 7.1 or later.</span></span><br/>                              |
| <span data-ttu-id="eb91c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="eb91c-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="eb91c-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb91c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb91c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb91c-130">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="eb91c-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





