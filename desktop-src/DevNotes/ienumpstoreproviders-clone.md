---
description: Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: 'IEnumPStoreProviders :: Clone, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdd7825a44dcea672eff24a15126921f0426a986
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530971"
---
# <a name="ienumpstoreprovidersclone-method"></a><span data-ttu-id="39019-103">IEnumPStoreProviders :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="39019-103">IEnumPStoreProviders::Clone method</span></span>

<span data-ttu-id="39019-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="39019-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="39019-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="39019-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="39019-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="39019-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="39019-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="39019-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="39019-108">Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="39019-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="39019-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39019-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="39019-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39019-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39019-111">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="39019-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39019-112">Pointeur vers un pointeur [**IEnumPStoreProviders**](ienumpstoreproviders.md) .</span><span class="sxs-lookup"><span data-stu-id="39019-112">A pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39019-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39019-113">Return value</span></span>

<span data-ttu-id="39019-114">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39019-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="39019-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39019-115">Requirements</span></span>



| <span data-ttu-id="39019-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39019-116">Requirement</span></span> | <span data-ttu-id="39019-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="39019-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39019-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="39019-118">Header</span></span><br/> | <dl> <span data-ttu-id="39019-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="39019-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="39019-120">DLL</span><span class="sxs-lookup"><span data-stu-id="39019-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="39019-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39019-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39019-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39019-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39019-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="39019-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
