---
description: L’interface IAMTimelineTransable ajoute DES transitions à un objet dans les services de modification DirectShow (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interface IAMTimelineTransable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545668"
---
# <a name="iamtimelinetransable-interface"></a><span data-ttu-id="27505-103">Interface IAMTimelineTransable</span><span class="sxs-lookup"><span data-stu-id="27505-103">IAMTimelineTransable interface</span></span>

> [!Note]  
> <span data-ttu-id="27505-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27505-104">\[Deprecated.</span></span> <span data-ttu-id="27505-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27505-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="27505-106">L' `IAMTimelineTransable` interface ajoute des transitions à un objet dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="27505-106">The `IAMTimelineTransable` interface adds transitions to an object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="27505-107">Cette interface est exposée par tout objet auquel des transitions peuvent être appliquées, y compris des pistes, des compositions et des groupes.</span><span class="sxs-lookup"><span data-stu-id="27505-107">This interface is exposed by any object that can have transitions applied to it, including tracks, compositions, and groups.</span></span> <span data-ttu-id="27505-108">Un objet qui implémente cette interface peut avoir un nombre quelconque de transitions, mais les transitions ne doivent pas se chevaucher dans le temps.</span><span class="sxs-lookup"><span data-stu-id="27505-108">An object that implements this interface can have any number of transitions, but the transitions must not overlap in time.</span></span>

> [!Note]  
> <span data-ttu-id="27505-109">L’audio ne prend pas en charge les transitions.</span><span class="sxs-lookup"><span data-stu-id="27505-109">Audio does not support transitions.</span></span> <span data-ttu-id="27505-110">Les objets dans les groupes audio peuvent exposer l' `IAMTimelineTransable` interface, mais l’application ne doit pas lui ajouter de transitions.</span><span class="sxs-lookup"><span data-stu-id="27505-110">Objects within audio groups can expose the `IAMTimelineTransable` interface, but the application should not add transitions to them.</span></span>

 

## <a name="members"></a><span data-ttu-id="27505-111">Membres</span><span class="sxs-lookup"><span data-stu-id="27505-111">Members</span></span>

<span data-ttu-id="27505-112">L’interface **IAMTimelineTransable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="27505-112">The **IAMTimelineTransable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="27505-113">**IAMTimelineTransable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="27505-113">**IAMTimelineTransable** also has these types of members:</span></span>

-   [<span data-ttu-id="27505-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="27505-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="27505-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="27505-115">Methods</span></span>

<span data-ttu-id="27505-116">L’interface **IAMTimelineTransable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="27505-116">The **IAMTimelineTransable** interface has these methods.</span></span>



| <span data-ttu-id="27505-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="27505-117">Method</span></span>                                                          | <span data-ttu-id="27505-118">Description</span><span class="sxs-lookup"><span data-stu-id="27505-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27505-119">**GetNextTrans**</span><span class="sxs-lookup"><span data-stu-id="27505-119">**GetNextTrans**</span></span>](iamtimelinetransable-getnexttrans.md)       | <span data-ttu-id="27505-120">Récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="27505-120">Retrieves the first transition that appears at the specified time or later.</span></span><br/>                                             |
| [<span data-ttu-id="27505-121">**GetNextTrans2**</span><span class="sxs-lookup"><span data-stu-id="27505-121">**GetNextTrans2**</span></span>](iamtimelinetransable-getnexttrans2.md)     | <span data-ttu-id="27505-122">Récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure, avec l’heure indiquée comme valeur **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="27505-122">Retrieves the first transition that appears at the specified time or later, with the time given as a **REFTIME** value.</span></span><br/> |
| [<span data-ttu-id="27505-123">**GetTransAtTime**</span><span class="sxs-lookup"><span data-stu-id="27505-123">**GetTransAtTime**</span></span>](iamtimelinetransable-gettransattime.md)   | <span data-ttu-id="27505-124">Récupère la transition la plus proche de l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="27505-124">Retrieves the transition nearest to the specified time.</span></span><br/>                                                                 |
| [<span data-ttu-id="27505-125">**GetTransAtTime2**</span><span class="sxs-lookup"><span data-stu-id="27505-125">**GetTransAtTime2**</span></span>](iamtimelinetransable-gettransattime2.md) | <span data-ttu-id="27505-126">Récupère la transition la plus proche de l’heure spécifiée, sous la forme d’une valeur **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="27505-126">Retrieves the transition nearest to the specified time, given as a **REFTIME** value.</span></span><br/>                                   |
| [<span data-ttu-id="27505-127">**TransAdd**</span><span class="sxs-lookup"><span data-stu-id="27505-127">**TransAdd**</span></span>](iamtimelinetransable-transadd.md)               | <span data-ttu-id="27505-128">Ajoute une transition à l’objet.</span><span class="sxs-lookup"><span data-stu-id="27505-128">Adds a transition to the object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="27505-129">**TransGetCount**</span><span class="sxs-lookup"><span data-stu-id="27505-129">**TransGetCount**</span></span>](iamtimelinetransable-transgetcount.md)     | <span data-ttu-id="27505-130">Récupère le nombre de transitions sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="27505-130">Retrieves the number of transitions on this object.</span></span><br/>                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="27505-131">Notes</span><span class="sxs-lookup"><span data-stu-id="27505-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="27505-132">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="27505-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="27505-133">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="27505-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="27505-134">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="27505-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27505-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27505-135">Requirements</span></span>



| <span data-ttu-id="27505-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27505-136">Requirement</span></span> | <span data-ttu-id="27505-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="27505-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27505-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="27505-138">Header</span></span><br/>  | <dl> <span data-ttu-id="27505-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="27505-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="27505-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="27505-140">Library</span></span><br/> | <dl> <span data-ttu-id="27505-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27505-141"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
