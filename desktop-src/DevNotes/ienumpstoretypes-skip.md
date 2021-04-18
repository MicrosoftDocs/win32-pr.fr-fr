---
description: Ignore le nombre spécifié d’éléments dans la séquence d’énumération.
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
ms.openlocfilehash: 511595dd55f66e91ae0f5606f9e047918e7ff0fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533203"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="76cf7-103">IEnumPStoreTypes :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="76cf7-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="76cf7-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76cf7-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="76cf7-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="76cf7-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="76cf7-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="76cf7-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="76cf7-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="76cf7-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="76cf7-108">Ignore le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="76cf7-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="76cf7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76cf7-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="76cf7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76cf7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76cf7-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76cf7-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76cf7-112">Nombre de types de fournisseurs à ignorer.</span><span class="sxs-lookup"><span data-stu-id="76cf7-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76cf7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76cf7-113">Return value</span></span>

<span data-ttu-id="76cf7-114">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76cf7-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="76cf7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76cf7-115">Requirements</span></span>



| <span data-ttu-id="76cf7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76cf7-116">Requirement</span></span> | <span data-ttu-id="76cf7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="76cf7-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76cf7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="76cf7-118">Header</span></span><br/> | <dl> <span data-ttu-id="76cf7-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="76cf7-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="76cf7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="76cf7-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="76cf7-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76cf7-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76cf7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76cf7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76cf7-123">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="76cf7-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
