---
description: Crée un énumérateur supplémentaire qui contient le même état d’énumération que l’énumérateur actuel.
ms.assetid: b4027520-62cc-40d4-b9fd-01fa9c652a54
title: 'IEnumPStoreTypes :: Clone, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4ac088ae708b62f458d7bba52127dadc8ef77c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543307"
---
# <a name="ienumpstoretypesclone-method"></a><span data-ttu-id="c5d94-103">IEnumPStoreTypes :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="c5d94-103">IEnumPStoreTypes::Clone method</span></span>

<span data-ttu-id="c5d94-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5d94-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="c5d94-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c5d94-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="c5d94-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="c5d94-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="c5d94-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="c5d94-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="c5d94-108">Crée un énumérateur supplémentaire qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c5d94-108">Creates an additional enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d94-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5d94-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="c5d94-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5d94-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d94-111">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c5d94-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d94-112">Pointeur vers un pointeur [**IEnumPStoreItems**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="c5d94-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d94-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5d94-113">Return value</span></span>

<span data-ttu-id="c5d94-114">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5d94-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d94-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5d94-115">Requirements</span></span>



| <span data-ttu-id="c5d94-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5d94-116">Requirement</span></span> | <span data-ttu-id="c5d94-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d94-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d94-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5d94-118">Header</span></span><br/> | <dl> <span data-ttu-id="c5d94-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d94-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="c5d94-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c5d94-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="c5d94-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5d94-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d94-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5d94-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d94-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="c5d94-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> <dt>

[<span data-ttu-id="c5d94-124">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="c5d94-124">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
