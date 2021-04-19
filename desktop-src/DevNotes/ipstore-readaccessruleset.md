---
description: Lit les règles d’accès pour un type donné.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'IPStore :: ReadAccessRuleSet, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533387"
---
# <a name="ipstorereadaccessruleset-method"></a><span data-ttu-id="59c8a-103">IPStore :: ReadAccessRuleSet, méthode</span><span class="sxs-lookup"><span data-stu-id="59c8a-103">IPStore::ReadAccessRuleSet method</span></span>

<span data-ttu-id="59c8a-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="59c8a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="59c8a-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="59c8a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="59c8a-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="59c8a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="59c8a-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="59c8a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="59c8a-108">\[Cette méthode n’est pas implémentée.\]</span><span class="sxs-lookup"><span data-stu-id="59c8a-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="59c8a-109">Lit les règles d’accès pour un type donné.</span><span class="sxs-lookup"><span data-stu-id="59c8a-109">Reads the access rules for a given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c8a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59c8a-110">Syntax</span></span>


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="59c8a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59c8a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c8a-112">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c8a-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8a-113">Réservé.</span><span class="sxs-lookup"><span data-stu-id="59c8a-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="59c8a-114">*PTYPE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c8a-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8a-115">Réservé.</span><span class="sxs-lookup"><span data-stu-id="59c8a-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="59c8a-116">*pSubtype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c8a-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8a-117">Réservé.</span><span class="sxs-lookup"><span data-stu-id="59c8a-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="59c8a-118">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c8a-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8a-119">Réservé.</span><span class="sxs-lookup"><span data-stu-id="59c8a-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="59c8a-120">*ppRules* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c8a-120">*ppRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8a-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="59c8a-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="59c8a-122">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c8a-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c8a-123">Réservé.</span><span class="sxs-lookup"><span data-stu-id="59c8a-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59c8a-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59c8a-124">Return value</span></span>

<span data-ttu-id="59c8a-125">Les appels à cette méthode échouent toujours.</span><span class="sxs-lookup"><span data-stu-id="59c8a-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c8a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59c8a-126">Requirements</span></span>



| <span data-ttu-id="59c8a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59c8a-127">Requirement</span></span> | <span data-ttu-id="59c8a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c8a-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59c8a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="59c8a-129">Header</span></span><br/> | <dl> <span data-ttu-id="59c8a-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c8a-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="59c8a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="59c8a-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="59c8a-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59c8a-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c8a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c8a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c8a-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="59c8a-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
