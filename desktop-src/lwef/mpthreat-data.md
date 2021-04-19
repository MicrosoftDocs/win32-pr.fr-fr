---
title: Structure MPTHREAT_DATA (MpClient. h)
description: Données de notification transmises en raison de la détection ou de la modification des menaces.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_DATA
- PMPTHREAT_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
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
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518123"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_indicateur MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_action MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





