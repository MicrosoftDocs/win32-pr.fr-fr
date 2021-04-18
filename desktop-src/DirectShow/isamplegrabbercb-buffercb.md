---
description: La méthode BufferCB est une méthode de rappel qui reçoit un pointeur vers l’exemple de mémoire tampon.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'ISampleGrabberCB :: BufferCB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533222"
---
# <a name="isamplegrabbercbbuffercb-method"></a><span data-ttu-id="d0c92-103">ISampleGrabberCB :: BufferCB, méthode</span><span class="sxs-lookup"><span data-stu-id="d0c92-103">ISampleGrabberCB::BufferCB method</span></span>

> [!Note]  
> <span data-ttu-id="d0c92-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d0c92-104">\[Deprecated.</span></span> <span data-ttu-id="d0c92-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0c92-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d0c92-106">La méthode **BufferCB** est une méthode de rappel qui reçoit un pointeur vers l’exemple de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d0c92-106">The **BufferCB** method is a callback method that receives a pointer to the sample buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c92-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0c92-107">Syntax</span></span>


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a><span data-ttu-id="d0c92-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0c92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c92-109">*SampleTime*</span><span class="sxs-lookup"><span data-stu-id="d0c92-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c92-110">Heure de début de l’échantillon, en secondes.</span><span class="sxs-lookup"><span data-stu-id="d0c92-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="d0c92-111">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="d0c92-111">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c92-112">Pointeur vers une mémoire tampon qui contient les exemples de données.</span><span class="sxs-lookup"><span data-stu-id="d0c92-112">Pointer to a buffer that contains the sample data.</span></span> <span data-ttu-id="d0c92-113">Le format des données dépend du type de support de la broche d’entrée de l’exemple de la accroche.</span><span class="sxs-lookup"><span data-stu-id="d0c92-113">The format of the data depends on the media type of the Sample Grabber's input pin.</span></span> <span data-ttu-id="d0c92-114">Pour accéder au type de média, appelez [**ISampleGrabber :: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="d0c92-114">To get the media type, call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0c92-115">*BufferLen*</span><span class="sxs-lookup"><span data-stu-id="d0c92-115">*BufferLen*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c92-116">Longueur de la mémoire tampon vers laquelle pointe *pbuffer*, en octets.</span><span class="sxs-lookup"><span data-stu-id="d0c92-116">Length of the buffer pointed to by *pBuffer*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c92-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0c92-117">Return value</span></span>

<span data-ttu-id="d0c92-118">Retourne S \_ OK en cas de réussite, ou un code d’erreur **HRESULT** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d0c92-118">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0c92-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d0c92-119">Remarks</span></span>

<span data-ttu-id="d0c92-120">Cette méthode de rappel reçoit un pointeur vers les données dans l’exemple de média le plus récent.</span><span class="sxs-lookup"><span data-stu-id="d0c92-120">This callback method receives a pointer to the data in the most recent media sample.</span></span>

> [!Note]  
> <span data-ttu-id="d0c92-121">Cette méthode reçoit un pointeur vers les données d’exemple d’origine, pas une copie.</span><span class="sxs-lookup"><span data-stu-id="d0c92-121">This method receives a pointer to the original sample data, not a copy.</span></span> <span data-ttu-id="d0c92-122">La documentation d’origine a indiqué de manière incorrecte que *pbuffer* contient une copie des données.</span><span class="sxs-lookup"><span data-stu-id="d0c92-122">The original documentation incorrectly stated that *pBuffer* contains a copy of the data.</span></span>

 

<span data-ttu-id="d0c92-123">Pour configurer le rappel, appelez [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="d0c92-123">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="d0c92-124">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="d0c92-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d0c92-125">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d0c92-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d0c92-126">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d0c92-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0c92-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0c92-127">Requirements</span></span>



| <span data-ttu-id="d0c92-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0c92-128">Requirement</span></span> | <span data-ttu-id="d0c92-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0c92-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c92-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0c92-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d0c92-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c92-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d0c92-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0c92-132">Library</span></span><br/> | <dl> <span data-ttu-id="d0c92-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0c92-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c92-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0c92-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c92-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="d0c92-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="d0c92-136">**Interface ISampleGrabberCB**</span><span class="sxs-lookup"><span data-stu-id="d0c92-136">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




