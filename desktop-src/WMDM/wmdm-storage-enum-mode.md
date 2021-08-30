---
title: Énumération WMDM_STORAGE_ENUM_MODE
description: Le \_ \_ \_ type d’énumération du mode enum de stockage WMDM définit la manière dont le contenu sur le stockage doit être énuméré. Cette énumération est utilisée par IWMDMStorage3 SetEnumPreference.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- WMDM_STORAGE_ENUM_MODE l’énumération des Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ba8b524618ebc0c5d40f9f4e9f0ad0871b7c8c39a0919d594a39248bc2d6dc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004769"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a>\_ \_ Énumération du mode enum de stockage WMDM \_

Le type d’énumération du **\_ \_ \_ mode enum de stockage WMDM** définit la manière dont le contenu sur le stockage doit être énuméré. Cette énumération est utilisée par [**IWMDMStorage3 :: SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**\_mode enum \_ brut**
</dt> <dd>

Énumère le contenu sur le stockage de la même manière qu’il est organisé dans le système de fichiers du stockage.

**MODE ÉNUMÉRer utiliser les préférences de l' \_ \_ \_ appareil \_**

Énumère le contenu sur le stockage en fonction de la préférence de l’appareil, comme indiqué par le paramètre d’appareil *UseMetadataViews* .

**\_vues de \_ métadonnées du mode enum \_**

Énumère le contenu sur le stockage en organisant le contenu en fonction d’une vue de métadonnées.

</dd> <dt>

<span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**MODE ÉNUMÉRer utiliser les préférences de l' \_ \_ \_ appareil \_**
</dt> <dd>

Énumère le contenu sur le stockage en fonction de la préférence de l’appareil, comme indiqué par le paramètre d’appareil *UseMetadataViews* .

**\_vues de \_ métadonnées du mode enum \_**

Énumère le contenu sur le stockage en organisant le contenu en fonction d’une vue de métadonnées.

</dd> <dt>

<span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**\_vues de \_ métadonnées du mode enum \_**
</dt> <dd>

Énumère le contenu sur le stockage en organisant le contenu en fonction d’une vue de métadonnées.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](enumeration-types.md)
</dt> </dl>

 

 





