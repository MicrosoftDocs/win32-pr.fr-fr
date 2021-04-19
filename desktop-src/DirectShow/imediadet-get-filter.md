---
description: La \_ méthode de filtre d’extraction récupère un pointeur vers le filtre source actuellement utilisé par le détecteur de média.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'IMediaDet :: get_Filter, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541305"
---
# <a name="imediadetget_filter-method"></a><span data-ttu-id="045ad-103">IMediaDet :: obtient la \_ méthode de filtre</span><span class="sxs-lookup"><span data-stu-id="045ad-103">IMediaDet::get\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="045ad-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="045ad-104">\[Deprecated.</span></span> <span data-ttu-id="045ad-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="045ad-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="045ad-106">La `get_Filter` méthode récupère un pointeur vers le filtre source actuellement utilisé par le détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="045ad-106">The `get_Filter` method retrieves a pointer to the source filter currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="045ad-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="045ad-107">Syntax</span></span>


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="045ad-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="045ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="045ad-109">*ppVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="045ad-109">*ppVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="045ad-110">Reçoit un pointeur vers l’interface **IUnknown** du filtre.</span><span class="sxs-lookup"><span data-stu-id="045ad-110">Receives a pointer to the filter's **IUnknown** interface.</span></span> <span data-ttu-id="045ad-111">Si aucun filtre source n’est utilisé, la valeur est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="045ad-111">If no source filter is in use, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="045ad-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="045ad-112">Return value</span></span>

<span data-ttu-id="045ad-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="045ad-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="045ad-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="045ad-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="045ad-115">Notes</span><span class="sxs-lookup"><span data-stu-id="045ad-115">Remarks</span></span>

<span data-ttu-id="045ad-116">Lorsque la méthode est retournée, si *\* ppVal* n’a pas la **valeur null**, l’interface **IUnknown** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="045ad-116">When the method returns, if *\*ppVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="045ad-117">Libérez l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="045ad-117">Release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="045ad-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="045ad-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="045ad-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="045ad-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="045ad-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="045ad-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="045ad-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="045ad-121">Requirements</span></span>



| <span data-ttu-id="045ad-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="045ad-122">Requirement</span></span> | <span data-ttu-id="045ad-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="045ad-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="045ad-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="045ad-124">Header</span></span><br/>  | <dl> <span data-ttu-id="045ad-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="045ad-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="045ad-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="045ad-126">Library</span></span><br/> | <dl> <span data-ttu-id="045ad-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="045ad-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="045ad-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="045ad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="045ad-129">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="045ad-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="045ad-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="045ad-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




