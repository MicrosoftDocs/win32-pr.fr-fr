---
description: La \_ méthode obtenir BorderColor récupère la couleur de la bordure autour des bords du motif de réinitialisation.
ms.assetid: 9d36cc49-c174-4b93-a030-ca8d2890c624
title: 'IDxtJpeg :: get_BorderColor, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f37c37865caf76839733ada376ec637747977ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539299"
---
# <a name="idxtjpegget_bordercolor-method"></a><span data-ttu-id="64e00-103">IDxtJpeg :: obten, \_ méthode BorderColor</span><span class="sxs-lookup"><span data-stu-id="64e00-103">IDxtJpeg::get\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="64e00-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="64e00-104">\[Deprecated.</span></span> <span data-ttu-id="64e00-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="64e00-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="64e00-106">La `get_BorderColor` méthode récupère la couleur de la bordure autour des bords du motif de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="64e00-106">The `get_BorderColor` method retrieves the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e00-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64e00-107">Syntax</span></span>


```C++
HRESULT get_BorderColor(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="64e00-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64e00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64e00-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="64e00-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="64e00-110">Reçoit la couleur.</span><span class="sxs-lookup"><span data-stu-id="64e00-110">Receives the color.</span></span> <span data-ttu-id="64e00-111">La valeur retournée est un nombre hexadécimal au format 0xRRGGBB, où RR est la valeur rouge, GG est la valeur verte et BB est la valeur bleue.</span><span class="sxs-lookup"><span data-stu-id="64e00-111">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64e00-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64e00-112">Return value</span></span>

<span data-ttu-id="64e00-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="64e00-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64e00-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="64e00-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="64e00-115">Notes</span><span class="sxs-lookup"><span data-stu-id="64e00-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="64e00-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="64e00-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="64e00-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="64e00-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="64e00-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="64e00-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64e00-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64e00-119">Requirements</span></span>



| <span data-ttu-id="64e00-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64e00-120">Requirement</span></span> | <span data-ttu-id="64e00-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="64e00-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64e00-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="64e00-122">Header</span></span><br/>  | <dl> <span data-ttu-id="64e00-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="64e00-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="64e00-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64e00-124">Library</span></span><br/> | <dl> <span data-ttu-id="64e00-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64e00-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64e00-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64e00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e00-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="64e00-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




