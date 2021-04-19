---
description: La méthode GetOutputBuffering récupère le nombre d’images rendues à l’avance pendant la version préliminaire.
ms.assetid: 93cb8d18-f1b7-48f9-af41-97f010304b05
title: 'IAMTimelineGroup :: GetOutputBuffering, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8213be882ca445775137a946d9064487b25f48af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531147"
---
# <a name="iamtimelinegroupgetoutputbuffering-method"></a><span data-ttu-id="bc6c5-103">IAMTimelineGroup :: GetOutputBuffering, méthode</span><span class="sxs-lookup"><span data-stu-id="bc6c5-103">IAMTimelineGroup::GetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="bc6c5-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-104">\[Deprecated.</span></span> <span data-ttu-id="bc6c5-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bc6c5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bc6c5-106">La `GetOutputBuffering` méthode récupère le nombre d’images rendues à l’avance pendant la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-106">The `GetOutputBuffering` method retrieves the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc6c5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc6c5-107">Syntax</span></span>


```C++
HRESULT GetOutputBuffering(
  [out] int *pnBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="bc6c5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc6c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc6c5-109">*pnBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bc6c5-109">*pnBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6c5-110">Reçoit le nombre de frames mis en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-110">Receives the number of buffered frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc6c5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc6c5-111">Return value</span></span>

<span data-ttu-id="bc6c5-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc6c5-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc6c5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc6c5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bc6c5-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bc6c5-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bc6c5-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bc6c5-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bc6c5-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bc6c5-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bc6c5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc6c5-118">Requirements</span></span>



| <span data-ttu-id="bc6c5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc6c5-119">Requirement</span></span> | <span data-ttu-id="bc6c5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc6c5-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6c5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc6c5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bc6c5-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc6c5-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bc6c5-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc6c5-123">Library</span></span><br/> | <dl> <span data-ttu-id="bc6c5-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc6c5-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc6c5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc6c5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6c5-126">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="bc6c5-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="bc6c5-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="bc6c5-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




