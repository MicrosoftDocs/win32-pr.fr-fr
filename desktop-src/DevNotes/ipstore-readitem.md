---
description: Lit l’élément de données spécifié à partir du stockage protégé.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'IPStore :: ReadItem, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521693"
---
# <a name="ipstorereaditem-method"></a><span data-ttu-id="550ba-103">IPStore :: ReadItem, méthode</span><span class="sxs-lookup"><span data-stu-id="550ba-103">IPStore::ReadItem method</span></span>

<span data-ttu-id="550ba-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="550ba-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="550ba-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="550ba-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="550ba-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="550ba-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="550ba-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="550ba-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="550ba-108">Lit l’élément de données spécifié à partir du stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="550ba-108">Reads the specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="550ba-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="550ba-109">Syntax</span></span>


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="550ba-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="550ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="550ba-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="550ba-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550ba-112">Zone de stockage du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="550ba-112">The provider storage area.</span></span>



| <span data-ttu-id="550ba-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="550ba-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="550ba-114">Signification</span><span class="sxs-lookup"><span data-stu-id="550ba-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="550ba-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="550ba-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="550ba-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="550ba-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="550ba-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="550ba-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="550ba-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="550ba-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="550ba-119">*pItemType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="550ba-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550ba-120">Pointeur vers un GUID qui identifie le type de données de l’élément à lire.</span><span class="sxs-lookup"><span data-stu-id="550ba-120">A pointer to a GUID that identifies the data type of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="550ba-121">*pItemSubtype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="550ba-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550ba-122">Pointeur vers un GUID qui identifie le sous-type de données de l’élément à lire.</span><span class="sxs-lookup"><span data-stu-id="550ba-122">A pointer to a GUID that identifies the data subtype of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="550ba-123">*szItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="550ba-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550ba-124">Pointeur vers une chaîne qui contient le nom assigné à l’élément de données stocké.</span><span class="sxs-lookup"><span data-stu-id="550ba-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="550ba-125">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="550ba-125">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550ba-126">**Valeur DWORD** qui indique la taille de la mémoire tampon qui contient l’élément de données stockées.</span><span class="sxs-lookup"><span data-stu-id="550ba-126">A **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="550ba-127">*pbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="550ba-127">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550ba-128">Pointeur vers une mémoire tampon qui contient l’élément de données stockées.</span><span class="sxs-lookup"><span data-stu-id="550ba-128">A pointer to a buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="550ba-129">*pPromptInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="550ba-129">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550ba-130">Pointeur vers une structure [**\_ PROMPTINFO PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="550ba-130">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="550ba-131">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="550ba-131">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550ba-132">Spécifie l’interface utilisateur et les comportements de sécurité pour l’opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="550ba-132">Specifies user interface and security behaviors for the read operation.</span></span>

<span data-ttu-id="550ba-133">Les valeurs d’indicateur peuvent être combinées avec un opérateur logique OR.</span><span class="sxs-lookup"><span data-stu-id="550ba-133">The flag values can be combined with a logical OR.</span></span>



| <span data-ttu-id="550ba-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="550ba-134">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="550ba-135">Signification</span><span class="sxs-lookup"><span data-stu-id="550ba-135">Meaning</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="550ba-136"><dt>**Fichier PST \_ \_ITEMDATA**</dt> <dt>0x00000004</dt> non restreint</span><span class="sxs-lookup"><span data-stu-id="550ba-136"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="550ba-137">Spécifie que le flux de données n’est pas sécurisé.</span><span class="sxs-lookup"><span data-stu-id="550ba-137">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="550ba-138">Par défaut, les appels d’élément sont sécurisés.</span><span class="sxs-lookup"><span data-stu-id="550ba-138">By default, item calls are secure.</span></span><br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <span data-ttu-id="550ba-139"><dt>**Fichier PST \_ INVITE de \_ requête**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="550ba-139"><dt>**PST\_PROMPT\_QUERY**</dt> <dt>0x00000008</dt></span></span> </dl>                            | <span data-ttu-id="550ba-140">Spécifie que la confirmation doit être retournée en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="550ba-140">Specifies that the confirmation be returned upon success.</span></span> <span data-ttu-id="550ba-141">Si l’interface utilisateur est activée, la réussite du **fichier PST \_ E \_ OK** est retournée.</span><span class="sxs-lookup"><span data-stu-id="550ba-141">If the user interface is enabled, a success of **PST\_E\_OK** is returned.</span></span> <span data-ttu-id="550ba-142">Si l’interface utilisateur n’est pas activée, la valeur de l' **\_ \_ élément \_ PST E** est retournée.</span><span class="sxs-lookup"><span data-stu-id="550ba-142">If the user interface is not enabled, a value of **PST\_E\_ITEM\_EXISTS** is returned.</span></span><br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="550ba-143"><dt>**Fichier PST \_ AUCUNE \_ \_ migration de l’interface utilisateur**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="550ba-143"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl>                  | <span data-ttu-id="550ba-144">N’affiche pas l’interface utilisateur, sauf si un mot de passe personnalisé est requis.</span><span class="sxs-lookup"><span data-stu-id="550ba-144">Do not show user interface unless a custom password is required.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="550ba-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="550ba-145">Return value</span></span>

<span data-ttu-id="550ba-146">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="550ba-146">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="550ba-147">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="550ba-147">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="550ba-148">Notes</span><span class="sxs-lookup"><span data-stu-id="550ba-148">Remarks</span></span>

<span data-ttu-id="550ba-149">Si **ReadItem** se termine correctement, l’application est chargée de libérer la mémoire tampon de données retournée à l’aide de la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .</span><span class="sxs-lookup"><span data-stu-id="550ba-149">If **ReadItem** completes successfully, the application is responsible for freeing the returned data buffer using the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="550ba-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="550ba-150">Requirements</span></span>



| <span data-ttu-id="550ba-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="550ba-151">Requirement</span></span> | <span data-ttu-id="550ba-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="550ba-152">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="550ba-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="550ba-153">Header</span></span><br/> | <dl> <span data-ttu-id="550ba-154"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="550ba-154"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="550ba-155">DLL</span><span class="sxs-lookup"><span data-stu-id="550ba-155">DLL</span></span><br/>    | <dl> <span data-ttu-id="550ba-156"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="550ba-156"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="550ba-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="550ba-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550ba-158">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="550ba-158">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="550ba-159">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="550ba-159">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
