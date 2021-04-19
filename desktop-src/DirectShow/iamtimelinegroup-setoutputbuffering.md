---
description: La méthode SetOutputBuffering spécifie le nombre d’images rendues à l’avance pendant la version préliminaire.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'IAMTimelineGroup :: SetOutputBuffering, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545609"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a><span data-ttu-id="25d60-103">IAMTimelineGroup :: SetOutputBuffering, méthode</span><span class="sxs-lookup"><span data-stu-id="25d60-103">IAMTimelineGroup::SetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="25d60-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="25d60-104">\[Deprecated.</span></span> <span data-ttu-id="25d60-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="25d60-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="25d60-106">La `SetOutputBuffering` méthode spécifie le nombre d’images rendues à l’avance pendant la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="25d60-106">The `SetOutputBuffering` method specifies the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="25d60-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25d60-107">Syntax</span></span>


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="25d60-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25d60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25d60-109">*nBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25d60-109">*nBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25d60-110">Nombre d’images à mettre en mémoire tampon pendant la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="25d60-110">Number of frames to buffer during preview.</span></span> <span data-ttu-id="25d60-111">Doit être supérieur ou égal à deux.</span><span class="sxs-lookup"><span data-stu-id="25d60-111">Must be two or greater.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25d60-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25d60-112">Return value</span></span>

<span data-ttu-id="25d60-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="25d60-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="25d60-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25d60-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="25d60-115">Notes</span><span class="sxs-lookup"><span data-stu-id="25d60-115">Remarks</span></span>

<span data-ttu-id="25d60-116">Une mémoire tampon plus grande requiert plus de mémoire, mais peut entraîner un aperçu plus lisse, en particulier lors d’effets ou de transitions qui nécessitent plus de temps pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="25d60-116">A larger buffer requires more memory but can result in smoother previewing, especially during effects or transitions that require more time to render.</span></span> <span data-ttu-id="25d60-117">La mémoire tampon par défaut est de 30 frames.</span><span class="sxs-lookup"><span data-stu-id="25d60-117">The default buffer is 30 frames.</span></span>

> [!Note]  
> <span data-ttu-id="25d60-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="25d60-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="25d60-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="25d60-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="25d60-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="25d60-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="25d60-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25d60-121">Requirements</span></span>



| <span data-ttu-id="25d60-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25d60-122">Requirement</span></span> | <span data-ttu-id="25d60-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="25d60-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25d60-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="25d60-124">Header</span></span><br/>  | <dl> <span data-ttu-id="25d60-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="25d60-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="25d60-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25d60-126">Library</span></span><br/> | <dl> <span data-ttu-id="25d60-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25d60-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25d60-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25d60-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25d60-129">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="25d60-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="25d60-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="25d60-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




