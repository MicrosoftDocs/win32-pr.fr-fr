---
description: La \_ méthode put MaskNum spécifie le code de réinitialisation SMPTE de la réinitialisation.
ms.assetid: d2d2382c-d920-49e7-b9b7-6897356a78de
title: IDxtJpeg ::p ut_MaskNum, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f814fab2654a5585567273301dab285c32a1019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525442"
---
# <a name="idxtjpegput_masknum-method"></a><span data-ttu-id="54791-103">IDxtJpeg ::p ut \_ MaskNum, méthode</span><span class="sxs-lookup"><span data-stu-id="54791-103">IDxtJpeg::put\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="54791-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="54791-104">\[Deprecated.</span></span> <span data-ttu-id="54791-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54791-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="54791-106">La `put_MaskNum` méthode spécifie le code de réinitialisation SMPTE de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="54791-106">The `put_MaskNum` method specifies the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="54791-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54791-107">Syntax</span></span>


```C++
HRESULT put_MaskNum(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="54791-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54791-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54791-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54791-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54791-110">Spécifie le code de réinitialisation SMPTE.</span><span class="sxs-lookup"><span data-stu-id="54791-110">Specifies the SMPTE wipe code.</span></span> <span data-ttu-id="54791-111">Pour obtenir la liste des réinitialisations SMPTE prises en charge, consultez la page [transition de réinitialisation SMPTE](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="54791-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54791-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54791-112">Return value</span></span>

<span data-ttu-id="54791-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="54791-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="54791-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="54791-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="54791-115">Notes</span><span class="sxs-lookup"><span data-stu-id="54791-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54791-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="54791-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="54791-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="54791-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="54791-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="54791-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54791-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54791-119">Requirements</span></span>



| <span data-ttu-id="54791-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54791-120">Requirement</span></span> | <span data-ttu-id="54791-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="54791-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54791-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="54791-122">Header</span></span><br/>  | <dl> <span data-ttu-id="54791-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="54791-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="54791-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54791-124">Library</span></span><br/> | <dl> <span data-ttu-id="54791-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54791-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54791-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54791-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54791-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="54791-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




