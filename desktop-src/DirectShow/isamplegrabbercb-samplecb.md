---
description: La méthode SampleCB est une méthode de rappel qui reçoit un pointeur vers l’exemple de média.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'ISampleGrabberCB :: SampleCB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533434"
---
# <a name="isamplegrabbercbsamplecb-method"></a><span data-ttu-id="38f94-103">ISampleGrabberCB :: SampleCB, méthode</span><span class="sxs-lookup"><span data-stu-id="38f94-103">ISampleGrabberCB::SampleCB method</span></span>

> [!Note]  
> <span data-ttu-id="38f94-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="38f94-104">\[Deprecated.</span></span> <span data-ttu-id="38f94-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38f94-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="38f94-106">La `SampleCB` méthode est une méthode de rappel qui reçoit un pointeur vers l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="38f94-106">The `SampleCB` method is a callback method that receives a pointer to the media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f94-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38f94-107">Syntax</span></span>


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="38f94-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38f94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f94-109">*SampleTime*</span><span class="sxs-lookup"><span data-stu-id="38f94-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="38f94-110">Heure de début de l’échantillon, en secondes.</span><span class="sxs-lookup"><span data-stu-id="38f94-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="38f94-111">*pSample*</span><span class="sxs-lookup"><span data-stu-id="38f94-111">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="38f94-112">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="38f94-112">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f94-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38f94-113">Return value</span></span>

<span data-ttu-id="38f94-114">Retourne S \_ OK en cas de réussite, ou un code d’erreur **HRESULT** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="38f94-114">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f94-115">Notes</span><span class="sxs-lookup"><span data-stu-id="38f94-115">Remarks</span></span>

<span data-ttu-id="38f94-116">Pour configurer le rappel, appelez [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="38f94-116">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="38f94-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="38f94-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="38f94-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="38f94-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="38f94-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="38f94-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="38f94-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38f94-120">Requirements</span></span>



| <span data-ttu-id="38f94-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38f94-121">Requirement</span></span> | <span data-ttu-id="38f94-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="38f94-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38f94-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="38f94-123">Header</span></span><br/>  | <dl> <span data-ttu-id="38f94-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="38f94-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="38f94-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38f94-125">Library</span></span><br/> | <dl> <span data-ttu-id="38f94-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38f94-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38f94-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38f94-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f94-128">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="38f94-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="38f94-129">**Interface ISampleGrabberCB**</span><span class="sxs-lookup"><span data-stu-id="38f94-129">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




