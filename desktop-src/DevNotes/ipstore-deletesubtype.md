---
description: Supprime un sous-type spécifié dans le type spécifié.
ms.assetid: 1c44a609-80af-4e28-b1b5-2b4faea143bd
title: IPStore ::D méthode eleteSubtype (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 6fd89c1dd00a71cb843596e08bc168b90008b180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542702"
---
# <a name="ipstoredeletesubtype-method"></a><span data-ttu-id="ed273-103">IPStore ::D méthode eleteSubtype</span><span class="sxs-lookup"><span data-stu-id="ed273-103">IPStore::DeleteSubtype method</span></span>

<span data-ttu-id="ed273-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed273-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ed273-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ed273-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ed273-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="ed273-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ed273-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ed273-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ed273-108">Supprime un sous-type spécifié dans le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed273-108">Deletes a specified subtype from within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed273-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed273-109">Syntax</span></span>


```C++
HRESULT DeleteSubtype(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in] const GUID    *pSubtype,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ed273-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed273-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed273-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed273-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed273-112">Spécifie si le type est local sur l’ordinateur ou s’il est associé uniquement à l’utilisateur en train de créer.</span><span class="sxs-lookup"><span data-stu-id="ed273-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="ed273-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed273-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="ed273-114">Signification</span><span class="sxs-lookup"><span data-stu-id="ed273-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="ed273-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="ed273-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="ed273-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="ed273-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="ed273-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ed273-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ed273-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="ed273-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ed273-119">*PTYPE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed273-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed273-120">Pointeur vers un GUID qui identifie le type de données du stockage.</span><span class="sxs-lookup"><span data-stu-id="ed273-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="ed273-121">*pSubtype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed273-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed273-122">Pointeur vers un GUID qui identifie le sous-type de données du stockage.</span><span class="sxs-lookup"><span data-stu-id="ed273-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="ed273-123">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed273-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed273-124">Réservé : doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="ed273-124">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed273-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed273-125">Return value</span></span>

<span data-ttu-id="ed273-126">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ed273-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="ed273-127">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="ed273-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed273-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed273-128">Requirements</span></span>



| <span data-ttu-id="ed273-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed273-129">Requirement</span></span> | <span data-ttu-id="ed273-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed273-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed273-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed273-131">Header</span></span><br/> | <dl> <span data-ttu-id="ed273-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed273-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ed273-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ed273-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="ed273-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed273-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed273-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed273-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed273-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="ed273-136">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
