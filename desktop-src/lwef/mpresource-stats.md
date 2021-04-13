---
title: Structure MPRESOURCE_STATS (MpClient. h)
description: Statistiques relatives aux ressources.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPRESOURCE_STATS
- PMPRESOURCE_STATS des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465935"
---
# <a name="mpresource_stats-structure"></a>MPRESOURCE, \_ structure des statistiques

Statistiques relatives aux ressources.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a>Membres

<dl> <dt>

**PPMProgress**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Progression approximative de l’analyse en ppm (parties par million). Défini sur **MPPROGRESS \_ non valide** si les informations de progression ne sont pas disponibles.

</dd> <dt>

**ProcessCount**
</dt> <dd>

Type : **UINT64**

</dd> <dd>

Nombre de processus analysés.

</dd> <dt>

**FileCount**
</dt> <dd>

Type : **UINT64**

</dd> <dd>

Nombre de fichiers analysés.

</dd> <dt>

**FileBytesCount**
</dt> <dd>

Type : **UINT64**

</dd> <dd>

Nombre d’octets analysés pour les fichiers.

</dd> <dt>

**RegKeyCount**
</dt> <dd>

Type : **UINT64**

</dd> <dd>

Nombre de RegKeys analysés.

</dd> <dt>

**Reserved**
</dt> <dd>

Type : **UINT64 \[ 4 \]**

</dd> <dd>

Champs réservés pour une utilisation ultérieure.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





