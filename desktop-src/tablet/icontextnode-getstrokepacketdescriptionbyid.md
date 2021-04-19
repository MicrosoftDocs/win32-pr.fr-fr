---
description: Récupère un tableau contenant les identificateurs de propriété de paquet pour le trait spécifié.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'IContextNode :: GetStrokePacketDescriptionById, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517283"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a><span data-ttu-id="5475f-103">IContextNode :: GetStrokePacketDescriptionById, méthode</span><span class="sxs-lookup"><span data-stu-id="5475f-103">IContextNode::GetStrokePacketDescriptionById method</span></span>

<span data-ttu-id="5475f-104">Récupère un tableau contenant les identificateurs de propriété de paquet pour le trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="5475f-104">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="5475f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5475f-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a><span data-ttu-id="5475f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5475f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5475f-107">*lStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5475f-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5475f-108">Identificateur du trait.</span><span class="sxs-lookup"><span data-stu-id="5475f-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="5475f-109">*pulStrokePacketDescriptionCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5475f-109">*pulStrokePacketDescriptionCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5475f-110">Nombre de propriétés de paquet dans chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="5475f-110">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="5475f-111">*ppStrokePacketDescriptionGuids* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5475f-111">*ppStrokePacketDescriptionGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5475f-112">Tableau contenant les identificateurs de propriété de paquet.</span><span class="sxs-lookup"><span data-stu-id="5475f-112">An array containing the packet property identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5475f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5475f-113">Return value</span></span>

<span data-ttu-id="5475f-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="5475f-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5475f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5475f-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="5475f-116">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppStrokePacketDescriptionGuids* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="5475f-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppStrokePacketDescriptionGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="5475f-117">\**ppStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point du trait.</span><span class="sxs-lookup"><span data-stu-id="5475f-117">\**ppStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="5475f-118">Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5475f-118">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5475f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5475f-119">Requirements</span></span>



| <span data-ttu-id="5475f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5475f-120">Requirement</span></span> | <span data-ttu-id="5475f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5475f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5475f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5475f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5475f-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5475f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5475f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5475f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5475f-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5475f-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5475f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="5475f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5475f-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5475f-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5475f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5475f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5475f-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5475f-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5475f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5475f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5475f-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="5475f-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5475f-132">**IContextNode::GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="5475f-132">**IContextNode::GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[<span data-ttu-id="5475f-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="5475f-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

