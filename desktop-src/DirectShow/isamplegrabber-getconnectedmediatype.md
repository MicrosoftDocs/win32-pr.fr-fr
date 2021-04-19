---
description: La méthode GetConnectedMediaType récupère le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'ISampleGrabber :: GetConnectedMediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532758"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a><span data-ttu-id="9b8ae-103">ISampleGrabber :: GetConnectedMediaType, méthode</span><span class="sxs-lookup"><span data-stu-id="9b8ae-103">ISampleGrabber::GetConnectedMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="9b8ae-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-104">\[Deprecated.</span></span> <span data-ttu-id="9b8ae-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9b8ae-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9b8ae-106">La `GetConnectedMediaType` méthode récupère le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-106">The `GetConnectedMediaType` method retrieves the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b8ae-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b8ae-107">Syntax</span></span>


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="9b8ae-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b8ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b8ae-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="9b8ae-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="9b8ae-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allouée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b8ae-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b8ae-111">Return value</span></span>

<span data-ttu-id="9b8ae-112">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-112">Returns one of the following values.</span></span>



| <span data-ttu-id="9b8ae-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9b8ae-113">Return code</span></span>                                                                                           | <span data-ttu-id="9b8ae-114">Description</span><span class="sxs-lookup"><span data-stu-id="9b8ae-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="9b8ae-115"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="9b8ae-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="9b8ae-116">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="9b8ae-116">**NULL** pointer argument.</span></span><br/>   |
| <dl> <span data-ttu-id="9b8ae-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9b8ae-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="9b8ae-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-118">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="9b8ae-119"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="9b8ae-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9b8ae-120">Le filtre n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-120">The filter is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b8ae-121">Notes</span><span class="sxs-lookup"><span data-stu-id="9b8ae-121">Remarks</span></span>

<span data-ttu-id="9b8ae-122">Cette méthode copie le type de média dans la structure de **\_ \_ type de média am** spécifiée par *PTYPE*.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-122">This method copies the media type into the **AM\_MEDIA\_TYPE** structure specified by *pType*.</span></span> <span data-ttu-id="9b8ae-123">L’appelant doit libérer le bloc de format du type de média.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-123">The caller must free the format block of the media type.</span></span> <span data-ttu-id="9b8ae-124">Vous pouvez utiliser la fonction **CoTaskMemFree** ou la fonction [**FreeMediaType**](freemediatype.md) dans la bibliothèque de classes de base.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-124">You can use the **CoTaskMemFree** function, or the [**FreeMediaType**](freemediatype.md) function in the base-class library.</span></span>

> [!Note]  
> <span data-ttu-id="9b8ae-125">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9b8ae-126">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9b8ae-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9b8ae-127">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9b8ae-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b8ae-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b8ae-128">Requirements</span></span>



| <span data-ttu-id="9b8ae-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b8ae-129">Requirement</span></span> | <span data-ttu-id="9b8ae-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b8ae-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8ae-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b8ae-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9b8ae-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b8ae-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9b8ae-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9b8ae-133">Library</span></span><br/> | <dl> <span data-ttu-id="9b8ae-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b8ae-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b8ae-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b8ae-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b8ae-136">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="9b8ae-136">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="9b8ae-137">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="9b8ae-137">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




