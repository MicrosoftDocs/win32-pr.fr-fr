---
description: Ferme un élément de données spécifié à partir du stockage protégé.
ms.assetid: 74919354-5e31-4ab5-9326-9f9aae206bd7
title: 'IPStore :: CloseItem, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CloseItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e5f550df0ffa4dd2f35a91e768d70bb0359b9a4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545469"
---
# <a name="ipstorecloseitem-method"></a><span data-ttu-id="50341-103">IPStore :: CloseItem, méthode</span><span class="sxs-lookup"><span data-stu-id="50341-103">IPStore::CloseItem method</span></span>

<span data-ttu-id="50341-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="50341-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="50341-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="50341-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="50341-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="50341-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="50341-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="50341-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="50341-108">Ferme un élément de données spécifié à partir du stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="50341-108">Closes a specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="50341-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50341-109">Syntax</span></span>


```C++
HRESULT CloseItem(
  [in]       PST_KEY Key,
  [in] const PSGUID  *pItemType,
  [in] const GUID    *pItemSubtype,
  [in]       LPCWSTR *szItemName,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="50341-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50341-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50341-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50341-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50341-112">Spécifie si le type est local sur l’ordinateur ou s’il est associé uniquement à l’utilisateur en train de créer.</span><span class="sxs-lookup"><span data-stu-id="50341-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="50341-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="50341-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="50341-114">Signification</span><span class="sxs-lookup"><span data-stu-id="50341-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="50341-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="50341-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="50341-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="50341-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="50341-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="50341-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="50341-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="50341-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="50341-119">*pItemType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50341-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50341-120">Pointeur vers un **GUID** qui identifie le type de données de l’élément à fermer.</span><span class="sxs-lookup"><span data-stu-id="50341-120">A pointer to a **GUID** that identifies the data type of the item to close.</span></span>

</dd> <dt>

<span data-ttu-id="50341-121">*pItemSubtype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50341-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50341-122">Pointeur vers un **GUID** qui indique le sous-type d’élément à fermer.</span><span class="sxs-lookup"><span data-stu-id="50341-122">A pointer to a **GUID** that indicates the item subtype to close.</span></span>

</dd> <dt>

<span data-ttu-id="50341-123">*szItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50341-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50341-124">Chaîne qui contient le nom de l’élément à fermer.</span><span class="sxs-lookup"><span data-stu-id="50341-124">A string that contains the name of the item to close.</span></span>

</dd> <dt>

<span data-ttu-id="50341-125">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50341-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50341-126">Réservé : doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="50341-126">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50341-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50341-127">Return value</span></span>

<span data-ttu-id="50341-128">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="50341-128">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="50341-129">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="50341-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="50341-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50341-130">Requirements</span></span>



| <span data-ttu-id="50341-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50341-131">Requirement</span></span> | <span data-ttu-id="50341-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="50341-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50341-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="50341-133">Header</span></span><br/> | <dl> <span data-ttu-id="50341-134"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="50341-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="50341-135">DLL</span><span class="sxs-lookup"><span data-stu-id="50341-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="50341-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50341-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50341-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50341-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50341-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="50341-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
