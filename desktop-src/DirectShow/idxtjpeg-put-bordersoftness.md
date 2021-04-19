---
description: La \_ méthode put BorderSoftness spécifie la largeur de la zone floue autour des bords du modèle de réinitialisation.
ms.assetid: 9fdbda7f-c89b-4ed8-8035-054bc28f3231
title: IDxtJpeg ::p ut_BorderSoftness, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c72f59798ca84d01be79110cd4792da0a77f408
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537857"
---
# <a name="idxtjpegput_bordersoftness-method"></a><span data-ttu-id="7df49-103">IDxtJpeg ::p ut \_ BorderSoftness, méthode</span><span class="sxs-lookup"><span data-stu-id="7df49-103">IDxtJpeg::put\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="7df49-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7df49-104">\[Deprecated.</span></span> <span data-ttu-id="7df49-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7df49-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7df49-106">La `put_BorderSoftness` méthode spécifie la largeur de la zone floue autour des bords du modèle de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="7df49-106">The `put_BorderSoftness` method specifies the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df49-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7df49-107">Syntax</span></span>


```C++
HRESULT put_BorderSoftness(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="7df49-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7df49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df49-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7df49-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df49-110">Largeur de la zone floue, en pixels.</span><span class="sxs-lookup"><span data-stu-id="7df49-110">The width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df49-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7df49-111">Return value</span></span>

<span data-ttu-id="7df49-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7df49-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7df49-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7df49-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df49-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7df49-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7df49-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="7df49-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7df49-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7df49-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7df49-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7df49-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7df49-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7df49-118">Requirements</span></span>



| <span data-ttu-id="7df49-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7df49-119">Requirement</span></span> | <span data-ttu-id="7df49-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7df49-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7df49-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7df49-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7df49-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7df49-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7df49-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7df49-123">Library</span></span><br/> | <dl> <span data-ttu-id="7df49-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7df49-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df49-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7df49-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df49-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="7df49-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




