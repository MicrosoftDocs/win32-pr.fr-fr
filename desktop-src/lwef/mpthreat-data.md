---
title: Structure MPTHREAT_DATA (MpClient. h)
description: Données de notification transmises en raison de la détection ou de la modification des menaces.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_DATA
- PMPTHREAT_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd6338a027e3b03971f357950bbc351acef0d3fcdca83b72130e0ea475164d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883229"
---
# <a name="mpthreat_data-structure"></a>\_Structure de données MPTHREAT

Données de notification transmises en raison de la détection ou de la modification des menaces.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**ThreatID**
</dt> <dd>

Type : **\_ ID MPTHREAT**

</dd> <dd>

Identificateur de la menace. Le bit supérieur est défini pour identifier les menaces liées à l’antivirus.

</dd> <dt>

**dwSessionID**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Session associée à la menace. Affectez la valeur-1 si aucune information spécifique à la session n’est disponible.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Type : **[ **\_ action MPTHREAT**](mpthreat-action.md)**

</dd> <dd>

L’action de menace a été tentée pour les événements **MPNOTIFY \_ Threat \_ Clean \_ réussite** / **MPNOTIFY \_ Threat \_ Clean \_ failed** .

</dd> <dt>

**dwStatus**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

État ou actions supplémentaires associées à l’action effectuée. Il s’agit d’une combinaison de bits indicateurs à partir de l' [**\_ indicateur MPSTATUS**](mpstatus-flag.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_indicateur MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_action MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





