---
description: La \_ méthode put OffsetY spécifie le décalage vertical de l’origine de la réinitialisation.
ms.assetid: 1dfd18cf-06ae-46eb-80d7-078efc243bb1
title: IDxtJpeg ::p ut_OffsetY, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f68a18d01acf519032bce31c28515bc7ac81c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545950"
---
# <a name="idxtjpegput_offsety-method"></a><span data-ttu-id="7689e-103">IDxtJpeg ::p \_ méthode offset ut</span><span class="sxs-lookup"><span data-stu-id="7689e-103">IDxtJpeg::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="7689e-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7689e-104">\[Deprecated.</span></span> <span data-ttu-id="7689e-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7689e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7689e-106">La `put_OffsetY` méthode spécifie le décalage vertical de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="7689e-106">The `put_OffsetY` method specifies the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="7689e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7689e-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="7689e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7689e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7689e-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7689e-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7689e-110">Décalage vertical de l’origine de la réinitialisation, en pixels.</span><span class="sxs-lookup"><span data-stu-id="7689e-110">The vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="7689e-111">Le centre de la réinitialisation est décalé par rapport à cette quantité.</span><span class="sxs-lookup"><span data-stu-id="7689e-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7689e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7689e-112">Return value</span></span>

<span data-ttu-id="7689e-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7689e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7689e-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7689e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7689e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7689e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7689e-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="7689e-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7689e-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7689e-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7689e-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7689e-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7689e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7689e-119">Requirements</span></span>



| <span data-ttu-id="7689e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7689e-120">Requirement</span></span> | <span data-ttu-id="7689e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7689e-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7689e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7689e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7689e-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7689e-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7689e-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7689e-124">Library</span></span><br/> | <dl> <span data-ttu-id="7689e-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7689e-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7689e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7689e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7689e-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="7689e-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




