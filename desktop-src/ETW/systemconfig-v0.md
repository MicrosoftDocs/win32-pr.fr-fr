---
description: Cette classe est la classe parente pour les événements de configuration matérielle. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 9da1a7ec-89b5-462b-a336-544e4b7adf96
title: Classe SystemConfig_V0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0
api_type:
- NA
api_location: ''
ms.openlocfilehash: 92d77d1ad3effdd2bf22a7df8112187b27666238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864250"
---
# <a name="systemconfig_v0-class"></a>SystemConfig \_ v0 (classe)

Cette classe est la classe parente pour les événements de configuration matérielle.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **SystemConfig \_ v0** ne définit aucun membre.

## <a name="remarks"></a>Notes

Pour les événements de configuration matérielle sur Windows XP, consultez la classe [**HWConfig**](hwconfig.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**SystemConfig**](systemconfig.md)
</dt> <dt>

[**\_Processeur SystemConfig v0 \_**](systemconfig-v0-cpu.md)
</dt> <dt>

[**SystemConfig \_ v0 \_ LogDisk**](systemconfig-v0-logdisk.md)
</dt> <dt>

[**\_ \_ Carte réseau SystemConfig v0**](systemconfig-v0-nic.md)
</dt> <dt>

[**SystemConfig \_ v0 \_ PhyDisk**](systemconfig-v0-phydisk.md)
</dt> <dt>

[**SystemConfig \_ v0 \_**](systemconfig-v0-power.md)
</dt> <dt>

[**\_Services SystemConfig v0 \_**](systemconfig-v0-services.md)
</dt> <dt>

[**\_Vidéo SystemConfig v0 \_**](systemconfig-v0-video.md)
</dt> </dl>

 

 




