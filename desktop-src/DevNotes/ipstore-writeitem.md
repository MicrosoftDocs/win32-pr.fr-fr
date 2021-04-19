---
description: Écrit un élément de données dans le stockage protégé.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'IPStore :: WriteItem, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545602"
---
# <a name="ipstorewriteitem-method"></a><span data-ttu-id="940bc-103">IPStore :: WriteItem, méthode</span><span class="sxs-lookup"><span data-stu-id="940bc-103">IPStore::WriteItem method</span></span>

<span data-ttu-id="940bc-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="940bc-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="940bc-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="940bc-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="940bc-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="940bc-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="940bc-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="940bc-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="940bc-108">Écrit un élément de données dans le stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="940bc-108">Writes a data item to protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="940bc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="940bc-109">Syntax</span></span>


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="940bc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="940bc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940bc-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="940bc-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940bc-112">Zone de stockage du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="940bc-112">The provider storage area.</span></span>



| <span data-ttu-id="940bc-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="940bc-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="940bc-114">Signification</span><span class="sxs-lookup"><span data-stu-id="940bc-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="940bc-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="940bc-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="940bc-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="940bc-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="940bc-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="940bc-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="940bc-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="940bc-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="940bc-119">*pItemType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="940bc-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940bc-120">Pointeur vers un **GUID** qui identifie le type de données de l’élément de données en cours d’écriture.</span><span class="sxs-lookup"><span data-stu-id="940bc-120">A pointer to a **GUID** that identifies the data type of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="940bc-121">*pItemSubtype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="940bc-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940bc-122">Pointeur vers un **GUID** qui identifie le sous-type de données de l’élément de données en cours d’écriture.</span><span class="sxs-lookup"><span data-stu-id="940bc-122">A pointer to a **GUID** that identifies the data subtype of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="940bc-123">*szItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="940bc-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940bc-124">Pointeur vers une chaîne qui contient le nom assigné à l’élément de données stocké.</span><span class="sxs-lookup"><span data-stu-id="940bc-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="940bc-125">*cbData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="940bc-125">*cbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="940bc-126">Pointeur vers une **valeur DWORD** qui indique la taille de la mémoire tampon qui contient l’élément de données stockées.</span><span class="sxs-lookup"><span data-stu-id="940bc-126">A pointer to a **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="940bc-127">*ppbData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="940bc-127">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="940bc-128">Pointeur vers une mémoire tampon qui contient l’élément de données en cours d’écriture.</span><span class="sxs-lookup"><span data-stu-id="940bc-128">A pointer to a buffer that contains the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="940bc-129">*pProomptInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="940bc-129">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940bc-130">Pointeur vers une [**structure \_ PROMPTINFO PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="940bc-130">Pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="940bc-131">*dwDefaultConfirmationStyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="940bc-131">*dwDefaultConfirmationStyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940bc-132">Style de confirmation par défaut.</span><span class="sxs-lookup"><span data-stu-id="940bc-132">The default confirmation style.</span></span>



| <span data-ttu-id="940bc-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="940bc-133">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="940bc-134">Signification</span><span class="sxs-lookup"><span data-stu-id="940bc-134">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <span data-ttu-id="940bc-135"><dt>**Fichier PST \_ CF \_ par défaut**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="940bc-135"><dt>**PST\_CF\_DEFAULT**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="940bc-136">Permet à l’utilisateur de choisir le style de confirmation.</span><span class="sxs-lookup"><span data-stu-id="940bc-136">Allows the user to choose the confirmation style.</span></span> <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <span data-ttu-id="940bc-137"><dt>**Fichier PST \_ CF \_ aucun**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="940bc-137"><dt>**PST\_CF\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="940bc-138">Force la création d’un élément silencieux.</span><span class="sxs-lookup"><span data-stu-id="940bc-138">Forces silent item creation.</span></span> <br/>                      |



 

</dd> <dt>

<span data-ttu-id="940bc-139">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="940bc-139">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940bc-140">L’interface utilisateur et les comportements de sécurité pour l’opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="940bc-140">The user interface and security behaviors for the write operation.</span></span>



| <span data-ttu-id="940bc-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="940bc-141">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="940bc-142">Signification</span><span class="sxs-lookup"><span data-stu-id="940bc-142">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <span data-ttu-id="940bc-143"><dt>**Fichier PST \_ AUCUN \_ remplacement**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="940bc-143"><dt>**PST\_NO\_OVERWRITE**</dt> <dt>0x00000002</dt></span></span> </dl>                            | <span data-ttu-id="940bc-144">Spécifie que l’élément doit être créé dans un stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="940bc-144">Specifies that the item be created in protected storage.</span></span> <span data-ttu-id="940bc-145">Le remplacement d’un élément existant n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="940bc-145">Overwriting of an existing item is disallowed.</span></span><br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="940bc-146"><dt>**Fichier PST \_ \_ITEMDATA**</dt> <dt>0x00000004</dt> non restreint</span><span class="sxs-lookup"><span data-stu-id="940bc-146"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="940bc-147">Spécifie que le flux de données n’est pas sécurisé.</span><span class="sxs-lookup"><span data-stu-id="940bc-147">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="940bc-148">Par défaut, les appels d’élément sont sécurisés.</span><span class="sxs-lookup"><span data-stu-id="940bc-148">By default, item calls are secure.</span></span><br/>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940bc-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="940bc-149">Return value</span></span>

<span data-ttu-id="940bc-150">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="940bc-150">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="940bc-151">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="940bc-151">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="940bc-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="940bc-152">Requirements</span></span>



| <span data-ttu-id="940bc-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="940bc-153">Requirement</span></span> | <span data-ttu-id="940bc-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="940bc-154">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="940bc-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="940bc-155">Header</span></span><br/> | <dl> <span data-ttu-id="940bc-156"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="940bc-156"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="940bc-157">DLL</span><span class="sxs-lookup"><span data-stu-id="940bc-157">DLL</span></span><br/>    | <dl> <span data-ttu-id="940bc-158"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="940bc-158"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="940bc-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="940bc-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940bc-160">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="940bc-160">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="940bc-161">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="940bc-161">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
