---
description: L’interface IRenderEngine2 permet à l’application de remplacer le filtre de redimensionnement vidéo par défaut utilisé par les services d’édition DirectShow (DES). Le moteur de rendu de base et le moteur de rendu intelligent prennent tous deux en charge cette interface.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interface IRenderEngine2 (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543324"
---
# <a name="irenderengine2-interface"></a><span data-ttu-id="7fc2b-104">Interface IRenderEngine2</span><span class="sxs-lookup"><span data-stu-id="7fc2b-104">IRenderEngine2 interface</span></span>

> [!Note]  
> <span data-ttu-id="7fc2b-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7fc2b-105">\[Deprecated.</span></span> <span data-ttu-id="7fc2b-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7fc2b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7fc2b-107">L' `IRenderEngine2` interface permet à l’application de remplacer le filtre de redimensionnement vidéo par défaut utilisé par les services d’édition DirectShow (des).</span><span class="sxs-lookup"><span data-stu-id="7fc2b-107">The `IRenderEngine2` interface enables the application to replace the default video resizing filter used by DirectShow Editing Services (DES).</span></span> <span data-ttu-id="7fc2b-108">Le [moteur de rendu de base](basic-render-engine.md) et le [moteur de rendu intelligent](smart-render-engine.md) prennent tous deux en charge cette interface.</span><span class="sxs-lookup"><span data-stu-id="7fc2b-108">The [Basic Render Engine](basic-render-engine.md) and the [Smart Render Engine](smart-render-engine.md) both support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="7fc2b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7fc2b-109">Members</span></span>

<span data-ttu-id="7fc2b-110">L’interface **IRenderEngine2** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7fc2b-110">The **IRenderEngine2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7fc2b-111">**IRenderEngine2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fc2b-111">**IRenderEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="7fc2b-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7fc2b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7fc2b-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7fc2b-113">Methods</span></span>

<span data-ttu-id="7fc2b-114">L’interface **IRenderEngine2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7fc2b-114">The **IRenderEngine2** interface has these methods.</span></span>



| <span data-ttu-id="7fc2b-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="7fc2b-115">Method</span></span>                                                  | <span data-ttu-id="7fc2b-116">Description</span><span class="sxs-lookup"><span data-stu-id="7fc2b-116">Description</span></span>                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fc2b-117">**SetResizerGUID**</span><span class="sxs-lookup"><span data-stu-id="7fc2b-117">**SetResizerGUID**</span></span>](irenderengine2-setresizerguid.md) | <span data-ttu-id="7fc2b-118">Spécifie le CLSID d’un filtre de redimensionnement personnalisé fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="7fc2b-118">Specifies the CLSID of a custom resizing filter provided by the application.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7fc2b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7fc2b-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7fc2b-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="7fc2b-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7fc2b-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7fc2b-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7fc2b-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7fc2b-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7fc2b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fc2b-123">Requirements</span></span>



| <span data-ttu-id="7fc2b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fc2b-124">Requirement</span></span> | <span data-ttu-id="7fc2b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fc2b-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc2b-126">Version</span><span class="sxs-lookup"><span data-stu-id="7fc2b-126">Version</span></span><br/> | <span data-ttu-id="7fc2b-127">DirectX 9,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7fc2b-127">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="7fc2b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fc2b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7fc2b-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc2b-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7fc2b-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7fc2b-130">Library</span></span><br/> | <dl> <span data-ttu-id="7fc2b-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fc2b-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fc2b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fc2b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc2b-133">Fournir un redimensionnement vidéo personnalisé</span><span class="sxs-lookup"><span data-stu-id="7fc2b-133">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
