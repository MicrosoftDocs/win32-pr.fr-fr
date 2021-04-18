---
description: La méthode GetMediaLength récupère la longueur du média de cet objet source.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'IAMTimelineSrc :: GetMediaLength, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540323"
---
# <a name="iamtimelinesrcgetmedialength-method"></a><span data-ttu-id="29d3c-103">IAMTimelineSrc :: GetMediaLength, méthode</span><span class="sxs-lookup"><span data-stu-id="29d3c-103">IAMTimelineSrc::GetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="29d3c-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="29d3c-104">\[Deprecated.</span></span> <span data-ttu-id="29d3c-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="29d3c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="29d3c-106">La `GetMediaLength` méthode récupère la longueur du média de cet objet source.</span><span class="sxs-lookup"><span data-stu-id="29d3c-106">The `GetMediaLength` method retrieves the media length of this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d3c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29d3c-107">Syntax</span></span>


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="29d3c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29d3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29d3c-109">*pLength*</span><span class="sxs-lookup"><span data-stu-id="29d3c-109">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="29d3c-110">Reçoit la longueur du média en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="29d3c-110">Receives the media length in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29d3c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29d3c-111">Return value</span></span>

<span data-ttu-id="29d3c-112">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="29d3c-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="29d3c-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="29d3c-113">Return code</span></span>                                                                                     | <span data-ttu-id="29d3c-114">Description</span><span class="sxs-lookup"><span data-stu-id="29d3c-114">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="29d3c-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="29d3c-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="29d3c-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="29d3c-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="29d3c-117"><dt>**\_NOTDETERMINED E**</dt></span><span class="sxs-lookup"><span data-stu-id="29d3c-117"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="29d3c-118">Les temps de support ne sont pas définis sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="29d3c-118">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="29d3c-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="29d3c-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="29d3c-120">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="29d3c-120">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="29d3c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="29d3c-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="29d3c-122">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="29d3c-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="29d3c-123">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="29d3c-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="29d3c-124">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="29d3c-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29d3c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29d3c-125">Requirements</span></span>



| <span data-ttu-id="29d3c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29d3c-126">Requirement</span></span> | <span data-ttu-id="29d3c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="29d3c-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29d3c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="29d3c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="29d3c-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="29d3c-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="29d3c-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="29d3c-130">Library</span></span><br/> | <dl> <span data-ttu-id="29d3c-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29d3c-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d3c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29d3c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d3c-133">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="29d3c-133">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="29d3c-134">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="29d3c-134">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[<span data-ttu-id="29d3c-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="29d3c-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




