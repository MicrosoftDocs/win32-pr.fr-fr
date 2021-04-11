---
title: Structure MPRESERVED_DATA (MpClient. h)
description: Données de notification réservées.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPRESERVED_DATA
- PMPRESERVED_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104548"
---
# <a name="mpreserved_data-structure"></a>\_Structure de données MPRESERVED

Données de notification réservées.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbReservedData**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille des données réservées, en octets.

</dd> <dt>

**pbReservedData**
</dt> <dd>

Type : **Byte \***

</dd> <dd>

Pointeur vers les données réservées.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





