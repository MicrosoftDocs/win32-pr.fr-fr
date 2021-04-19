---
description: La \_ méthode put Height spécifie la hauteur du rectangle cible.
ms.assetid: 032b5468-bce8-4492-abbe-e442131ebe3a
title: IDxtCompositor ::p ut_Height, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_Height
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 883a3261b6322a69e0e1612b724a9f570953dc97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525478"
---
# <a name="idxtcompositorput_height-method"></a><span data-ttu-id="14461-103">IDxtCompositor : méthode :p ut \_ Height</span><span class="sxs-lookup"><span data-stu-id="14461-103">IDxtCompositor::put\_Height method</span></span>

> [!Note]  
> <span data-ttu-id="14461-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="14461-104">\[Deprecated.</span></span> <span data-ttu-id="14461-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="14461-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="14461-106">La `put_Height` méthode spécifie la hauteur du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="14461-106">The `put_Height` method specifies the height of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="14461-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14461-107">Syntax</span></span>


```C++
HRESULT put_Height(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="14461-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14461-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14461-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14461-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14461-110">Hauteur, en pixels, du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="14461-110">The height of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14461-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14461-111">Return value</span></span>

<span data-ttu-id="14461-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="14461-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14461-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14461-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14461-114">Notes</span><span class="sxs-lookup"><span data-stu-id="14461-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="14461-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="14461-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="14461-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="14461-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="14461-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="14461-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="14461-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14461-118">Requirements</span></span>



| <span data-ttu-id="14461-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14461-119">Requirement</span></span> | <span data-ttu-id="14461-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="14461-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14461-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="14461-121">Header</span></span><br/>  | <dl> <span data-ttu-id="14461-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="14461-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="14461-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14461-123">Library</span></span><br/> | <dl> <span data-ttu-id="14461-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14461-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14461-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14461-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14461-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="14461-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




