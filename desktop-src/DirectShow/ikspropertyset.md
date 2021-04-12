---
description: L’interface IKsPropertySet a été conçue à l’origine comme un moyen efficace de définir et de récupérer les propriétés de l’appareil sur les pilotes WDM, à l’aide de KSProxy pour traduire les appels de la méthode COM en mode utilisateur dans les jeux de propriétés en mode noyau utilisés par les pilotes de classe de streaming WDM. Cette interface est désormais également utilisée pour transmettre des informations strictement entre les composants logiciels. Dans certains cas, les composants logiciels doivent implémenter cette interface, ou l’interface IKsControl (documentée dans DirectShow DDK). Par exemple, si vous écrivez un décodeur logiciel MPEG-2 pour une utilisation avec le navigateur DVD, vous devez implémenter l’une de ces interfaces et prendre en charge les jeux de propriétés relatives aux DVD que le navigateur enverra au décodeur. Les codes confidentiels peuvent prendre en charge l’une de ces interfaces pour permettre à d’autres broches ou filtres de définir ou de récupérer leurs propriétés. Notez qu’une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h. Les deux interfaces ne sont pas compatibles. L’interface IKsControl, documentée dans le DDK DirectShow, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Interface IKsPropertySet (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480769"
---
# <a name="ikspropertyset-interface"></a><span data-ttu-id="9eeb5-109">Interface IKsPropertySet</span><span class="sxs-lookup"><span data-stu-id="9eeb5-109">IKsPropertySet interface</span></span>

<span data-ttu-id="9eeb5-110">L' `IKsPropertySet` interface a été conçue à l’origine comme un moyen efficace de définir et de récupérer les propriétés de l’appareil sur les pilotes WDM, à l’aide de KSProxy pour traduire les appels de la méthode com en mode utilisateur dans les jeux de propriétés en mode noyau utilisés par les pilotes de classe de streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-110">The `IKsPropertySet` interface was originally designed as an efficient way to set and retrieve device properties on WDM drivers, using KSProxy to translate the user-mode COM method calls into the kernel-mode property sets used by WDM streaming class drivers.</span></span> <span data-ttu-id="9eeb5-111">Cette interface est désormais également utilisée pour transmettre des informations strictement entre les composants logiciels.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-111">This interface is now also used to pass information strictly between software components.</span></span>

<span data-ttu-id="9eeb5-112">Dans certains cas, les composants logiciels doivent implémenter cette interface, ou l’interface **IKsControl** (documentée dans DirectShow DDK).</span><span class="sxs-lookup"><span data-stu-id="9eeb5-112">In some cases, software components must implement either this interface, or else the **IKsControl** interface (documented in the DirectShow DDK).</span></span> <span data-ttu-id="9eeb5-113">Par exemple, si vous écrivez un décodeur logiciel MPEG-2 pour une utilisation avec le [navigateur DVD](dvd-navigator-filter.md), vous devez implémenter l’une de ces interfaces et prendre en charge les jeux de propriétés relatives aux DVD que le navigateur enverra au décodeur.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-113">For example, if you are writing a software MPEG-2 decoder for use with the [DVD Navigator](dvd-navigator-filter.md), you must implement one of these interfaces and also support the DVD-related property sets that the Navigator will send to the decoder.</span></span> <span data-ttu-id="9eeb5-114">Les codes confidentiels peuvent prendre en charge l’une de ces interfaces pour permettre à d’autres broches ou filtres de définir ou de récupérer leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-114">Pins may support one of these interfaces to allow other pins or filters to set or retrieve their properties.</span></span>

> [!Note]  
> <span data-ttu-id="9eeb5-115">Une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-115">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="9eeb5-116">Les deux interfaces ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-116">The two interfaces are not compatible.</span></span> <span data-ttu-id="9eeb5-117">L’interface **IKsControl** , documentée dans le DDK DirectShow, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-117">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

## <a name="members"></a><span data-ttu-id="9eeb5-118">Membres</span><span class="sxs-lookup"><span data-stu-id="9eeb5-118">Members</span></span>

<span data-ttu-id="9eeb5-119">L’interface **IKsPropertySet** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9eeb5-119">The **IKsPropertySet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9eeb5-120">**IKsPropertySet** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9eeb5-120">**IKsPropertySet** also has these types of members:</span></span>

-   [<span data-ttu-id="9eeb5-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9eeb5-121">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9eeb5-122">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9eeb5-122">Methods</span></span>

<span data-ttu-id="9eeb5-123">L’interface **IKsPropertySet** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-123">The **IKsPropertySet** interface has these methods.</span></span>



| <span data-ttu-id="9eeb5-124">Méthode</span><span class="sxs-lookup"><span data-stu-id="9eeb5-124">Method</span></span>                                                  | <span data-ttu-id="9eeb5-125">Description</span><span class="sxs-lookup"><span data-stu-id="9eeb5-125">Description</span></span>                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eeb5-126">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="9eeb5-126">**Get**</span></span>](ikspropertyset-get.md)                       | <span data-ttu-id="9eeb5-127">Récupère une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-127">Retrieves a property identified by a property set GUID and a property ID.</span></span><br/> |
| [<span data-ttu-id="9eeb5-128">**QuerySupported**</span><span class="sxs-lookup"><span data-stu-id="9eeb5-128">**QuerySupported**</span></span>](ikspropertyset-querysupported.md) | <span data-ttu-id="9eeb5-129">Détermine si un objet prend en charge un jeu de propriétés spécifié.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-129">Determines whether an object supports a specified property set.</span></span><br/>           |
| [<span data-ttu-id="9eeb5-130">**Définissez**</span><span class="sxs-lookup"><span data-stu-id="9eeb5-130">**Set**</span></span>](ikspropertyset-set.md)                       | <span data-ttu-id="9eeb5-131">Définit une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-131">Sets a property identified by a property set GUID and a property ID.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="9eeb5-132">Notes</span><span class="sxs-lookup"><span data-stu-id="9eeb5-132">Remarks</span></span>

<span data-ttu-id="9eeb5-133">Vous devez inclure KS. h avant ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-133">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eeb5-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9eeb5-134">Requirements</span></span>



| <span data-ttu-id="9eeb5-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eeb5-135">Requirement</span></span> | <span data-ttu-id="9eeb5-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eeb5-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eeb5-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eeb5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9eeb5-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eeb5-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9eeb5-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eeb5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9eeb5-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eeb5-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9eeb5-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="9eeb5-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eeb5-142"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eeb5-142"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="9eeb5-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9eeb5-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="9eeb5-144"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eeb5-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eeb5-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9eeb5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eeb5-146">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="9eeb5-146">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
