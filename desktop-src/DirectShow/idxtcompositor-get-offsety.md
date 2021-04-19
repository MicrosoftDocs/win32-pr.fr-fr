---
description: La méthode d’extraction \_ de décalage récupère le décalage vertical du rectangle cible.
ms.assetid: 78bb3565-7a98-4a64-a2f2-6c34edb47733
title: 'IDxtCompositor :: get_OffsetY, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e3e8cb2e4552aceb53cf447125ddcc42659d575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525464"
---
# <a name="idxtcompositorget_offsety-method"></a><span data-ttu-id="30bcb-103">IDxtCompositor :: obtient la \_ méthode OffsetY</span><span class="sxs-lookup"><span data-stu-id="30bcb-103">IDxtCompositor::get\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="30bcb-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="30bcb-104">\[Deprecated.</span></span> <span data-ttu-id="30bcb-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30bcb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="30bcb-106">La `get_OffsetY` méthode récupère le décalage vertical du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="30bcb-106">The `get_OffsetY` method retrieves the vertical offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="30bcb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30bcb-107">Syntax</span></span>


```C++
HRESULT get_OffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="30bcb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30bcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30bcb-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="30bcb-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="30bcb-110">Reçoit, en pixels, le décalage vertical du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="30bcb-110">Receives the vertical offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30bcb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30bcb-111">Return value</span></span>

<span data-ttu-id="30bcb-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="30bcb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30bcb-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30bcb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30bcb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="30bcb-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30bcb-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="30bcb-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="30bcb-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="30bcb-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="30bcb-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="30bcb-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30bcb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30bcb-118">Requirements</span></span>



| <span data-ttu-id="30bcb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30bcb-119">Requirement</span></span> | <span data-ttu-id="30bcb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="30bcb-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30bcb-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="30bcb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="30bcb-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="30bcb-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="30bcb-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30bcb-123">Library</span></span><br/> | <dl> <span data-ttu-id="30bcb-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30bcb-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30bcb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30bcb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30bcb-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="30bcb-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




