---
title: Structure MPCLEAN_DATA (MpClient. h)
description: Données de notification transmises à la fonction de rappel propre.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPCLEAN_DATA
- PMPCLEAN_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece20324fc06fb68a813b374a698b2e27264068c9051bb2a5fff328c7ad328d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476337"
---
# <a name="mpclean_data-structure"></a>\_Structure de données MPCLEAN

Données de notification transmises à la fonction de rappel propre.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**ThreatID**
</dt> <dd>

Type : **\_ ID MPTHREAT**

</dd> <dd>

Identificateur de la menace pour le nettoyage des menaces **MPNOTIFY \_ \_ \_ Démarrer** / **MPNOTIFY nettoyage des menaces \_ \_ \_ réussies** / **MPNOTIFY nettoyer les événements \_ \_ \_ ayant échoué** . Le bit supérieur est défini pour identifier les menaces liées à l’antivirus.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Type : **[ **\_ action MPTHREAT**](mpthreat-action.md)**

</dd> <dd>

Action de la menace pour le nettoyage des menaces **MPNOTIFY \_ \_ \_ Démarrer** / **MPNOTIFY nettoyer les menaces \_ \_ \_ réussies** / **MPNOTIFY \_ nettoyer les \_ menaces \_ ayant échoué** . Consultez [**\_ action MPTHREAT**](mpthreat-action.md).

</dd> <dt>

**dwStatus**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

État ou actions supplémentaires associées à l’action effectuée. Il s’agit d’une combinaison de bits indicateurs à partir de l' [**\_ indicateur MPSTATUS**](mpstatus-flag.md).

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Type : **PMPRESOURCE \_ info**

</dd> <dd>

Les informations sur les ressources pour les événements **MPNOTIFY \_ Clean \_ Threat \_ Start** / **MPNOTIFY \_ Clean \_ Threat \_ réussie** / **MPNOTIFY \_ Clean \_ Threat \_ failed** . Consultez [**MPRESOURCE \_ info**](mpresource-info.md).

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

[**\_indicateur MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_action MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





