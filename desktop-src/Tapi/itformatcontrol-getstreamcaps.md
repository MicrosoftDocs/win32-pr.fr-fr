---
description: La méthode GetStreamCaps récupère les fonctionnalités associées à un index de format donné.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'ITFormatControl :: GetStreamCaps, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533115"
---
# <a name="itformatcontrolgetstreamcaps-method"></a><span data-ttu-id="38d02-103">ITFormatControl :: GetStreamCaps, méthode</span><span class="sxs-lookup"><span data-stu-id="38d02-103">ITFormatControl::GetStreamCaps method</span></span>

<span data-ttu-id="38d02-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="38d02-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="38d02-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="38d02-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="38d02-106">La méthode **GetStreamCaps** récupère les fonctionnalités associées à un index de format donné.</span><span class="sxs-lookup"><span data-stu-id="38d02-106">The **GetStreamCaps** method retrieves the capabilities associated with a given format index.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d02-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38d02-107">Syntax</span></span>


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="38d02-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38d02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d02-109">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38d02-109">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38d02-110">Index du format détecté.</span><span class="sxs-lookup"><span data-stu-id="38d02-110">Index of the format being probed.</span></span>

</dd> <dt>

<span data-ttu-id="38d02-111">*ppMediaType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38d02-111">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38d02-112">Pointeur vers un descripteur de **\_ \_ type de média am** du format terminal.</span><span class="sxs-lookup"><span data-stu-id="38d02-112">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="38d02-113">Pour plus d’informations sur le **\_ \_ type de média am**, consultez la documentation de DirectX.</span><span class="sxs-lookup"><span data-stu-id="38d02-113">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> <dt>

<span data-ttu-id="38d02-114">*pStreamConfigCaps* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38d02-114">*pStreamConfigCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38d02-115">Structure [**d' \_ \_ \_ embouts de configuration de flux TAPI**](tapi-stream-config-caps.md) qui fournit des informations détaillées sur les fonctionnalités de flux.</span><span class="sxs-lookup"><span data-stu-id="38d02-115">A [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure that gives detailed information concerning stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="38d02-116">*pfEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38d02-116">*pfEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38d02-117">Indique si le format associé à l’index actuel est activé.</span><span class="sxs-lookup"><span data-stu-id="38d02-117">Indicates whether the format associated with the current index is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38d02-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38d02-118">Return value</span></span>

<span data-ttu-id="38d02-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="38d02-119">This method can return one of these values.</span></span>



| <span data-ttu-id="38d02-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="38d02-120">Return code</span></span>                                                                                   | <span data-ttu-id="38d02-121">Description</span><span class="sxs-lookup"><span data-stu-id="38d02-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="38d02-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38d02-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="38d02-123">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="38d02-123">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="38d02-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="38d02-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="38d02-125">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="38d02-125">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="38d02-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38d02-126">Requirements</span></span>



| <span data-ttu-id="38d02-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38d02-127">Requirement</span></span> | <span data-ttu-id="38d02-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="38d02-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="38d02-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="38d02-129">TAPI version</span></span><br/> | <span data-ttu-id="38d02-130">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="38d02-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="38d02-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="38d02-131">Header</span></span><br/>       | <dl> <span data-ttu-id="38d02-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="38d02-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="38d02-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38d02-133">Library</span></span><br/>      | <dl> <span data-ttu-id="38d02-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38d02-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="38d02-135">DLL</span><span class="sxs-lookup"><span data-stu-id="38d02-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="38d02-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38d02-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d02-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38d02-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d02-138">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="38d02-138">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="38d02-139">**\_majuscules de la configuration de flux TAPI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38d02-139">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




