---
description: Obtient le nombre spécifié de noms d’éléments de données suivant dans la séquence d’énumération.
ms.assetid: 6f30bf64-bd63-43d7-ab7e-f64e372c723b
title: 'IEnumPStoreItems :: Next, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 967f2f84553b87965d5b2c92d99e347cb259264b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526632"
---
# <a name="ienumpstoreitemsnext-method"></a><span data-ttu-id="65a40-103">IEnumPStoreItems :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="65a40-103">IEnumPStoreItems::Next method</span></span>

<span data-ttu-id="65a40-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="65a40-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="65a40-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="65a40-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="65a40-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="65a40-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="65a40-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="65a40-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="65a40-108">Obtient le nombre spécifié de noms d’éléments de données suivant dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="65a40-108">Gets the next specified number of data item names in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a40-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65a40-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="65a40-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65a40-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a40-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65a40-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a40-112">Nombre d’éléments de données demandés.</span><span class="sxs-lookup"><span data-stu-id="65a40-112">The number of data items requested.</span></span>

</dd> <dt>

<span data-ttu-id="65a40-113">*rgelt* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65a40-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65a40-114">Pointeur vers une chaîne dans laquelle retourner le nom de l’élément de données.</span><span class="sxs-lookup"><span data-stu-id="65a40-114">A pointer to a string in which to return the data item name.</span></span>

</dd> <dt>

<span data-ttu-id="65a40-115">*pceltFetched* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="65a40-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="65a40-116">Pointeur vers le nombre de noms d’éléments de données réellement fournis.</span><span class="sxs-lookup"><span data-stu-id="65a40-116">A pointer to the number of data item names actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a40-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65a40-117">Return value</span></span>

<span data-ttu-id="65a40-118">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65a40-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="65a40-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65a40-119">Requirements</span></span>



| <span data-ttu-id="65a40-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65a40-120">Requirement</span></span> | <span data-ttu-id="65a40-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="65a40-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65a40-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="65a40-122">Header</span></span><br/> | <dl> <span data-ttu-id="65a40-123"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="65a40-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="65a40-124">DLL</span><span class="sxs-lookup"><span data-stu-id="65a40-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="65a40-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65a40-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65a40-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65a40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a40-127">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="65a40-127">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
