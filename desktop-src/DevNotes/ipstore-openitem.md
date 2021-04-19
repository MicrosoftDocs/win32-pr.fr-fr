---
description: Ouvre un élément pour plusieurs accès.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'IPStore :: OpenItem, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537354"
---
# <a name="ipstoreopenitem-method"></a><span data-ttu-id="6b27b-103">IPStore :: OpenItem, méthode</span><span class="sxs-lookup"><span data-stu-id="6b27b-103">IPStore::OpenItem method</span></span>

<span data-ttu-id="6b27b-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6b27b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6b27b-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6b27b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6b27b-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="6b27b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6b27b-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="6b27b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6b27b-108">Ouvre un élément pour plusieurs accès.</span><span class="sxs-lookup"><span data-stu-id="6b27b-108">Opens an item for multiple accesses.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b27b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b27b-109">Syntax</span></span>


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6b27b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b27b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b27b-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b27b-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b27b-112">Spécifie si le type est local sur l’ordinateur ou s’il est associé uniquement à l’utilisateur en train de créer.</span><span class="sxs-lookup"><span data-stu-id="6b27b-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="6b27b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b27b-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="6b27b-114">Signification</span><span class="sxs-lookup"><span data-stu-id="6b27b-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="6b27b-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="6b27b-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="6b27b-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="6b27b-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="6b27b-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6b27b-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6b27b-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="6b27b-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b27b-119">*pItemType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b27b-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b27b-120">Pointeur vers un GUID qui identifie le type de données de l’élément à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="6b27b-120">A pointer to a GUID that identifies the data type of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="6b27b-121">*pItemSubtype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b27b-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b27b-122">Pointeur vers un GUID qui indique le sous-type d’élément à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="6b27b-122">A pointer to a GUID that indicates the item subtype to open.</span></span>

</dd> <dt>

<span data-ttu-id="6b27b-123">*szItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b27b-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b27b-124">Chaîne qui contient le nom de l’élément à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="6b27b-124">A string that contains the name of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="6b27b-125">*ModeFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b27b-125">*ModeFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b27b-126">Décrit les modes d’accès auxquels appartient un ensemble spécifié de clauses d’accès.</span><span class="sxs-lookup"><span data-stu-id="6b27b-126">Describes the access modes to which a specified set of access clauses pertains.</span></span> <span data-ttu-id="6b27b-127">Pour plus d’informations, consultez [**types Pstore**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="6b27b-127">For more information, see [**PStore Types**](pstore-types.md).</span></span>



| <span data-ttu-id="6b27b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b27b-128">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="6b27b-129">Signification</span><span class="sxs-lookup"><span data-stu-id="6b27b-129">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="6b27b-130"><dt>**Fichier PST \_ LIRE**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="6b27b-130"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="6b27b-131">Mode d’accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="6b27b-131">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="6b27b-132"><dt>**Fichier PST \_ ÉCRIRE**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="6b27b-132"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="6b27b-133">Mode d’accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="6b27b-133">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b27b-134">*pProomptInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b27b-134">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b27b-135">Pointeur vers une structure [**\_ PROMPTINFO PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="6b27b-135">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6b27b-136">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b27b-136">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b27b-137">Réservé : doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="6b27b-137">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b27b-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b27b-138">Return value</span></span>

<span data-ttu-id="6b27b-139">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b27b-139">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="6b27b-140">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="6b27b-140">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b27b-141">Notes</span><span class="sxs-lookup"><span data-stu-id="6b27b-141">Remarks</span></span>

<span data-ttu-id="6b27b-142">L’utilisation de **OpenItem** pour ouvrir un élément dans la base de données de stockage protégée requiert qu’il soit fermé à l’aide de [**IPStore :: CloseItem**](ipstore-closeitem.md) pour empêcher une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="6b27b-142">Using **OpenItem** to open an item in the protected storage database requires that it eventually be closed using [**IPStore::CloseItem**](ipstore-closeitem.md) to prevent a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b27b-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b27b-143">Requirements</span></span>



| <span data-ttu-id="6b27b-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b27b-144">Requirement</span></span> | <span data-ttu-id="6b27b-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b27b-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b27b-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b27b-146">Header</span></span><br/> | <dl> <span data-ttu-id="6b27b-147"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b27b-147"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6b27b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="6b27b-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="6b27b-149"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b27b-149"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b27b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b27b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b27b-151">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="6b27b-151">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="6b27b-152">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="6b27b-152">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
