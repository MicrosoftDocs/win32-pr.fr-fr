---
description: Ajoute des données de trait pour un seul trait à IInkAnalyzer et assigne un identificateur de culture spécifique au trait.
ms.assetid: 65eb805e-05ed-4144-b17e-872c47ab33fa
title: 'IInkAnalyzer :: AddStrokeForLanguage, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 674a58ef891d919d09f86f28a35748de3537db91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862702"
---
# <a name="iinkanalyzeraddstrokeforlanguage-method"></a><span data-ttu-id="cbe02-103">IInkAnalyzer :: AddStrokeForLanguage, méthode</span><span class="sxs-lookup"><span data-stu-id="cbe02-103">IInkAnalyzer::AddStrokeForLanguage method</span></span>

<span data-ttu-id="cbe02-104">Ajoute des données de trait pour un seul trait à [**IInkAnalyzer**](iinkanalyzer.md) et assigne un identificateur de culture spécifique au trait.</span><span class="sxs-lookup"><span data-stu-id="cbe02-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns a specific culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbe02-105">Syntax</span></span>


```C++
HRESULT AddStrokeForLanguage(
  [in]  LONG         lStrokeId,
  [in]  LONG         lStrokeLCID,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="cbe02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbe02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbe02-107">*lStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbe02-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe02-108">Identificateur du trait à ajouter.</span><span class="sxs-lookup"><span data-stu-id="cbe02-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="cbe02-109">*lStrokeLCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbe02-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe02-110">Identificateur de culture à assigner au trait.</span><span class="sxs-lookup"><span data-stu-id="cbe02-110">The culture identifier to assign to the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="cbe02-111">*ulStrokePacketDataCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbe02-111">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe02-112">Nombre de paquets dans le trait.</span><span class="sxs-lookup"><span data-stu-id="cbe02-112">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="cbe02-113">*plStrokePacketData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbe02-113">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe02-114">Tableau contenant les données de paquet pour le trait.</span><span class="sxs-lookup"><span data-stu-id="cbe02-114">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="cbe02-115">*ulStrokePacketDescriptionCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbe02-115">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe02-116">Nombre de propriétés dans chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="cbe02-116">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="cbe02-117">*pStrokePacketDescriptionGuids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbe02-117">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe02-118">Tableau contenant les identificateurs de propriété de paquet.</span><span class="sxs-lookup"><span data-stu-id="cbe02-118">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="cbe02-119">*ppContextNodeStrokeAddedTo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cbe02-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe02-120">Pointeur dont la valeur est définie sur le pointeur du [**IContextNode**](icontextnode.md) qui contient le trait nouvellement ajouté.</span><span class="sxs-lookup"><span data-stu-id="cbe02-120">A pointer whose value is set to the pointer of the [**IContextNode**](icontextnode.md) that contains the newly added stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbe02-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbe02-121">Return value</span></span>

<span data-ttu-id="cbe02-122">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="cbe02-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cbe02-123">Notes</span><span class="sxs-lookup"><span data-stu-id="cbe02-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cbe02-124">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeStrokeAddedTo* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="cbe02-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="cbe02-125">Quand *ppContextNodeStrokeAddedTo* a la valeur **null**, il indique que l’appelant ne s’intéresse pas à la valeur de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="cbe02-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="cbe02-126">[**IInkAnalyzer**](iinkanalyzer.md) ajoute le trait à un [**IContextNode**](icontextnode.md) de type UnclassifiedInk (consultez [types de nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="cbe02-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="cbe02-127">Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="cbe02-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="cbe02-128">[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture *lStrokeLCID* au trait et ajoute le trait au premier nœud de contexte UnclassifiedInk sous le nœud racine de l’analyseur d’encre qui contient des traits avec le même identificateur de culture.</span><span class="sxs-lookup"><span data-stu-id="cbe02-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns *lStrokeLCID* culture identifier to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="cbe02-129">Si l’analyseur d’encre n’a pas de nœud avec le même identificateur de culture, il crée un nœud de contexte UnclassifiedInk sous son nœud racine et ajoute le trait au nouveau nœud de contexte UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="cbe02-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="cbe02-130">*plStrokePacketData* contient des données de paquet pour tous les points du trait.</span><span class="sxs-lookup"><span data-stu-id="cbe02-130">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="cbe02-131">*pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point du trait.</span><span class="sxs-lookup"><span data-stu-id="cbe02-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="cbe02-132">Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="cbe02-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="cbe02-133">Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la région et de la zone englobante du trait ajouté.</span><span class="sxs-lookup"><span data-stu-id="cbe02-133">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="cbe02-134">Si le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur de trait, le **IInkAnalyzer** retourne un **HRESULT** d' **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="cbe02-134">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe02-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbe02-135">Requirements</span></span>



| <span data-ttu-id="cbe02-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbe02-136">Requirement</span></span> | <span data-ttu-id="cbe02-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbe02-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe02-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbe02-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe02-139">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbe02-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cbe02-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbe02-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe02-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbe02-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cbe02-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbe02-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbe02-143"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cbe02-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cbe02-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cbe02-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbe02-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbe02-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cbe02-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbe02-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe02-147">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="cbe02-147">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cbe02-148">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="cbe02-148">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="cbe02-149">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="cbe02-149">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="cbe02-150">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="cbe02-150">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="cbe02-151">**IInkAnalyzer :: RemoveStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="cbe02-151">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="cbe02-152">**IInkAnalyzer :: RemoveStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="cbe02-152">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="cbe02-153">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="cbe02-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

