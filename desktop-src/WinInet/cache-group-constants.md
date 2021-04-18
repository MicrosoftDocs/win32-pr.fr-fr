---
title: Constantes de groupe de caches (Wininet. h)
description: La liste suivante contient les constantes utilisées par les fonctions de groupe de cache.
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a08efa37ad78fa3351d12fa43491c7b62ee64af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511795"
---
# <a name="cache-group-constants"></a><span data-ttu-id="ea22b-103">Constantes de groupe de caches</span><span class="sxs-lookup"><span data-stu-id="ea22b-103">Cache Group Constants</span></span>

<span data-ttu-id="ea22b-104">La liste suivante contient les constantes utilisées par les fonctions de groupe de cache.</span><span class="sxs-lookup"><span data-stu-id="ea22b-104">The following list contains the constants used by the cache group functions.</span></span>

<dl> <dt>

<span data-ttu-id="ea22b-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**attribut CACHEGROUP de \_ \_ base**</span><span class="sxs-lookup"><span data-stu-id="ea22b-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**CACHEGROUP\_ATTRIBUTE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea22b-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-107">Récupère les indicateurs, le type et les attributs de quota de disque du groupe de cache.</span><span class="sxs-lookup"><span data-stu-id="ea22b-107">Retrieves the flags, type, and disk quota attributes of the cache group.</span></span> <span data-ttu-id="ea22b-108">Utilisé par la fonction [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="ea22b-108">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**\_indicateur d’attribut CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="ea22b-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**CACHEGROUP\_ATTRIBUTE\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea22b-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-111">Définit ou récupère les indicateurs associés au groupe de cache.</span><span class="sxs-lookup"><span data-stu-id="ea22b-111">Sets or retrieves the flags associated with the cache group.</span></span> <span data-ttu-id="ea22b-112">Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="ea22b-112">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**\_attribut CACHEGROUP \_ \_ tout accéder**</span><span class="sxs-lookup"><span data-stu-id="ea22b-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP\_ATTRIBUTE\_GET\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-114">égale</span><span class="sxs-lookup"><span data-stu-id="ea22b-114">0xffffffff</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-115">Récupère tous les attributs du groupe de caches.</span><span class="sxs-lookup"><span data-stu-id="ea22b-115">Retrieves all the attributes of the cache group.</span></span> <span data-ttu-id="ea22b-116">Utilisé par la fonction [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="ea22b-116">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**\_attribut CACHEGROUP \_ GroupName**</span><span class="sxs-lookup"><span data-stu-id="ea22b-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP\_ATTRIBUTE\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-118">0x000000010</span><span class="sxs-lookup"><span data-stu-id="ea22b-118">0x000000010</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-119">Définit ou récupère le nom de groupe du groupe de caches.</span><span class="sxs-lookup"><span data-stu-id="ea22b-119">Sets or retrieves the group name of the cache group.</span></span> <span data-ttu-id="ea22b-120">Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="ea22b-120">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**\_quota d’attribut CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="ea22b-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**CACHEGROUP\_ATTRIBUTE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea22b-122">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-123">Définit ou récupère le quota de disque associé au groupe de caches.</span><span class="sxs-lookup"><span data-stu-id="ea22b-123">Sets or retrieves the disk quota associated with the cache group.</span></span> <span data-ttu-id="ea22b-124">Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="ea22b-124">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**\_stockage des attributs CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="ea22b-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**CACHEGROUP\_ATTRIBUTE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-126">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ea22b-126">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-127">Définit ou récupère le stockage du propriétaire du groupe associé au groupe de caches.</span><span class="sxs-lookup"><span data-stu-id="ea22b-127">Sets or retrieves the group owner storage associated with the cache group.</span></span> <span data-ttu-id="ea22b-128">Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="ea22b-128">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**\_type d’attribut CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="ea22b-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**CACHEGROUP\_ATTRIBUTE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea22b-130">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-131">Définit ou récupère le type de groupe de cache.</span><span class="sxs-lookup"><span data-stu-id="ea22b-131">Sets or retrieves the cache group type.</span></span> <span data-ttu-id="ea22b-132">Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="ea22b-132">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP \_ indicateur \_ FLUSHURL \_ OnDelete**</span><span class="sxs-lookup"><span data-stu-id="ea22b-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP\_FLAG\_FLUSHURL\_ONDELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea22b-134">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-135">Indique que toutes les entrées de cache associées au groupe de cache doivent être supprimées, sauf si l’entrée appartient à un autre groupe de caches.</span><span class="sxs-lookup"><span data-stu-id="ea22b-135">Indicates that all the cache entries associated with the cache group should be deleted, unless the entry belongs to another cache group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**\_indicateur CACHEGROUP \_ GIDONLY**</span><span class="sxs-lookup"><span data-stu-id="ea22b-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP\_FLAG\_GIDONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea22b-137">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-138">Indique que la fonction doit uniquement créer un GROUPID unique pour le groupe de cache et ne pas créer le groupe réel.</span><span class="sxs-lookup"><span data-stu-id="ea22b-138">Indicates that the function should only create a unique GROUPID for the cache group and not create the actual group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**\_indicateur CACHEGROUP \_ NONPURGEABLE**</span><span class="sxs-lookup"><span data-stu-id="ea22b-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP\_FLAG\_NONPURGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-140">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea22b-140">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-141">Indique que le groupe de cache ne peut pas être purgé.</span><span class="sxs-lookup"><span data-stu-id="ea22b-141">Indicates that the cache group cannot be purged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**\_masque CACHEGROUP ReadWrite \_**</span><span class="sxs-lookup"><span data-stu-id="ea22b-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP\_READWRITE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-143">0x0000003c</span><span class="sxs-lookup"><span data-stu-id="ea22b-143">0x0000003c</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-144">Définit le type, le quota de disque, le nom de groupe et les attributs de stockage du propriétaire du groupe de cache.</span><span class="sxs-lookup"><span data-stu-id="ea22b-144">Sets the type, disk quota, group name, and owner storage attributes of the cache group.</span></span> <span data-ttu-id="ea22b-145">Utilisé par la fonction [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="ea22b-145">This is used by the [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP \_ Rechercher \_ tout**</span><span class="sxs-lookup"><span data-stu-id="ea22b-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP\_SEARCH\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea22b-147">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-148">Indique que tous les groupes de caches dans le système de l’utilisateur doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="ea22b-148">Indicates that all of the cache groups in the user's system should be enumerated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP \_ recherche \_ BYURL**</span><span class="sxs-lookup"><span data-stu-id="ea22b-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP\_SEARCH\_BYURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-150">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea22b-150">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-151">Actuellement non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ea22b-151">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**TYPE de CACHEGROUP \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="ea22b-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**CACHEGROUP\_TYPE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea22b-153">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-154">Indique que le type de groupe de cache n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ea22b-154">Indicates that the cache group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_taille de \_ stockage du propriétaire du groupe \_**</span><span class="sxs-lookup"><span data-stu-id="ea22b-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**GROUP\_OWNER\_STORAGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-156">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea22b-156">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-157">Longueur du groupe de stockage du propriétaire du groupe.</span><span class="sxs-lookup"><span data-stu-id="ea22b-157">Length of the group owner storage array.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ea22b-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_longueur maximale du GroupName \_**</span><span class="sxs-lookup"><span data-stu-id="ea22b-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**GROUPNAME\_MAX\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea22b-159">0x00000078</span><span class="sxs-lookup"><span data-stu-id="ea22b-159">0x00000078</span></span>
</dt> <dt>



<span data-ttu-id="ea22b-160">Nombre maximal de caractères autorisés pour un nom de groupe de caches.</span><span class="sxs-lookup"><span data-stu-id="ea22b-160">Maximum number of characters allowed for a cache group name.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea22b-161">Notes</span><span class="sxs-lookup"><span data-stu-id="ea22b-161">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea22b-162">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="ea22b-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="ea22b-163">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="ea22b-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="ea22b-164">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="ea22b-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea22b-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea22b-165">Requirements</span></span>



| <span data-ttu-id="ea22b-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea22b-166">Requirement</span></span> | <span data-ttu-id="ea22b-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea22b-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ea22b-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea22b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ea22b-169">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea22b-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ea22b-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea22b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ea22b-171">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea22b-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ea22b-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea22b-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea22b-173"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea22b-173"><dt>Wininet.h</dt></span></span> </dl> |



 

