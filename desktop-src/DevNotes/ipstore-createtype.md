---
description: Crée le type spécifié avec le nom spécifié.
ms.assetid: eb85477c-d750-46d2-8b32-450f672e7601
title: 'IPStore :: CreateType, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7a8c855fd5b50adf41986ef27a1bd296894b12bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537361"
---
# <a name="ipstorecreatetype-method"></a><span data-ttu-id="441fc-103">IPStore :: CreateType, méthode</span><span class="sxs-lookup"><span data-stu-id="441fc-103">IPStore::CreateType method</span></span>

<span data-ttu-id="441fc-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="441fc-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="441fc-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="441fc-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="441fc-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="441fc-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="441fc-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="441fc-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="441fc-108">Crée le type spécifié avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="441fc-108">Creates the specified type with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="441fc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="441fc-109">Syntax</span></span>


```C++
HRESULT CreateType(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO pInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="441fc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="441fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="441fc-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="441fc-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441fc-112">Spécifie si le type est local sur l’ordinateur ou s’il est associé uniquement à l’utilisateur en train de créer.</span><span class="sxs-lookup"><span data-stu-id="441fc-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="441fc-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="441fc-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="441fc-114">Signification</span><span class="sxs-lookup"><span data-stu-id="441fc-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="441fc-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="441fc-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="441fc-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="441fc-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="441fc-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="441fc-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="441fc-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="441fc-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="441fc-119">*PTYPE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="441fc-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441fc-120">Pointeur vers un **GUID** qui identifie le type de données du stockage.</span><span class="sxs-lookup"><span data-stu-id="441fc-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="441fc-121">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="441fc-121">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441fc-122">Pointeur vers une structure [**\_ TypeInfo PST**](pst-typeinfo.md) qui contient le nom du type de données.</span><span class="sxs-lookup"><span data-stu-id="441fc-122">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure that contains the name of the data type.</span></span>

</dd> <dt>

<span data-ttu-id="441fc-123">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="441fc-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441fc-124">Réservé : doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="441fc-124">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="441fc-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="441fc-125">Return value</span></span>

<span data-ttu-id="441fc-126">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="441fc-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="441fc-127">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="441fc-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="441fc-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="441fc-128">Requirements</span></span>



| <span data-ttu-id="441fc-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="441fc-129">Requirement</span></span> | <span data-ttu-id="441fc-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="441fc-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="441fc-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="441fc-131">Header</span></span><br/> | <dl> <span data-ttu-id="441fc-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="441fc-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="441fc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="441fc-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="441fc-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="441fc-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="441fc-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="441fc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="441fc-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="441fc-136">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="441fc-137">**\_TypeInfo PST**</span><span class="sxs-lookup"><span data-stu-id="441fc-137">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
