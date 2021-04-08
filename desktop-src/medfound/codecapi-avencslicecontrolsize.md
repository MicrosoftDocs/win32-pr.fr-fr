---
description: Spécifie la taille de la tranche en unités de mégaoctets (Mo), de bits ou de ligne Mo.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: CODECAPI_AVEncSliceControlSize, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111862"
---
# <a name="codecapi_avencslicecontrolsize-property"></a><span data-ttu-id="dc6f7-103">CODECAPI \_ propriété AVEncSliceControlSize</span><span class="sxs-lookup"><span data-stu-id="dc6f7-103">CODECAPI\_AVEncSliceControlSize property</span></span>

<span data-ttu-id="dc6f7-104">Spécifie la taille de la tranche en unités de mégaoctets (Mo), de bits ou de ligne Mo.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-104">Specifies the size of the slice in units of megabyte (MB), bits, or MB row.</span></span>

## <a name="data-type"></a><span data-ttu-id="dc6f7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="dc6f7-105">Data type</span></span>

<span data-ttu-id="dc6f7-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="dc6f7-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="dc6f7-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="dc6f7-107">Property GUID</span></span>

<span data-ttu-id="dc6f7-108">**CODECAPI \_ AVEncSliceControlSize**</span><span class="sxs-lookup"><span data-stu-id="dc6f7-108">**CODECAPI\_AVEncSliceControlSize**</span></span>

## <a name="remarks"></a><span data-ttu-id="dc6f7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="dc6f7-109">Remarks</span></span>

<span data-ttu-id="dc6f7-110">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="dc6f7-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="dc6f7-111">La signification de la valeur de CODECAPI \_ AVEncSliceControlSize est contrôlée par la propriété [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) .</span><span class="sxs-lookup"><span data-stu-id="dc6f7-111">The meaning of the value of CODECAPI\_AVEncSliceControlSize is controlled by the [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) property.</span></span> <span data-ttu-id="dc6f7-112">Le tableau suivant illustre la façon dont les \_ Propriétés CODECAPI AVEncSliceControlSize et CODECAPI \_ AVEncSliceControlMode contrôlent la taille et le nombre de secteurs dans un frame.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-112">The following table illustrates how the CODECAPI\_AVEncSliceControlSize and CODECAPI\_AVEncSliceControlMode properties control the size and number of slices in a frame.</span></span>



| <span data-ttu-id="dc6f7-113">\_Paramètre CODECAPI AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="dc6f7-113">CODECAPI\_AVEncSliceControlMode setting</span></span> | <span data-ttu-id="dc6f7-114">Signification de la valeur</span><span class="sxs-lookup"><span data-stu-id="dc6f7-114">Meaning of value</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6f7-115">0</span><span class="sxs-lookup"><span data-stu-id="dc6f7-115">0</span></span>                                       | <span data-ttu-id="dc6f7-116">Il s’agit d’un entier qui indique la taille de chaque tranche dans le frame en unités de blocs macros.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-116">This is an integer that indicates the size of each slice in the frame in units of macroblocks.</span></span> <br/> <span data-ttu-id="dc6f7-117">L’encodeur doit rejeter le paramètre lorsque la valeur est supérieure au nombre de blocs macros dans le frame.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-117">The encoder should reject the setting when the value is greater than the number of macroblocks in the frame.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="dc6f7-118">1</span><span class="sxs-lookup"><span data-stu-id="dc6f7-118">1</span></span>                                       | <span data-ttu-id="dc6f7-119">Il s’agit d’un entier qui indique la taille de chaque tranche dans le frame en unités de bits.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-119">This is an integer that indicates the size of each slice in the frame in units of bits.</span></span> <br/> <span data-ttu-id="dc6f7-120">L’encodeur doit démarrer une nouvelle tranche au niveau du bloc macro qui entraîne le dépassement de cette valeur du nombre de bits dans la tranche (la taille de chaque tranche sera toujours inférieure ou égale à cette valeur).</span><span class="sxs-lookup"><span data-stu-id="dc6f7-120">The encoder should start a new slice at the macroblock that causes the number of bits in the slice to exceed this value (so the size of each slice will always be less than or equal than this value).</span></span> <span data-ttu-id="dc6f7-121">Cela signifie que la taille de la dernière tranche peut être beaucoup plus petite que cette valeur.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-121">This means that the last slice size could be significantly smaller than this value.</span></span> <br/> |
| <span data-ttu-id="dc6f7-122">2</span><span class="sxs-lookup"><span data-stu-id="dc6f7-122">2</span></span>                                       | <span data-ttu-id="dc6f7-123">Il s’agit d’un entier qui indique la taille de chaque tranche dans le frame en unités de lignes bloc macro.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-123">This is an integer that indicates the size of each slice in the frame in units of macroblock rows.</span></span> <br/> <span data-ttu-id="dc6f7-124">L’encodeur doit rejeter le paramètre lorsque la valeur est supérieure au nombre de lignes bloc macro dans le frame.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-124">The encoder should reject the setting when the value is greater than the number of macroblock rows in the frame.</span></span><br/>                                                                                                                                                                 |



 

<span data-ttu-id="dc6f7-125">Si l’application ne définit pas de valeur pour [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), l’encodeur doit renvoyer une erreur.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-125">If the application does not set a value for [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), the encoder should return an error.</span></span>

<span data-ttu-id="dc6f7-126">La valeur par défaut recommandée consiste à avoir une seule tranche pour l’ensemble du frame.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-126">The recommended default is to have a single slice for whole frame.</span></span>

<span data-ttu-id="dc6f7-127">Certains encodeurs peuvent coder les tranches en parallèle et, par conséquent, les performances peuvent être affectées en fonction des paramètres de contrôle de la tranche.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-127">Some encoders might encode slices in parallel and so performance could be affected depending on the slice control settings.</span></span> <span data-ttu-id="dc6f7-128">Par exemple, l’encodage d’un frame en tant que tranche unique peut être plus lent que si le frame était encodé comme plusieurs tranches.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-128">For example, encoding a frame as a single slice might be slower than if the frame was encoded as multiple slices.</span></span>

<span data-ttu-id="dc6f7-129">Les paramètres de contrôle de la tranche sont dynamiques et peuvent être modifiés au cours de la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="dc6f7-129">The slice control settings are dynamic and can be changed during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc6f7-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc6f7-130">Requirements</span></span>



| <span data-ttu-id="dc6f7-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc6f7-131">Requirement</span></span> | <span data-ttu-id="dc6f7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc6f7-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6f7-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc6f7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dc6f7-134">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dc6f7-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="dc6f7-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc6f7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dc6f7-136">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dc6f7-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dc6f7-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc6f7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc6f7-138"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc6f7-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc6f7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc6f7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc6f7-140">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc6f7-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




