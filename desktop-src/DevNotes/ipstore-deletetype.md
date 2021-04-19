---
description: Supprime un type spécifié de la base de données de stockage protégée.
ms.assetid: 5e3a08eb-e16b-4d9f-82be-241eb3137d17
title: IPStore ::D méthode eleteType (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7833dd59a10b0194347e906d5c5a4711585dea14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521625"
---
# <a name="ipstoredeletetype-method"></a><span data-ttu-id="fc3b0-103">IPStore ::D méthode eleteType</span><span class="sxs-lookup"><span data-stu-id="fc3b0-103">IPStore::DeleteType method</span></span>

<span data-ttu-id="fc3b0-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="fc3b0-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="fc3b0-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="fc3b0-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="fc3b0-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="fc3b0-108">Supprime un type spécifié de la base de données de stockage protégée.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-108">Deletes a specified type from the protected storage database.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc3b0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc3b0-109">Syntax</span></span>


```C++
HRESULT DeleteType(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fc3b0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc3b0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc3b0-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc3b0-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc3b0-112">Spécifie si le type est local sur l’ordinateur ou s’il est associé uniquement à l’utilisateur en train de créer.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="fc3b0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc3b0-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="fc3b0-114">Signification</span><span class="sxs-lookup"><span data-stu-id="fc3b0-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="fc3b0-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="fc3b0-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="fc3b0-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="fc3b0-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="fc3b0-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="fc3b0-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fc3b0-119">*PTYPE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc3b0-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc3b0-120">Pointeur vers un **GUID** qui identifie le type de données du stockage.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="fc3b0-121">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc3b0-121">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc3b0-122">Réservé : doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-122">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc3b0-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc3b0-123">Return value</span></span>

<span data-ttu-id="fc3b0-124">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fc3b0-124">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="fc3b0-125">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="fc3b0-125">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc3b0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc3b0-126">Requirements</span></span>



| <span data-ttu-id="fc3b0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc3b0-127">Requirement</span></span> | <span data-ttu-id="fc3b0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc3b0-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3b0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc3b0-129">Header</span></span><br/> | <dl> <span data-ttu-id="fc3b0-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc3b0-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="fc3b0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fc3b0-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="fc3b0-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc3b0-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc3b0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc3b0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc3b0-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="fc3b0-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
