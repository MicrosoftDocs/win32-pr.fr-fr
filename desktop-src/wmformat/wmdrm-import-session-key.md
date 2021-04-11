---
title: Structure WMDRM_IMPORT_SESSION_KEY (Drmexternals. h)
description: La \_ \_ \_ structure de la clé de session d’importation WMDRM contient la clé de session pour l’importation de contenu protégé.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- Structure WMDRM_IMPORT_SESSION_KEY format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105304"
---
# <a name="wmdrm_import_session_key-structure"></a>Structure de la clé de session d' \_ importation WMDRM \_ \_

La structure de la **\_ clé de \_ session \_ d’importation WMDRM** contient la clé de session pour l’importation de contenu protégé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwKeyType**
</dt> <dd>

Type de clé de session. Définissez sur le \_ type de frappe WMDRM \_ .

</dd> <dt>

**cbKey**
</dt> <dd>

Taille de la clé de session, en octets. Cette valeur peut être aussi importante que nécessaire, étant donné les limites d’une seule opération OAEP RSA sur l’ensemble du message (cette structure plus la clé de session).

</dd> <dt>

**rgbKey**
</dt> <dd>

Adresse d’une mémoire tampon contenant la clé de session. La taille de la mémoire tampon doit correspondre à la valeur de **cbKey**. Les données de la mémoire tampon sont une valeur de clé générée de façon aléatoire.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure, y compris la mémoire tampon contenant la clé de session, doit être chiffrée à l’aide de la clé publique de l’ordinateur Windows Media DRM et incluse dans le membre **pbEncryptedSessionKeyMessage** de la structure d' [**importation/ \_ exportation \_ \_ WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                      |
| Version<br/>                  | SDK Windows Media format 11<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





