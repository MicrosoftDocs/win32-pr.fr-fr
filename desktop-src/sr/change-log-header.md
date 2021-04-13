---
title: Structure CHANGE_LOG_HEADER
description: En-tête du journal des modifications.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- Restauration du système de la structure CHANGE_LOG_HEADER
- PCHANGE_LOG_HEADER de la restauration du système du pointeur de structure
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383995"
---
# <a name="change_log_header-structure"></a>MODIFIER \_ la \_ structure d’en-tête de journal

\[Ces informations s’appliquent uniquement à Windows XP avec Service Pack 2 (SP2).\]

En-tête du journal des modifications.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**RecordHeader**
</dt> <dd>

Structure [**d' \_ en-tête d’enregistrement**](record-header.md) . Le membre **dwRecordType** doit être défini sur RecordTypeLogHeader (0). Le membre **dwRecordSize** doit tenir compte de tous les membres, ainsi que de la valeur **DWORD** supplémentaire qui suit cet en-tête. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

**dwMagicNum**
</dt> <dd>

Ce membre doit être défini sur 0xabcdef12.

</dd> <dt>

**dwLogVersion**
</dt> <dd>

Ce membre doit être défini sur 2.

</dd> <dt>

**DataHeader**
</dt> <dd>

Structure [**d' \_ en-tête d’enregistrement**](record-header.md) . Le membre **dwRecordType** doit être défini sur **RecordTypeVolumePath** (2).

</dd> <dt>

**byteData**
</dt> <dd>

Début d’une chaîne terminée par le caractère null qui spécifie le chemin d’accès du volume.

</dd> </dl>

## <a name="remarks"></a>Notes

Cet en-tête est suivi d’une valeur **DWORD** qui doit être identique à la valeur du membre **dwRecordSize** de **RecordHeader**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                            |
| Fin de la prise en charge des clients<br/>    | Windows XP SP2<br/>                       |



 

 





