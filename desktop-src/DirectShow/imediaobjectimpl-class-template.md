---
description: Le modèle de classe IMediaObjectImpl fournit une implémentation de base pour l’interface IMediaObject. Pour plus d’informations sur l’utilisation de ce modèle, consultez Utilisation du modèle de classe DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Modèle de classe IMediaObjectImpl (Dmoimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526570"
---
# <a name="imediaobjectimpl-class-template"></a><span data-ttu-id="7da60-104">Modèle de classe IMediaObjectImpl</span><span class="sxs-lookup"><span data-stu-id="7da60-104">IMediaObjectImpl Class Template</span></span>

<span data-ttu-id="7da60-105">Le `IMediaObjectImpl` modèle de classe fournit une implémentation de base pour l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="7da60-105">The `IMediaObjectImpl` class template provides a base implementation for the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="7da60-106">Pour plus d’informations sur l’utilisation de ce modèle, consultez [utilisation du modèle de classe DMO](using-the-dmo-class-template.md).</span><span class="sxs-lookup"><span data-stu-id="7da60-106">For more information on using this template, see [Using the DMO Class Template](using-the-dmo-class-template.md).</span></span>

<span data-ttu-id="7da60-107">Ce `IMediaObjectImpl` modèle expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="7da60-107">This `IMediaObjectImpl` template exposes the following members.</span></span>



| <span data-ttu-id="7da60-108">Classe imbriquée</span><span class="sxs-lookup"><span data-stu-id="7da60-108">Nested Class</span></span>                              | <span data-ttu-id="7da60-109">Description</span><span class="sxs-lookup"><span data-stu-id="7da60-109">Description</span></span>                                  |
|-------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="7da60-110">**LockIt**</span><span class="sxs-lookup"><span data-stu-id="7da60-110">**LockIt**</span></span>](imediaobjectimpl-lockit.md) | <span data-ttu-id="7da60-111">Classe d’assistance qui verrouille et déverrouille la classe DMO.</span><span class="sxs-lookup"><span data-stu-id="7da60-111">Helper class that locks and unlocks the DMO.</span></span> |



 



| <span data-ttu-id="7da60-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="7da60-112">Method</span></span>                                                                      | <span data-ttu-id="7da60-113">Description</span><span class="sxs-lookup"><span data-stu-id="7da60-113">Description</span></span>                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="7da60-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span></span>                     | <span data-ttu-id="7da60-115">Détermine si tous les flux non facultatifs ont des types de média.</span><span class="sxs-lookup"><span data-stu-id="7da60-115">Determines whether all of the non-optional streams have media types.</span></span> |
| <span data-ttu-id="7da60-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span></span>                             | <span data-ttu-id="7da60-117">Récupère le type de média actuel pour un flux d’entrée spécifié.</span><span class="sxs-lookup"><span data-stu-id="7da60-117">Retrieves the current media type for a specified input stream.</span></span>       |
| <span data-ttu-id="7da60-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span></span>                       | <span data-ttu-id="7da60-119">Interroge si le type de média a été défini sur un flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7da60-119">Queries whether the media type was set on an input stream.</span></span>           |
| <span data-ttu-id="7da60-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span></span>   | <span data-ttu-id="7da60-121">Interroge si un flux d’entrée peut accepter davantage d’entrées.</span><span class="sxs-lookup"><span data-stu-id="7da60-121">Queries whether an input stream can accept more input.</span></span>               |
| <span data-ttu-id="7da60-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span></span>   | <span data-ttu-id="7da60-123">Interroge si un flux d’entrée peut accepter un type de média donné.</span><span class="sxs-lookup"><span data-stu-id="7da60-123">Queries whether an input stream can accept a given media type.</span></span>       |
| <span data-ttu-id="7da60-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span></span> | <span data-ttu-id="7da60-125">Interroge si un flux de sortie peut accepter un type de média donné.</span><span class="sxs-lookup"><span data-stu-id="7da60-125">Queries whether an output stream can accept a given media type.</span></span>      |
| <span data-ttu-id="7da60-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span></span>                                       | <span data-ttu-id="7da60-127">Verrouille la DMO</span><span class="sxs-lookup"><span data-stu-id="7da60-127">Locks the DMO</span></span>                                                        |
| <span data-ttu-id="7da60-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span></span>                           | <span data-ttu-id="7da60-129">Récupère le type de média actuel pour un flux de sortie spécifié.</span><span class="sxs-lookup"><span data-stu-id="7da60-129">Retrieves the current media type for a specified output stream.</span></span>      |
| <span data-ttu-id="7da60-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span></span>                     | <span data-ttu-id="7da60-131">Interroge si le type de média a été défini sur un flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="7da60-131">Queries whether the media type was set on an output stream.</span></span>          |
| <span data-ttu-id="7da60-132">[**Bloquer**](/previous-versions/ms809101(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7da60-132">[**Unlock**](/previous-versions/ms809101(v=msdn.10))</span></span>                                   | <span data-ttu-id="7da60-133">Déverrouille le</span><span class="sxs-lookup"><span data-stu-id="7da60-133">Unlocks the DMO</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="7da60-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7da60-134">Requirements</span></span>



| <span data-ttu-id="7da60-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7da60-135">Requirement</span></span> | <span data-ttu-id="7da60-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7da60-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da60-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="7da60-137">Header</span></span><br/>  | <dl> <span data-ttu-id="7da60-138"><dt>Dmoimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7da60-138"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="7da60-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7da60-139">Library</span></span><br/> | <dl> <span data-ttu-id="7da60-140"><dt>Dmoguids. lib ; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7da60-140"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7da60-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7da60-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da60-142">Référence DMO</span><span class="sxs-lookup"><span data-stu-id="7da60-142">DMO Reference</span></span>](dmo-reference.md)
</dt> <dt>

[<span data-ttu-id="7da60-143">Utilisation du modèle de classe DMO</span><span class="sxs-lookup"><span data-stu-id="7da60-143">Using the DMO Class Template</span></span>](using-the-dmo-class-template.md)
</dt> </dl>

 

 
