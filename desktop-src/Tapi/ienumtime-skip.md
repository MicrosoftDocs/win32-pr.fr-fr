---
description: 'IEnumTime :: Skip, méthode-la méthode Skip ignore le nombre spécifié d’éléments dans la séquence d’énumération.'
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: 'IEnumTime :: Skip, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190a98c14cb8f551276a173e2d73872d876f2ceb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090717"
---
# <a name="ienumtimeskip-method"></a><span data-ttu-id="549ea-103">IEnumTime :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="549ea-103">IEnumTime::Skip method</span></span>

<span data-ttu-id="549ea-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="549ea-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="549ea-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="549ea-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="549ea-106">La méthode **Skip** ignore le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="549ea-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="549ea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="549ea-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="549ea-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="549ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="549ea-109">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="549ea-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="549ea-110">Nombre d'éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="549ea-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="549ea-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="549ea-111">Return value</span></span>

<span data-ttu-id="549ea-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="549ea-112">This method can return one of these values.</span></span>



| <span data-ttu-id="549ea-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="549ea-113">Return code</span></span>                                                                             | <span data-ttu-id="549ea-114">Description</span><span class="sxs-lookup"><span data-stu-id="549ea-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="549ea-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="549ea-116">Le nombre d’éléments ignorés était *celt*.</span><span class="sxs-lookup"><span data-stu-id="549ea-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="549ea-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="549ea-118">Le nombre d’éléments ignorés n’est pas *celt*.</span><span class="sxs-lookup"><span data-stu-id="549ea-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="549ea-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="549ea-119">Requirements</span></span>



| <span data-ttu-id="549ea-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="549ea-120">Requirement</span></span> | <span data-ttu-id="549ea-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="549ea-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="549ea-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="549ea-122">TAPI version</span></span><br/> | <span data-ttu-id="549ea-123">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="549ea-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="549ea-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="549ea-124">Header</span></span><br/>       | <dl> <span data-ttu-id="549ea-125"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="549ea-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="549ea-126">Library</span></span><br/>      | <dl> <span data-ttu-id="549ea-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="549ea-128">DLL</span><span class="sxs-lookup"><span data-stu-id="549ea-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="549ea-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="549ea-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="549ea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="549ea-131">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="549ea-131">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




