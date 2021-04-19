---
description: La \_ méthode obtenir SrcWidth récupère la largeur du rectangle source.
ms.assetid: 373bb108-5f0b-47f3-a39a-ed43b536e612
title: 'IDxtCompositor :: get_SrcWidth, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abd368c32b11b064f37c5c416cd944ee999272b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529932"
---
# <a name="idxtcompositorget_srcwidth-method"></a><span data-ttu-id="b566b-103">IDxtCompositor :: \_ SrcWidth, méthode</span><span class="sxs-lookup"><span data-stu-id="b566b-103">IDxtCompositor::get\_SrcWidth method</span></span>

> [!Note]  
> <span data-ttu-id="b566b-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b566b-104">\[Deprecated.</span></span> <span data-ttu-id="b566b-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b566b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b566b-106">La `get_SrcWidth` méthode récupère la largeur du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="b566b-106">The `get_SrcWidth` method retrieves the width of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b566b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b566b-107">Syntax</span></span>


```C++
HRESULT get_SrcWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b566b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b566b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b566b-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b566b-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b566b-110">Reçoit la largeur du rectangle source, en pixels.</span><span class="sxs-lookup"><span data-stu-id="b566b-110">Receives the width of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b566b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b566b-111">Return value</span></span>

<span data-ttu-id="b566b-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b566b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b566b-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b566b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b566b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b566b-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b566b-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b566b-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b566b-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b566b-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b566b-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b566b-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b566b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b566b-118">Requirements</span></span>



| <span data-ttu-id="b566b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b566b-119">Requirement</span></span> | <span data-ttu-id="b566b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b566b-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b566b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b566b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b566b-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b566b-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b566b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b566b-123">Library</span></span><br/> | <dl> <span data-ttu-id="b566b-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b566b-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b566b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b566b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b566b-126">**Interface IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="b566b-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




