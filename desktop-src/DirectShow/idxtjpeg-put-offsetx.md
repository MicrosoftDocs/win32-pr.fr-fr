---
description: La \_ méthode put OffsetX spécifie le décalage horizontal de l’origine de la réinitialisation.
ms.assetid: 7bc721fd-7e72-49d4-90ae-a193df46326c
title: IDxtJpeg ::p ut_OffsetX, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 70bb908be3f2e2173ebae12f45e24600b38a0441
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523464"
---
# <a name="idxtjpegput_offsetx-method"></a><span data-ttu-id="996dd-103">IDxtJpeg ::p ut \_ offsetn, méthode</span><span class="sxs-lookup"><span data-stu-id="996dd-103">IDxtJpeg::put\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="996dd-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="996dd-104">\[Deprecated.</span></span> <span data-ttu-id="996dd-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="996dd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="996dd-106">La `put_OffsetX` méthode spécifie le décalage horizontal de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="996dd-106">The `put_OffsetX` method specifies the horizontal offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="996dd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="996dd-107">Syntax</span></span>


```C++
HRESULT put_OffsetX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="996dd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="996dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="996dd-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="996dd-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="996dd-110">Décalage horizontal de l’origine de la réinitialisation, en pixels.</span><span class="sxs-lookup"><span data-stu-id="996dd-110">The horizontal offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="996dd-111">Le centre de la réinitialisation est décalé par rapport à cette quantité.</span><span class="sxs-lookup"><span data-stu-id="996dd-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="996dd-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="996dd-112">Return value</span></span>

<span data-ttu-id="996dd-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="996dd-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="996dd-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="996dd-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="996dd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="996dd-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="996dd-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="996dd-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="996dd-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="996dd-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="996dd-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="996dd-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="996dd-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="996dd-119">Requirements</span></span>



| <span data-ttu-id="996dd-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="996dd-120">Requirement</span></span> | <span data-ttu-id="996dd-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="996dd-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="996dd-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="996dd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="996dd-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="996dd-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="996dd-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="996dd-124">Library</span></span><br/> | <dl> <span data-ttu-id="996dd-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="996dd-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="996dd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="996dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996dd-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="996dd-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




