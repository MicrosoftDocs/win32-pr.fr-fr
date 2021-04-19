---
description: Ignore le nombre spécifié d’éléments spécifiés dans la séquence d’énumération donnée.
ms.assetid: 1459c18a-ccff-451f-8904-32858cc72b78
title: 'IEnumPStoreItems :: Skip, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 912dea836ec5ac04ddaf54de9f7f7b609e4e23ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545649"
---
# <a name="ienumpstoreitemsskip-method"></a><span data-ttu-id="3f391-103">IEnumPStoreItems :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="3f391-103">IEnumPStoreItems::Skip method</span></span>

<span data-ttu-id="3f391-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f391-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="3f391-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3f391-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="3f391-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="3f391-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="3f391-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="3f391-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="3f391-108">Ignore le nombre spécifié d’éléments spécifiés dans la séquence d’énumération donnée.</span><span class="sxs-lookup"><span data-stu-id="3f391-108">Skips over the next specified number of items in the given enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f391-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f391-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="3f391-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f391-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f391-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f391-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f391-112">Nombre d’éléments de données à ignorer.</span><span class="sxs-lookup"><span data-stu-id="3f391-112">The number of data items to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f391-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f391-113">Return value</span></span>

<span data-ttu-id="3f391-114">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f391-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f391-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f391-115">Requirements</span></span>



| <span data-ttu-id="3f391-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f391-116">Requirement</span></span> | <span data-ttu-id="3f391-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f391-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f391-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f391-118">Header</span></span><br/> | <dl> <span data-ttu-id="3f391-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f391-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="3f391-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3f391-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="3f391-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f391-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f391-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f391-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f391-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="3f391-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
