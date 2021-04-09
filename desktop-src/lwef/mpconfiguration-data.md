---
title: Structure MPCONFIGURATION_DATA (MpClient. h)
description: Contient des données sur les modifications de configuration, y compris les anciennes et nouvelles valeurs.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPCONFIGURATION_DATA
- PMPCONFIGURATION_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032711"
---
# <a name="mpconfiguration_data-structure"></a>\_Structure de données MPCONFIGURATION

Contient des données sur les modifications de configuration, y compris les anciennes et nouvelles valeurs.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**ConfigurationName**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Nom de la configuration qui a été modifiée.

</dd> <dt>

**DataType**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Type de données utilisé.

</dd> <dt>

**PreviousDataSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille des données précédentes, en octets.

</dd> <dt>

**pPreviousData**
</dt> <dd>

Type : **Byte \** _

</dd> <dd>

Pointeur vers les données précédentes.

</dd> <dt>

_ *CurrentDataSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille des nouvelles données, en octets.

</dd> <dt>

**pCurrentData**
</dt> <dd>

Type : **Byte \***

</dd> <dd>

Pointeur vers de nouvelles données.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





