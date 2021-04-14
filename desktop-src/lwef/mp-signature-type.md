---
title: Énumération MP_SIGNATURE_TYPE (MpClient. h)
description: Types de signature possibles.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMP_SIGNATURE_TYPE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465166"
---
# <a name="mp_signature_type-enumeration"></a>\_Énumération du type de signature MP \_

Types de signature possibles.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**\_ \_ logiciel anti-programme malveillant de signature MP**
</dt> <dd>

Signatures antivirus et antispyware.

</dd> <dt>

<span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**SIGNATURE du pack d' \_ \_ antivirus**
</dt> <dd>

Signatures d’antivirus uniquement.

</dd> <dt>

<span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**antispyware de \_ signature MP \_**
</dt> <dd>

Uniquement les signatures anti-espion.

</dd> <dt>

<span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**\_signature MP \_ NIS**
</dt> <dd>

Signatures NIS.

</dd> <dt>

<span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**\_types de signature MP \_ \_ MaxValue**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





