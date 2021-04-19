---
description: L’interface IAMTimelineVirtualTrack fournit des méthodes pour travailler avec des pistes virtuelles dans les services de modification DirectShow (DES). Les compositions et les suivis prennent en charge cette interface.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Interface IAMTimelineVirtualTrack (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525450"
---
# <a name="iamtimelinevirtualtrack-interface"></a><span data-ttu-id="076c2-104">Interface IAMTimelineVirtualTrack</span><span class="sxs-lookup"><span data-stu-id="076c2-104">IAMTimelineVirtualTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="076c2-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="076c2-105">\[Deprecated.</span></span> <span data-ttu-id="076c2-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="076c2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="076c2-107">L' `IAMTimelineVirtualTrack` interface fournit des méthodes pour travailler avec des pistes virtuelles dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="076c2-107">The `IAMTimelineVirtualTrack` interface provides methods for working with virtual tracks in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="076c2-108">Les compositions et les suivis prennent en charge cette interface.</span><span class="sxs-lookup"><span data-stu-id="076c2-108">Compositions and tracks support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="076c2-109">Membres</span><span class="sxs-lookup"><span data-stu-id="076c2-109">Members</span></span>

<span data-ttu-id="076c2-110">L’interface **IAMTimelineVirtualTrack** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="076c2-110">The **IAMTimelineVirtualTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="076c2-111">**IAMTimelineVirtualTrack** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="076c2-111">**IAMTimelineVirtualTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="076c2-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="076c2-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="076c2-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="076c2-113">Methods</span></span>

<span data-ttu-id="076c2-114">L’interface **IAMTimelineVirtualTrack** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="076c2-114">The **IAMTimelineVirtualTrack** interface has these methods.</span></span>



| <span data-ttu-id="076c2-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="076c2-115">Method</span></span>                                                               | <span data-ttu-id="076c2-116">Description</span><span class="sxs-lookup"><span data-stu-id="076c2-116">Description</span></span>                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="076c2-117">**SetTrackDirty**</span><span class="sxs-lookup"><span data-stu-id="076c2-117">**SetTrackDirty**</span></span>](iamtimelinevirtualtrack-settrackdirty.md)       | <span data-ttu-id="076c2-118">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="076c2-118">Not supported.</span></span><br/>                         |
| [<span data-ttu-id="076c2-119">**TrackGetPriority**</span><span class="sxs-lookup"><span data-stu-id="076c2-119">**TrackGetPriority**</span></span>](iamtimelinevirtualtrack-trackgetpriority.md) | <span data-ttu-id="076c2-120">Récupère le niveau de priorité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="076c2-120">Retrieves the object's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="076c2-121">Notes</span><span class="sxs-lookup"><span data-stu-id="076c2-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="076c2-122">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="076c2-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="076c2-123">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="076c2-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="076c2-124">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="076c2-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="076c2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="076c2-125">Requirements</span></span>



| <span data-ttu-id="076c2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="076c2-126">Requirement</span></span> | <span data-ttu-id="076c2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="076c2-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="076c2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="076c2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="076c2-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="076c2-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="076c2-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="076c2-130">Library</span></span><br/> | <dl> <span data-ttu-id="076c2-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="076c2-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
