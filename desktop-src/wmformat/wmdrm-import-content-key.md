---
title: Structure WMDRM_IMPORT_CONTENT_KEY (Drmexternals. h)
description: La \_ \_ \_ structure de clé de contenu d’importation WMDRM stocke la clé de contenu utilisée pour l’importation de contenu protégé.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- Structure WMDRM_IMPORT_CONTENT_KEY format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f7ced03d841d71e104384fff3f7abdfdd13890746f8052cf43264dacd22c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083793"
---
# <a name="wmdrm_import_content_key-structure"></a>\_Structure de \_ clé du contenu d’importation WMDRM \_

La structure de **\_ clé de \_ contenu \_ d’importation WMDRM** stocke la clé de contenu utilisée pour l’importation de contenu protégé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Version.

</dd> <dt>

**cbStructSize**
</dt> <dd>

Taille de la structure en octets.

</dd> <dt>

**dwIVKeyType**
</dt> <dd>

Type de clé du vecteur d’initialisation. Définissez sur le \_ type de frappe WMDRM \_ .

</dd> <dt>

**cbIVKey**
</dt> <dd>

Taille de la clé du vecteur d’initialisation, en octets.

</dd> <dt>

**dwContentKeyType**
</dt> <dd>

Type de clé de contenu. Définissez sur le \_ type de cocktail de type de l’entrée WMDRM \_ .

</dd> <dt>

**cbContentKey**
</dt> <dd>

Taille de la clé de contenu en octets.

</dd> <dt>

**rgbKeyData**
</dt> <dd>

Adresse d’une mémoire tampon contenant la clé de contenu. La taille de la mémoire tampon doit correspondre à la valeur de **cbContentKey**. Cette clé doit correspondre à la clé importée à partir du message de licence XMR.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure, y compris la mémoire tampon qui contient la clé de session, doit être chiffrée à l’aide de la clé de session et incluse dans le membre **pbEncryptedKeyMessage** de la structure d' [**importation/ \_ exportation \_ \_ WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

## <a name="requirements"></a>Configuration requise



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

 

 





