---
title: Structure DRM_PLAYLIST_CONTENT_ID (Drmexternals. h)
description: La structure de l’ID de contenu de la \_ sélection DRM \_ contient des \_ informations sur le contenu à copier sur CD dans le cadre d’une gravure de sélection.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- Structure DRM_PLAYLIST_CONTENT_ID format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293854"
---
# <a name="drm_playlist_content_id-structure"></a>Structure de l’ID de contenu de la \_ sélection DRM \_ \_

La structure de l’ID de contenu de la **\_ sélection \_ \_ DRM** contient des informations sur le contenu à copier sur CD dans le cadre d’une gravure de sélection.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**lpcwszV2Header**
</dt> <dd>

En-tête DRM. utilisez ce membre si le contenu est protégé par Windows Media DRM version 2 ou ultérieure.

</dd> <dt>

**lpcszV1KID**
</dt> <dd>

ID de la clé. utilisez ce membre si le contenu est protégé par Windows Media DRM version 1.

</dd> <dt>

**pbOtherData**
</dt> <dd>

Mémoire tampon contenant des données supplémentaires.

</dd> <dt>

**cbOtherData**
</dt> <dd>

Taille de la mémoire tampon **pbOtherData** en octets.

</dd> <dt>

**dwUniqueIDForSession**
</dt> <dd>

Identificateur unique du contenu à utiliser dans la session active.

</dd> <dt>

**dwValidFields**
</dt> <dd>

**Valeur DWORD** indiquant les champs valides de cette structure.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                      |
| Version<br/>                  | Windows Kit de développement logiciel (SDK) Media format 11<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





