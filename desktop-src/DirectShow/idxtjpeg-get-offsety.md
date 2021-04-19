---
description: La méthode d’extraction \_ de décalage récupère le décalage vertical de l’origine de la réinitialisation.
ms.assetid: 0d8b8df2-b916-4143-b1f1-7912ef3fa025
title: 'IDxtJpeg :: get_OffsetY, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76c0d60ac5150fcec1bde63ccb4e03d820c38ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533015"
---
# <a name="idxtjpegget_offsety-method"></a><span data-ttu-id="23410-103">IDxtJpeg :: obtient la \_ méthode OffsetY</span><span class="sxs-lookup"><span data-stu-id="23410-103">IDxtJpeg::get\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="23410-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="23410-104">\[Deprecated.</span></span> <span data-ttu-id="23410-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="23410-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="23410-106">La `get_OffsetY` méthode récupère le décalage vertical de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="23410-106">The `get_OffsetY` method retrieves the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="23410-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23410-107">Syntax</span></span>


```C++
HRESULT get_OffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="23410-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23410-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23410-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="23410-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="23410-110">Reçoit, en pixels, le décalage vertical de l’origine de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="23410-110">Receives the vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="23410-111">Le centre de la réinitialisation est décalé par rapport à cette quantité.</span><span class="sxs-lookup"><span data-stu-id="23410-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23410-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23410-112">Return value</span></span>

<span data-ttu-id="23410-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="23410-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23410-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23410-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="23410-115">Notes</span><span class="sxs-lookup"><span data-stu-id="23410-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23410-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="23410-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="23410-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="23410-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="23410-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="23410-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23410-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23410-119">Requirements</span></span>



| <span data-ttu-id="23410-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23410-120">Requirement</span></span> | <span data-ttu-id="23410-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="23410-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23410-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="23410-122">Header</span></span><br/>  | <dl> <span data-ttu-id="23410-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="23410-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="23410-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23410-124">Library</span></span><br/> | <dl> <span data-ttu-id="23410-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23410-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23410-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23410-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23410-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="23410-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




