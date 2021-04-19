---
description: Récupère un tableau qui contient les données de propriété de paquet pour le trait spécifié.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'IContextNode :: GetStrokePacketDataById, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514836"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a><span data-ttu-id="b08f2-103">IContextNode :: GetStrokePacketDataById, méthode</span><span class="sxs-lookup"><span data-stu-id="b08f2-103">IContextNode::GetStrokePacketDataById method</span></span>

<span data-ttu-id="b08f2-104">Récupère un tableau qui contient les données de propriété de paquet pour le trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="b08f2-104">Retrieves an array containing the packet property data for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="b08f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b08f2-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="b08f2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b08f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b08f2-107">*strokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b08f2-107">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b08f2-108">Identificateur du trait.</span><span class="sxs-lookup"><span data-stu-id="b08f2-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="b08f2-109">*pStrokePacketDataCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b08f2-109">*pStrokePacketDataCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b08f2-110">Longueur du tableau de données du paquet.</span><span class="sxs-lookup"><span data-stu-id="b08f2-110">The length of the packet data array.</span></span>

</dd> <dt>

<span data-ttu-id="b08f2-111">*pplStrokePacketData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b08f2-111">*pplStrokePacketData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b08f2-112">Pointeur vers les données du paquet pour le trait.</span><span class="sxs-lookup"><span data-stu-id="b08f2-112">A pointer to the packet data for the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b08f2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b08f2-113">Return value</span></span>

<span data-ttu-id="b08f2-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b08f2-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b08f2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b08f2-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b08f2-116">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *pplStrokePacketData* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="b08f2-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokePacketData* when you no longer need the information.</span></span>

 

<span data-ttu-id="b08f2-117">*plStrokePacketData* contient des données de paquet pour tous les points du trait.</span><span class="sxs-lookup"><span data-stu-id="b08f2-117">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="b08f2-118">Pour obtenir les types de données de paquet inclus pour chaque point du trait, utilisez [**IContextNode :: GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span><span class="sxs-lookup"><span data-stu-id="b08f2-118">To get the types of packet data included for each point in the stroke, use [**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b08f2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b08f2-119">Requirements</span></span>



| <span data-ttu-id="b08f2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b08f2-120">Requirement</span></span> | <span data-ttu-id="b08f2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b08f2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b08f2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b08f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b08f2-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b08f2-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b08f2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b08f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b08f2-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b08f2-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b08f2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b08f2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b08f2-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b08f2-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b08f2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b08f2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b08f2-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b08f2-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b08f2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b08f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b08f2-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b08f2-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b08f2-132">**IContextNode::GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="b08f2-132">**IContextNode::GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[<span data-ttu-id="b08f2-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b08f2-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

