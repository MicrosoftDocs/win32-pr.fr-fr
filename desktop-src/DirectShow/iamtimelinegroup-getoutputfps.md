---
description: La méthode GetOutputFPS récupère la fréquence d’images de sortie de ce groupe.
ms.assetid: e6dfa4a9-4d44-4ce7-9aec-3564fd337ff6
title: 'IAMTimelineGroup :: GetOutputFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f02e7db36e5ea61e3c738b4c2d92678674bfcec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529023"
---
# <a name="iamtimelinegroupgetoutputfps-method"></a><span data-ttu-id="7ed0e-103">IAMTimelineGroup :: GetOutputFPS, méthode</span><span class="sxs-lookup"><span data-stu-id="7ed0e-103">IAMTimelineGroup::GetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="7ed0e-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7ed0e-104">\[Deprecated.</span></span> <span data-ttu-id="7ed0e-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ed0e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ed0e-106">La `GetOutputFPS` méthode récupère la fréquence d’images de sortie de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="7ed0e-106">The `GetOutputFPS` method retrieves the output frame rate of this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ed0e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ed0e-107">Syntax</span></span>


```C++
HRESULT GetOutputFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="7ed0e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ed0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ed0e-109">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="7ed0e-109">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="7ed0e-110">Reçoit la fréquence d’images en sortie, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="7ed0e-110">Receives the output frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ed0e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ed0e-111">Return value</span></span>

<span data-ttu-id="7ed0e-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ed0e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ed0e-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ed0e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ed0e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7ed0e-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ed0e-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="7ed0e-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ed0e-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ed0e-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ed0e-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7ed0e-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ed0e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ed0e-118">Requirements</span></span>



| <span data-ttu-id="7ed0e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ed0e-119">Requirement</span></span> | <span data-ttu-id="7ed0e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ed0e-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed0e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ed0e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7ed0e-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ed0e-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ed0e-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ed0e-123">Library</span></span><br/> | <dl> <span data-ttu-id="7ed0e-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ed0e-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ed0e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ed0e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed0e-126">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="7ed0e-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="7ed0e-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="7ed0e-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




