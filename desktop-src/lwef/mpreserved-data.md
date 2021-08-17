---
title: Structure MPRESERVED_DATA (MpClient. h)
description: Données de notification réservées.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPRESERVED_DATA
- PMPRESERVED_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
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
ms.openlocfilehash: faabacdcfb581f9b4fc7e9d9a42464dd61e152ca533865acfb7231a711f02317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747653"
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
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





