---
description: La \_ méthode obtenir OffsetX récupère le décalage horizontal de l’origine de la réinitialisation.
ms.assetid: 0ca97bb9-9359-4098-9e80-1847da4154ec
title: 'IDxtJpeg :: get_OffsetX, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d18d8ede94700f2de2fe49e44031675c7c91c930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525554"
---
# <a name="idxtjpegget_offsetx-method"></a><span data-ttu-id="f2d02-103">IDxtJpeg :: obtient l' \_ OffsetX, méthode</span><span class="sxs-lookup"><span data-stu-id="f2d02-103">IDxtJpeg::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="f2d02-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f2d02-104">\[Deprecated.</span></span> <span data-ttu-id="f2d02-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f2d02-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f2d02-106">La `get_OffsetX` méthode récupère le décalage horizontal de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="f2d02-106">The `get_OffsetX` method retrieves the horizontal offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2d02-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2d02-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f2d02-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2d02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d02-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f2d02-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d02-110">Reçoit, en pixels, le décalage horizontal de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="f2d02-110">Receives the horizontal offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="f2d02-111">Le centre de la réinitialisation est décalé par rapport à cette quantité.</span><span class="sxs-lookup"><span data-stu-id="f2d02-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2d02-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2d02-112">Return value</span></span>

<span data-ttu-id="f2d02-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f2d02-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f2d02-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2d02-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2d02-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f2d02-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f2d02-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f2d02-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f2d02-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f2d02-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f2d02-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f2d02-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2d02-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2d02-119">Requirements</span></span>



| <span data-ttu-id="f2d02-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2d02-120">Requirement</span></span> | <span data-ttu-id="f2d02-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2d02-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d02-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2d02-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f2d02-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2d02-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f2d02-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2d02-124">Library</span></span><br/> | <dl> <span data-ttu-id="f2d02-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2d02-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2d02-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2d02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2d02-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="f2d02-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




