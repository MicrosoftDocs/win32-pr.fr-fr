---
description: La méthode CanStep détermine si le décodeur MPEG-2 sur le système local peut effectuer une exécution pas à pas dans une direction spécifiée.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Méthode CanStep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033409"
---
# <a name="canstep-method"></a><span data-ttu-id="03de7-103">Méthode CanStep</span><span class="sxs-lookup"><span data-stu-id="03de7-103">CanStep Method</span></span>

> [!Note]  
> <span data-ttu-id="03de7-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="03de7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="03de7-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="03de7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="03de7-106">La `CanStep` méthode détermine si le décodeur MPEG-2 sur le système local peut effectuer un pas à pas détaillé dans une direction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="03de7-106">The `CanStep` method determines whether the MPEG-2 decoder on the local system can perform frame stepping in a specified direction.</span></span>

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a><span data-ttu-id="03de7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03de7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03de7-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span><span class="sxs-lookup"><span data-stu-id="03de7-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span></span>
</dt> <dd>

<span data-ttu-id="03de7-109">Booléen utilisé comme indicateur pour spécifier la direction, l’avant ou l’arrière, de la capacité de l’exécution pas à pas du décodeur.</span><span class="sxs-lookup"><span data-stu-id="03de7-109">Boolean used as a flag to specify the direction, forward or backward, of decoder's frame-stepping ability.</span></span>



| <span data-ttu-id="03de7-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="03de7-110">Value</span></span> | <span data-ttu-id="03de7-111">Description</span><span class="sxs-lookup"><span data-stu-id="03de7-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="03de7-112">true</span><span class="sxs-lookup"><span data-stu-id="03de7-112">true</span></span>  | <span data-ttu-id="03de7-113">L’étape de décodage peut-elle reculer ?</span><span class="sxs-lookup"><span data-stu-id="03de7-113">Can decoder step backward?</span></span>                           |
| <span data-ttu-id="03de7-114">false</span><span class="sxs-lookup"><span data-stu-id="03de7-114">false</span></span> | <span data-ttu-id="03de7-115">L’étape de décodage peut-elle progresser ?</span><span class="sxs-lookup"><span data-stu-id="03de7-115">Can decoder step forward?</span></span> <span data-ttu-id="03de7-116">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="03de7-116">This is the default value.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03de7-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03de7-117">Return Value</span></span>

<span data-ttu-id="03de7-118">Retourne une valeur booléenne true si le décodeur peut effectuer un pas à pas détaillé dans la direction spécifiée, et false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="03de7-118">Returns a Boolean value of true if the decoder can step in the specified direction, and false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="03de7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="03de7-119">Remarks</span></span>

<span data-ttu-id="03de7-120">Les décodeurs MPEG-2 ne prennent pas tous en charge les nouvelles fonctionnalités d’exécution pas à pas dans DirectShow® 8,0.</span><span class="sxs-lookup"><span data-stu-id="03de7-120">Not all hardware MPEG-2 decoders support the new frame stepping capabilities in DirectShow® 8.0.</span></span> <span data-ttu-id="03de7-121">Cette méthode interroge le décodeur pour ses fonctionnalités de pas à pas de frame.</span><span class="sxs-lookup"><span data-stu-id="03de7-121">This method queries the decoder for its frame stepping capabilities.</span></span> <span data-ttu-id="03de7-122">Si le décodeur peut effectuer un pas à pas, une application peut utiliser la méthode [**Step**](step-method.md) pour parcourir les frames.</span><span class="sxs-lookup"><span data-stu-id="03de7-122">If the decoder can perform frame stepping, an application can use the [**Step**](step-method.md) method to step through frames.</span></span> <span data-ttu-id="03de7-123">Cette méthode retourne toujours la **valeur true** si un décodeur logiciel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="03de7-123">This method will always return **true** if a software decoder is being used.</span></span>

 

 



