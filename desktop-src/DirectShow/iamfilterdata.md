---
description: En savoir plus sur l’interface IAMFilterData, qui convertit les informations de filtre en données binaires compressées. Cette interface a été déconseillée.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interface IAMFilterData (fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1e43e0f16ddfdee596f0dc6bd736ed86fc6fa37d
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989434"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="e7c4b-104">Interface IAMFilterData</span><span class="sxs-lookup"><span data-stu-id="e7c4b-104">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="e7c4b-105">Cette interface a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e7c4b-105">This interface has been deprecated.</span></span> <span data-ttu-id="e7c4b-106">Les nouvelles applications doivent utiliser l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) à la place.</span><span class="sxs-lookup"><span data-stu-id="e7c4b-106">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="e7c4b-107">L' `IAMFilterData` interface convertit les informations de filtre en données binaires compressées, qui peuvent être stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="e7c4b-107">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="e7c4b-108">L’objet mappeur de filtre expose cette interface.</span><span class="sxs-lookup"><span data-stu-id="e7c4b-108">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="e7c4b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e7c4b-109">Members</span></span>

<span data-ttu-id="e7c4b-110">L’interface **IAMFilterData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e7c4b-110">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e7c4b-111">**IAMFilterData** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e7c4b-111">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="e7c4b-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e7c4b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e7c4b-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e7c4b-113">Methods</span></span>

<span data-ttu-id="e7c4b-114">L’interface **IAMFilterData** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e7c4b-114">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="e7c4b-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="e7c4b-115">Method</span></span>                                                     | <span data-ttu-id="e7c4b-116">Description</span><span class="sxs-lookup"><span data-stu-id="e7c4b-116">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="e7c4b-117">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="e7c4b-117">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="e7c4b-118">Crée des données de Registre binaires pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="e7c4b-118">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="e7c4b-119">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="e7c4b-119">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="e7c4b-120">Décompresse les données de Registre binaires pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="e7c4b-120">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7c4b-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="e7c4b-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e7c4b-122">L’en-tête de \_ données. h se trouve dans le répertoire de l' [exemple du mappeur](mapper-sample.md) dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="e7c4b-122">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7c4b-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e7c4b-123">Requirements</span></span>



| <span data-ttu-id="e7c4b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7c4b-124">Requirement</span></span> | <span data-ttu-id="e7c4b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7c4b-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c4b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7c4b-126">Header</span></span><br/> | <dl> <span data-ttu-id="e7c4b-127"><dt>Données de fil \_ . h</dt></span><span class="sxs-lookup"><span data-stu-id="e7c4b-127"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7c4b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7c4b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c4b-129">Interfaces déconseillées</span><span class="sxs-lookup"><span data-stu-id="e7c4b-129">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
