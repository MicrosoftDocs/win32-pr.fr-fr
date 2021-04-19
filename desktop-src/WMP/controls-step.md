---
title: Controls. Step, méthode
description: La méthode STEP fait en sorte que l’élément multimédia vidéo actuel fige la lecture sur le frame suivant ou le frame précédent.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- méthode STEP du lecteur Windows Media
- Step, méthode lecteur Windows Media, classe Controls
- Classe Controls lecteur Windows Media, méthode STEP
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537475"
---
# <a name="controlsstep-method"></a><span data-ttu-id="bcf89-106">Controls. Step, méthode</span><span class="sxs-lookup"><span data-stu-id="bcf89-106">Controls.step method</span></span>

<span data-ttu-id="bcf89-107">La méthode **Step** fait en sorte que l’élément multimédia vidéo actuel fige la lecture sur le frame suivant ou le frame précédent.</span><span class="sxs-lookup"><span data-stu-id="bcf89-107">The **step** method causes the current video media item to freeze playback on the next frame or the previous frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf89-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcf89-108">Syntax</span></span>


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a><span data-ttu-id="bcf89-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcf89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf89-110">*frameCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcf89-110">*frameCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf89-111">**Nombre** (**long**) indiquant le nombre de frames à exécuter avant le gel.</span><span class="sxs-lookup"><span data-stu-id="bcf89-111">**Number** (**long**) indicating how many frames to step before freezing.</span></span> <span data-ttu-id="bcf89-112">Doit être défini à 1 ou-1.</span><span class="sxs-lookup"><span data-stu-id="bcf89-112">Must currently be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf89-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcf89-113">Return value</span></span>

<span data-ttu-id="bcf89-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bcf89-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf89-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bcf89-115">Remarks</span></span>

<span data-ttu-id="bcf89-116">Cette méthode ne prend actuellement en charge que les paramètres 1 ou-1. vous ne pouvez donc pas effectuer un pas à pas d’un seul Frame à la fois.</span><span class="sxs-lookup"><span data-stu-id="bcf89-116">This method currently only supports the parameters 1 or -1, so you can only step one frame at a time.</span></span>

<span data-ttu-id="bcf89-117">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bcf89-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf89-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcf89-118">Requirements</span></span>



| <span data-ttu-id="bcf89-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcf89-119">Requirement</span></span> | <span data-ttu-id="bcf89-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcf89-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf89-121">Version</span><span class="sxs-lookup"><span data-stu-id="bcf89-121">Version</span></span><br/> | <span data-ttu-id="bcf89-122">Lecteur Windows Media pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bcf89-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="bcf89-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf89-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="bcf89-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf89-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf89-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcf89-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf89-126">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="bcf89-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="bcf89-127">**Objet DVD**</span><span class="sxs-lookup"><span data-stu-id="bcf89-127">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





