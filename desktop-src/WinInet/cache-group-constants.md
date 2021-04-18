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
# <a name="cache-group-constants"></a>Constantes de groupe de caches

La liste suivante contient les constantes utilisées par les fonctions de groupe de cache.

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**attribut CACHEGROUP de \_ \_ base**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Récupère les indicateurs, le type et les attributs de quota de disque du groupe de cache. Utilisé par la fonction [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**\_indicateur d’attribut CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Définit ou récupère les indicateurs associés au groupe de cache. Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**\_attribut CACHEGROUP \_ \_ tout accéder**
</dt> <dd> <dl> <dt>

égale
</dt> <dt>



Récupère tous les attributs du groupe de caches. Utilisé par la fonction [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**\_attribut CACHEGROUP \_ GroupName**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



Définit ou récupère le nom de groupe du groupe de caches. Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**\_quota d’attribut CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Définit ou récupère le quota de disque associé au groupe de caches. Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**\_stockage des attributs CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Définit ou récupère le stockage du propriétaire du groupe associé au groupe de caches. Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**\_type d’attribut CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Définit ou récupère le type de groupe de cache. Cela est utilisé par les fonctions [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) et [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP \_ indicateur \_ FLUSHURL \_ OnDelete**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indique que toutes les entrées de cache associées au groupe de cache doivent être supprimées, sauf si l’entrée appartient à un autre groupe de caches.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**\_indicateur CACHEGROUP \_ GIDONLY**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indique que la fonction doit uniquement créer un GROUPID unique pour le groupe de cache et ne pas créer le groupe réel.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**\_indicateur CACHEGROUP \_ NONPURGEABLE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indique que le groupe de cache ne peut pas être purgé.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**\_masque CACHEGROUP ReadWrite \_**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



Définit le type, le quota de disque, le nom de groupe et les attributs de stockage du propriétaire du groupe de cache. Utilisé par la fonction [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP \_ Rechercher \_ tout**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indique que tous les groupes de caches dans le système de l’utilisateur doivent être énumérés.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP \_ recherche \_ BYURL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Actuellement non implémenté.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**TYPE de CACHEGROUP \_ \_ non valide**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indique que le type de groupe de cache n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_taille de \_ stockage du propriétaire du groupe \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Longueur du groupe de stockage du propriétaire du groupe.


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_longueur maximale du GroupName \_**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



Nombre maximal de caractères autorisés pour un nom de groupe de caches.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

