---
description: Obtient le nombre spécifié de fournisseurs suivant dans la séquence d’énumération.
ms.assetid: 9ef8d330-6f78-4063-825c-9cf5b4f283cf
title: 'IEnumPStoreProviders :: Next, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f468d29682c4e3767d4d8fe7d59e60976f103484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532806"
---
# <a name="ienumpstoreprovidersnext-method"></a><span data-ttu-id="bcf95-103">IEnumPStoreProviders :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="bcf95-103">IEnumPStoreProviders::Next method</span></span>

<span data-ttu-id="bcf95-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bcf95-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="bcf95-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bcf95-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="bcf95-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="bcf95-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="bcf95-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="bcf95-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="bcf95-108">Obtient le nombre spécifié de fournisseurs suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="bcf95-108">Gets the next specified number of providers in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf95-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcf95-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="bcf95-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcf95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf95-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcf95-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf95-112">Nombre de types de fournisseurs demandés.</span><span class="sxs-lookup"><span data-stu-id="bcf95-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="bcf95-113">*rgelt* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bcf95-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf95-114">Pointeur vers une chaîne dans laquelle retourner le nom du type de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bcf95-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="bcf95-115">*pceltFetched* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bcf95-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf95-116">Pointeur vers le nombre de types de fournisseurs réellement fournis.</span><span class="sxs-lookup"><span data-stu-id="bcf95-116">A pointer to the number of provider types that was actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf95-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcf95-117">Return value</span></span>

<span data-ttu-id="bcf95-118">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bcf95-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf95-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcf95-119">Requirements</span></span>



| <span data-ttu-id="bcf95-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcf95-120">Requirement</span></span> | <span data-ttu-id="bcf95-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcf95-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf95-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcf95-122">Header</span></span><br/> | <dl> <span data-ttu-id="bcf95-123"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf95-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="bcf95-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf95-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="bcf95-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf95-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf95-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcf95-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf95-127">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="bcf95-127">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
