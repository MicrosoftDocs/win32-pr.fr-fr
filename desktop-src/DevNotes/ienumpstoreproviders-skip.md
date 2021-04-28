---
description: 'IEnumPStoreProviders :: Skip, méthode-ignore le nombre spécifié d’éléments dans la séquence d’énumération.'
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: 'IEnumPStoreProviders :: Skip, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2f74c44de172d9235d9768b8f484405b5e8fb7fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096747"
---
# <a name="ienumpstoreprovidersskip-method"></a><span data-ttu-id="3b288-103">IEnumPStoreProviders :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="3b288-103">IEnumPStoreProviders::Skip method</span></span>

<span data-ttu-id="3b288-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b288-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="3b288-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3b288-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="3b288-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="3b288-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="3b288-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="3b288-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="3b288-108">Ignore le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="3b288-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b288-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b288-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="3b288-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b288-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b288-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b288-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b288-112">Nombre de types de fournisseurs à ignorer.</span><span class="sxs-lookup"><span data-stu-id="3b288-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b288-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3b288-113">Return value</span></span>

<span data-ttu-id="3b288-114">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b288-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b288-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b288-115">Requirements</span></span>



| <span data-ttu-id="3b288-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b288-116">Requirement</span></span> | <span data-ttu-id="3b288-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b288-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b288-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b288-118">Header</span></span><br/> | <dl> <span data-ttu-id="3b288-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b288-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="3b288-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3b288-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="3b288-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b288-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b288-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b288-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b288-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="3b288-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
