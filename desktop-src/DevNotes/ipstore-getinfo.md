---
description: Retourne des informations sur le fournisseur de stockage.
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: 'IPStore :: GetInfo, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7747c3acf15a60f5556a8855ef4825715ef5050b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525933"
---
# <a name="ipstoregetinfo-method"></a><span data-ttu-id="d5142-103">IPStore :: GetInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="d5142-103">IPStore::GetInfo method</span></span>

<span data-ttu-id="d5142-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d5142-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d5142-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d5142-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d5142-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="d5142-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d5142-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d5142-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d5142-108">Retourne des informations sur le fournisseur de stockage.</span><span class="sxs-lookup"><span data-stu-id="d5142-108">Returns information on the storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5142-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5142-109">Syntax</span></span>


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="d5142-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5142-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5142-111">*ppProperties* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5142-111">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5142-112">Pointeur vers une structure **PPST \_ providerinfo retourné par** qui contient des informations sur le fournisseur de stockage.</span><span class="sxs-lookup"><span data-stu-id="d5142-112">A pointer to a **PPST\_PROVIDERINFO** structure that contains information about the storage provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5142-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5142-113">Return value</span></span>

<span data-ttu-id="d5142-114">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5142-114">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="d5142-115">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="d5142-115">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5142-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5142-116">Requirements</span></span>



| <span data-ttu-id="d5142-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5142-117">Requirement</span></span> | <span data-ttu-id="d5142-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5142-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5142-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5142-119">Header</span></span><br/> | <dl> <span data-ttu-id="d5142-120"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5142-120"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d5142-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d5142-121">DLL</span></span><br/>    | <dl> <span data-ttu-id="d5142-122"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5142-122"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5142-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5142-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5142-124">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="d5142-124">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
