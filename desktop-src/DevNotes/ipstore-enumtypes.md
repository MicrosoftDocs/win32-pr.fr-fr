---
description: Retourne une interface pour l’énumération des types actuellement enregistrés dans la base de données protégée.
ms.assetid: 0c0c2ad7-90b0-4fc0-8972-82eb159653be
title: 'IPStore :: EnumTypes, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 73166a9fc1d76ae9f67528636eda567b9fa190a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525934"
---
# <a name="ipstoreenumtypes-method"></a><span data-ttu-id="28e67-103">IPStore :: EnumTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="28e67-103">IPStore::EnumTypes method</span></span>

<span data-ttu-id="28e67-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="28e67-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="28e67-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="28e67-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="28e67-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="28e67-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="28e67-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="28e67-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="28e67-108">Retourne une interface pour l’énumération des types actuellement enregistrés dans la base de données protégée.</span><span class="sxs-lookup"><span data-stu-id="28e67-108">Returns an interface for enumerating types that are currently registered in the protected database.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e67-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28e67-109">Syntax</span></span>


```C++
HRESULT EnumTypes(
  [in] PST_KEY          Key,
  [in] DWORD            dwFlags,
  [in] IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="28e67-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28e67-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e67-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28e67-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e67-112">Spécifie si le type est local sur l’ordinateur ou s’il est associé uniquement à l’utilisateur en train de créer.</span><span class="sxs-lookup"><span data-stu-id="28e67-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="28e67-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="28e67-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="28e67-114">Signification</span><span class="sxs-lookup"><span data-stu-id="28e67-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="28e67-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="28e67-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="28e67-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="28e67-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="28e67-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="28e67-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="28e67-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="28e67-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="28e67-119">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28e67-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e67-120">Réservé : doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="28e67-120">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="28e67-121">*ppEnum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28e67-121">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e67-122">Pointeur vers une interface [**IEnumPStoreTypes**](ienumpstoretypes.md) utilisée pour effectuer les tâches d’énumération.</span><span class="sxs-lookup"><span data-stu-id="28e67-122">A pointer to an [**IEnumPStoreTypes**](ienumpstoretypes.md) interface that is used to perform the enumeration tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e67-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28e67-123">Return value</span></span>

<span data-ttu-id="28e67-124">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28e67-124">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="28e67-125">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="28e67-125">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e67-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28e67-126">Requirements</span></span>



| <span data-ttu-id="28e67-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28e67-127">Requirement</span></span> | <span data-ttu-id="28e67-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="28e67-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28e67-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="28e67-129">Header</span></span><br/> | <dl> <span data-ttu-id="28e67-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="28e67-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="28e67-131">DLL</span><span class="sxs-lookup"><span data-stu-id="28e67-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="28e67-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28e67-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e67-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28e67-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e67-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="28e67-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
