---
description: La \_ méthode obtenir MaskNum récupère le code de réinitialisation SMPTE de la réinitialisation.
ms.assetid: 49710d40-acc0-453e-ac9c-882794a0b82d
title: 'IDxtJpeg :: get_MaskNum, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 869809fdea6e1c329088abca50a1670239554327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532582"
---
# <a name="idxtjpegget_masknum-method"></a><span data-ttu-id="863b8-103">IDxtJpeg :: \_ MaskNum, méthode</span><span class="sxs-lookup"><span data-stu-id="863b8-103">IDxtJpeg::get\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="863b8-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="863b8-104">\[Deprecated.</span></span> <span data-ttu-id="863b8-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="863b8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="863b8-106">La `get_MaskNum` méthode récupère le code de réinitialisation SMPTE de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="863b8-106">The `get_MaskNum` method retrieves the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="863b8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="863b8-107">Syntax</span></span>


```C++
HRESULT get_MaskNum(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="863b8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="863b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="863b8-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="863b8-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="863b8-110">Reçoit le code de réinitialisation SMPTE.</span><span class="sxs-lookup"><span data-stu-id="863b8-110">Receives the SMPTE wipe code.</span></span> <span data-ttu-id="863b8-111">Pour obtenir la liste des réinitialisations SMPTE prises en charge, consultez la page [transition de réinitialisation SMPTE](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="863b8-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="863b8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="863b8-112">Return value</span></span>

<span data-ttu-id="863b8-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="863b8-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="863b8-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="863b8-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="863b8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="863b8-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="863b8-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="863b8-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="863b8-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="863b8-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="863b8-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="863b8-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="863b8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="863b8-119">Requirements</span></span>



| <span data-ttu-id="863b8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="863b8-120">Requirement</span></span> | <span data-ttu-id="863b8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="863b8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="863b8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="863b8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="863b8-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="863b8-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="863b8-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="863b8-124">Library</span></span><br/> | <dl> <span data-ttu-id="863b8-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="863b8-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="863b8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="863b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="863b8-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="863b8-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




