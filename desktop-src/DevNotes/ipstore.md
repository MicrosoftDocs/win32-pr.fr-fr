---
description: Fournit des méthodes COM-standard pour gérer les éléments de données de stockage protégés.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: IPStore, interface (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539550"
---
# <a name="ipstore-interface"></a><span data-ttu-id="cb112-103">Interface IPStore</span><span class="sxs-lookup"><span data-stu-id="cb112-103">IPStore interface</span></span>

<span data-ttu-id="cb112-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cb112-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="cb112-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cb112-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="cb112-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="cb112-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="cb112-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="cb112-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="cb112-108">\[Cette interface peut être modifiée ou non disponible dans les futures versions de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cb112-108">\[This interface may be altered or unavailable in future versions of Windows.\]</span></span>

<span data-ttu-id="cb112-109">Fournit des méthodes COM-standard pour gérer les éléments de données de stockage protégés.</span><span class="sxs-lookup"><span data-stu-id="cb112-109">Provides COM-standard methods to manage protected storage data items.</span></span> <span data-ttu-id="cb112-110">La méthode [**PStoreCreateInstance**](pstorecreateinstance.md) retourne un pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="cb112-110">The [**PStoreCreateInstance**](pstorecreateinstance.md) method returns a pointer to this interface.</span></span>

## <a name="members"></a><span data-ttu-id="cb112-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cb112-111">Members</span></span>

<span data-ttu-id="cb112-112">L’interface **IPStore** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cb112-112">The **IPStore** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cb112-113">**IPStore** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb112-113">**IPStore** also has these types of members:</span></span>

-   [<span data-ttu-id="cb112-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb112-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cb112-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb112-115">Methods</span></span>

<span data-ttu-id="cb112-116">L’interface **IPStore** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cb112-116">The **IPStore** interface has these methods.</span></span>



| <span data-ttu-id="cb112-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb112-117">Method</span></span>                                                   | <span data-ttu-id="cb112-118">Description</span><span class="sxs-lookup"><span data-stu-id="cb112-118">Description</span></span>                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb112-119">**CloseItem**</span><span class="sxs-lookup"><span data-stu-id="cb112-119">**CloseItem**</span></span>](ipstore-closeitem.md)                   | <span data-ttu-id="cb112-120">Ferme un élément de données spécifié à partir du stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="cb112-120">Closes a specified data item from protected storage.</span></span><br/>                                                       |
| [<span data-ttu-id="cb112-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="cb112-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)           | <span data-ttu-id="cb112-122">Crée le sous-type spécifié dans le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="cb112-122">Creates the specified subtype within the specified type.</span></span><br/>                                                   |
| [<span data-ttu-id="cb112-123">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="cb112-123">**CreateType**</span></span>](ipstore-createtype.md)                 | <span data-ttu-id="cb112-124">Crée le type spécifié avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="cb112-124">Creates the specified type with the specified name.</span></span><br/>                                                        |
| [<span data-ttu-id="cb112-125">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="cb112-125">**DeleteItem**</span></span>](ipstore-deleteitem.md)                 | <span data-ttu-id="cb112-126">Supprime l’élément spécifié du stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="cb112-126">Deletes the specified item from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="cb112-127">**DeleteSubtype**</span><span class="sxs-lookup"><span data-stu-id="cb112-127">**DeleteSubtype**</span></span>](ipstore-deletesubtype.md)           | <span data-ttu-id="cb112-128">Supprime le sous-type d’élément spécifié du stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="cb112-128">Deletes the specified item subtype from the protected storage.</span></span><br/>                                             |
| [<span data-ttu-id="cb112-129">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="cb112-129">**DeleteType**</span></span>](ipstore-deletetype.md)                 | <span data-ttu-id="cb112-130">Supprime le type spécifié du stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="cb112-130">Deletes the specified type from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="cb112-131">**EnumItems**</span><span class="sxs-lookup"><span data-stu-id="cb112-131">**EnumItems**</span></span>](ipstore-enumitems.md)                   | <span data-ttu-id="cb112-132">Retourne le pointeur d’interface d’un sous-type pour l’énumération des éléments dans la base de données de stockage protégée.</span><span class="sxs-lookup"><span data-stu-id="cb112-132">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span><br/>        |
| [<span data-ttu-id="cb112-133">**EnumSubtypes**</span><span class="sxs-lookup"><span data-stu-id="cb112-133">**EnumSubtypes**</span></span>](ipstore-enumsubtypes.md)             | <span data-ttu-id="cb112-134">Retourne une interface pour l’énumération des sous-types des types actuellement enregistrés dans la base de données protégée.</span><span class="sxs-lookup"><span data-stu-id="cb112-134">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span><br/> |
| [<span data-ttu-id="cb112-135">**EnumTypes**</span><span class="sxs-lookup"><span data-stu-id="cb112-135">**EnumTypes**</span></span>](ipstore-enumtypes.md)                   | <span data-ttu-id="cb112-136">Retourne une interface pour énumérer les types actuellement enregistrés dans la base de données protégée.</span><span class="sxs-lookup"><span data-stu-id="cb112-136">Returns an interface for enumerating the types currently registered in the protected database.</span></span><br/>             |
| [<span data-ttu-id="cb112-137">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="cb112-137">**GetInfo**</span></span>](ipstore-getinfo.md)                       | <span data-ttu-id="cb112-138">Récupère des informations sur le fournisseur de stockage.</span><span class="sxs-lookup"><span data-stu-id="cb112-138">Retrieves information about the storage provider.</span></span><br/>                                                          |
| [<span data-ttu-id="cb112-139">**GetProvParam**</span><span class="sxs-lookup"><span data-stu-id="cb112-139">**GetProvParam**</span></span>](ipstore-getprovparam.md)             | <span data-ttu-id="cb112-140">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="cb112-140">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="cb112-141">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="cb112-141">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)         | <span data-ttu-id="cb112-142">Récupère les informations associées à un sous-type.</span><span class="sxs-lookup"><span data-stu-id="cb112-142">Retrieves information associated with a subtype.</span></span><br/>                                                           |
| [<span data-ttu-id="cb112-143">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="cb112-143">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)               | <span data-ttu-id="cb112-144">Récupère les informations associées à un type.</span><span class="sxs-lookup"><span data-stu-id="cb112-144">Retrieves information associated with a type.</span></span><br/>                                                              |
| [<span data-ttu-id="cb112-145">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="cb112-145">**OpenItem**</span></span>](ipstore-openitem.md)                     | <span data-ttu-id="cb112-146">Ouvre un élément pour plusieurs accès.</span><span class="sxs-lookup"><span data-stu-id="cb112-146">Opens an item for multiple accesses.</span></span><br/>                                                                       |
| [<span data-ttu-id="cb112-147">**ReadAccessRuleSet**</span><span class="sxs-lookup"><span data-stu-id="cb112-147">**ReadAccessRuleSet**</span></span>](ipstore-readaccessruleset.md)   | <span data-ttu-id="cb112-148">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="cb112-148">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="cb112-149">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="cb112-149">**ReadItem**</span></span>](ipstore-readitem.md)                     | <span data-ttu-id="cb112-150">Lit l’élément de données spécifié à partir du stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="cb112-150">Reads the specified data item from protected storage.</span></span><br/>                                                      |
| [<span data-ttu-id="cb112-151">**SetProvParam**</span><span class="sxs-lookup"><span data-stu-id="cb112-151">**SetProvParam**</span></span>](ipstore-setprovparam.md)             | <span data-ttu-id="cb112-152">Définit les informations de paramètre spécifiées.</span><span class="sxs-lookup"><span data-stu-id="cb112-152">Sets the specified parameter information.</span></span><br/>                                                                  |
| [<span data-ttu-id="cb112-153">**WriteAccessRuleset**</span><span class="sxs-lookup"><span data-stu-id="cb112-153">**WriteAccessRuleset**</span></span>](ipstore-writeaccessruleset.md) | <span data-ttu-id="cb112-154">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="cb112-154">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="cb112-155">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="cb112-155">**WriteItem**</span></span>](ipstore-writeitem.md)                   | <span data-ttu-id="cb112-156">Écrit un élément de données dans le stockage protégé.</span><span class="sxs-lookup"><span data-stu-id="cb112-156">Writes a data item to protected storage.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="cb112-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb112-157">Requirements</span></span>



| <span data-ttu-id="cb112-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb112-158">Requirement</span></span> | <span data-ttu-id="cb112-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb112-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb112-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb112-160">Header</span></span><br/> | <dl> <span data-ttu-id="cb112-161"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb112-161"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="cb112-162">DLL</span><span class="sxs-lookup"><span data-stu-id="cb112-162">DLL</span></span><br/>    | <dl> <span data-ttu-id="cb112-163"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb112-163"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
