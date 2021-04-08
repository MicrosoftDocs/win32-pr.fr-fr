---
title: IManipulationProcessor propriété MinimumScaleRotateRadius
description: Spécifie la taille des contacts à distance sur un mouvement de mise à l’échelle ou de rotation pour déclencher la manipulation.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Touche Windows de la propriété MinimumScaleRotateRadius
- Propriété MinimumScaleRotateRadius Windows tactile, interface IManipulationProcessor
- Interface IManipulationProcessor Windows tactile, propriété MinimumScaleRotateRadius
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678613"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a><span data-ttu-id="f4a6b-106">IManipulationProcessor :: MinimumScaleRotateRadius, propriété</span><span class="sxs-lookup"><span data-stu-id="f4a6b-106">IManipulationProcessor::MinimumScaleRotateRadius property</span></span>

<span data-ttu-id="f4a6b-107">Spécifie la taille des contacts à distance sur un mouvement de mise à l’échelle ou de rotation pour déclencher la manipulation.</span><span class="sxs-lookup"><span data-stu-id="f4a6b-107">Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.</span></span>

<span data-ttu-id="f4a6b-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f4a6b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a6b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4a6b-109">Syntax</span></span>


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a><span data-ttu-id="f4a6b-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f4a6b-110">Property value</span></span>

<span data-ttu-id="f4a6b-111">Spécifie la distance minimale entre les contacts pour déclencher des mouvements d’échelle ou de rotation.</span><span class="sxs-lookup"><span data-stu-id="f4a6b-111">Specifies the minimum distance between contacts to trigger scale or rotate gestures.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f4a6b-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f4a6b-112">Error codes</span></span>

## <a name="remarks"></a><span data-ttu-id="f4a6b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f4a6b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4a6b-114">Cette propriété est définie en centipixels (centièmes de pixel).</span><span class="sxs-lookup"><span data-stu-id="f4a6b-114">This property is set in centipixels (100ths of a pixel).</span></span>

 

<span data-ttu-id="f4a6b-115">Si vous définissez cette valeur, le processeur de manipulation ignore les gestes dont le rayon est trop petit.</span><span class="sxs-lookup"><span data-stu-id="f4a6b-115">Setting this value will make the manipulation processor ignore gestures that have too small of a radius.</span></span> <span data-ttu-id="f4a6b-116">Cela est utile si vous souhaitez empêcher un utilisateur de manipuler un objet pour qu’il soit trop petit pour un rayon.</span><span class="sxs-lookup"><span data-stu-id="f4a6b-116">This is useful if you want to prevent a user from manipulating an object to too small of a radius.</span></span> <span data-ttu-id="f4a6b-117">Par exemple, si vous utilisez un processeur de manipulation avec un cercle et que vous souhaitez vous assurer qu’il gère un rayon supérieur à 100 pixels, vous devez définir cette valeur sur 10000.</span><span class="sxs-lookup"><span data-stu-id="f4a6b-117">For example, if you are using a manipulation processor with a circle and want the ensure that it maintains a radius greater than 100 pixels, you would set this value to 10000.</span></span>

## <a name="examples"></a><span data-ttu-id="f4a6b-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="f4a6b-118">Examples</span></span>


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a><span data-ttu-id="f4a6b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4a6b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a6b-120">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="f4a6b-120">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




