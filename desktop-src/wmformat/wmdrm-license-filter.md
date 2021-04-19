---
title: Structure WMDRM_LICENSE_FILTER (wmdrmsdk. h)
description: La \_ \_ structure de filtre de licence WMDRM définit les paramètres de filtrage à utiliser lors de la création d’une énumération de licence.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- Structure WMDRM_LICENSE_FILTER format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539211"
---
# <a name="wmdrm_license_filter-structure"></a>Structure de filtre de \_ licence WMDRM \_

La structure de **\_ \_ filtre de licence WMDRM** définit les paramètres de filtrage à utiliser lors de la création d’une énumération de licence.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Spécifie un numéro de version minimal pour les licences retournées.

</dd> <dt>

**bstrKID**
</dt> <dd>

Spécifie un ID de clé pour lequel filtrer les licences. Seules les licences avec l’ID de clé spécifié seront incluses dans l’énumération.

</dd> <dt>

**bstrRights**
</dt> <dd>

Spécifie un ensemble de droits pour le filtrage des licences. Seules les licences qui fournissent tous les droits spécifiés seront incluses dans l’énumération.

</dd> <dt>

**bstrAllowedSourceIDs**
</dt> <dd>

Spécifie les sources de contenu protégé à inclure dans la recherche de licence.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée par la méthode [**IWMDRMLicenseManagement :: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





