---
description: Crée le sous-type spécifié dans le type spécifié.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'IPStore :: CreateSubtype, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520811"
---
# <a name="ipstorecreatesubtype-method"></a><span data-ttu-id="ec67f-103">IPStore :: CreateSubtype, méthode</span><span class="sxs-lookup"><span data-stu-id="ec67f-103">IPStore::CreateSubtype method</span></span>

<span data-ttu-id="ec67f-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ec67f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ec67f-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ec67f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ec67f-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="ec67f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ec67f-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ec67f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ec67f-108">Crée le sous-type spécifié dans le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec67f-108">Creates the specified subtype within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec67f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec67f-109">Syntax</span></span>


```C++
HRESULT CreateSubtype(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ec67f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec67f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec67f-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec67f-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec67f-112">Spécifie la zone de stockage du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ec67f-112">Specifies the provider storage area.</span></span>



| <span data-ttu-id="ec67f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec67f-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="ec67f-114">Signification</span><span class="sxs-lookup"><span data-stu-id="ec67f-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="ec67f-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="ec67f-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="ec67f-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="ec67f-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="ec67f-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ec67f-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ec67f-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="ec67f-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ec67f-119">*PTYPE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec67f-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec67f-120">Pointeur vers un **GUID** qui identifie le type de données du stockage.</span><span class="sxs-lookup"><span data-stu-id="ec67f-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="ec67f-121">*pSubtype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec67f-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec67f-122">Pointeur vers un **GUID** qui identifie le sous-type de données du stockage.</span><span class="sxs-lookup"><span data-stu-id="ec67f-122">A pointer to a **GUID** that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="ec67f-123">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec67f-123">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec67f-124">Pointeur vers une structure [**\_ TypeInfo PST**](pst-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ec67f-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ec67f-125">*pRules* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec67f-125">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec67f-126">Pointeur vers une structure [**\_ ACCESSRULESET PST**](pst-accessruleset.md) .</span><span class="sxs-lookup"><span data-stu-id="ec67f-126">A pointer to a [**PST\_ACCESSRULESET**](pst-accessruleset.md) structure.</span></span>

<span data-ttu-id="ec67f-127">**Windows XP :** Ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ec67f-127">**Windows XP:** This parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="ec67f-128">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec67f-128">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec67f-129">Réservé doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="ec67f-129">Reserved; must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec67f-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec67f-130">Return value</span></span>

<span data-ttu-id="ec67f-131">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ec67f-131">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="ec67f-132">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="ec67f-132">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec67f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec67f-133">Requirements</span></span>



| <span data-ttu-id="ec67f-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec67f-134">Requirement</span></span> | <span data-ttu-id="ec67f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec67f-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec67f-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec67f-136">Header</span></span><br/> | <dl> <span data-ttu-id="ec67f-137"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec67f-137"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ec67f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ec67f-138">DLL</span></span><br/>    | <dl> <span data-ttu-id="ec67f-139"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec67f-139"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec67f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec67f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec67f-141">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="ec67f-141">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="ec67f-142">**\_ACCESSRULESET PST**</span><span class="sxs-lookup"><span data-stu-id="ec67f-142">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> <dt>

[<span data-ttu-id="ec67f-143">**\_TypeInfo PST**</span><span class="sxs-lookup"><span data-stu-id="ec67f-143">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
