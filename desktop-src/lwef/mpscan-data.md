---
title: Structure MPSCAN_DATA (MpClient. h)
description: Analyser les données passées au rappel.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPSCAN_DATA
- PMPSCAN_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b7c00357b8f104fff42b94de552d52979c364dee64a82bb8e438946319c8c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975989"
---
# <a name="mpscan_data-structure"></a>\_Structure de données MPSCAN

Analyser les données passées au rappel.

Cette structure contient des statistiques cumulatives sur les menaces et les ressources. Ces champs stat sont toujours valides.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**ScanType**
</dt> <dd>

Type : **[ **MPSCAN \_**](mpscan-type.md)**

</dd> <dd>

Type d’analyse.

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Type : **PMPRESOURCE \_ info**

</dd> <dd>

Informations sur la ressource. Consultez [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Type : **[ **\_ statistiques MPRESOURCE**](mpresource-stats.md)**

</dd> <dd>

Statistiques cumulatives relatives aux ressources.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Type : **[ **\_ statistiques MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Statistiques des menaces avec la réussite de l’analyse.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**statistiques de MPRESOURCE \_**](mpresource-stats.md)
</dt> <dt>

[**\_type MPSCAN**](mpscan-type.md)
</dt> <dt>

[**statistiques de MPTHREAT \_**](mpthreat-stats.md)
</dt> </dl>

 

 





