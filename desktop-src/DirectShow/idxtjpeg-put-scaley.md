---
description: La méthode de mise à l' \_ échelle put spécifie le degré d’étirement vertical de la réinitialisation.
ms.assetid: 1dd84540-b249-482c-9cb7-aab8c7dc4d25
title: IDxtJpeg ::p ut_ScaleY, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65a8b736dc66ec9dad20b1e261ecd7b0c4556774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525197"
---
# <a name="idxtjpegput_scaley-method"></a><span data-ttu-id="50e40-103">IDxtJpeg : méthode de mise à l’échelle de :p ut \_</span><span class="sxs-lookup"><span data-stu-id="50e40-103">IDxtJpeg::put\_ScaleY method</span></span>

> [!Note]  
> <span data-ttu-id="50e40-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50e40-104">\[Deprecated.</span></span> <span data-ttu-id="50e40-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="50e40-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="50e40-106">La `put_ScaleY` méthode spécifie la quantité d’étirement vertical de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="50e40-106">The `put_ScaleY` method specifies the amount by which the wipe is stretched vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e40-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50e40-107">Syntax</span></span>


```C++
HRESULT put_ScaleY(
  [in] double newVal
);
```



## <a name="parameters"></a><span data-ttu-id="50e40-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50e40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e40-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50e40-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e40-110">Valeur de l’étirement vertical de la réinitialisation, sous la forme d’un pourcentage de la définition de la réinitialisation d’origine.</span><span class="sxs-lookup"><span data-stu-id="50e40-110">The amount by which the wipe is stretched vertically, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="50e40-111">Par exemple, la valeur 1,0 signifie aucun étirement, et 2,0 signifie l’étirement de 200%.</span><span class="sxs-lookup"><span data-stu-id="50e40-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e40-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50e40-112">Return value</span></span>

<span data-ttu-id="50e40-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="50e40-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50e40-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="50e40-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="50e40-115">Notes</span><span class="sxs-lookup"><span data-stu-id="50e40-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="50e40-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="50e40-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="50e40-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="50e40-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="50e40-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="50e40-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="50e40-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50e40-119">Requirements</span></span>



| <span data-ttu-id="50e40-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50e40-120">Requirement</span></span> | <span data-ttu-id="50e40-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="50e40-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50e40-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="50e40-122">Header</span></span><br/>  | <dl> <span data-ttu-id="50e40-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="50e40-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="50e40-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50e40-124">Library</span></span><br/> | <dl> <span data-ttu-id="50e40-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50e40-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50e40-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50e40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e40-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="50e40-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




