---
description: 'L’interface IResize doit être prise en charge par n’importe quel filtre de redimensionnement vidéo personnalisé pour les services de modification DirectShow (DES). Pour définir un filtre de redimensionnement personnalisé, appelez la méthode IRenderEngine2 :: SetResizerGUID sur le moteur de rendu.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interface IResize (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538754"
---
# <a name="iresize-interface"></a><span data-ttu-id="fd8fb-104">Interface IResize</span><span class="sxs-lookup"><span data-stu-id="fd8fb-104">IResize interface</span></span>

> [!Note]  
> <span data-ttu-id="fd8fb-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-105">\[Deprecated.</span></span> <span data-ttu-id="fd8fb-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fd8fb-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fd8fb-107">L' `IResize` interface doit être prise en charge par n’importe quel filtre de redimensionnement vidéo personnalisé pour les services d’édition DirectShow (des).</span><span class="sxs-lookup"><span data-stu-id="fd8fb-107">The `IResize` interface must be supported by any custom video resizer filter for DirectShow Editing Services (DES).</span></span> <span data-ttu-id="fd8fb-108">Pour définir un filtre de redimensionnement personnalisé, appelez la méthode [**IRenderEngine2 :: SetResizerGUID**](irenderengine2-setresizerguid.md) sur le moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-108">To set a custom resizer filter, call the [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) method on the render engine.</span></span>

## <a name="members"></a><span data-ttu-id="fd8fb-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fd8fb-109">Members</span></span>

<span data-ttu-id="fd8fb-110">L’interface **IResize** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fd8fb-110">The **IResize** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fd8fb-111">**IResize** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd8fb-111">**IResize** also has these types of members:</span></span>

-   [<span data-ttu-id="fd8fb-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fd8fb-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fd8fb-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fd8fb-113">Methods</span></span>

<span data-ttu-id="fd8fb-114">L’interface **IResize** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-114">The **IResize** interface has these methods.</span></span>



| <span data-ttu-id="fd8fb-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="fd8fb-115">Method</span></span>                                          | <span data-ttu-id="fd8fb-116">Description</span><span class="sxs-lookup"><span data-stu-id="fd8fb-116">Description</span></span>                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="fd8fb-117">**récupération inversée \_**</span><span class="sxs-lookup"><span data-stu-id="fd8fb-117">**get\_InputSize**</span></span>](iresize-get-inputsize.md) | <span data-ttu-id="fd8fb-118">Retourne la taille d’entrée actuelle du filtre de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-118">Returns the resizer filter's current input size.</span></span><br/>  |
| [<span data-ttu-id="fd8fb-119">**Obtient le \_ MediaType**</span><span class="sxs-lookup"><span data-stu-id="fd8fb-119">**get\_MediaType**</span></span>](iresize-get-mediatype.md) | <span data-ttu-id="fd8fb-120">Retourne le type de média de sortie du filtre de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-120">Returns the resizer filter's output media type.</span></span><br/>   |
| [<span data-ttu-id="fd8fb-121">**récupérer la \_ taille**</span><span class="sxs-lookup"><span data-stu-id="fd8fb-121">**get\_Size**</span></span>](iresize-get-size.md)           | <span data-ttu-id="fd8fb-122">Retourne la taille de sortie actuelle et le mode Stretch.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-122">Returns the current output size and stretch mode.</span></span><br/> |
| [<span data-ttu-id="fd8fb-123">**Placer le \_ MediaType**</span><span class="sxs-lookup"><span data-stu-id="fd8fb-123">**put\_MediaType**</span></span>](iresize-put-mediatype.md) | <span data-ttu-id="fd8fb-124">Définit le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-124">Sets the output media type.</span></span><br/>                       |
| [<span data-ttu-id="fd8fb-125">**taille de l’put \_**</span><span class="sxs-lookup"><span data-stu-id="fd8fb-125">**put\_Size**</span></span>](iresize-put-size.md)           | <span data-ttu-id="fd8fb-126">Définit la taille de sortie et le mode Stretch.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-126">Sets the output size and stretch mode.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="fd8fb-127">Notes</span><span class="sxs-lookup"><span data-stu-id="fd8fb-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd8fb-128">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fd8fb-129">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fd8fb-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fd8fb-130">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fd8fb-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd8fb-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd8fb-131">Requirements</span></span>



| <span data-ttu-id="fd8fb-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd8fb-132">Requirement</span></span> | <span data-ttu-id="fd8fb-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd8fb-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8fb-134">Version</span><span class="sxs-lookup"><span data-stu-id="fd8fb-134">Version</span></span><br/> | <span data-ttu-id="fd8fb-135">DirectX 9,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fd8fb-135">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="fd8fb-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd8fb-136">Header</span></span><br/>  | <dl> <span data-ttu-id="fd8fb-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd8fb-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fd8fb-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fd8fb-138">Library</span></span><br/> | <dl> <span data-ttu-id="fd8fb-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd8fb-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd8fb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd8fb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8fb-141">Fournir un redimensionnement vidéo personnalisé</span><span class="sxs-lookup"><span data-stu-id="fd8fb-141">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
