---
description: La \_ méthode put SrcOffsetX spécifie le décalage horizontal du rectangle source.
ms.assetid: 54f38dfd-3804-4ce4-ac70-5c7933e1a03f
title: IDxtCompositor ::p ut_SrcOffsetX, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcOffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a23cf2a07a209509cf55129ecd77ee8e035f5341
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533475"
---
# <a name="idxtcompositorput_srcoffsetx-method"></a><span data-ttu-id="f5a46-103">IDxtCompositor ::p ut \_ SrcOffsetX, méthode</span><span class="sxs-lookup"><span data-stu-id="f5a46-103">IDxtCompositor::put\_SrcOffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="f5a46-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f5a46-104">\[Deprecated.</span></span> <span data-ttu-id="f5a46-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5a46-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5a46-106">La `put_SrcOffsetX` méthode spécifie le décalage horizontal du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="f5a46-106">The `put_SrcOffsetX` method specifies the horizontal offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a46-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5a46-107">Syntax</span></span>


```C++
HRESULT put_SrcOffsetX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f5a46-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5a46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a46-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5a46-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a46-110">Décalage horizontal du rectangle source, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f5a46-110">The horizontal offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a46-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5a46-111">Return value</span></span>

<span data-ttu-id="f5a46-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f5a46-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5a46-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5a46-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a46-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f5a46-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f5a46-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f5a46-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5a46-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a46-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f5a46-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f5a46-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5a46-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5a46-118">Requirements</span></span>



| <span data-ttu-id="f5a46-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5a46-119">Requirement</span></span> | <span data-ttu-id="f5a46-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5a46-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a46-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5a46-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f5a46-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a46-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f5a46-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5a46-123">Library</span></span><br/> | <dl> <span data-ttu-id="f5a46-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5a46-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a46-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5a46-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a46-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="f5a46-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




