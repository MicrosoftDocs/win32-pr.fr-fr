---
description: La \_ méthode obtenir SrcOffsetY récupère le décalage vertical du rectangle source.
ms.assetid: b692e71b-c7a9-437c-9127-fa517e817883
title: 'IDxtCompositor :: get_SrcOffsetY, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcOffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fbe254037d35504a46aed519f1030a9d0aff0d02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541411"
---
# <a name="idxtcompositorget_srcoffsety-method"></a><span data-ttu-id="0ae12-103">IDxtCompositor :: \_ SrcOffsetY, méthode</span><span class="sxs-lookup"><span data-stu-id="0ae12-103">IDxtCompositor::get\_SrcOffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="0ae12-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0ae12-104">\[Deprecated.</span></span> <span data-ttu-id="0ae12-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0ae12-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0ae12-106">La `get_SrcOffsetY` méthode récupère le décalage vertical du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="0ae12-106">The `get_SrcOffsetY` method retrieves the vertical offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ae12-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ae12-107">Syntax</span></span>


```C++
HRESULT get_SrcOffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0ae12-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ae12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ae12-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0ae12-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0ae12-110">Reçoit, en pixels, le décalage vertical du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="0ae12-110">Receives the vertical offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ae12-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ae12-111">Return value</span></span>

<span data-ttu-id="0ae12-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0ae12-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ae12-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ae12-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ae12-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0ae12-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0ae12-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0ae12-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0ae12-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0ae12-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0ae12-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0ae12-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0ae12-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ae12-118">Requirements</span></span>



| <span data-ttu-id="0ae12-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ae12-119">Requirement</span></span> | <span data-ttu-id="0ae12-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ae12-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ae12-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ae12-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0ae12-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ae12-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0ae12-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ae12-123">Library</span></span><br/> | <dl> <span data-ttu-id="0ae12-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ae12-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ae12-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ae12-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ae12-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="0ae12-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




