---
description: Destiné à définir les informations de paramètre spécifiées.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'IPStore :: GetProvParam, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540172"
---
# <a name="ipstoregetprovparam-method"></a><span data-ttu-id="aa007-103">IPStore :: GetProvParam, méthode</span><span class="sxs-lookup"><span data-stu-id="aa007-103">IPStore::GetProvParam method</span></span>

<span data-ttu-id="aa007-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aa007-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="aa007-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="aa007-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="aa007-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="aa007-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="aa007-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="aa007-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="aa007-108">\[Cette méthode n’est pas implémentée.\]</span><span class="sxs-lookup"><span data-stu-id="aa007-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="aa007-109">Destiné à définir les informations de paramètre spécifiées.</span><span class="sxs-lookup"><span data-stu-id="aa007-109">Intended to set the specified parameter information.</span></span> <span data-ttu-id="aa007-110">Notez, toutefois, qu’elle n’est pas implémentée et échouera toujours.</span><span class="sxs-lookup"><span data-stu-id="aa007-110">Note, however, that it is not implemented and will always fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa007-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa007-111">Syntax</span></span>


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="aa007-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa007-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa007-113">*dwParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aa007-113">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa007-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="aa007-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="aa007-115">*pcbData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="aa007-115">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa007-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="aa007-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="aa007-117">*ppbData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="aa007-117">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa007-118">Réservé.</span><span class="sxs-lookup"><span data-stu-id="aa007-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="aa007-119">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aa007-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa007-120">Réservé.</span><span class="sxs-lookup"><span data-stu-id="aa007-120">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa007-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa007-121">Return value</span></span>

<span data-ttu-id="aa007-122">Les appels à cette méthode échouent toujours.</span><span class="sxs-lookup"><span data-stu-id="aa007-122">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa007-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa007-123">Requirements</span></span>



| <span data-ttu-id="aa007-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa007-124">Requirement</span></span> | <span data-ttu-id="aa007-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa007-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa007-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa007-126">Header</span></span><br/> | <dl> <span data-ttu-id="aa007-127"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa007-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="aa007-128">DLL</span><span class="sxs-lookup"><span data-stu-id="aa007-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="aa007-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa007-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa007-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa007-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa007-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="aa007-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
