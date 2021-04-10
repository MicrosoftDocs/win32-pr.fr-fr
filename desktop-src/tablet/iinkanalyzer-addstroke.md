---
description: Ajoute des données de trait pour un seul trait à IInkAnalyzer et assigne l’identificateur de culture du thread d’entrée actif au trait.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'IInkAnalyzer :: AddStroke, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc946e7975772eb7be6fff54d01bb1a6dae8ebe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201506"
---
# <a name="iinkanalyzeraddstroke-method"></a><span data-ttu-id="97e4d-103">IInkAnalyzer :: AddStroke, méthode</span><span class="sxs-lookup"><span data-stu-id="97e4d-103">IInkAnalyzer::AddStroke method</span></span>

<span data-ttu-id="97e4d-104">Ajoute des données de trait pour un seul trait à [**IInkAnalyzer**](iinkanalyzer.md) et assigne l’identificateur de culture du thread d’entrée actif au trait.</span><span class="sxs-lookup"><span data-stu-id="97e4d-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="97e4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97e4d-105">Syntax</span></span>


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="97e4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97e4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97e4d-107">*lStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97e4d-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97e4d-108">Identificateur du trait à ajouter.</span><span class="sxs-lookup"><span data-stu-id="97e4d-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="97e4d-109">*ulStrokePacketDataCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97e4d-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97e4d-110">Nombre de paquets dans le trait.</span><span class="sxs-lookup"><span data-stu-id="97e4d-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="97e4d-111">*plStrokePacketData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97e4d-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97e4d-112">Tableau contenant les données de paquet pour le trait.</span><span class="sxs-lookup"><span data-stu-id="97e4d-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="97e4d-113">*ulStrokePacketDescriptionCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97e4d-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97e4d-114">Nombre de propriétés de paquet dans chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="97e4d-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="97e4d-115">*pStrokePacketDescriptionGuids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97e4d-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97e4d-116">Tableau contenant les identificateurs de propriété de paquet.</span><span class="sxs-lookup"><span data-stu-id="97e4d-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="97e4d-117">*ppContextNodeStrokeAddedTo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="97e4d-117">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97e4d-118">Pointeur vers le [**IContextNode**](icontextnode.md) auquel le [**IInkAnalyzer**](iinkanalyzer.md) a ajouté le trait.</span><span class="sxs-lookup"><span data-stu-id="97e4d-118">A pointer to the [**IContextNode**](icontextnode.md) to which the [**IInkAnalyzer**](iinkanalyzer.md) added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97e4d-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97e4d-119">Return value</span></span>

<span data-ttu-id="97e4d-120">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="97e4d-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97e4d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="97e4d-121">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="97e4d-122">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeStrokeAddedTo* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="97e4d-122">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="97e4d-123">Quand *ppContextNodeStrokeAddedTo* a la valeur **null**, il indique que l’appelant ne s’intéresse pas à la valeur de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="97e4d-123">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="97e4d-124">[**IInkAnalyzer**](iinkanalyzer.md) ajoute le trait à un [**IContextNode**](icontextnode.md) de type UnclassifiedInk (consultez [types de nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="97e4d-124">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="97e4d-125">Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="97e4d-125">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="97e4d-126">[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture du thread d’entrée actif au trait et ajoute le trait au premier nœud de contexte UnclassifiedInk sous le nœud racine de l’analyseur d’encre qui contient des traits avec le même identificateur de culture.</span><span class="sxs-lookup"><span data-stu-id="97e4d-126">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="97e4d-127">Si l’analyseur d’encre n’a pas de nœud avec le même identificateur de culture, il crée un nœud de contexte UnclassifiedInk sous son nœud racine et ajoute le trait au nouveau nœud de contexte UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="97e4d-127">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="97e4d-128">*plStrokePacketData* contient des données de paquet pour tous les points du trait.</span><span class="sxs-lookup"><span data-stu-id="97e4d-128">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="97e4d-129">*pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point du trait.</span><span class="sxs-lookup"><span data-stu-id="97e4d-129">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="97e4d-130">Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="97e4d-130">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="97e4d-131">Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la région et de la zone englobante du trait ajouté.</span><span class="sxs-lookup"><span data-stu-id="97e4d-131">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="97e4d-132">Si le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur de trait, le **IInkAnalyzer** retourne un **HRESULT** d' **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="97e4d-132">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e4d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97e4d-133">Requirements</span></span>



| <span data-ttu-id="97e4d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97e4d-134">Requirement</span></span> | <span data-ttu-id="97e4d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="97e4d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97e4d-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e4d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="97e4d-137">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97e4d-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="97e4d-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e4d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="97e4d-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e4d-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="97e4d-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="97e4d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e4d-141"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="97e4d-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="97e4d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="97e4d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97e4d-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97e4d-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="97e4d-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97e4d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e4d-145">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="97e4d-145">**InkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="97e4d-146">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="97e4d-146">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="97e4d-147">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="97e4d-147">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="97e4d-148">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="97e4d-148">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="97e4d-149">**IInkAnalyzer :: RemoveStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="97e4d-149">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="97e4d-150">**IInkAnalyzer :: RemoveStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="97e4d-150">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="97e4d-151">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="97e4d-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

