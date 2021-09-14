---
title: Énumération MP_HASH_TYPE (MpClient. h)
description: Types de hachage possibles.
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- MP_HASH_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMP_HASH_TYPE de l’héritage des Windows fonctionnalités d’environnement du pointeur d’énumération
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c36e709d165845b729673df4aaea1042a7ee49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236430"
---
# <a name="mp_hash_type-enumeration"></a>\_Énumération de type de hachage MP \_

Types de hachage possibles.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**\_type de hachage MP \_ \_ None**
</dt> <dd>

Aucun hachage.

</dd> <dt>

<span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**\_Type de hachage MP \_ \_ CRC32**
</dt> <dd>

CRC32

</dd> <dt>

<span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**\_Type de hachage MP \_ \_ MD5**
</dt> <dd>

MD5

</dd> <dt>

<span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**\_Type de hachage MP \_ \_ SHA1**
</dt> <dd>

SHA1

</dd> <dt>

<span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**\_Type de hachage MP \_ \_ SHA256**
</dt> <dd>

SHA 256

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





