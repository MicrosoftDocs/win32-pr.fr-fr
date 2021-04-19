---
description: La méthode AreYouBlank détermine si la piste est vide (ne contient aucun objet source).
ms.assetid: 05d02753-6e40-4307-9445-c3cbc835f75e
title: 'IAMTimelineTrack :: AreYouBlank, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.AreYouBlank
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 289fac360f989504d3eb5108f8c2388ac4a06b09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539569"
---
# <a name="iamtimelinetrackareyoublank-method"></a><span data-ttu-id="3440a-103">IAMTimelineTrack :: AreYouBlank, méthode</span><span class="sxs-lookup"><span data-stu-id="3440a-103">IAMTimelineTrack::AreYouBlank method</span></span>

> [!Note]  
> <span data-ttu-id="3440a-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3440a-104">\[Deprecated.</span></span> <span data-ttu-id="3440a-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3440a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3440a-106">La `AreYouBlank` méthode détermine si la piste est vide (ne contient aucun objet source).</span><span class="sxs-lookup"><span data-stu-id="3440a-106">The `AreYouBlank` method determines whether the track is blank (contains no source objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="3440a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3440a-107">Syntax</span></span>


```C++
HRESULT AreYouBlank(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3440a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3440a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3440a-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="3440a-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="3440a-110">Reçoit une valeur booléenne spécifiant si la piste est vide.</span><span class="sxs-lookup"><span data-stu-id="3440a-110">Receives a Boolean value specifying whether the track is blank.</span></span> <span data-ttu-id="3440a-111">Si la valeur est **true**, la piste est vide et ne contient aucun objet source.</span><span class="sxs-lookup"><span data-stu-id="3440a-111">If the value is **TRUE**, the track is blank and contains no source objects.</span></span> <span data-ttu-id="3440a-112">Si la **valeur est false**, la piste n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="3440a-112">If **FALSE**, the track is not blank.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3440a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3440a-113">Return value</span></span>

<span data-ttu-id="3440a-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3440a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3440a-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3440a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3440a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3440a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3440a-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3440a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3440a-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3440a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3440a-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3440a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3440a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3440a-120">Requirements</span></span>



| <span data-ttu-id="3440a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3440a-121">Requirement</span></span> | <span data-ttu-id="3440a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3440a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3440a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3440a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3440a-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3440a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3440a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3440a-125">Library</span></span><br/> | <dl> <span data-ttu-id="3440a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3440a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3440a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3440a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3440a-128">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="3440a-128">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="3440a-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3440a-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




