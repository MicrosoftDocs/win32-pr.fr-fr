---
description: 'La méthode GetMediaLength2 récupère la longueur du média de cet objet source. Cette méthode est équivalente à IAMTimelineSrc :: GetMediaLength, mais prend des valeurs REFTIME.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'IAMTimelineSrc :: GetMediaLength2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528369"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a><span data-ttu-id="4085d-104">IAMTimelineSrc :: GetMediaLength2, méthode</span><span class="sxs-lookup"><span data-stu-id="4085d-104">IAMTimelineSrc::GetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="4085d-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="4085d-105">\[Deprecated.</span></span> <span data-ttu-id="4085d-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4085d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4085d-107">La `GetMediaLength2` méthode récupère la longueur du média de cet objet source.</span><span class="sxs-lookup"><span data-stu-id="4085d-107">The `GetMediaLength2` method retrieves the media length of this source object.</span></span> <span data-ttu-id="4085d-108">Cette méthode est équivalente à [**IAMTimelineSrc :: GetMediaLength**](iamtimelinesrc-getmedialength.md), mais prend des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="4085d-108">This method is equivalent to [**IAMTimelineSrc::GetMediaLength**](iamtimelinesrc-getmedialength.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="4085d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4085d-109">Syntax</span></span>


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="4085d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4085d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4085d-111">*pLength*</span><span class="sxs-lookup"><span data-stu-id="4085d-111">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="4085d-112">Reçoit la durée du média en secondes.</span><span class="sxs-lookup"><span data-stu-id="4085d-112">Receives the media length in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4085d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4085d-113">Return value</span></span>

<span data-ttu-id="4085d-114">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="4085d-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="4085d-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4085d-115">Return code</span></span>                                                                                     | <span data-ttu-id="4085d-116">Description</span><span class="sxs-lookup"><span data-stu-id="4085d-116">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="4085d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4085d-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="4085d-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="4085d-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="4085d-119"><dt>**\_NOTDETERMINED E**</dt></span><span class="sxs-lookup"><span data-stu-id="4085d-119"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="4085d-120">Les temps de support ne sont pas définis sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="4085d-120">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="4085d-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="4085d-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="4085d-122">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="4085d-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="4085d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4085d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4085d-124">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="4085d-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4085d-125">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4085d-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4085d-126">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4085d-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4085d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4085d-127">Requirements</span></span>



| <span data-ttu-id="4085d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4085d-128">Requirement</span></span> | <span data-ttu-id="4085d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4085d-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4085d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="4085d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4085d-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4085d-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4085d-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4085d-132">Library</span></span><br/> | <dl> <span data-ttu-id="4085d-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4085d-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4085d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4085d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4085d-135">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="4085d-135">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="4085d-136">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="4085d-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




