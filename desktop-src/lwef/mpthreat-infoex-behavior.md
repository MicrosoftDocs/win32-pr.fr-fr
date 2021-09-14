---
title: Structure MPTHREAT_INFOEX_BEHAVIOR (MpClient. h)
description: Contient des informations spécifiques à la modification du comportement.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_INFOEX_BEHAVIOR
- PMPTHREAT_INFOEX_BEHAVIOR des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227814"
---
# <a name="mpthreat_infoex_behavior-structure"></a>MPTHREAT \_ \_ structure de comportement INFOEX

Contient des informations spécifiques à la modification du comportement.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a>Membres

<dl> <dt>

**SignatureID**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

ID de signature de modification de comportement fourni par le moteur au moment de la détection.

</dd> <dt>

**EngineVersion**
</dt> <dd>

Type : **ULONGLONG**

</dd> <dd>

Version du module moteur.

</dd> <dt>

**ASDeltaSignatureVersion**
</dt> <dd>

Type : **ULONGLONG**

</dd> <dd>

Version de signature du logiciel anti-espion.

</dd> <dt>

**AVDeltaSignatureVersion**
</dt> <dd>

Type : **ULONGLONG**

</dd> <dd>

Version de signature de l’antivirus

</dd> <dt>

**HashType**
</dt> <dd>

Type : **[ **\_ \_ type de hachage MP**](mp-hash-type.md)**

</dd> <dd>

Type de hachage utilisé. Consultez [**\_ \_ type de hachage MP**](mp-hash-type.md).

</dd> <dt>

**FidelityValue**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Valeur de fidélité.

</dd> <dt>

**HashValue**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Hachage du fichier.

</dd> <dt>

**TargetFileName**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Chemin d’accès et nom du fichier ciblé.

</dd> <dt>

**TargetFileHash**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Hachage du fichier ciblé.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type de hachage MP \_**](mp-hash-type.md)
</dt> </dl>

 

 





