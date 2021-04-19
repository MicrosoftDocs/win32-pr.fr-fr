---
description: L’interface ISmartRenderEngine fournit des méthodes qui prennent en charge la recompression intelligente dans les services d’édition DirectShow (DES). Le moteur de rendu intelligent expose cette interface.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Interface ISmartRenderEngine (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544435"
---
# <a name="ismartrenderengine-interface"></a><span data-ttu-id="62c4e-104">Interface ISmartRenderEngine</span><span class="sxs-lookup"><span data-stu-id="62c4e-104">ISmartRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="62c4e-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="62c4e-105">\[Deprecated.</span></span> <span data-ttu-id="62c4e-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62c4e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="62c4e-107">L' `ISmartRenderEngine` interface fournit des méthodes qui prennent en charge la recompression intelligente dans les [services d’édition DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="62c4e-107">The `ISmartRenderEngine` interface provides methods that support smart recompression in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="62c4e-108">Le moteur de rendu intelligent expose cette interface.</span><span class="sxs-lookup"><span data-stu-id="62c4e-108">The smart render engine exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="62c4e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="62c4e-109">Members</span></span>

<span data-ttu-id="62c4e-110">L’interface **ISmartRenderEngine** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="62c4e-110">The **ISmartRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="62c4e-111">**ISmartRenderEngine** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="62c4e-111">**ISmartRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="62c4e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="62c4e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="62c4e-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="62c4e-113">Methods</span></span>

<span data-ttu-id="62c4e-114">L’interface **ISmartRenderEngine** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="62c4e-114">The **ISmartRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="62c4e-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="62c4e-115">Method</span></span>                                                                | <span data-ttu-id="62c4e-116">Description</span><span class="sxs-lookup"><span data-stu-id="62c4e-116">Description</span></span>                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="62c4e-117">**GetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="62c4e-117">**GetGroupCompressor**</span></span>](ismartrenderengine-getgroupcompressor.md)   | <span data-ttu-id="62c4e-118">Récupère le filtre de compression pour le groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="62c4e-118">Retrieves the compression filter for the specified group.</span></span><br/>                 |
| [<span data-ttu-id="62c4e-119">**SetFindCompressorCB**</span><span class="sxs-lookup"><span data-stu-id="62c4e-119">**SetFindCompressorCB**</span></span>](ismartrenderengine-setfindcompressorcb.md) | <span data-ttu-id="62c4e-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="62c4e-120">Not implemented.</span></span><br/>                                                          |
| [<span data-ttu-id="62c4e-121">**SetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="62c4e-121">**SetGroupCompressor**</span></span>](ismartrenderengine-setgroupcompressor.md)   | <span data-ttu-id="62c4e-122">Spécifie un filtre de compression à utiliser lors du rendu du groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="62c4e-122">Specifies a compression filter to use when rendering the specified group.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62c4e-123">Notes</span><span class="sxs-lookup"><span data-stu-id="62c4e-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="62c4e-124">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="62c4e-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="62c4e-125">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="62c4e-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="62c4e-126">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="62c4e-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62c4e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62c4e-127">Requirements</span></span>



| <span data-ttu-id="62c4e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62c4e-128">Requirement</span></span> | <span data-ttu-id="62c4e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="62c4e-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62c4e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="62c4e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="62c4e-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c4e-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="62c4e-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="62c4e-132">Library</span></span><br/> | <dl> <span data-ttu-id="62c4e-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62c4e-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c4e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62c4e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c4e-135">Rendu d’un projet</span><span class="sxs-lookup"><span data-stu-id="62c4e-135">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
