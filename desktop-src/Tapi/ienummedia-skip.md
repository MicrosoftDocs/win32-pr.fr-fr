---
description: 'IEnumMedia :: Skip, méthode-la méthode Skip ignore le nombre spécifié d’éléments dans la séquence d’énumération.'
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: 'IEnumMedia :: Skip, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8c600a201d6800fcb04dba5f208fd5cb810078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084187"
---
# <a name="ienummediaskip-method"></a><span data-ttu-id="32e17-103">IEnumMedia :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="32e17-103">IEnumMedia::Skip method</span></span>

<span data-ttu-id="32e17-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="32e17-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="32e17-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="32e17-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="32e17-106">La méthode **Skip** ignore le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="32e17-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e17-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32e17-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="32e17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32e17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32e17-109">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32e17-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32e17-110">Nombre d'éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="32e17-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32e17-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="32e17-111">Return value</span></span>

<span data-ttu-id="32e17-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="32e17-112">This method can return one of these values.</span></span>



| <span data-ttu-id="32e17-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="32e17-113">Return code</span></span>                                                                             | <span data-ttu-id="32e17-114">Description</span><span class="sxs-lookup"><span data-stu-id="32e17-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="32e17-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="32e17-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="32e17-116">Le nombre d’éléments ignorés était *celt*.</span><span class="sxs-lookup"><span data-stu-id="32e17-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="32e17-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="32e17-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="32e17-118">Le nombre d’éléments ignorés n’est pas *celt*.</span><span class="sxs-lookup"><span data-stu-id="32e17-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="32e17-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32e17-119">Requirements</span></span>



| <span data-ttu-id="32e17-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32e17-120">Requirement</span></span> | <span data-ttu-id="32e17-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="32e17-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32e17-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="32e17-122">TAPI version</span></span><br/> | <span data-ttu-id="32e17-123">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="32e17-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="32e17-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="32e17-124">Header</span></span><br/>       | <dl> <span data-ttu-id="32e17-125"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="32e17-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="32e17-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="32e17-126">Library</span></span><br/>      | <dl> <span data-ttu-id="32e17-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32e17-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="32e17-128">DLL</span><span class="sxs-lookup"><span data-stu-id="32e17-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="32e17-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32e17-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e17-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32e17-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e17-131">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="32e17-131">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




