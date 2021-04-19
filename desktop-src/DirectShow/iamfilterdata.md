---
description: Notez que cette interface est dépréciée.
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
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543600"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="022ff-103">Interface IAMFilterData</span><span class="sxs-lookup"><span data-stu-id="022ff-103">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="022ff-104">Cette interface a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="022ff-104">This interface has been deprecated.</span></span> <span data-ttu-id="022ff-105">Les nouvelles applications doivent utiliser l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) à la place.</span><span class="sxs-lookup"><span data-stu-id="022ff-105">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="022ff-106">L' `IAMFilterData` interface convertit les informations de filtre en données binaires compressées, qui peuvent être stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="022ff-106">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="022ff-107">L’objet mappeur de filtre expose cette interface.</span><span class="sxs-lookup"><span data-stu-id="022ff-107">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="022ff-108">Membres</span><span class="sxs-lookup"><span data-stu-id="022ff-108">Members</span></span>

<span data-ttu-id="022ff-109">L’interface **IAMFilterData** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="022ff-109">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="022ff-110">**IAMFilterData** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="022ff-110">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="022ff-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="022ff-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="022ff-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="022ff-112">Methods</span></span>

<span data-ttu-id="022ff-113">L’interface **IAMFilterData** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="022ff-113">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="022ff-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="022ff-114">Method</span></span>                                                     | <span data-ttu-id="022ff-115">Description</span><span class="sxs-lookup"><span data-stu-id="022ff-115">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="022ff-116">**CreateFilterData**</span><span class="sxs-lookup"><span data-stu-id="022ff-116">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="022ff-117">Crée des données de Registre binaires pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="022ff-117">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="022ff-118">**ParseFilterData**</span><span class="sxs-lookup"><span data-stu-id="022ff-118">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="022ff-119">Décompresse les données de Registre binaires pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="022ff-119">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="022ff-120">Notes</span><span class="sxs-lookup"><span data-stu-id="022ff-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="022ff-121">L’en-tête de \_ données. h se trouve dans le répertoire de l' [exemple du mappeur](mapper-sample.md) dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="022ff-121">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="022ff-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="022ff-122">Requirements</span></span>



| <span data-ttu-id="022ff-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="022ff-123">Requirement</span></span> | <span data-ttu-id="022ff-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="022ff-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="022ff-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="022ff-125">Header</span></span><br/> | <dl> <span data-ttu-id="022ff-126"><dt>Données de fil \_ . h</dt></span><span class="sxs-lookup"><span data-stu-id="022ff-126"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="022ff-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="022ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022ff-128">Interfaces déconseillées</span><span class="sxs-lookup"><span data-stu-id="022ff-128">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
