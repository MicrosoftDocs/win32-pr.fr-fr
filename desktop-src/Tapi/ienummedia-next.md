---
description: La méthode suivante obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'IEnumMedia :: Next, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04b92220d8fe93058533427ff8cc7bcc7ad7a02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541520"
---
# <a name="ienummedianext-method"></a><span data-ttu-id="f5d22-103">IEnumMedia :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="f5d22-103">IEnumMedia::Next method</span></span>

<span data-ttu-id="f5d22-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f5d22-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f5d22-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f5d22-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f5d22-106">La méthode **suivante** obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="f5d22-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d22-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5d22-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="f5d22-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5d22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d22-109">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5d22-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d22-110">Nombre d’éléments demandés.</span><span class="sxs-lookup"><span data-stu-id="f5d22-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="f5d22-111">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f5d22-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d22-112">Pointeur vers l’interface [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="f5d22-112">Pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f5d22-113">*pceltFetched* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f5d22-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d22-114">Pointeur vers le nombre d’éléments réellement fournis.</span><span class="sxs-lookup"><span data-stu-id="f5d22-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="f5d22-115">Peut avoir la **valeur null** si *celt* est un.</span><span class="sxs-lookup"><span data-stu-id="f5d22-115">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d22-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5d22-116">Return value</span></span>

<span data-ttu-id="f5d22-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f5d22-117">This method can return one of these values.</span></span>



| <span data-ttu-id="f5d22-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5d22-118">Value</span></span>                                                                                     | <span data-ttu-id="f5d22-119">Signification</span><span class="sxs-lookup"><span data-stu-id="f5d22-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="f5d22-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d22-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f5d22-121">La méthode a retourné la valeur *celt* Number of Elements.</span><span class="sxs-lookup"><span data-stu-id="f5d22-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="f5d22-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d22-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="f5d22-123">Le nombre d’éléments restants était inférieur à *celt*.</span><span class="sxs-lookup"><span data-stu-id="f5d22-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="f5d22-124"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d22-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="f5d22-125">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="f5d22-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="f5d22-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f5d22-126">Remarks</span></span>

<span data-ttu-id="f5d22-127">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITMedia**](itmedia.md) retournée par **IEnumMedia :: Next**.</span><span class="sxs-lookup"><span data-stu-id="f5d22-127">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **IEnumMedia::Next**.</span></span> <span data-ttu-id="f5d22-128">L’application doit appeler **Release** sur l’interface **ITMedia** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="f5d22-128">The application must call **Release** on the **ITMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d22-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5d22-129">Requirements</span></span>



| <span data-ttu-id="f5d22-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5d22-130">Requirement</span></span> | <span data-ttu-id="f5d22-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5d22-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d22-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f5d22-132">TAPI version</span></span><br/> | <span data-ttu-id="f5d22-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f5d22-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f5d22-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5d22-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f5d22-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d22-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5d22-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5d22-136">Library</span></span><br/>      | <dl> <span data-ttu-id="f5d22-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5d22-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f5d22-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f5d22-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="f5d22-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d22-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5d22-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5d22-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d22-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="f5d22-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




