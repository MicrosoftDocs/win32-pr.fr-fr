---
description: Écrit les règles d’accès pour le type donné.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: 'IPStore :: WriteAccessRuleset, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7399ff800087720d65cb45e80ccab080a7df9baf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538008"
---
# <a name="ipstorewriteaccessruleset-method"></a><span data-ttu-id="e7a47-103">IPStore :: WriteAccessRuleset, méthode</span><span class="sxs-lookup"><span data-stu-id="e7a47-103">IPStore::WriteAccessRuleset method</span></span>

<span data-ttu-id="e7a47-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e7a47-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="e7a47-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e7a47-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="e7a47-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="e7a47-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="e7a47-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="e7a47-108">\[Cette méthode n’est pas implémentée.\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="e7a47-109">Écrit les règles d’accès pour le type donné.</span><span class="sxs-lookup"><span data-stu-id="e7a47-109">Writes the access rules for the given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a47-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7a47-110">Syntax</span></span>


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e7a47-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7a47-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7a47-112">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a47-113">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e7a47-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e7a47-114">*PTYPE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a47-115">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e7a47-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e7a47-116">*pSubtype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a47-117">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e7a47-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e7a47-118">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a47-119">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e7a47-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e7a47-120">*pRules* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-120">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a47-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e7a47-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e7a47-122">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a47-123">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e7a47-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7a47-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7a47-124">Return value</span></span>

<span data-ttu-id="e7a47-125">Les appels à cette méthode échouent toujours.</span><span class="sxs-lookup"><span data-stu-id="e7a47-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a47-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7a47-126">Requirements</span></span>



| <span data-ttu-id="e7a47-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7a47-127">Requirement</span></span> | <span data-ttu-id="e7a47-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7a47-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a47-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7a47-129">Header</span></span><br/> | <dl> <span data-ttu-id="e7a47-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7a47-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="e7a47-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e7a47-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="e7a47-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7a47-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7a47-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7a47-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a47-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="e7a47-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
