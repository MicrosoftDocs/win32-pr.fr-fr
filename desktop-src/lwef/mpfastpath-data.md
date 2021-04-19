---
title: Structure MPFASTPATH_DATA (MpClient. h)
description: Notification de mise à jour FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPFASTPATH_DATA
- PMPFASTPATH_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
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
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513773"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type de FASTPATH MP \_**](mp-fastpath-type.md)
</dt> <dt>

[**\_type de limite de persistance MP \_ \_**](mp-persistence-limit-type.md)
</dt> <dt>

[**\_type de signature MP \_**](mp-signature-type.md)
</dt> </dl>

 

 





