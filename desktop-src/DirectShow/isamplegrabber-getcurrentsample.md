---
description: La méthode GetCurrentSample n’est pas implémentée.
ms.assetid: 0c903498-3c1d-4e95-a797-ca8cfded25f2
title: 'ISampleGrabber :: GetCurrentSample, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentSample
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9a21f50f84f030502cfd3243d36595e465e1b85b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531014"
---
# <a name="isamplegrabbergetcurrentsample-method"></a><span data-ttu-id="46cf2-103">ISampleGrabber :: GetCurrentSample, méthode</span><span class="sxs-lookup"><span data-stu-id="46cf2-103">ISampleGrabber::GetCurrentSample method</span></span>

> [!Note]  
> <span data-ttu-id="46cf2-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="46cf2-104">\[Deprecated.</span></span> <span data-ttu-id="46cf2-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46cf2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="46cf2-106">La méthode `GetCurrentSample` n'est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="46cf2-106">The `GetCurrentSample` method is not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="46cf2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46cf2-107">Syntax</span></span>


```C++
HRESULT GetCurrentSample(
   IMediaSample **ppSample
);
```



## <a name="parameters"></a><span data-ttu-id="46cf2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46cf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46cf2-109">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="46cf2-109">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="46cf2-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="46cf2-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46cf2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46cf2-111">Return value</span></span>

<span data-ttu-id="46cf2-112">Retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="46cf2-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="46cf2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="46cf2-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46cf2-114">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="46cf2-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="46cf2-115">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="46cf2-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="46cf2-116">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="46cf2-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46cf2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46cf2-117">Requirements</span></span>



| <span data-ttu-id="46cf2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46cf2-118">Requirement</span></span> | <span data-ttu-id="46cf2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="46cf2-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46cf2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="46cf2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="46cf2-121"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="46cf2-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="46cf2-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46cf2-122">Library</span></span><br/> | <dl> <span data-ttu-id="46cf2-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46cf2-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46cf2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46cf2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46cf2-125">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="46cf2-125">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="46cf2-126">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="46cf2-126">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




