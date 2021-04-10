---
title: Structure MPSCAN_RESULT (MpClient. h)
description: Résultats d’une analyse.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSCAN_RESULT
- PMPSCAN_RESULT des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200584"
---
# <a name="mpscan_result-structure"></a>\_Structure de résultat MPSCAN

Résultats d’une analyse.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a>Membres

<dl> <dt>

**ScanType**
</dt> <dd>

Type : **[ **MPSCAN \_**](mpscan-type.md)**

</dd> <dd>

Type d’analyse. Consultez [**\_ type MPSCAN**](mpscan-type.md).

</dd> <dt>

**Source**
</dt> <dd>

Type : **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Source d’analyse, telle que l’utilisateur ou le système initié. Consultez [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ScanGuid**
</dt> <dd>

Type : **GUID**

</dd> <dd>

Identificateur d’analyse.

</dd> <dt>

**StartTime**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

Heure de début de l’analyse.

</dd> <dt>

**EndTime**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

Heure de fin de l’analyse.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Type : **[ **\_ statistiques MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Statistiques relatives aux menaces. Consultez [**MPTHREAT \_ Statistics**](mpthreat-stats.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Type : **[ **\_ statistiques MPRESOURCE**](mpresource-stats.md)**

</dd> <dd>

Statistiques relatives aux ressources. Consultez [**MPRESOURCE \_ Statistics**](mpresource-stats.md).

</dd> <dt>

**SignatureVersion**
</dt> <dd>

Type : **ULONGLONG**

</dd> <dd>

Version de signature utilisée pour l’analyse.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**statistiques de MPRESOURCE \_**](mpresource-stats.md)
</dt> <dt>

[**\_type MPSCAN**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**statistiques de MPTHREAT \_**](mpthreat-stats.md)
</dt> </dl>

 

 





