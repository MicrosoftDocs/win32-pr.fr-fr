---
description: L’interface IAMTimelineSplittable fractionne un objet Timeline dans les services de modification DirectShow (DES). Les sources, les effets, les transitions et les suivis implémentent cette interface.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interface IAMTimelineSplittable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523020"
---
# <a name="iamtimelinesplittable-interface"></a><span data-ttu-id="9842f-104">Interface IAMTimelineSplittable</span><span class="sxs-lookup"><span data-stu-id="9842f-104">IAMTimelineSplittable interface</span></span>

> [!Note]  
> <span data-ttu-id="9842f-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9842f-105">\[Deprecated.</span></span> <span data-ttu-id="9842f-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9842f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9842f-107">L' `IAMTimelineSplittable` interface fractionne un objet Timeline dans les [services d’édition DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="9842f-107">The `IAMTimelineSplittable` interface splits a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="9842f-108">Les sources, les effets, les transitions et les suivis implémentent cette interface.</span><span class="sxs-lookup"><span data-stu-id="9842f-108">Sources, effects, transitions, and tracks implement this interface.</span></span>

## <a name="members"></a><span data-ttu-id="9842f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9842f-109">Members</span></span>

<span data-ttu-id="9842f-110">L’interface **IAMTimelineSplittable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9842f-110">The **IAMTimelineSplittable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9842f-111">**IAMTimelineSplittable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9842f-111">**IAMTimelineSplittable** also has these types of members:</span></span>

-   [<span data-ttu-id="9842f-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9842f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9842f-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9842f-113">Methods</span></span>

<span data-ttu-id="9842f-114">L’interface **IAMTimelineSplittable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9842f-114">The **IAMTimelineSplittable** interface has these methods.</span></span>



| <span data-ttu-id="9842f-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="9842f-115">Method</span></span>                                             | <span data-ttu-id="9842f-116">Description</span><span class="sxs-lookup"><span data-stu-id="9842f-116">Description</span></span>                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9842f-117">**SplitAt**</span><span class="sxs-lookup"><span data-stu-id="9842f-117">**SplitAt**</span></span>](iamtimelinesplittable-splitat.md)   | <span data-ttu-id="9842f-118">Fractionne l’objet à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9842f-118">Splits the object at the specified time.</span></span><br/>                                                  |
| [<span data-ttu-id="9842f-119">**SplitAt2**</span><span class="sxs-lookup"><span data-stu-id="9842f-119">**SplitAt2**</span></span>](iamtimelinesplittable-splitat2.md) | <span data-ttu-id="9842f-120">Fractionne l’objet à l’heure spécifiée, spécifié en tant que valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="9842f-120">Splits the object at the specified time, specified as a [**REFTIME**](reftime.md) value.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9842f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="9842f-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9842f-122">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="9842f-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9842f-123">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9842f-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9842f-124">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9842f-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9842f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9842f-125">Requirements</span></span>



| <span data-ttu-id="9842f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9842f-126">Requirement</span></span> | <span data-ttu-id="9842f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9842f-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9842f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9842f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9842f-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9842f-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9842f-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9842f-130">Library</span></span><br/> | <dl> <span data-ttu-id="9842f-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9842f-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
