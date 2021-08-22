---
title: Structure MPFASTPATH_DATA (MpClient. h)
description: Notification de mise à jour FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPFASTPATH_DATA
- PMPFASTPATH_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e138e9c45657cfc4ebeba1d1dbeed38070b6e07d09c512ec96835a04702d0c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556149"
---
# <a name="mpfastpath_data-structure"></a>\_Structure de données MPFASTPATH

Notification de mise à jour FastPath.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**SignatureType**
</dt> <dd>

Type : **[ **\_ \_ type de signature MP**](mp-signature-type.md)**

</dd> <dd>

Type de signature.

</dd> <dt>

**FastPathSignatureType**
</dt> <dd>

Type : **[ **MP \_ FASTPATH \_ type**](mp-fastpath-type.md)**

</dd> <dd>

Type de signature FastPath.

</dd> <dt>

**FastPathSignatureVersion**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Version de signature de FastPath (facultatif).

</dd> <dt>

**CompilationTimestamp**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

Horodatage de compilation (UTC).

</dd> <dt>

**PersistenceType**
</dt> <dd>

Type : **[ **\_ \_ \_ type de limite de persistance MP**](mp-persistence-limit-type.md)**

</dd> <dd>

Type de persistance (facultatif).

</dd> <dt>

**PersistenceValue**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Valeur de persistance (facultatif).

</dd> <dt>

**PersistencePath**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Chemin de persistance (facultatif).

</dd> <dt>

**Motif**
</dt> <dd>

Type : raison de la **[ **suppression du pack d' \_ installation \_**](mp-removal-reason.md)**

</dd> <dd>

Raison de la suppression de la signature.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type de FASTPATH MP \_**](mp-fastpath-type.md)
</dt> <dt>

[**\_type de limite de persistance MP \_ \_**](mp-persistence-limit-type.md)
</dt> <dt>

[**\_type de signature MP \_**](mp-signature-type.md)
</dt> </dl>

 

 





