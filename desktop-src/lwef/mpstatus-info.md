---
title: Structure MPSTATUS_INFO (MpClient. h)
description: Informations d’État pour le gestionnaire de protection contre les programmes malveillants.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSTATUS_INFO
- PMPSTATUS_INFO des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740132"
---
# <a name="mpstatus_info-structure"></a>\_Structure d’informations MPSTATUS

Informations d’État pour le gestionnaire de protection contre les programmes malveillants.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**ProductStatus**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

État général du produit. Il s’agit d’une combinaison de bits indicateurs à partir de l' [**\_ indicateur MPSTATUS**](mpstatus-flag.md).

</dd> <dt>

**LastQuickScan**
</dt> <dd>

Type : **[ **MPSCAN \_ result**](mpscan-result.md)**

</dd> <dd>

Résultats de la dernière analyse par le gestionnaire de protection contre les programmes malveillants. Consultez [**\_ résultat de MPSCAN**](mpscan-result.md).

</dd> <dt>

**LastFullScan**
</dt> <dd>

Type : **[ **MPSCAN \_ result**](mpscan-result.md)**

</dd> <dd>

Résultats de la dernière analyse complète par le gestionnaire de protection contre les programmes malveillants. Consultez [**\_ résultat de MPSCAN**](mpscan-result.md).

</dd> <dt>

**ThreatStats**
</dt> <dd>

Type : **[ **\_ statistiques MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Statistiques actives sur les menaces. Consultez [**MPTHREAT \_ Statistics**](mpthreat-stats.md).

</dd> <dt>

**ThreatState**
</dt> <dd>

Type : **[**MPTHREAT \_ stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ Threat \_ Stat \_ Max \_ value + 1\]**

</dd> <dd>

Données de statistiques supplémentaires sur les menaces, telles que le nombre de menaces. Consultez [**\_ \_ données statistiques MPTHREAT**](mpthreat-stats-data.md).

</dd> <dt>

**Composant**
</dt> <dd>

Type : **[**MPCOMPONENT \_ Status**](mpcomponent-status.md) \[ MPCOMPONENT \_ MaxValue + 1\]**

</dd> <dd>

Tableau d’États pour plusieurs composants. Utilisez une valeur de l’énumération [**MPCOMPONENT \_ ID**](mpcomponent-id.md) en tant qu’index dans le tableau.

</dd> <dt>

**ProductExpirationTime**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

Horodateur d’expiration du produit dans UNC. Cela est valide uniquement si l’état d’expiration est défini.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ID MPCOMPONENT**](mpcomponent-id.md)
</dt> <dt>

[**État de MPCOMPONENT \_**](mpcomponent-status.md)
</dt> <dt>

[**résultat de MPSCAN \_**](mpscan-result.md)
</dt> <dt>

[**\_indicateur MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**statistiques de MPTHREAT \_**](mpthreat-stats.md)
</dt> <dt>

[**\_données statistiques \_ MPTHREAT**](mpthreat-stats-data.md)
</dt> </dl>

 

 





