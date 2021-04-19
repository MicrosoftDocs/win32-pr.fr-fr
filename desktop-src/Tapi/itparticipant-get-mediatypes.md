---
description: La \_ méthode obtenir MediaTypes obtient les types de média associés à un participant.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'ITParticipant :: get_MediaTypes, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540138"
---
# <a name="itparticipantget_mediatypes-method"></a><span data-ttu-id="a8e49-103">ITParticipant :: \_ MediaTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="a8e49-103">ITParticipant::get\_MediaTypes method</span></span>

<span data-ttu-id="a8e49-104">\[en **savoir \_ plus MediaTypes** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a8e49-104">\[**get\_MediaTypes** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a8e49-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a8e49-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a8e49-106">La méthode **obtenir \_ MediaTypes** obtient les [**types de média**](tapimediatype--constants.md) associés à un participant.</span><span class="sxs-lookup"><span data-stu-id="a8e49-106">The **get\_MediaTypes** method gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e49-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8e49-107">Syntax</span></span>


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="a8e49-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8e49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8e49-109">*plMediaType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a8e49-109">*plMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8e49-110">Pointeur vers les indicateurs de type de média, tels que la \_ vidéo TAPIMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="a8e49-110">Pointer to media type flags, such as TAPIMEDIATYPE\_VIDEO.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8e49-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8e49-111">Return value</span></span>

<span data-ttu-id="a8e49-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a8e49-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a8e49-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a8e49-113">Return code</span></span>                                                                                   | <span data-ttu-id="a8e49-114">Description</span><span class="sxs-lookup"><span data-stu-id="a8e49-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a8e49-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a8e49-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a8e49-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a8e49-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a8e49-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a8e49-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a8e49-118">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a8e49-118">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a8e49-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="a8e49-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a8e49-120">Le paramètre *plMediaType* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="a8e49-120">The *plMediaType* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="a8e49-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8e49-121">Requirements</span></span>



| <span data-ttu-id="a8e49-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8e49-122">Requirement</span></span> | <span data-ttu-id="a8e49-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8e49-123">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e49-124">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a8e49-124">TAPI version</span></span><br/> | <span data-ttu-id="a8e49-125">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a8e49-125">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="a8e49-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8e49-126">Header</span></span><br/>       | <dl> <span data-ttu-id="a8e49-127"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e49-127"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8e49-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a8e49-128">Library</span></span><br/>      | <dl> <span data-ttu-id="a8e49-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8e49-129"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="a8e49-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a8e49-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="a8e49-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8e49-131"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8e49-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8e49-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e49-133">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="a8e49-133">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="a8e49-134">**types de médias**</span><span class="sxs-lookup"><span data-stu-id="a8e49-134">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

 




