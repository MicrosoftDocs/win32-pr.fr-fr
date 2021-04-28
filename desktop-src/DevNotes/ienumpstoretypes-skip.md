---
description: 'IEnumPStoreTypes :: Skip, méthode-ignore le nombre spécifié d’éléments dans la séquence d’énumération.'
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: 'IEnumPStoreTypes :: Skip, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdc656af2a8f50d02d2f88545d189d9c9285a7f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096737"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="ef26a-103">IEnumPStoreTypes :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="ef26a-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="ef26a-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ef26a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ef26a-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ef26a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ef26a-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="ef26a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ef26a-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ef26a-108">Ignore le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="ef26a-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef26a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef26a-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="ef26a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef26a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef26a-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef26a-112">Nombre de types de fournisseurs à ignorer.</span><span class="sxs-lookup"><span data-stu-id="ef26a-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef26a-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ef26a-113">Return value</span></span>

<span data-ttu-id="ef26a-114">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef26a-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef26a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef26a-115">Requirements</span></span>



| <span data-ttu-id="ef26a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef26a-116">Requirement</span></span> | <span data-ttu-id="ef26a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef26a-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef26a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef26a-118">Header</span></span><br/> | <dl> <span data-ttu-id="ef26a-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ef26a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ef26a-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="ef26a-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef26a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef26a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef26a-123">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="ef26a-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
