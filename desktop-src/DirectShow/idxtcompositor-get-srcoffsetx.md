---
description: La \_ méthode obtenir SrcOffsetX récupère le décalage horizontal du rectangle source.
ms.assetid: 528a5306-86bd-4ae2-ad03-57247362c5b5
title: 'IDxtCompositor :: get_SrcOffsetX, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcOffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ee116537061986a556854aed093b5e9a414016e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535306"
---
# <a name="idxtcompositorget_srcoffsetx-method"></a><span data-ttu-id="8d9c9-103">IDxtCompositor :: \_ SrcOffsetX, méthode</span><span class="sxs-lookup"><span data-stu-id="8d9c9-103">IDxtCompositor::get\_SrcOffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="8d9c9-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8d9c9-104">\[Deprecated.</span></span> <span data-ttu-id="8d9c9-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8d9c9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8d9c9-106">La `get_SrcOffsetX` méthode récupère le décalage horizontal du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="8d9c9-106">The `get_SrcOffsetX` method retrieves the horizontal offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9c9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d9c9-107">Syntax</span></span>


```C++
HRESULT get_SrcOffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8d9c9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d9c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9c9-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8d9c9-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9c9-110">Reçoit, en pixels, le décalage horizontal du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="8d9c9-110">Receives the horizontal offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9c9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d9c9-111">Return value</span></span>

<span data-ttu-id="8d9c9-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8d9c9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d9c9-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8d9c9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9c9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8d9c9-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8d9c9-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="8d9c9-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8d9c9-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8d9c9-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8d9c9-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8d9c9-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d9c9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d9c9-118">Requirements</span></span>



| <span data-ttu-id="8d9c9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d9c9-119">Requirement</span></span> | <span data-ttu-id="8d9c9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d9c9-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9c9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d9c9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8d9c9-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d9c9-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8d9c9-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d9c9-123">Library</span></span><br/> | <dl> <span data-ttu-id="8d9c9-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d9c9-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d9c9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d9c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9c9-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="8d9c9-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




