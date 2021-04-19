---
description: La méthode STEP avance le DVD-Video flux du nombre spécifié de frames.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Step, méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521900"
---
# <a name="step-method"></a><span data-ttu-id="70120-103">Step, méthode</span><span class="sxs-lookup"><span data-stu-id="70120-103">Step Method</span></span>

> [!Note]  
> <span data-ttu-id="70120-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70120-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="70120-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="70120-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="70120-106">La `Step` méthode avance le DVD-Video flux du nombre spécifié de frames.</span><span class="sxs-lookup"><span data-stu-id="70120-106">The `Step` method advances the DVD-Video stream by the specified number of frames.</span></span>

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a><span data-ttu-id="70120-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70120-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70120-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="70120-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="70120-109">Spécifie le nombre de frames à exécuter pas à pas sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="70120-109">Specifies the number of frames to step as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70120-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="70120-110">Return Value</span></span>

<span data-ttu-id="70120-111">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="70120-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70120-112">Notes</span><span class="sxs-lookup"><span data-stu-id="70120-112">Remarks</span></span>

<span data-ttu-id="70120-113">Avant d’appeler cette méthode, appelez [**CanStep**](canstep-method.md) pour déterminer si le décodeur prend en charge l’exécution pas à pas.</span><span class="sxs-lookup"><span data-stu-id="70120-113">Before calling this method, call [**CanStep**](canstep-method.md) to determine whether the decoder supports frame stepping.</span></span>

<span data-ttu-id="70120-114">Si le DVD-Video est lu en mode inverse lorsque cette méthode est appelée et que le décodeur prend en charge l’exécution pas à pas de l’image inverse, l’exécution pas à pas est effectuée en sens inverse.</span><span class="sxs-lookup"><span data-stu-id="70120-114">If the DVD-Video is playing in reverse mode when this method is called, and the decoder supports reverse frame stepping, then the frame stepping is done in reverse.</span></span>

 

 



