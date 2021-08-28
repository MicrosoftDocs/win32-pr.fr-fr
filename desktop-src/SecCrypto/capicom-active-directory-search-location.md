---
description: Indique l’emplacement où rechercher un magasin de certificats Active Directory.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Énumération CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 52f205717f3ba361c2c15dafc6e53f6cef3cd9d41cbbbf2ed243c60a74c2ca62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879439"
---
# <a name="capicom_active_directory_search_location-enumeration"></a>\_Énumération de l' \_ \_ emplacement de recherche Active Directory \_ CAPICOM

Le type d’énumération de l' **emplacement de \_ recherche d’active \_ Directory \_ \_ CAPICOM** indique l’emplacement dans lequel Rechercher un [*magasin de certificats*](../secgloss/c-gly.md)Active Directory.

## <a name="members"></a>Membres



| Membre                               | Description                                  | Valeur |
|--------------------------------------|----------------------------------------------|-------|
| **Rechercher dans CAPICOM \_ \_**             | Effectue une recherche dans tous les emplacements disponibles.<br/> | 0     |
| **\_catalogue global de recherche \_ CAPICOM \_** | Recherche uniquement dans le catalogue global.<br/> | 1     |
| **\_ \_ domaine par défaut de recherche \_ CAPICOM** | Recherche uniquement le domaine par défaut.<br/> | 2     |



## <a name="remarks"></a>Remarques

Ce type d’énumération est utilisé par la propriété suivante :

-   [**Paramètres. ActiveDirectorySearchLocation**](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
