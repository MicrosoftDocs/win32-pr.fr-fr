---
description: Supprime l’élément spécifié du stockage protégé.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: IPStore ::D méthode eleteItem (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537825"
---
# <a name="ipstoredeleteitem-method"></a><span data-ttu-id="a67e5-103">IPStore ::D méthode eleteItem</span><span class="sxs-lookup"><span data-stu-id="a67e5-103">IPStore::DeleteItem method</span></span>

<span data-ttu-id="a67e5-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a67e5-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a67e5-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a67e5-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a67e5-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="a67e5-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a67e5-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a67e5-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a67e5-108">Supprime l’élément spécifié du stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="a67e5-108">Deletes the specified item from the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="a67e5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a67e5-109">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a67e5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a67e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a67e5-111">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a67e5-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a67e5-112">Zone de stockage du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a67e5-112">The provider storage area.</span></span>



| <span data-ttu-id="a67e5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a67e5-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="a67e5-114">Signification</span><span class="sxs-lookup"><span data-stu-id="a67e5-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="a67e5-115"><dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="a67e5-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="a67e5-116">Le stockage est conservé dans la section utilisateur actuel du Registre.</span><span class="sxs-lookup"><span data-stu-id="a67e5-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="a67e5-117"><dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a67e5-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="a67e5-118">Le stockage est conservé dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="a67e5-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a67e5-119">*pItemType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a67e5-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a67e5-120">Pointeur vers un **GUID** qui identifie le type de données de l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a67e5-120">A pointer to a **GUID** that identifies the data type of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="a67e5-121">*pItemSubType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a67e5-121">*pItemSubType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a67e5-122">**GUID** qui indique le sous-type d’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a67e5-122">A **GUID** that indicates the item subtype to delete.</span></span>

</dd> <dt>

<span data-ttu-id="a67e5-123">*szItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a67e5-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a67e5-124">Chaîne qui contient le nom de l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a67e5-124">A string that contains the name of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="a67e5-125">*pPromptInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a67e5-125">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a67e5-126">Pointeur vers une structure [**\_ PROMPTINFO PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a67e5-126">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a67e5-127">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a67e5-127">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a67e5-128">Spécifie l’interface utilisateur et les comportements de sécurité pour l’opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="a67e5-128">Specifies user interface and security behaviors for the delete operation.</span></span>



| <span data-ttu-id="a67e5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a67e5-129">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="a67e5-130">Signification</span><span class="sxs-lookup"><span data-stu-id="a67e5-130">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="a67e5-131"><dt>**Fichier PST \_ AUCUNE \_ \_ migration de l’interface utilisateur**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="a67e5-131"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="a67e5-132">N’affiche pas l’interface utilisateur, sauf si un mot de passe personnalisé est requis.</span><span class="sxs-lookup"><span data-stu-id="a67e5-132">Do not show user interface unless a custom password is required.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a67e5-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a67e5-133">Return value</span></span>

<span data-ttu-id="a67e5-134">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a67e5-134">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="a67e5-135">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="a67e5-135">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a67e5-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a67e5-136">Requirements</span></span>



| <span data-ttu-id="a67e5-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a67e5-137">Requirement</span></span> | <span data-ttu-id="a67e5-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="a67e5-138">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a67e5-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="a67e5-139">Header</span></span><br/> | <dl> <span data-ttu-id="a67e5-140"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a67e5-140"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a67e5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a67e5-141">DLL</span></span><br/>    | <dl> <span data-ttu-id="a67e5-142"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a67e5-142"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a67e5-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a67e5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a67e5-144">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="a67e5-144">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="a67e5-145">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="a67e5-145">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
