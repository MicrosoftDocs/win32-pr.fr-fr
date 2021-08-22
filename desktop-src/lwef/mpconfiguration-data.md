---
title: Structure MPCONFIGURATION_DATA (MpClient. h)
description: Contient des données sur les modifications de configuration, y compris les anciennes et nouvelles valeurs.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPCONFIGURATION_DATA
- PMPCONFIGURATION_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
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
ms.openlocfilehash: 192cb4d2e35d1b471ef92fb976535bb1e6ed733e2f29ebf86d357f722904514c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114579"
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

Type : **Byte \***

</dd> <dd>

Pointeur vers les données précédentes.

</dd> <dt>

**CurrentDataSize**
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
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





