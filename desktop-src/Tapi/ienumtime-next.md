---
description: 'IEnumTime :: Next, méthode-la méthode suivante obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: 'IEnumTime :: Next, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1487136b0e3e41ba11a23ba92500d2aa0758df79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118387"
---
# <a name="ienumtimenext-method"></a><span data-ttu-id="b75b1-103">IEnumTime :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="b75b1-103">IEnumTime::Next method</span></span>

<span data-ttu-id="b75b1-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b75b1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b75b1-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="b75b1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b75b1-106">La méthode **suivante** obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="b75b1-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="b75b1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b75b1-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="b75b1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b75b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b75b1-109">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b75b1-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b75b1-110">Nombre d’éléments demandés.</span><span class="sxs-lookup"><span data-stu-id="b75b1-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="b75b1-111">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b75b1-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b75b1-112">Pointeur vers l’interface [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="b75b1-112">Pointer to the [**ITTime**](ittime.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b75b1-113">*pceltFetched* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b75b1-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b75b1-114">Pointeur vers le nombre d’éléments réellement fournis.</span><span class="sxs-lookup"><span data-stu-id="b75b1-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="b75b1-115">Peut avoir la **valeur null** si *celt* a la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="b75b1-115">May be **NULL** if *celt* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b75b1-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b75b1-116">Return value</span></span>

<span data-ttu-id="b75b1-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b75b1-117">This method can return one of these values.</span></span>



| <span data-ttu-id="b75b1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b75b1-118">Value</span></span>                                                                                     | <span data-ttu-id="b75b1-119">Signification</span><span class="sxs-lookup"><span data-stu-id="b75b1-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="b75b1-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b75b1-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b75b1-121">La méthode a retourné la valeur *celt* Number of Elements.</span><span class="sxs-lookup"><span data-stu-id="b75b1-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="b75b1-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b75b1-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="b75b1-123">Le nombre d’éléments restants était inférieur à *celt*.</span><span class="sxs-lookup"><span data-stu-id="b75b1-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="b75b1-124"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b75b1-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b75b1-125">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="b75b1-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="b75b1-126">Notes </span><span class="sxs-lookup"><span data-stu-id="b75b1-126">Remarks</span></span>

<span data-ttu-id="b75b1-127">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITTime**](ittime.md) retournée par **IEnumTime :: Next**.</span><span class="sxs-lookup"><span data-stu-id="b75b1-127">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **IEnumTime::Next**.</span></span> <span data-ttu-id="b75b1-128">L’application doit appeler **Release** sur l’interface **ITTime** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="b75b1-128">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b75b1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b75b1-129">Requirements</span></span>



| <span data-ttu-id="b75b1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b75b1-130">Requirement</span></span> | <span data-ttu-id="b75b1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b75b1-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b75b1-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b75b1-132">TAPI version</span></span><br/> | <span data-ttu-id="b75b1-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b75b1-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b75b1-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b75b1-134">Header</span></span><br/>       | <dl> <span data-ttu-id="b75b1-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b75b1-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b75b1-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b75b1-136">Library</span></span><br/>      | <dl> <span data-ttu-id="b75b1-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b75b1-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b75b1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b75b1-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="b75b1-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b75b1-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b75b1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b75b1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75b1-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="b75b1-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




