---
description: Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: 'IEnumPStoreItems :: Clone, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 919c0359f5c7f6d3ab547f53a105246c43e20fb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544354"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="febbf-103">IEnumPStoreItems :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="febbf-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="febbf-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="febbf-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="febbf-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="febbf-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="febbf-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="febbf-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="febbf-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="febbf-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="febbf-108">Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.</span><span class="sxs-lookup"><span data-stu-id="febbf-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="febbf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="febbf-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="febbf-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="febbf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="febbf-111">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="febbf-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="febbf-112">Pointeur vers un pointeur [**IEnumPStoreItems**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="febbf-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="febbf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="febbf-113">Return value</span></span>

<span data-ttu-id="febbf-114">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="febbf-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="febbf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="febbf-115">Requirements</span></span>



| <span data-ttu-id="febbf-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="febbf-116">Requirement</span></span> | <span data-ttu-id="febbf-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="febbf-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="febbf-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="febbf-118">Header</span></span><br/> | <dl> <span data-ttu-id="febbf-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="febbf-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="febbf-120">DLL</span><span class="sxs-lookup"><span data-stu-id="febbf-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="febbf-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="febbf-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="febbf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="febbf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="febbf-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="febbf-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
